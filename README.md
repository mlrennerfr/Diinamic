# Diinamic
Clustering analysis on single-molecule localization microscopy data


In contrast to the images obtained with optical microscopy, SMLM techniques generate datasets of molecular coordinates in 2D or 3D. Several approaches have been proposed to analyze the spatial organization and morphology of molecular clusters from this kind of data. However, many characteristics arising from the preparation of the sample as well as the targeted molecule itself make some type of algorithms more suitable than others. Some analysis strategies may be more appropriate than others depending on how the experiment was run. 
Diinamic is a MATLAB-based modulable sequence of cluster detection steps that couples a space fragmentation method with a local density calculation. The space fragmentation step can be done by using an intensity-thresholded rendered image (Diinamic-R) or Voronoi tessellation (Diinamic-V). This step helps reducing the relative importance of low-intensity signals arising from out of focus fluorophores or autofluorescence. 
In Diinamic-R, the use of a grid-based selection, whose grid size is based on the pixel size of rendered images, introduces a density criterium that also considers the localization precision. The use of the smallest possible grid size also made the choice of the size unambiguous, and the analysis independent of the shape and size of clusters.
Please refer to the article for more information about how the analysis is done and now parameters must be chosen:
Paupiah et al (2023). “Introducing Diinamic, a flexible and robust method for clustering analysis in single molecule localization microscopy”. Submitted to Biological Imaging.
If you have difficulties to implement the analysis, please contact marianne.renner@sorbonne-universite.fr

To use Diinamic, you have to:

1)	Perform single molecule detection on your recordings, correct for stage drift if needed and correct for multiple detection presence if possible. 

2)	Convert your detection data. Diinamic uses its proper data organization stored in .mat type files (Matlab). You can convert your data files from .csv format  into Diinamic format using ConvertData.m. 
On ConvertData window, choose the list of files to convert with "Load file(s) to convert" and indicate the column number that encodes the different type of data indicated on the window. By default, the column numbers correspond to .csv files produced by ThunderSTORM. 
Please ask for help if your data is different and you do not know how to modify the code.

3)	Select ROIs using Segment.m.

4)	Run Cluster.m to choose the type of clustering analysis.

There are help files (help folder) to use Segment.m and Cluster.m GUIs.






