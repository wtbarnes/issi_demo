# Python Tools for Field-Aligned Hydrodynamic Models

This repo contains materials for my demo/presentation of using Python tools to configure, parse, 
and visualize results from field-aligned hydrodynamic models of flares for the ISSI Meeting ["Interrogating Field-Aligned Solar Flare Models: Comparing, Contrasting And Improving"](http://www.issibern.ch/teams/fieldsolflare/).

## Outline

**Title:** Collaborative Development of Python Tools for Configuring, Analyzing, and Visualizing Field-Aligned Hydrodynamic Simulations

* Discuss commonalities between 1D codes
  * Predict (roughly) the same quantities
  * With same shape (distance versus time)
  * Required inputs: boundary conditions, initial conditions, total time, loop length,...
* Differences?
  * Not all quantities common to all codes (e.g. HYDRAD computes electron and ion temperature, RADYN does not)
  * Configuration parameters tailored heavily to each code
* Common tasks
  * Parse results into some data structure as function of time and space
  * Plot hydrodynamic quantities as a function of space for multiple snapshots in time
  * Plot quantities as a function of time and space (i.e. time-distance plots)
  * Compute derived quantities (e.g. spectra, light curves)
* Current state:
  * Multiple tools in multiple languages (mostly IDL, some Python, others???) with lots of overlap
  * E.g. Will, Jeff, Steve all have their own tools for configuring, parsing, plotting HYDRAD
  * Often not a lot of thought goes into post-processing scripts; end up being messy, kludged together
  * Lots of time reinventing the wheel
  * If there is little code re-use, a lot of maintenance is required (or things break!)
  * Difficult to compare results
* Proposal (maybe a bit radical...)
  * Common API *across* field-aligned codes
  * Underlying logic separated from user-interface
  * Code *collaboratively* and *openly* developed in Python
  * Documentation and testing, best practices
* Demo of `hydrad_tools`
  * (Briefly) Configuring HYDRAD runs
  * Parsing HYDRAD results
  * Visualizing HYDRAD results
  * A prototype for applying `hydrad_tools` to RADYN
* TODOs at Meeting
  * Does anyone actually want this? Are we happy with current tooling? (totally fine!)
  * Agree on common functionality
  * Discuss an ideal interface


## Materials

* Slides? (a few to outline ideas)
* Jupyter notebook to demo parsing of HYDRAD results
* Jupyter notebook to demo parsing of RADYN results with same API
* Supplementary materials demoing `hydrad_tools` that can be discussed throughout the week