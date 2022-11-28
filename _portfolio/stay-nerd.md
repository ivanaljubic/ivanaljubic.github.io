---
title: "StayNerd: Solver for Steiner Trees and Related Problems"
excerpt: "Short description about the project"
collection: portfolio
---

<b> (['&#643;t&#652;&#618;n&#601;])</b>
<br> by <a href="http://www.dei.unipd.it/~fisch/"> Matteo Fischetti</a>, <a href="http://homepage.univie.ac.at/markus.leitner/">Markus Leitner</a>, <a href="http://www.essec.edu/en/staff/faculty/ivana-ljubic"> Ivana Ljubić</a>, Martin Luipersbeck, <a href="http://or.dei.unibo.it/staff/michele-monaci">Michele Monaci</a>, Max Resch, <a href="http://www.dei.unipd.it/~salvagni/">Domenico Salvagnin</a>, <a href="http://homepage.univie.ac.at/markus.sinnl/">Markus Sinnl</a> University of Padua and University of Vienna

## DESCRIPTION

<td> 
	<a href="http://dimacs11.zib.de/">11th DIMACS Implementation Challenge</a> was dedicated to the study of Steiner tree problems. The code available at this web-site provides implementations of algorithms for finding exact and heuristic solutions for the following problem types: 
	<ul>
		<li> The Steiner tree problem in graphs (STP)</li>
		<li> The prize-collecting Steiner tree problem (PCSTP)</li>
		<li> The rooted prize-collecting Steiner tree problem (RPCSTP)</li>
		<li> The maximum-weight connected subgraph problem (MWCS), and</li>
		<li> The degree-constrained Steiner tree problem (DCST)</li>
	</ul>
	According to the <a href="http://dimacs11.zib.de/contest/results/results.html"> results of the 11th DIMACS Challenge</a>, our exact solver (aka <b style="color:red">MOZARTBALLS</b>) and heuristic solver (aka <b style="color:red">STAYNERD</b>) are the winners in most of the categories for the selected group of problems. Both, exact and heuristic algorithms are available in the provided package (corresponding to the version published in the Mathematical Programming Computation, 2017), and can be turned on/off by appropriate parameter settings (see <a href="{{site.url}}/docs/stay-nerd/staynerd_user_manual.pdf">user-manual</a> for more details). 
</td>

## REFERENCE

<td>  
	Please refer to the following publication when using our solver: <br> <b>M. Fischetti, M. Leitner, I. Ljubić, M. Luipersbeck, M. Monaci, M. Resch, D, Salvagnin, M. Sinnl <br> <a href="https://link.springer.com/article/10.1007/s12532-016-0111-0">Thinning out Steiner trees: a node based model for uniform edge costs</a> <br> Mathematical Programming Computation 9(2): 203-229, 2017, DOI: 10.1007/s12532-016-0111-0</b>
</td>

## PROBLEM DEFINITION

### STP/DCST

<td> 
	Let <em>G = (V, E, T, c) </em> be an undirected graph, with the set of nodes <em>V</em> and its subset <em>T</em> called terminals, and with the edges <em>E</em> associated with non-negative costs <em>c</em>. The <b>  Steiner Tree Problem in Graphs (STP)</b> consists of finding a connected subgraph <em>T = (V' ,E' )</em> of <em>G</em> that  connects all terminals and minimizes the sum of the costs of the edges needed to establish the network. <br> Given, in addition, a maximum node degree function <em>d</em> associated to each node, the <b> degree-constrained Steiner tree problem (DCST)</b> consists of finding a Steiner tree of minimum cost that does not violate maximum node degrees given by <em>d</em>. 
</td>

### PCSTP/RPCSTP

<td> 
	Let <em>G = (V, E, c, p) </em> be an undirected graph, with the set of nodes <em>V</em> associated with non-negative node-profits <em>p</em>, and with the set of edges <em>E</em> associated with non-negative costs <em>c</em>. The <b>  Prize-Collecting Steiner Tree Problem (PCSTP)</b> consists of finding a connected subgraph <em>T = (V' ,E' )</em> of <em>G</em> that maximizes the sum of collected node-profits minus the costs of the edges needed to establish the network. <br> Given, in addition, a root node <em>r</em>, the <b>Rooted Prize-Collecting Steiner Tree Problem (RPCSTP)</b> consists of finding a rooted PCSTP of maximum weight that contains the root node. 
</td>

### MWCS:

<td> 
	Let <em>G = (V, E, w) </em> be an undirected graph, with the set of nodes <em>V</em> associated with node-weights <em>w</em>, and with the set of edges <em>E</em>. The <b>  Maximum-Weight Connected Subgraph Problem (MWCS) </b> consists of finding a connected subgraph <em>T = (V' ,E' )</em> of <em>G</em> that maximizes the sum of collected node-weights. <br>
</td>

## STAYNERD SOLVER

<td> 
The provided executable is a 64-bit Linux binary (compiled with GCC 4.9.2, requiring GLIBC version 2.3 or later). For running the solver, the user is required to provide dynamic CPLEX libraries. <br> By default, a CPLEX installation will only include static libaries, so the corresponding dynamic libary files must be generated manually from the set of static library files.  For this purpose the following software is required:
	<ul>
		<li> GCC version 4.9.2 or greater</li>
		<li> IBM ILOG CPLEX Optimization Studio (version 12.6)</li>
	</ul>
Steps necessary to build the dynamic libraries and verify that the solver works correctly:
	<ol>
		<li> Set the environment variable  CPLEX_DIR to the base directory of the CPLEX installation on your system (e.g., /opt/ibm/ILOG/CPLEX_Studio126).</li>
		<li> Run the script <CODE><b>make_cplex_dynamic.sh</b></CODE> provided with the binary to create the dynamic CPLEX library files libconcert.so, libcplex.so and libilocplex.so.</li>
		<li> Make sure that the dynamic libraries are placed in the same directory as the solver binary <CODE><b>staynerd</b></CODE> and the license file <CODE><b>staynerd.license</b></CODE>.</li>
		<li> A simple way to run the solver is as follows (see <a href="staynerd_user_manual.pdf">user manual</a> for more options): <br><CODE><b>staynerd [inputfile] [timelimit] [threads] [outputfile]</b></CODE></li>
	</ol>

<b> <a href="{{site.url}}/docs/stay-nerd/staynerd.zip"> DOWNLOAD THE PACKAGE HERE </a></b> <br>
<b> <a href="mailto:ivana.ljubic@essec.edu?subject=[STAYNERD]%20Licence%20Key%20Request&amp;cc=martin.luipersbeck@univie.ac.at,markus.sinnl@univie.ac.at">SEND US EMAIL REQUEST FOR OBTAINING A VALID LICENSE KEY </a></b>

</td>

## User Manual and Input Format

<td>
	User manual can be downloaded <a href="{{site.url}}/docs/stay-nerd/staynerd_user_manual.pdf">HERE</a>. <br> Input format recognized by our solver is the <a href="http://dimacs11.zib.de/downloads.html"><b> STP format</b> defined at the 11th Dimacs Challenge</a>.
</td>

## Licensing

<td>
This code is free software to be used for academic purpose only. If you use it in your research, give the credits to our publication: <br>
<b>M. Fischetti, M. Leitner, I. Ljubić, M. Luipersbeck, M. Monaci, M. Resch, D, Salvagnin, M. Sinnl <br> Thinning out Steiner trees: a node based model for uniform edge costs,<br> Mathematical Programming Computation 9(2): 203-229, 2017, DOI: 10.1007/s12532-016-0111-0 </b><br><br>

Part of the staynerd code makes use of the following software (for which you might need a valid license in order to be able to run the code):

<ul>
	<li> CPLEX 12.6 or later</li>
	<li> <a href="http://www.ogdf.net/doku.php">OGDF library</a>, (we thank to the OGDF team for granting us a special permission to statically link the OGDF library)  <br>
	OGDF is GPL software, see also: M. Chimani, C. Gutwenger, M. J&uuml;nger, G. W. Klau, K. Klein, P. Mutzel. The Open Graph Drawing Framework (OGDF). Chapter 17 in: R. Tamassia (ed.), Handbook of Graph Drawing and Visualization, CRC Press, 2014.</li>
	<li> <a href="http://www.davideisenstat.com/dtree/"> dtree: dynamic trees a la carte </a></li>
</ul>
The staynerd-code has been developed with academic CPLEX and OGDF license for non-commercial purposes only.
