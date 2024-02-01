== Introduction ==
[[https://github.com/emartineznunez/AutoMeKin/blob/main/logo.png|center]]

AutoMeKin (formerly ''tsscds'') has been designed to discover reaction mechanisms in an automated fashion. Transition states are located using MD simulations and Graph Theory algorithms. Monte Carlo simulations afford kinetic results. The only input is a starting structure in XYZ format. The method is described in these two publications: [http://onlinelibrary.wiley.com/doi/10.1002/jcc.23790/abstract 1]
[http://pubs.rsc.org/en/content/articlelanding/2015/cp/c5cp02175h#!divAbstract 2]. At present [http://openmopac.net/ MOPAC2016], [https://www.entos.ai/qcore/documentation/ Entos Qcore] and Gaussian (G09/G16) are interfaced with AutoMeKin. The program has been tested on the following Linux distros: CentOS 7, Red Hat Enterprise Linux and Ubuntu 20.04 LTS.

To give you a flavor of the capabilities of the program you can try our [http://rxnkin.usc.es/amk/ web interface] or [https://colab.research.google.com/github/emartineznunez/AutoMeKin/blob/main/AutoMeKin.ipynb Google Colab]


[[https://github.com/emartineznunez/AutoMeKin/blob/main/Web.png|center]]

[https://twitter.com/AutoMeKin2021 Twitter]

</div>

== Developers team==
'''Emilio Martinez-Nunez''', George L. Barnes, Carles Bo, Diego Garay-Ruiz, David R. Glowacki, Sabine Kopec, Daniel Pelaez-Ruiz, Aurelio Rodriguez, Roberto Rodriguez-Fernandez, Robin J. Shannon, James J. P. Stewart, Pablo G. Tahoces and Saulo A. Vazquez

'''Address'''<br />
Departamento de Química Física, Facultade de Química, Avda. das Ciencias s/n, 15782 Santiago de Compostela, SPAIN<br />
[mailto:emilio.nunez@usc.es email me]

==License==
MIT License

Copyright (C) 2021 AutoMeKin

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

==Install the code==
To install the code follow the [[Installation instructions]]

==Tutorial==


Download [https://github.com/emartineznunez/AutoMeKin/blob/main/docs/tutorial.pdf tutorial]

The tutorial can be more easily followed executing the example:

https://colab.research.google.com/github/emartineznunez/AutoMeKin/blob/main/AutoMeKin.ipynb

==Program execution==
Unless you donwloaded the singularity container (in that case skip this step), to start using any of the scripts of the program, load the amk/2021 module:

<code>module load amk/2021</code>

To run the low-level calculations use:

<code>nohup llcalcs.sh molecule.dat ntasks niter runningtasks >llcalcs.log 2>&1 &</code>

where:<br />
<code>molecule</code> is  the name of your molecule<br />
<code>ntasks</code> is the number of tasks<br />
<code>niter</code> is the number of iterations<br />
<code>runningtasks</code> is the number of simultaneous tasks

To run the high-level calculations use:

<code>nohup hlcalcs.sh molecule.dat runningtasks >hlcalcs.log 2>&1 &</code>

For more details, follow the instructions given in the tutorial: https://github.com/emartineznunez/AutoMeKin/blob/main/docs/tutorial.pdf

==Reference==
If you use '''AutoMeKin''', please cite the following publications:

<ol start="1">
<li>[https://onlinelibrary.wiley.com/doi/full/10.1002/jcc.26734 <span style="font-size:100%">E Martínez-Nuñez, G.L. Barnes, D.R. Glowacki, S. Kopec, D. Pelaez, A. Rodriguez, R. Rodriguez-Fernandez, R.J. Shannon, J.J.P. Stewart, P.G. Tahoces, S.A. Vazquez, J. Comput. Chem. 2021, 42, 2036</span>]</li>
<li>[http://onlinelibrary.wiley.com/doi/10.1002/jcc.23790/abstract <span style="font-size:100%">E. Martínez-Núñez, J. Comput. Chem. 2015, 36, 222</span>]</li>
<li>[http://pubs.rsc.org/en/content/articlelanding/2015/cp/c5cp02175h#!divAbstract <span style="font-size:100%">E. Martínez-Núñez, Phys. Chem. Chem. Phys. 2015,17, 14912</span>]</li>
<li>[http://OpenMOPAC.net <span style="font-size:100%">J. J. P. Stewart, MOPAC2016, Stewart Computational Chemistry: Colorado Springs, CO, USA, HTTP://OpenMOPAC.net, 2016.</span>]</li>
</ol>

If you use the older version '''tsscds''', please cite, instead of ref 1 above, the following one:

[https://onlinelibrary.wiley.com/doi/full/10.1002/jcc.25370 <span style="font-size:100%">A. Rodriguez, R. Rodriguez-Fernandez, S.A. Vazquez, G.L. Barnes, J.J.P. Stewart, E Martínez-Nuñez, J. Comput. Chem. 2018, 39, 1922</span>]

==Works that employ AutoMeKin==

The following works employ AutoMeKin: [[Works]]

==Changelog==
Consult the [[Latest changes]]

==Web interface and Google Colab==
AutoMeKin can be used through our [http://rxnkin.usc.es/amk/ web interface].

The tutorial example (formic acid) can be easily tested on Google Colab using this 
link:

https://colab.research.google.com/github/emartineznunez/AutoMeKin/blob/main/AutoMeKin.ipynb

==News==
AutoMeKin is now interfaced with Gaussian 16 (from rev. 1131)

The Python library [https://github.com/dgarayr/amk_tools '''amk-tools'''] can be employed to read, process and visualize reaction networks generated by AutoMeKin and is available in the latest singularity container (and through our web interface). Here is the paper describing the new tool: [https://pubs.acs.org/doi/10.1021/acsphyschemau.1c00051 <span style="font-size:100%"> Garay-Ruiz et al. ACS Phys. Chem. Au 2022]

AutoMekin got the [https://geqc.rseq.org/emilio-martinez-nunez-and-mireia-via-nadal-recieve-the-geqc-rseq-2021-methodology-development-prize/ GEQC-RSEQ 2021 Methodology Development Prize].

AutoMeKin now includes '''barrierless channels'''. However, these channels are not considered in the kinetics.

AutoMeKin has been interfaced with [https://www.entos.ai/qcore/documentation/ '''Entos Qcore'''].

AutoMeKin has been interfaced with '''BXDE''' to enhance its efficiency ([https://onlinelibrary.wiley.com/doi/full/10.1002/syst.201900024 <span style="font-size:100%"> R. A. Jara-Toro et al. ChemSystemsChem doi: 10.1002/syst.201900024</span>]).

The method has also been recently generalized in a collaboration with Dani Pelaez and co-workers to study '''van der Waals structures''' ([https://onlinelibrary.wiley.com/doi/abs/10.1002/qua.26008 <span style="font-size:100%"> S. Kopec et al. Int. J. Quantum Chem. 2019, 119, e26008 </span>]) and also to generate sum-of-products PESs for quantum dynamics ([https://www.frontiersin.org/articles/10.3389/fchem.2019.00576/full <span style="font-size:100%"> R. Panades-Barrueta et al. Frontiers in Chemistry 2019, 7, 576</span>]).




