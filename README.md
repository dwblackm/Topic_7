# Topic_7
Python Module
This module will demonstrate how to use the clip tool to create a new shapefile which includes the area of interest for further commands to be executed later.
## Note


# clip
GRASS GIS module clip will allow the user to overlay a polygon on one or more target features (layers) and extract from the target feature (or features) only the target feature data that lies within the area outlined by the clip polygon. 

  




<img src="r_patch_smooth_overview.png" width=600 border=0><br>
Difference between fixed overlap width and spatially variable overlap.

<p>
For spatially variable overlap, options <b>parallel_smoothing</b>
and <b>difference_reach</b> can be specified.
Option <b>parallel_smoothing</b> smoothes the overlap zone in direction
parallel to the edge.
Option <b>difference_reach</b> enables to increase the sensitivity to higher
differences on the edges by taking maximum difference values in the cells
close to edges.

<img src="r_patch_smooth_parallel_smoothing.png" border=0><br>
Effect of <b>parallel_smoothing</b> option shown on overlap zone (created by specifying <b>overlap</b> option).
Image A shows result with value 3 and B with value 9.


Option <b>blend_mask</b> (experimental) can be used to specify which edges of
the input_a DEM should be excluded from the blending. This is useful when
DEMs A and B have identical edges (on the coast, for example) and we want
to preserve only A (not blend it with B along the coast).
The <b>blend_mask</b> raster can be created by digitizing area approximately around the excluded edges,
so that the edge of DEM A is inside the areas and the rest are NULLs.
This option requires more testing.

## Installation
Module r.patch.smooth must be run from GRASS GIS 7 environment. Within GRASS session, run in command line:

    g.extension r.patch.smooth url=https://github.com/petrasovaa/r.patch.smooth
