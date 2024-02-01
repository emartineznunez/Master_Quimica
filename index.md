## AutoMeKin 

## Introduction

```{=html}
<div style="column-count:2;-moz-column-count:2;-webkit-column-count:2">
```
![](Automekin.png "Automekin.png") AutoMeKin (formerly *tsscds*) has
been designed to discover reaction mechanisms in an automated fashion.
Transition states are located using MD simulations and Graph Theory
algorithms. Monte Carlo simulations afford kinetic results. The only
input is a starting structure in XYZ format. The method is described in
these two publications:
[1](http://onlinelibrary.wiley.com/doi/10.1002/jcc.23790/abstract)
[2](http://pubs.rsc.org/en/content/articlelanding/2015/cp/c5cp02175h#!divAbstract).
At present [MOPAC2016](http://openmopac.net/), [Entos
Qcore](https://www.entos.ai/qcore/documentation/) and Gaussian (G09/G16)
are interfaced with AutoMeKin. The program has been tested on the
following Linux distros: CentOS 7, Red Hat Enterprise Linux and Ubuntu
20.04 LTS.

To give you a flavor of the capabilities of the program you can try our
[web interface](http://rxnkin.usc.es/amk/) or [Google
Colab](https://colab.research.google.com/github/emartineznunez/AutoMeKin/blob/main/AutoMeKin.ipynb)

[Twitter](https://twitter.com/AutoMeKin2021)

![](Web.png "Web.png")

```{=html}
</div>
```
## Developers team {#developers_team}

**Emilio Martinez-Nunez**, George L. Barnes, Carles Bo, Diego
Garay-Ruiz, David R. Glowacki, Sabine Kopec, Daniel Pelaez-Ruiz, Aurelio
Rodriguez, Roberto Rodriguez-Fernandez, Robin J. Shannon, James J. P.
Stewart, Pablo G. Tahoces and Saulo A. Vazquez

**Address**\
Departamento de Química Física, Facultade de Química, Avda. das Ciencias
s/n, 15782 Santiago de Compostela, SPAIN\
[email me](mailto:emilio.nunez@usc.es)

## License

MIT License

Copyright (C) 2021 AutoMeKin

Permission is hereby granted, free of charge, to any person obtaining a
copy of this software and associated documentation files (the
\"Software\"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be included
in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED \"AS IS\", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Install the code {#install_the_code}

To install the code follow the [Installation
instructions](Installation_instructions "wikilink")

## Tutorial

Download [ tutorial ](Media:tutorial2021.pdf "wikilink")\
The tutorial can be more easily followed executing the example:

[`https://colab.research.google.com/github/emartineznunez/AutoMeKin/blob/main/AutoMeKin.ipynb`](https://colab.research.google.com/github/emartineznunez/AutoMeKin/blob/main/AutoMeKin.ipynb)

## Program execution {#program_execution}

Unless you donwloaded the singularity container (in that case skip this
step), to start using any of the scripts of the program, load the
amk/2021 module:

`module load amk/2021`

To run the low-level calculations use:

`nohup llcalcs.sh molecule.dat ntasks niter runningtasks >llcalcs.log 2>&1 &`

where:\
`molecule` is the name of your molecule\
`ntasks` is the number of tasks\
`niter` is the number of iterations\
`runningtasks` is the number of simultaneous tasks

To run the high-level calculations use:

`nohup hlcalcs.sh molecule.dat runningtasks >hlcalcs.log 2>&1 &`

For more details, follow the instructions given in the [ tutorial
](Media:Tutorial2020.pdf "wikilink")

## Reference

If you use **AutoMeKin**, please cite the following publications:

1.  [`<span style="font-size:100%">`{=html}E Martínez-Nuñez, G.L.
    Barnes, D.R. Glowacki, S. Kopec, D. Pelaez, A. Rodriguez, R.
    Rodriguez-Fernandez, R.J. Shannon, J.J.P. Stewart, P.G. Tahoces,
    S.A. Vazquez, J. Comput. Chem. 2021, 42,
    2036`</span>`{=html}](https://onlinelibrary.wiley.com/doi/full/10.1002/jcc.26734)
2.  [`<span style="font-size:100%">`{=html}E. Martínez-Núñez, J. Comput.
    Chem. 2015, 36,
    222`</span>`{=html}](http://onlinelibrary.wiley.com/doi/10.1002/jcc.23790/abstract)
3.  [`<span style="font-size:100%">`{=html}E. Martínez-Núñez, Phys.
    Chem. Chem. Phys. 2015,17,
    14912`</span>`{=html}](http://pubs.rsc.org/en/content/articlelanding/2015/cp/c5cp02175h#!divAbstract)
4.  [`<span style="font-size:100%">`{=html}J. J. P. Stewart, MOPAC2016,
    Stewart Computational Chemistry: Colorado Springs, CO, USA,
    <HTTP://OpenMOPAC.net>, 2016.`</span>`{=html}](http://OpenMOPAC.net)

If you use the older version **tsscds**, please cite, instead of ref 1
above, the following one:

[`<span style="font-size:100%">`{=html}A. Rodriguez, R.
Rodriguez-Fernandez, S.A. Vazquez, G.L. Barnes, J.J.P. Stewart, E
Martínez-Nuñez, J. Comput. Chem. 2018, 39,
1922`</span>`{=html}](https://onlinelibrary.wiley.com/doi/full/10.1002/jcc.25370)

## Works that employ AutoMeKin {#works_that_employ_automekin}

The following works employ AutoMeKin: [Works](Works "wikilink")

## Changelog

Consult the [Latest changes](Latest_changes "wikilink")

## Web interface and Google Colab {#web_interface_and_google_colab}

AutoMeKin can be used through our [web
interface](http://rxnkin.usc.es/amk/).

The tutorial example (formic acid) can be easily tested on Google Colab
using this link:

[`https://colab.research.google.com/github/emartineznunez/AutoMeKin/blob/main/AutoMeKin.ipynb`](https://colab.research.google.com/github/emartineznunez/AutoMeKin/blob/main/AutoMeKin.ipynb)

## News

AutoMeKin is now interfaced with Gaussian 16 (from rev. 1131)

The Python library [**amk-tools**](https://github.com/dgarayr/amk_tools)
can be employed to read, process and visualize reaction networks
generated by AutoMeKin and is available in the latest singularity
container (and through our web interface). Here is the paper describing
the new tool: [`<span style="font-size:100%">`{=html} Garay-Ruiz et al.
ACS Phys. Chem. Au
2022](https://pubs.acs.org/doi/10.1021/acsphyschemau.1c00051)

AutoMekin got the [GEQC-RSEQ 2021 Methodology Development
Prize](https://geqc.rseq.org/emilio-martinez-nunez-and-mireia-via-nadal-recieve-the-geqc-rseq-2021-methodology-development-prize/).

AutoMeKin now includes **barrierless channels**. However, these channels
are not considered in the kinetics.

AutoMeKin has been interfaced with [**Entos
Qcore**](https://www.entos.ai/qcore/documentation/).

AutoMeKin has been interfaced with **BXDE** to enhance its efficiency
([`<span style="font-size:100%">`{=html} R. A. Jara-Toro et al.
ChemSystemsChem doi:
10.1002/syst.201900024`</span>`{=html}](https://onlinelibrary.wiley.com/doi/full/10.1002/syst.201900024)).

The method has also been recently generalized in a collaboration with
Dani Pelaez and co-workers to study **van der Waals structures**
([`<span style="font-size:100%">`{=html} S. Kopec et al. Int. J. Quantum
Chem. 2019, 119, e26008
`</span>`{=html}](https://onlinelibrary.wiley.com/doi/abs/10.1002/qua.26008))
and also to generate sum-of-products PESs for quantum dynamics
([`<span style="font-size:100%">`{=html} R. Panades-Barrueta et al.
Frontiers in Chemistry 2019, 7,
576`</span>`{=html}](https://www.frontiersin.org/articles/10.3389/fchem.2019.00576/full)).

Return to [Contents](#toc "wikilink")

Return to [Main_Page](Main_Page "wikilink")
