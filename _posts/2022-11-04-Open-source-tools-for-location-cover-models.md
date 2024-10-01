---
  layout: post
---

Updates 2022/11/04

Our paper on '[Open-source approaches for location cover models: capabilities and efficiency](https://link.springer.com/10.1007/s10109-021-00350-w)' has been published on Journal of Geographical Systems. This paper critically reviews the open source tools for location cover models (more specifically, MCLP and LSCP) using ArcGIS location-allocation analysis as the baseline.

So, what are location cover models? Location cover models aim to locate a set of facilities in potential locations in order to maximise the coverage of demand or to minimise the facilities needed. Two representative models are the Location Set Covering Model (LSCP) and Maximum Coverage Location Model (MCLP).

# SpOpt

"Spopt is an open-source Python library for solving optimization problems with spatial data". It comes from the region module in PySAL and now it is under active development. Note that this library is not reviewed in our paper as it came out after the paper.

I would highly recommend this library, as it is very handy and convenient. Moreover, it is not dependent on ArcGIS.

More details about this library can be found on [its Github repo](https://github.com/pysal/spopt) and [this paper](https://joss.theoj.org/papers/10.21105/joss.03330).

# ArcGIS location-allocation analysis 

This tool is part of the network analysis tools in ArcGIS, and it can be used within ArcGIS Desktop or ArcPy.

Three reasons for not using this tool:

1. It is not free and not open source
2. It only accommodates network distance
3. It uses heuristics to solve the models, so there is no guarantee that the solutions generated are optimal. Moreover, there is no warning or message on this issue, which is a bit misleading as users would think the solution is optimal.

See [this link](http://desktop.arcgis.com/en/arcmap/latest/extensions/network-analyst/algorithms-used-by-network-analyst.htm).

# PySpatialOpt

This is a Python library for location cover models. To use this package, you would need ArcGIS and QGIS to preprocess the data and to generate the service areas. It needs a mixed programming sovler to solve the problems, including lp_solve, Gurobi, CPLEX, XPRESS, and GLPK.

See [this link](https://github.com/apulverizer/pyspatialopt).

The author is also developing a similar open-source package called [allagash](https://github.com/apulverizer/allagash). As the author said, this one is a lot refined and intergrated with Geopandas and the ArcGIS API for Python, and the documentation is much better with full Jupyter notebook examples and a Docker image. 

# Maxcovr

This is a R package for MCLP and LSCP. See [this link](https://github.com/njtierney/maxcovr) for more details.

A limitation of this package is that it only uses the Haversine distance, which is a type of the greater distance distance.

# ELP Solver

This tool is a Excel worksheet and is based on Visual Basic language. Like ArcGIS, it uses heuristics to solve the models, so the solutions obtained are not necessarily optimal. Moreover, it is not scalable to big data. In the case police surveillance towers in York of our paper, there are 591 demand points and 1821 potential sites, leading to over five million rows of pairwise distance. ELP solver is unable to solve this problem, as the number of pairwise distance exceeds the maximum number of rows (1,048,576) in Excel.

See [this link](https://people.bath.ac.uk/ge277/index.php/flp-spreadsheet-solver/).

# Reference

1. Chen, H., Murray, A. T., & Jiang, R. (2021). Open-source approaches for location cover models: capabilities and efficiency. Journal of Geographical Systems, 23(3), 361–380. https://doi.org/10.1007/s10109-021-00350-w
2. Feng, X., Barcelos, G., Gaboardi, J. D., Knaap, E., Wei, R., Wolf, L. J., Zhao, Q., & Rey, S. J. (2022). spopt: a python package for solving spatial optimization problems in PySAL. Journal of Open Source Software, 7(74), 3330. https://doi.org/10.21105/joss.03330

