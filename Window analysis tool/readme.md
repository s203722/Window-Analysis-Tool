


## Step 1 - Download the tool

The tool will come in a zip-file with the tool and two folders. One folder for the BIM model that will be changed, and another folder with the model that has the changes saved.

## Step 2 - How to open the tool

Before opening the tool it is important that the model that will be analyzed is in the model folder. After making sure that is the case, the tool can then be opened.

For windows do the following:

The tool has to be opened in Blender. This will be done by first opening Blender. After this go to the fan “Scripting” where the tool can be dragged and dropped into Blender. The tool should now be open.

For mac:

To open the tool on mac you first have to open Blender through the terminal. To do this press “Command + Space Bar” and type in “Terminal”

After the terminal is open you then have to write the path of Blender and end it with “-con”

An example of this can be seen down below, where the path can be different depending on the Blender installation.

"/Applications/Blender.app/Contents/MacOS/Blender" -con

The following youtube video shows how to find the path and open Blender in the terminal

[https://www.youtube.com/watch?v=RbQCzk-ef3g](https://www.youtube.com/watch?v=RbQCzk-ef3g)

## Step 3 - How to run the tool

After opening the tool, you will have to make sure that “modelname” on line 23 is the same as the BIM model name. If that is not the case you will have to change the “modelname” to be equal to what the BIM model name is. Remember to have the BIM model name in quotation marks. An example of this could be: modelname = “LLYN - ARK”

  

You can now run the tool by either pressing the run script button below the scripting fan.

## Step 4 - How to see the results

To see the results you have to open the console window.

For windows:

To see the results of the analysis quickly you can open the console window by going to the “Window” fan and choosing “Toggle System Console”. Here you will be able to see the result of the analysis.

For mac

The results of the analysis can be found in the same terminal used to open Blender.

## Step 5 - How to change parameters

Parameters if a window requires a crane

The parameters the tool uses to check if the window requires a crane can be found in line 68.

![](https://lh7-us.googleusercontent.com/r2rQehUzZ5wRT9HfdNw1ttQo9XZvqu9xXHIuYthyyPfW2gkT0X--b8r2kaHDko_mQcLKsJn8ddbzP7Gar5ChXS_4LMsk1vmPe6WynaBP-ijkiyJ6E7pr_pLAxUitgGoSJdXdQYQZ9-dHAsG_-6flMw)

If you want to increase the height, workers can lift the window and change the first parameter called “z_coordinate”. If you want to change the area, change the second parameter “area”. The code means that if the window is higher than 1.5 m and has an area larger than 1.5 the window requires a crane. If one of these is above the given parameter the window requires a crane.

  

You can also change the area at line 70.

![](https://lh7-us.googleusercontent.com/k0Mt8LP30jq3Abm446B8VO25qH-xl1qOEHjr_bG1qTGTiQC9hx_hQyVcxj-ndpEx3BaqkFLK7GevvovV-gP3d0fJwBJ1jbabRFD6hIsSTHZI70sYo1ztxs-O8EpkfUAo6R4gg6zBHn6MU2o2XCiUrQ)

This also represents the area of the window. Meaning that if the window has a larger area than 6 m^2 it will require a crane, but it does not take the height into account, which means that all windows with an area larger than 6 m^2 needs a crane.

  

Change van name and size

The code to change the parameters for the van size and types can be found from line 119 to 124.

![](https://lh7-us.googleusercontent.com/Xw-AvklEmCvfLJUpRh1SWrtnVXfV-UTijXZKOr1DV7VQhsx0rJ46b8bBIoedFisnXXm1c9O4m41VUucaHq4g20mR0Qw2a0O-wV-bJBQE-73U2nXH_KEc1sZnhAKzzrN3-8mRAMLc1ZBJAYCIKZ5Q-g)

Here you can change the length and width of the vans and also what they should be called.

The “5 axeled truck” is for every window that does not fit in the smaller vans. If bigger vans are used the 5 axeled van might become obsolete.

  

Change window weight workers can carry

If you want to change the weight the workers can carry you have to go to line 154.

![](https://lh7-us.googleusercontent.com/J-myU-CxIznXv4-rXw53KtHgv27UgDW5fI3BmHdp6foMnCWWcQg9cFVYa1fsV3MI2u-A-6AxoaOussBbi-V5nAMAVURSeQUlMknJv8-pEhvBmavgUFqhQvLDGySNg6EoPGQEIA7kes2BxuzKBtWX8w)

Here you can change the total weight two workers can carry.

## Step 6 - Save changes

To save the changes use the code on line 228.

![](https://lh7-us.googleusercontent.com/TZSFUG_boQ77CEgHDMutBoCdZBMuHZfwWv4Mktv4i9wGjZff4MoLqIwy5IOSVozIufSUUdnqWyEJhxJbmO0_ZUtN6_rrCpyvK_tEi2aljgmRUgtqD5rTxZ9DVZsrjW2n2zw_TGi2Sx91F6QnW_iBXw)

Here you will have to delete the hashtag # and change the model_file_path to where the “LLYN - ARK - Output” is on your computer.
