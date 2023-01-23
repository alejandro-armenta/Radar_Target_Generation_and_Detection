
2D CFAR Process:

I created 2 for loops that runs on each grid, then for each grid I sum up the noise values within training cells, I make sure not to sum up guard cells and the CUT cell. 

Then I average the noise level so that I can use it to threshold power values within the CUT cell.

After that I created a CFAROutput map that stores the thresholded values (1 or 0) based on the comparison of the RDM power value within the CUT cell and the threshold.


Selection of Training, Guard Cells and Offset:

I picked a grid dimension based on the RDM dimensions. So the range dimensions are larger than the doppler dimensions.

I chose the offset looking at the power values in the RDM map, so that the threshold should be above all the noise values.


Steps taken to suppress the non-thresholded cells at the edges:

So I initialized the CFAROutput map with zeros, in that way i didn't need to suppress edge cells.