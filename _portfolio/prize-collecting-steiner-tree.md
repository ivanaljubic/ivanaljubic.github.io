---
title: "Prize-Collecting Steiner Tree Problem: A branch-and-cut algorithm (DHEA)"
excerpt: "Short descirption about the project"
collection: portfolio
---

## Intro

Let <em>G = (V,E, c, p) </em> be an undirected graph, with the vertices <em>V</em> associated with non-negative profits <em>p</em>, and with the edges <em>E</em> associated with non-negative costs <em>c</em>. The graph may correspond to the local street map, for example, with the edges representing street segments and vertices representing street intersections and the location of potential customers. The profit <em>p</em> associated with a vertex is an estimate of the potential gain of revenue caused by that customer being connected to the network and receiving its service. Vertices corresponding to street intersections have profit zero. The cost <em>c</em> associated with an edge is the cost of establishing the connection, i.e., of laying the pipe or cable on the corresponding street segment.

## Definition

<td> 
    The Linear Prize-Collecting Steiner Tree problem (PCST) consists of finding a connected subgraph <em>T = (V' ,E' )</em> of <em>G</em>, that maximizes <em>profit(T)</em> which is defined as the sum of all node-prizes taken into the solution <em>minus</em> the costs of the edges needed to establish the network.
    <br>
    Alternatively, one can <em> minimize</em> the edge-costs for establishing the network <em> plus </em> the penalties of the vertices outside of the solution.
</td>

<table cellspacing=10 cellpadding=1>
<tr>
<td valign=top> 
    <b> An input graph  <em>G</em>: hollow circles represent customers</b>
    <img src="{{site.url}}/images/pcstp/example1.jpg" height=400>
</td>

<td valign=top> 
    <b> A feasible but not optimal PCST solution  </b>
    <img src="{{site.url}}/images/pcstp/example2.jpg" height=470>
</td>
</tr>
</table>

## Download

<td>
    <ul>
        <li> <b> dhea-code</b> is a branch-and-cut algorithm for solving the undirected prize-collecting Steiner tree problem. Main features of the algorithm are described in:</li>
            <ul>
                <li> I. Ljubić, R. Weiskircher, U. Pferschy, G. Klau, P. Mutzel, and M. Fischetti:<br><a href="http://www.ads.tuwien.ac.at/publications/bib/pdf/MPB_PCSTP.pdf">An algorithmic framework for the exact solution of the prize-collecting Steiner tree problem.</a> <br> Mathematical Programming, Series B, 105(2-3):427-449, 2006. </li>
                <li> Ivana Ljubić.<br><em> <a href="http://www.ads.tuwien.ac.at/publications/bib/pdf/ljubicPhD.pdf"> Exact and Memetic Algorithms for Two Network Design Problems.</a></em><br>PhD thesis, Faculty of Computer Science, Vienna University of Technology, November 2004.</li>
            </ul>
        <!--                If you find dhea-code useful for your own research, please cite these publications. -->
        <li> Executable-File for 64-bit machines can be downloaded <font color=red> <b> <a href="{{site.url}}/docs/pcstp/64bit/dhea">HERE</a></b></font></li>
        <li> Executable-File for 32-bit machines (Linux/Unix-Platform) can be downloaded <font color=red> <b> <a href="{{site.url}}/docs/pcstp/32bit/dhea">HERE</a></b></font></li>
        <li> <a href="{{site.url}}/docs/pcstp/dhea-Manual.pdf">User Manual</a></li>
    </ul>
</td>

## Related Applications

<td>
    <ul> 
        <li> k-CARDINALITY TREES: using an extension of the dhea-code, we are able to solve all the instances of the <a href="http://iridia.ulb.ac.be/~cblum/kctlib/bestknown/index.html">KCT-LIB</a> to provable optimality. See our <a href="http://homepage.univie.ac.at/ivana.ljubic/research/publications/kcard.pdf">paper</a>. More details are coming soon...</li>
        <li> BIOINFORMATICS: The dhea code has been successfully used in a recent study to find functional modules in cancer interactome data. For further details see <a href="https://www.mi.fu-berlin.de/w/LiSA/Heinz">HEINZ</a> library and a web-page of <a href="http://page.mi.fu-berlin.de/gunnar/">Gunnar Klau</a>.</li>
    </ul>
</td>

## Licensing © 2003 - 2008

<td>
    This code is free software. You can redistribute it and/or modify it under the terms of the GNU Lesser General Public License as published by the Free Software Foundation; either version 2.1 of the License, or (at your option) any later version. This code is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU Lesser General Public License for more details. The dhea-code has been developed with non-commercial LEDA/CPLEX licenses for academic purposes only. Part of the dhea code makes use of the following software, whose licences you will need in order to be able to run the dhea-code:
    <ul> 
        <li> <a href="http://www.algorithmic-solutions.com/leda/index.htm">LEDA 5.1.1</a>, owned by <a href="http://www.algorithmic-solutions.com/">Algorithmic Solutions Software GmbH</a>.</li>
        <!-- may not be used by companies or other commercial users, and it may be used for academic purposes only! -->
        <li> <a href="http://www.ilog.com/products/cplex/">CPLEX 10.0</a>, owned by <a href="http://www.ilog.com">ILOG</a>.</li>
    </ul>
