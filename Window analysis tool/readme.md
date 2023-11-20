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

After opening the tool, you will have to make sure that “modelname” on line 23 is the same as the BIM model name. If that is not the case you will have to change the “modelname” to be equal to what the BIM model name is. Remember to have the BIM model name in quotation marks. An example of this could be: modelname = “LLYN - ARK” or see the picture below

![](https://lh7-us.googleusercontent.com/0CbKWan4b8wLKPQe9FY55uEVfUzrb6ze0wm-0WWiuS291zMeySMo43WC3hY6dAu3fe7VZpJwFuKZGoaNO8N0iGnvpX_t_gwPrfM1k2Otu7DnavUhfedDgkK9jJLo-Mp6HjMhXzY8X6hY7TaEgaURJg)

You can now run the tool by either pressing the run script button below the scripting fan.

To check if the window has run correctly there should comesome text called bpy.ops.text.run_script() in the lower left corner, see picture below

![](https://lh7-us.googleusercontent.com/sCrVkbO4PeVjMFE8j9BT54J83EoRLOq0A9Cn2Sdi0zmoSBeijHp1t1cvjDCQv1Vi80JHKhepJTe6hxowWVgbSgkrHChZWVBfJb-w1-ibUBgGi8FXYY0t-_Psi9JrRxpgCdwC4aKNjAzEwY9zwj11Iw)

## Step 4 - How to see the results

To see the results you have to open the console window.

### For windows:

To see the results of the analysis quickly you can open the console window by going to the “Window” fan and choosing “Toggle System Console”. Here you will be able to see the result of the analysis.

### For mac

The results of the analysis can be found in the same terminal used to open Blender.

## Step 5 - How to change parameters

### Parameters if a window requires a crane

The parameters the tool uses to check if the window requires a crane can be found in line 68.

![](https://lh7-us.googleusercontent.com/hY4RkiDXyfTI3u-8QNIszMm0qF_cgF4YEs-0nQCNhkJeQEogy_aG4usbVznr9DgZRUvEdvGiLY__ySutNsByxE6bZpSBV6u5DdzJHOa_42Q6QYJsiI4r1gSH37N7CMASdhfSUe94nt8fyBzQGj5rSg)

If you want to increase the height, workers can lift the window and change the first parameter called “z_coordinate”. If you want to change the area, change the second parameter “area”. The code means that if the window is higher than 1.5 m and has an area larger than 1.5 the window requires a crane. If one of these is above the given parameter the window requires a crane.

  

You can also change the area at line 70.

![](https://lh7-us.googleusercontent.com/Vopl9YNETbQBTAQrvLVaMMsQpu1JgcBIBuNQpKTuQQiuM_EK2aCHw_17qfgAZuaeGAKHGfFv6mu0cde3fUu_uMGcgzpx9NG6fxNUKcV6QjeDENsqVFp9E1yOBNg_ETFTi2atKg0itDK2FJJjq_dDLA)

This also represents the area of the window. Meaning that if the window has a larger area than 6 m^2 it will require a crane, but it does not take the height into account, which means that all windows with an area larger than 6 m^2 needs a crane.

  

### Change van name and size

The code to change the parameters for the van size and types can be found from line 119 to 124.

![](https://lh7-us.googleusercontent.com/hzzxjkk6TFNIM8Wz43HUPcFzE3Bx1DpWhdgPCnC7-COzUdzOB7_1rgrh1NkzzDRMC9EXdw7CurJ-AG25HTZLRxECs_CYtY2sXsS-UxGrAr381rndlNl2ZC5R9E6jN8pqDAr3Ew5chLfd4DUYa5U2TA)

Here you can change the length and width of the vans and also what they should be called.

The “5 axeled truck” is for every window that does not fit in the smaller vans. If bigger vans are used the 5 axeled van might become obsolete.

  

### Change window weight workers can carry

If you want to change the weight the workers can carry you have to go to line 154.

![](https://lh7-us.googleusercontent.com/Q7TjjoDnTE9gOuHomS5y6mJY9cj4VD2ndUJZsrbxYPPokAToFhzZrrjQHrFQFf3keHHk54qCA6RqTT2SwqcD9GBi_dlfdfTwZSniXPX_go43W65-QwvChkGqDH9IgvCNDWNpJK2iDeT8QjruVR_jUg)

Here you can change the total weight two workers can carry.

## Step 6 - Save changes

To save the changes use the code on line 228.

![](https://lh7-us.googleusercontent.com/ts-puSunzfOinsI0R98tZbUo9cSo6_vjwiLB8Ba8gDTVi8xKs65BrqHjbMrI3oghTqhK7HB3am0IYbTO7lB-Gv2Y5DuAyJF1ymdl7C0lzvXn7k0KOCRaD9EL3R2LoOFEwZV_QAkRM4bnjjpe7OaPpw)

Here you will have to delete the hashtag # and change the model_file_path to where the “LLYN - ARK - Output” is on your computer.
