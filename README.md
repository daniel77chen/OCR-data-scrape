# OCR-data-scrape
scrape data from ekg data image 

## what does this project do ##
* it will search your "unprocessed images folder (you'll have to set this up the first time) and use OCR on each to scrape the data you wanted and write them to an excel sheet (you'll have to set this up the first time)
* units will be deleted so it should just be digits and . in the cells of the excel
* if there were no errors, itll move all the files in the "unprocessed images folder" to the "processed images folder" (you'll have to set this up the first time)
* i stored the two folders as well as the excel in the same folder but you can do whatever you want. 

## how to use ##
1. download and install uipath studio community version 
2. download the contents of this repository (go to this [link](https://github.com/daniel77chen/OCR-data-scrape) then click code --> download zip) 
3. extract the contents of the zip and paste a folder containing the contents of this repo in your Uipath folder (most likely in your Documents folder if 
  you didnt mess around during installation) 
4. open your uipath studio app --> start --> open local project --> browse your File explorer and click on "project.json" inside your downloaded folder
5. click on "project" on the left side --> click on main.xaml
6. edit the Multiple Assign Activity, change the first file path to a folder where you'll store unprocessed images. right now it's "C:\Users\kim77\Pictures\Randy UiPath\UnProcessed Images"
  - dont forget the "" 
7. change the second file path as well to a folder where you'll store processed images
8. change the third file path as well to the excel document you want to edit 
9. save 
10. to run, click <ctrl F6>
  - do **NOT** have anything besides those images in the "unprocessed images folder", I forgot to prevent the user from doing that so yah. might cause it to crash or something
  - make sure your excel file is **NOT** open, it cannot edit the file while it's open and will cause the program to crash
  - dont touch the computer while it's running. it needs to have the image open to scan for text. takes around 15-20 sec per image 
  - when it's done, assuming there were no errors, the excel file should be updated (changes will be appended) and all images in the "unprocessed images folder will be moved to the "processed images folder"
    - **any images in the destination folder that have the same name as those in the source folder will be overwritten** 
11. in the future, just follow 4, 5, 10 to run the program
   
