## Step 1 - Download the tool

The tool will come in a zip-file with the tool and two folders. One folder for the BIM model that will be changed, and another folder with the model that has the changes saved.

## Step 2 - How to open the tool

Before opening the tool it is important that the model that will be analyzed is in the model folder. After making sure that is the case, the tool can then be opened.

### For windows:

The tool has to be opened in Blender. This will be done by first opening Blender. After this go to the fan “Scripting” where the tool can be dragged and dropped into Blender. The tool should now be open.

### For mac:

To open the tool on mac you first have to open Blender through the terminal. To do this press “Command + Space Bar” and type in “Terminal”

After the terminal is open you then have to write the path of Blender and end it with “-con”

An example of this can be seen down below, where the path can be different depending on the Blender installation.

"/Applications/Blender.app/Contents/MacOS/Blender" -con

The following youtube video shows how to find the path and open Blender in the terminal

[https://www.youtube.com/watch?v=RbQCzk-ef3g](https://www.youtube.com/watch?v=RbQCzk-ef3g)

## Step 3 - How to run the tool

After opening the tool, you will have to make sure that “modelname” on line 24 is the same as the BIM model name. If that is not the case you will have to change the “modelname” to be equal to what the BIM model name is. Remember to have the BIM model name in quotation marks. An example of this could be: modelname = “LLYN - ARK” or see the picture below

![](https://lh7-us.googleusercontent.com/HPZrFemaf03UfvBBJI3s3xd2tqmsmJuiXu4tnQGOng6P0FEsKpZ_ufrMwZb-jr6dwvJY8_yG2XOeI7KcX7mPPXlCjzOg2GufkjYCvmh6jTaRf-O98spw6CSoz0uf4BhgsODf8ZYBzdGrgAQdWtvMuQ)

You can now run the tool by pressing the run script button below the scripting fan.

To check if the window has run correctly there should be a text called bpy.ops.text.run_script() in the lower left corner, see picture below

![](https://lh7-us.googleusercontent.com/z2PQfoU85_icos9_0bRhoqHHNWIxkR3gwSlXby9iWtowPd6zwul8uKdJOC3msWkQWE8PgRIhAtyshpjSrJlNec_1NzqDaGQGkoqee1qXxQi2NQnSGERZW2GaiQ5aKaa_xRL9A6chZG7yQRF_D12yBw)

## Step 4 - How to see the results

To see the results you have to open the console window.

### For windows:

To see the results of the analysis quickly you can open the console window by going to the “Window” fan and choosing “Toggle System Console”. Here you will be able to see the result of the analysis.

### For mac

The results of the analysis can be found in the same terminal used to open Blender.

## Step 5 - How to change parameters

### Parameters if a window requires a crane

The parameters the tool uses to check if the window requires a crane can be found in line 72.

![](https://lh7-us.googleusercontent.com/6r2bokoRpaZOHy5ouaQ1DbFzDz_K9CsetAOUNSD_DvEYUIvAxwZzKHextwtvLk4nPCuHdBIPbBsPqFiKIRg6tKNvRUZ_cVgSz1fPngwhAR0pShwvRl17VzABF-OvMjj-A81pWN5lJpQrzRHBC_QEZw)

If you want to increase the height, workers can lift the window and change the first parameter called “z_coordinate”. If you want to change the area, change the second parameter “area”. The code means that if the window is higher than 1.5 m and has an area larger than 1.5 the window requires a crane. If one of these is above the given parameter the window requires a crane.

  

You can also change the area at line 74.

![](https://lh7-us.googleusercontent.com/ZUjvBjYBLE5VrNJt4VjUeAOGvxuMRK3dpg6Cq4oDtkQaU_42fcJ2KNvYQwOyetUj4OnfdaJuJbBB1U_cbPZEFrU4SF_xbfE2E0URmN99tjxITR8SboE5DcetjU_IrYraOM16p0g8Dd3JqN09Y2gTOA)

This also represents the area of the window. Meaning that if the window has a larger area than 6 m^2 it will require a crane, but it does not take the height into account, which means that all windows with an area larger than 6 m^2 needs a crane.

  

### Change van name and size

The code to change the parameters for the van size and types can be found from line 128 to 133.

![](https://lh7-us.googleusercontent.com/GN_zzpdt-jC9AHynRgWPjDYW_RpPodkb7P3MMK1ovUuBmayk7nlCVWNPNpGczzbm_1bVXx2uWbifwQBG7WJVLKW3Yd4SgvOpQB2lFJlX6Gih5qHZzqXPci6P3iSb6ZAm-wsKstF1tCMNvz4fC1_OpQ)

Here you can change the length and width of the vans and also what they should be called.

The “5 axeled truck” is for every window that does not fit in the smaller vans. If bigger vans are used the 5 axeled van might become obsolete.

  

### Change window weight workers can carry

If you want to change the weight the workers can carry you have to go to line 164.

![](https://lh7-us.googleusercontent.com/b0BASEdDF4Rwrd_zVWq7-vyVs8ZhaMjkz_5ifjcsj9vbTlKzb5r8wf7cUOsHqaH6EiNws_AobJF2uxoHWYVToh66VgWALaL5B9qfmrRO5WIl_YIBv6p14qMPc2137Du7T7wNlvZjqx2o0IuHaZmRVw)

Here you can change the total weight two workers can carry.

## Step 6 - Save changes

To save the changes use the code on line 240.

![](https://lh7-us.googleusercontent.com/eEOJD_DfyAV1IdcLTY_FtOiD_elyvSQI7w4F7yMKLKUM-YrnmvC7TDKG1fTWN6sRi1RUekKjCM4YhYPkC5V2YsOQ0ch0q2vWeXH4fANit2A_jyF9eeO67Z-gRIx4SUnxePU7hiDXi52g1WmNwDllsg)

Here you will have to delete the hashtag # and change the model_file_path to where the “LLYN - ARK - Output” is on your computer.