</td>

## Benchmark instances

<td>
    <ul>
        <li> Instances from <a href="http://www.research.att.com/~mgcr/data/index.html"> Mauricio Resende's web-page</a>:</li>
        <ul>
            <li> Groups C and D: <a href="{{site.url}}/docs/pcstp/instances/SteinCD.tgz">Download</a> (4MB)</li>
            <li> K and P groups: <a href="{{site.url}}/docs/pcstp/instances/KP.zip"> Download</a> (0.3MB)</li>
        </ul>
        <li> Group E: <a href="{{site.url}}/docs/pcstp/instances/E.tgz"> Download</a> (5.8MB)</li>
        <li> Real-world instances: <a href="{{site.url}}/docs/pcstp/instances/Cologne1.zip"> Cologne1</a> (8.9MB) and <a href="{{site.url}}/docs/pcstp/instances/Cologne2.zip"> Cologne2</a> (48.4MB)</li>
        <li> <b> After preprocessing described in Ljubić et al. (2006): </b> <a href="{{site.url}}/docs/pcstp/instances/ReducedCDEKP.zip"> Download groups C, D, E, K, P</a> (4.5MB). Due to vertex-elimination and fixing, optimal solution values for reduced instances are different from the original ones.</li>
    </ul>
</td>

## Bibliography

<td>
    <ol>
        <li> A.S. da Cunha, A. Lucena, N. Maculan, and M.G.C. Resende:A relax-and-cut algorithm for the prize-collecting Steiner problem in graphs. Discrete Applied Mathematics. article in press. (2008), doi:10.1016/j.dam.2008.02.014</li>
        <li> E. Uchoa: Reduction tests for the prize-collecting Steiner problem. Oper. Res. Lett. 34(4): 437-444. 2006.</li>
        <li> I. Ljubić, R. Weiskircher, U. Pferschy, G. Klau, P. Mutzel, and M. Fischetti: <a href="http://www.ads.tuwien.ac.at/publications/bib/pdf/MPB_PCSTP.pdf">An algorithmic framework for the exact solution of the prize-collecting Steiner tree problem.</a> Mathematical Programming, Series B, 105(2-3):427-449, 2006.</li>
        <li> O. Chapovska, A. P. Punnen: Variations of the prize-collecting Steiner tree problem. Networks 47(4): 199-205. 2006</li>
        <li> A. Moser: <a href="http://www.ads.tuwien.ac.at/publications/bib/pdf/moser_05.pdf">Finding Provably Optimal Solutions for the (Prize Collecting) Steiner Tree Problem</a>. Master Thesis. Vienna University of Technology, 2005.</li>
        <li> G.W. Klau, I. Ljubić, A. Moser, P. Mutzel, P. Neuner, U. Pferschy, and R. Weiskircher. Combining a memetic algorithm with integer programming to solve the prize-collecting Steiner tree problem. In K. Deb, editor, Proceedings of the Genetic and Evolutionary Computation Conference (GECCO-2004), volume 3102 of LNCS, pages 1304-1315. Springer-Verlag, 2004.</li>
        <li> A. Lucena, M. G. C. Resende: Strong lower bounds for the prize collecting Steiner problem in graphs. Discrete Applied Mathematics 141(1-3): 277-294. 2004.</li>
        <li> S. A. Canuto, M. G. C. Resende, and C. C. Ribeiro. Local search with perturbations for the prize-collecting Steiner tree problem in graphs. Networks, 38:50-58, 2001.</li>
        <li> D. S. Johnson, M. Minkoff, and S. Phillips. The prize-collecting Steiner tree problem: Theory and practice. In Proceedings of 11th ACM-SIAM Symposium on Discrete Algorithms, pages 760-769, San Francisco, CA, 2000.</li>
        <li> S. Engevall, M. G&ouml;the-Lundgren, and P. V&auml;arbrand. A strong lower bound for the node weighted Steiner tree problem. Networks, 31(1):11-17, 1998.</li>
        <li> M. X. Goemans and D. P.Williamson. The primal-dual method for approximation algorithms and its application to network design problems. In D. S. Hochbaum, editor, Approximation algorithms for NP-hard problems, pages 144-191. P. W. S. Publishing Co., 1996.</li>
        <li> D. Bienstock, M. X. Goemans, D. Simchi-Levi, and D. Williamson. A note on the prize-collecting traveling salesman problem. Mathematical Programming, 59:413-420, 1993.</li>
    </ol>
</td>
