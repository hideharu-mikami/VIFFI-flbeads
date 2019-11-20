-------------------------------------------

Copyright (c) 2019 Hideharu Mikami
Released under the MIT license
https://opensource.org/licenses/mit-license.php

-----Last Test Time: 2019/11/15/10:40 -----

Test Environment : Win 10 1809
NI LabVIEW Provessional Development System 18.0f2
NI Vision Development Module 2018 SP1

--------------------------------------------

There are 5 folders and 8 .vi files in this folder. The folders contain sub-VIs, which are needed for running the VIs. For reproduction of data in the paper, you need to download source image files at Google drive (see below).

Supplementary Fig.9
Supplementary Fig.10
Supplementary Fig.11b
Supplementary Fig.13
Supplementary Fig.15

Supplementary Fig.9.vi
Supplementary Fig.10.vi
Supplementary Fig.11b.vi
Supplementary Fig.11b-2.vi
Supplementary Fig.13.vi
Supplementary Fig.13-2.vi
Supplementary Fig.15.vi
Supplementary Fig.15-2.vi

-------------------------------------------

Instrallation guite

Step 1. Install LabVIEW.

Step 2. Activate your license.

Step 3. Install Vision Development Module.

Step 4. Copy the dataset to a local folder.

Typical installation time is 15 minutes.

--------------------------------------------

Supplementary Fig.9.vi

This code creates log intensity histograms for 8-peak fluorescent beads that evaluate imaging sensitivity of an instrument.

Step 1. Open Supplementary Fig.9.vi.

Step 2. Click "file path" and choose Supplementary Fig.9\CLDATA_vif.VIF (600 images of 8-peak fluorescent beads).

Step 3. Choose either 0 (ch1) or 1 (ch2) in "channel"

Step 4. Run the code. A histogram will show up. Boudaries between subpopulations should be manually set on "8peak boundary FL" (for ch1) and "8peak boundary PE" (for ch2). Then, "peak positions" is updated. "peak positions" indicates peak positions of the histogram except for the leftmost one (blank beads). 

Step 5. Read the peak position for blank beads in the histogram and input the value to "blank position" manually. Then, the detection limit is shown in "MESF".

Step 6. Histograms for a complete set of data can be reviewed by clicking "load file" and running the code.

Step 7. You can export data by right-clicking an object (histogram, table, etc.) and selecting "Expoprt".

Typical run time is a few seconds.


Reproduction instruction:

Step 1'. Download files from https://drive.google.com/open?id=1ZOGMh0ciH9KX7SS9-KzuTRumZ_shxH6g and put all the files in the same folder.

Step 2'. Click "file path" and choose CLDATA_vif.VIF (downloaded one).

Step 3'. Follow Steps 3-5 and 7.

Typical run time is several minutes.

--------------------------------------------

Supplementary Fig.10.vi

This code creates cropped images of cells and their mask images from raw image frames obtained by Camware (camera control software for pco.edge 5.5). 

Step 1. Open Supplementary Fig.10.vi

Step 2. Click "file path" and choose Supplementary Fig.10\testimages.tif (50 sample image).

Step 3. Run the code. Change the value of "frame index". If cell(s) are present in the frame, cropped images and mask images are created.

Step 4. If you click "review all imgs" and "save img" and run the code, cropped images are saved as binary files at the upper folder.

Typical run time is a few seconds.

--------------------------------------------

Supplementary Fig.11b.vi, Supplementary Fig.11b-2.vi, 

These codes create a detaset of area of 6-micrometer fluorescent beads from raw image frames.

Step 1. Open Supplementary Fig.11b.vi

Step 2. Click "filepath" and choose Supplementary Fig.11b\testimages.FIRE (600 images in a binary format).

Step 3. Run the code. Calculated diameter is shown at "diameter[um]". Diameter values are saved as a binary file (.info) in the same folder.

Step 4. Open Supplementary Fig.11b-2.vi

Step 5. Select a binary file, which contains diameter values, at "filepath".
 
Step 6. Run the code. Area values are shown in "area". You can export the data by right-clicking the object and selecting "Export".

Typical run time is a few seconds for both files.


Reproduction instruction:

Step 1'. Download files from https://drive.google.com/open?id=1ZOGMh0ciH9KX7SS9-KzuTRumZ_shxH6g and put all the files in the same folder.

Step 2'. Open Supplementary Fig.11b.vi and click "filepath" and choose a downloaded file.

Step 3'. Diameter values are saved as binary files (.info) in the same folder. All files in the same folder are processed automatically.

Step 4'. Follow Steps 4-6. All .info files in the same folders are loaded to generated a combined result.

Typical run time is several seconds.

--------------------------------------------

Supplementary Fig.13.vi, Supplementary Fig.13-2.vi, 

These codes create a detaset of diameter of 1-micrometer fluorescent beads from raw image frames.

Step 1. Open Supplementary Fig.13.vi

Step 2. Click "filepath" and choose Supplementary Fig.11b\testimages.FIRE (600 images in a binary format).

Step 3. Run the code. Calculated radius is shown at "radius[pixels]". Radius values are saved as a binary file (.info) in the same folder.

Step 4. Open Supplementary Fig.13-2.vi

Step 5. Select a binary file, which contains radius values, at "filepath".
 
Step 6. Run the code. Diameter values are shown in "diameter[um]". You can export the data by right-clicking the object and selecting "Export".

Typical run time is a few seconds for both files.


Reproduction instruction:

Step 1'. Download files from https://drive.google.com/open?id=1lSjP6xJzd7NAxGPubAGKoai3Rehm2V-M and put all the files in the same folder.

Step 2'. Open Supplementary Fig.13.vi and click "filepath" and choose a downloaded file.

Step 3'. Diameter values are saved as binary files (.info) in the same folder. All files in the same folder are processed automatically.

Step 4'. Follow Steps 4-6. All .info files in the same folders are loaded to generated a combined result.

Typical run time is several seconds.

--------------------------------------------

Supplementary Fig.15.vi, Supplementary Fig.15-2.vi, 

These codes create a detaset of diameters of 200-nm fluorescent beads from raw image frames.

Step 1. Open Supplementary Fig.15.vi

Step 2. Click "filepath" and choose Supplementary Fig.11b\testimages.FIRE (600 images in a binary format).

Step 3. Run the code. Calculated radii are shown at "radius ch1x[pixels]", "radius ch1y[pixels]", "radius ch2x[pixels]", and "radius ch2y[pixels]". Radii values are saved as a binary file (.info) in the same folder.

Step 4. Open Supplementary Fig.15-2.vi

Step 5. Select a binary file, which contains radii values, at "filepath".
 
Step 6. Run the code. Diameter values are shown in "widths [um] (red x, red y, green x, green y)". You can export the data by right-clicking the object and selecting "Export".

Typical run time is a few seconds for both files.


Reproduction instruction:

Step 1'. Download files from https://drive.google.com/open?id=1vVZy2GMDq9_zYuzHYQltyY8EYfa8UoOz and put all the files in the same folder.

Step 2'. Open Supplementary Fig.15.vi and click "filepath" and choose a downloaded file.

Step 3'. Diameter values are saved as binary files (.info) in the same folder. All files in the same folder are processed automatically.

Step 4'. Follow Steps 4-6. All .info files in the same folders are loaded to generated a combined result.

Typical run time is several seconds.


--------------------------------------------

