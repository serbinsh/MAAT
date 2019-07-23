# The Multi-Assumption Architecture and Testbed (MAAT) modelling system. #



### MAAT Version 1.2 ###

The multi-assumption architecture and testbed (MAAT) is a modelling framework designed to facilitate simple and rapid comparison of multiple modelling hypotheses and assumptions, i.e. ways in which to represent processes, in a systems context.
MAAT is designed to easily specify and run large ensembles of simulations.
Ensembles can vary in process representation, parameter values, and environmental conditions.
Built in sensitivity analysis and uncertainty quantification (SA/UQ) can be used to assess variability in model caused output by multiple ways in which to represent processes. 

The MAAT framework is a model wrapper and a model coding syntax that can be used to define a model of a system.
The wrapper and the system model are separated and the syntax allows the wrapper to pass system-model specific information to the model without any system-model specific information contained in the wrapper. 
All system-model specific information is contained within the system model and initialisation files. 
This separation of wrapper and system model allows rapid development of new system models and system model components (e.g. process representations) without the need to edit the wrapper.

Current systems models that come packaged with the MAAT are a leaf-scale model of photosynthesis, a simple ground-water model detailed in Dai et al (2017 WRR), and a simple 'Hello World' type example and template for building new system models. 

MAAT is written in R and uses the object oriented programming package 'proto' to develop the wrapper and model objects. 
MAAT has been developed on Linux Ubuntu 16.04 and is designed to be run from the command line (and in some instances from within the R console or IDE like Rstudio).

### version 1.2 ###

* Complete structural overhaul of how wrapper and model objects are built for a higher level of generalisation and minimal duplication.
* Functions are now proper methods of the fns object which has the model object as parent.
* init_MAAT.R and XMl files should be compatible with v1.1 files.
* Adding new semi-analytical solver functions, work in progress.
* Canopy struncture system model developments, work in progress.
* MCMC DREAM algorithm added for parameter estimation, also a work in progress.
* A number of bug fixes.

#### v1.2.1
* mostly under-the-hood structural changes
* small incompatibility with v1.2 for a few leaf function names (solver, electron transport, gas_diff, 1 / 2 more)  


### Use guidelines ### 

If you want to use this code then please do! 
If you plan to publish using this code, communicating your intentions with code authors at an early stage is the use-policy (i.e. when the study is being designed and simulations are being run, well before manuscript drafting).

Please be respectful of other people's work and their willingness to open source their code. 
The master branch is very close to the cutting edge developments in MAAT, which allows for good code integration and software best practice. 
Please be aware that the authors of these developments are likely to have not yet published what they are intending to, please contact them to discuss use. 
Older code is fine to use without co-authorship, but it is rcommended that code authors be contacted. 
This is a balance, and likely no single rule really fits all situations. 
So get in touch and we'll work something out that's agreeable to all parties.

### MAAT installation ###

https://github.com/walkeranthonyp/MAAT/wiki/MAAT-installation

### Run simulations with MAAT ###

https://github.com/walkeranthonyp/MAAT/wiki/Run-MAAT-simulations

### Contribution guidelines ###

* For development please [fork this repo and sync to the main repo](https://help.github.com/articles/fork-a-repo/), create your own dev branch, and then [use the pull request functionality on GitHub](https://help.github.com/articles/creating-a-pull-request/).
Before starting new feature branches please make sure your fork and clone is up to date with the latest master branch on this repo.
 
* Code review - by walkeranthonyp 

* If you using this code and you are developing additional system models, please use pull requests to integrate your models back up with this central repo.
This will help to maintain a central code-base and the principles of open science, facilitating other people's work and benefitting everyone.  


### Related publications ###

Walker, A. P., Ye, M., Lu, D., De Kauwe, M. G., Gu, L., Medlyn, B. E., Rogers, A., and Serbin, S. P.: The multi-assumption architecture and testbed (MAAT v1.0): R code for generating ensembles with dynamic model structure and analysis of epistemic uncertainty from multiple sources, Geosci. Model Dev., 11, 3159-3185, 2018, [doi.org/10.5194/gmd-11-3159-2018](https://doi.org/10.5194/gmd-11-3159-2018)

Dai, H., Ye, M., Walker, A.P., Chen, X., 2017. A new process sensitivity index to identify important system processes under process model and parametric uncertainty. Water Resour. Res. 53, 3476–3490. [doi.org/10.1002/2016WR019715](https://doi.org/10.1002/2016WR019715)

Walker, A.P., Carter, K.R., Gu, L., Hanson, P.J., Malhotra, A., Norby, R.J., Sebestyen, S.D., Wullschleger, S.D., Weston, D.J., 2017. Biophysical drivers of seasonal variability in Sphagnum gross primary production in a northern temperate bog. J. Geophys. Res. Biogeosci. 122, 2016JG003711. [doi.org/10.1002/2016JG003711](https://doi.org/10.1002/2016JG003711)


### Sponsorship ###

We are grateful of the support from the U.S. Department of Energy (DOE) Office of Science, Biological and Environmental Research (BER). 

Elements of this work are supported through various [DOE BER](https://www.energy.gov/science/ber/biological-and-environmental-research) projects.
[NGEE Tropics](https://ngee-tropics.lbl.gov/) supports the development of the leaf and canopy scale photosynthesis models. 
Development of the MAAT framework and early versions of the photosynthesis models were supported by the [ORNL Terrestrial Ecosystem Science SFA](https://tes-sfa.ornl.gov/).    



### Please direct questions to ###

Anthony Walker (walkerap@ornl.gov)



<!-- END -->
