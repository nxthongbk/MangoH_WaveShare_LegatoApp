# MangoH-Waveshare-Legato App
Legato App to display Waveshare eink via framebuffer 


### 1. Clone Legato app:
    

### 2. Generate Image Data :
Download Lcd2hex from link: https://www.waveshare.com/wiki/File:Image2Lcd.7z

* Open a picture with drawing tool comes with Windows system, create a new image, and set the pixel to 128x250 (real resolution: 122x250; logic resolution: 128x250).
    
* Because this module can only display two gray level (Only black and white), we need to convert picture to monochrome bitmap before converting it to array. That is, File --> BMP picture --> Monochrome Bitmap.
    There is a monochrome bitmap on examples pack for demonstration (raspberrypi/python/monocolor.bmp).
    
* Use Image2Lcd.exe software to generate corresponding array for picture (.c file). Open picture with this software, set the parameters:
    Output data type: C language array
    Scanning mode: vertical scanning
    Output gray: single color (gray level of two)
    Maximum width and height: 128 and 250
    Include the data of Image Header: Don’t check
    Inverse color: Check (Check: the white on image will be converted to 1, and black is converted to 0)
    
* Click Save, to generate .c file. Copy the corresponding array into your project, and you can display picture by calling this array.

<img align="left" src="https://user-images.githubusercontent.com/17214533/49282013-a1c8f500-f4c0-11e8-9dc5-7ce926a24903.png">

![marty-mcfly](https://user-images.githubusercontent.com/17214533/49282013-a1c8f500-f4c0-11e8-9dc5-7ce926a24903.png)

### 3. Update your Image Data and rebuild app

    Get data generate from Lcd2hex tool and update to IMAGE_DATA 

### 4. Install to app to MangoH Red and check Image on screen

    




