## Install Dependencies:
========================

# Host Machine OS - Ubuntu.

1.# For Tesseract 4.0 perform following steps:
```
sudo add-apt-repository ppa:alex-p/tesseract-ocr
sudo apt-get update
sudo apt install tesseract-ocr
sudo apt install libtesseract-dev
```
2.# For OpenCV follow these steps:

cd to main project directory "i.e OCR_Cpp"

Then perform following steps:
```
$ cd openCV
$ cd Ubuntu
$ chmod +x * 
$ ./opencv_latest.sh
```
come out of the openCV directory(back to the OCR_Cpp directory)  

3.Run the following command with flags and options to make an executable of the ocr.cpp file as below:
 ```
$ g++ -O3 -std=c++11 ocr.cpp `pkg-config --cflags --libs tesseract opencv` -o ocr
```
4.Save the test image file in the current directory, for example ocrTestImage.png.

5.Run the executable along with the image file that you want to recognise the text of as follow.
```
$ ./ocr ocrTestImage.png
```
