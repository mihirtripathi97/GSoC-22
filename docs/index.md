# Google Summer of Code 2022 Report

## Project: Bayesian Excess Variance (Bexvar) in Stingray

The aim of the [project](https://summerofcode.withgoogle.com/programs/2022/projects/rG1XqJqK) was to implement the Bayesian excess variance (Bexvar) 
method 
in [Stingray](https://docs.stingray.science/index.html) (A Python library for the analysis of astronomical time series). 


The [Stingray](https://stingray.science/) project is a sub-organization of [OpenAstronomy](https://openastronomy.org/), which is a collaboration between open-source astronomy and astrophysics projects to share resources, ideas, and to improve code.

### Proposed Deliverables:  

| Deliverables                                                     	| Status  	|
|------------------------------------------------------------------	|---------	|
| Implementation of the Bexvar method into Stingray infrastructure 	| Achived 	|
| Inclusion of tests to ensure code’s performance and stability    	| Achived 	|
| Complete documentation and tutorials for the method              	| Achived 	|

### Project Summary:
The Bexvar method have been implemented along with tests and documentation into the Stingray repository.  

The `bexvar()` method implemented in bexvar module facilitates users to obtain posterior distributions on the Bayesian excess variance, given a light curve data as input parameters.  
It is developed on the bases of the work by [Buchner et al. (2021)](https://arxiv.org/abs/2106.14529).
The modularized structure and support for default values of optional input parameters such as `frac_exp`, `bg_counts` and `bg_ratio` makes the method generalized and easy to use on any light curve data.  

The method has been tested with multiple functional and unit tests to ensure its reliability.  A detailed documentation along with tutorials have been created.  

In addition to the proposed deliverables, an effort to include `bexvar()` method as a method to Stingray’s `Lightcurve` class is in progress.
This work would also includes preliminary addition of new optional parameters (`frac_exp`, `bg_counts` and `bg_ratio`) into Stingray’s `Lightcurve` class.
This will enable users to use facilities provided by the `Lightcurve` class on data containing these attributes. 
Along with these the work will include support for non-uniform sampling in Stingray `Lightcurve`.
This will facilitate users to create Stingray `Lightcurve` object with non-uniform time bins and use `Lightcurve` class methods to analyse the data.

### Repositories:  
<https://github.com/StingraySoftware/stingray>   

<https://github.com/StingraySoftware/notebooks>  

### Pull Requests:  

| Pull Request                                                                  | Status   | Description                                                                                                                                          |
|-------------------------------------------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bayesian Excess Variance (Bexvar) in Stingray – GsoC’22 project](https://github.com/StingraySoftware/stingray/pull/664) | ![badge](https://shields.io/badge/PR-Merged-blueviolet?style=for-the-badge&logo=appveyor)    | The core of the project, includes implementation of bexvar() method,<br>along with documentation and tests                                           |
| [Add find_bexvar() method in Lightcurve class and its relevant tests – GsoC’22](https://github.com/StingraySoftware/stingray/pull/669) | ![badge](https://shields.io/badge/PR-Approved-success?style=for-the-badge&logo=appveyor)     | Contains work done to add `bexvar()` method in Stingray’s `Lightcurve` class, <br> addition of three new optional parameters in `Lightcurve` class and <br> work done to facilitate `Lightcurve` creation with non-uniform time sampling       |
| [Bexvar tutorial notebook](https://github.com/StingraySoftware/notebooks/pull/58)                                                      | ![badge](https://shields.io/badge/PR-In_Review-lightgreen?style=for-the-badge&logo=appveyor) | A jupyter notebook showcasing the usage of bexvar method with examples.<br>It also includes a section summarizing theoretical explanation of bexvar. |


### Beyond GSoC:

At the time of this writing, support for new parameters added in `Lightcurve` class is being worked upon.  
While the bexvar method is successfully implemented in Stingray, the logical next steps would be to work on improvement of its speed and investigate on possible vectorization of some of the internal functions.

### Acknowledgement:
I would like to thank my mentors, [Matteo Bachetti](https://github.com/matteobachetti) and [Daniela Huppenkothen](https://github.com/dhuppenkothen) for their continuous support during the entire project. It would not have been possible for me to complete this project without their incredible support and guidance. 
I am thankful for their careful PR reviews, for insightful suggestions on various aspects of project, for detailed explanations to my quarries and for providing me an overall positive and motivating environment for the project. I am very fortunate to have them as mentors for this project.
 

### Blogs:
List of blogs created during the scope of these project.  
•	[GSoC @ Stingray blog #0](https://medium.com/@mihirtripathi97/gsoc-stingray-blog-0-bb7ba9c5026c)  
•	[GSoC @ Stingray: Beginning of the journey. blog #1](https://medium.com/@mihirtripathi97/gsoc-stingray-beginning-of-the-journey-blog-1-7ed5a47bec65)  
•	[GSoC @ Stingray: Diving into coding period. blog #2](https://medium.com/@mihirtripathi97/gsoc-stingray-diving-into-coding-period-blog-2-f24a03c00014)  
•	[GSoC @ Stingray: Testing Testing Testing … #blog 3](https://medium.com/@mihirtripathi97/gsoc-stingray-testing-testing-testing-9d1572ac43ef)  

### Profiles:
LinkedIn:  <https://www.linkedin.com/in/mihir-tripathi>  
Github: <https://github.com/mihirtripathi97>  
Medium: <https://medium.com/@mihirtripathi97>


