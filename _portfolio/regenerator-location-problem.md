---
title: "Regenerator Location Problem"
excerpt: "Short descirption about the project"
collection: portfolio
---

## Intro

In optical networks, the strength of an optical signal deteriorates as it gets farther from the source due to transmission impairments in the fiber (attenuation, dispersion, cross-talk). In other words, the distance an optical signal may be sent without losing or falsifying the information is limited. Therefore, it is necessary to regenerate the signals periodically using regenerators. Given an optical network, the regenerator location problem searches for the subset of regenerators to be installed at minimum cost, so that each pair of nodes can communicate with each other.

## Definition

<td> 
	Mathematically, the regenerator location problem (RLP) can be described as follows. We are given:
	<ol>
		<li> a network <em>G = {N,F,D} </em> where <em> N</em>  is the set of nodes, <em> F</em>  is the set of edges, and <em> D</em>  is the associated distance matrix of edges,</li>
		<li> a maximum distance of <em>dmax</em> that determines how far a signal can traverse before its quality deteriorates and needs to be regenerated, and</li>
		<li> a non-negative cost <em>w(i)</em> for installing regenerator at node <em>i</em>, for each <em>i</em> in <em>N</em>.</li>
	</ol>
	The goal is to determine a subset of nodes <em> L</em> of minimum cost, such that for every pair of nodes in <em> N</em>  there exists a path in <em> G</em> with the property that there is no subpath (i.e., a subsequence of edges on the path) with length  <em> > dmax</em>  without internal regenerators.
</td>

## Complexity

The problem is NP-complete (see [1]). <br> In case of uniform regenerator costs, the RLP is equivalent to the Maximum Leaf Spanning Tree Problem (MLSTP) (aka the <a href="http://en.wikipedia.org/wiki/Connected_dominating_set">Minimum Connected Dominating Set problem</a>).

<table cellspacing=10 cellpadding=1>
<tr>
<td valign=top> 
    <b> Input graph  <em>G</em> after preprocessing <br> (two nodes are connected iff the length of the <br> shortest path <em> &le;dmax</em>)</b>
    <img src="{{site.url}}/images/rlp/Input.jpg" height=400>
</td>

<td valign=top> 
    <b> A feasible RLP solution </b>
    <img src="{{site.url}}/images/rlp/Input1.jpg" height=470>
</td>

<td valign=top> 
    <b> Corresponding MLSTP solution </b>
    <img src="{{site.url}}/images/rlp/Input2.jpg" height=470>
</td>
</tr>
</table>

## Benchmark Instances

<td>
	<ul>
		<li> Here you can download instances that have been used in our paper:<br>The regenerator location problem, <em> Networks 55(3): 205-220, 2010</em>, by S. Chen, I. Ljubić, and S. Raghavan.<br>This is one of the two most cited Networks paper in 2010. </li>
		<li> Three groups of instances are available:
			<ul>
				<li> <a href="{{site.url}}/docs/rlp/instances/random.zip">randomly generated instances</a> (40-100 nodes)</li>
				<li> <a href="{{site.url}}/docs/rlp/instances/weighted.zip">weighted instances</a> (40-100 nodes)</li>
				<li> <a href="{{site.url}}/docs/rlp/instances/large.zip">larger randomly generated instances</a> (200-500 nodes)</li>
			</ul>
		</li>
	</ul>
</td>

## Data Format

<td>
	Graphs are provided after preprocessing, i.e., we proceed with the distance matrix <em>D</em> as follows: a node pair <em>(u,v)</em> is connected by an edge iff the length of the shortest path between <em>u</em> and <em>v</em> is <em> &le;dmax</em>. The nodes that are not connected by an edge are called <b>not directly connected</b> or NDC node pairs.
	<ul>
		<li> Each instance file starts with "nNodes" which is the number of total nodes and then "nPairs" which is the number of NDC node pairs, followed by a nNodes  x nNodes matrix <em>A</em>, denoted by "Cost", and followed by a list of NDC node pairs, denoted by "UnPairedArc". Finally, if instances are weighted, before providing the "Cost" matrix, a list of node weights, denoted by "Weight" is given.</li>
		<li> <em>a(u,v)</em>=0 in the matrix "Cost" indicates that there is a direct connection between nodes <em>u</em> and <em>v</em>.</li>
	</ul>
</td>

## Binliography

<td>
	<ol>
		<li> S. Chen, I. Ljubić, and S. Raghavan: <a href="http://onlinelibrary.wiley.com/doi/10.1002/net.20366/pdf">The regenerator location problem</a>, Networks 55(3): 205-220, 2010</li>
	</ol>
</td>
