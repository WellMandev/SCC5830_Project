# SCC5830_FinalProject

Title: Identification of nitrogen nutritional status in Brachiaria brizantha cv. Xaraés applying segmentation and analysis image in RGB system.
Wellington Renato Mancin - NUSP:8458603
Abstract: The objective of this project is to indicate through color using RGB system if the forage grass Brachiaria brizantha cv. Xaraés has sufficient or deficient nitrogen status. To do this, it is necessary to obtain an image of the grass in the field under a black background, perform the image segmentation to extract only the diagnostic leaf of the grass and apply other processing so that through the average values in RGB it is possible to indicate if the area of pasture is sufficient or deficient in nitrogen.

# 1. Main Objective:
To indicate through leaf color of Brachiaria brizantha cv. Xaraés using RGB system, if this has sufficient or deficient nitrogen status, reling on the principle that N status of the plants can be describe by RGB wavelengths reflection, and that the leaf spectral signature can be accurately determined from field images acquired with a digital camera. 

# 2. The description of input images:
The file "Foto1.png", acquired by the student, is an example of an image obtained in the field, containing by the base in black background and leaves of Xaraés grass to be analyzed as to its composition in RGB. The RGB color can be converted to HSB color. The mean value RGB or HSB of leaf will be applied to vegetation indexes. Leaves texture will not be analyzed. Details image: 

![Original_img](https://github.com/WellMandev/SCC5830_Project/blob/master/Foto1.jpg)

# 3. The steps taken are:
Gaussian type low pass; histogram equalization to normalize intensity levels; image conversion in grayscale; segmentation - through the Otsu threshold. 
Details: The file "Foto1-bin.jpg" 

![Binarized_img](https://github.com/WellMandev/SCC5830_Project/blob/master/Foto1-bin.jpg)

After: apply erode function; replaces black background from original img to white. 
Details:The file "Foto1-segment.png"

![Segmented_img](https://github.com/WellMandev/SCC5830_Project/blob/master/Foto1-segment.jpg.png)

Next: extraction of the mean RGB value of grass leaves and color analysis with methods 'media_ind_cor()' and 'convertRGB_HSL()'.


# Conclusion:
The initial purpose was achieved generating the segmented image without the background, making it possible to extract RGB values only from the leaves of the grass.
All necessary steps have been successfully implemented using Java language. The code example can be seen in the "code" file.
![Code](https://github.com/WellMandev/SCC5830_Project/blob/master/code)
The greatest difficulties in implementing the code were:
- image conversion to array and array to image
- calculation of the value automatic Otsu treshold
- equalize histogram
- RGB to HSB conversion
