---
title: "Real-World Instances for the Steiner Tree Problem in Graphs"
excerpt: "Short descirption about the project"
collection: portfolio
---

by <a href="http://homepage.univie.ac.at/markus.leitner/">Markus Leitner</a>, <a href="http://homepage.univie.ac.at/ivana.ljubic/"> Ivana Ljubić</a> , Martin Luipersbeck, <a href="http://www.fh-kaernten.at/ueber-die-fh/mitarbeiterinnen/detail.html?per_oid=-1025000000000006254">Markus Prossegger</a>, Max Resch <br> University of Vienna

## Input

Let <em>G = (V, E, T, c) </em> be an undirected graph, with the set of vertices <em>V</em> and its subset <em>T</em> called terminals, and with the edges <em>E</em> associated with non-negative costs <em>c</em>.

## Definition

The Steiner Tree Problem in Graphs (STP) consists of finding a connected subgraph <em>T = (V' ,E' )</em> of <em>G</em> that connects all terminals and minimizes the sum of the costs of the edges needed to establish the network.

In network design applications the edges of the input graph typically correspond to the local street map, with the edges vertices representing street intersections and the location of potential customers. The cost <em>c</em> associated with an edge is the cost of establishing the connection, i.e., of laying the pipe or cable on the corresponding street segment.

## New Benchmark Instances

<td>
	We propose two new sets of benchmark instances for the STP that are derived from real-world examples of telecommunication networks:
	<ul>
		<li> <b> GEO Instances:</b> This set contains 23 instances originating from an Austrian city, with different deployment areas and different density concerning the number of terminals.  The graphs contain between 42 481 and 235 686 nodes, 52 552 and 366 093 edges, and between 88 and 6313 terminals.  The <i>simple preprocessing step</i> (see below) was skipped for the GEO instances, it deemed unnecessary, hence no comparison data is available for this step.</li>
		<li> <b>I Instances:</b> This set contains 85 instances representing deployment areas from various Austrian cities, but they also include rural areas with  smaller population density and very sparse infrastructure. The coordinates and construction data of the set I cannot be disclosed to the public. The instances we publish are modified in a way that does not allow inference of the original data. This is the reason why only <i>simple preprocessed data</i> (see below) is available for the I-instances. The underlying graphs contain between 7886 and 178 810 nodes, 9265 and 239 552 edges, and between 38 and 4991 terminals.</li>
	</ul>
</td>

## Downloads

<td> 
	GEO instances are available in their original form (including node-coordinates), or after <i>advanced preprocessing</i> as proposed by Ribeiro et al.[4], and implemented in <a href="http://www.cs.princeton.edu/~rwerneck/bossa/">Bossa</a>. I Instances are available after <i>simple preprocessing</i> (node one- and two-degree test), or after advanced preprocessing. All instances are provided in the <a href="http://steinlib.zib.de">SteinLib</a> format.
	<ul>
		<li> <b> GEO Instances: </b> <a href="{{site.url}}/docs/stp/instances/geo_original.tar.xz"> Original Instances</a> and <a href="{{site.url}}/docs/stp/instances/geo_advanced_preprocessed.tar.xz"> Instances after <i>Advanced Preprocessing</i></a></li>
		<li> <b>I Instances:</b>  <a href="{{site.url}}/docs/stp/instances/I_simple_preprocessed.tar.xz">Instances after <i>Simple Preprocessing</i></a> and <a href="{{site.url}}/docs/stp/instances/I_advanced_preprocessed.tar.xz">Instances after <i>Advanced Preprocessing</i></a></li>
	</ul>
</td>

## Documentation

<td> 
	M. Leitner, I. Ljubić, M. Luipersbeck, M. Prossegger, M. Resch: <a href="{{site.url}}/docs/stp/realworld-stp-report-short.pdf">New Real-world Instances for the Steiner Tree Problem in Graphs</a>, Technical Report, ISOR, Uni Wien, 2014
</td>

<table cellspacing=10 cellpadding=1>
<tr>
<td valign=top> 
    <b> Instance GEO-107 </b>
    <img src="{{site.url}}/images/stp/U-G107.png" height=400>
</td>

<td valign=top> 
    <b> Instance GEO-203 </b>
    <img src="{{site.url}}/images/stp/U-G203.png" height=470>
</td>

<td valign=top> 
    <b> Instance GEO-309 </b>
    <img src="{{site.url}}/images/stp/U-G309.png" height=470>
</td>
</tr>
</table>

## Bibliography:

<td>
	<ol>
		<li> <a href="http://www.cs.princeton.edu/~rwerneck/bossa/">Bossa</a> <!--, R.F.F. Werneck --></li>
		<li> T. Koch and A.  Martin: Solving Steiner tree problems in graphs to optimality, Networks 32(3), pp. 207-232, 1998</li>
		<li> M. Prossegger:  Generation of a Weighted Network Graph based-on Hybrid Spatial Data, Proceedings of The Fifth International Conference on Advanced Geographic Information Systems, Applications, and Services, GEOProcessing, Nice, France, pp. 120--124, 2013</li>
		<li> C.C. Ribeiro, E. Uchoa, R.F.F. Werneck: A hybrid GRASP with perturbations for the Steiner problem in graphs, INFORMS Journal on Computing 14(3), pp. 228-246,2002</li>
		<li> <a href="http://steinlib.zib.de">SteinLib</a></li>
	</ol>
</td>
