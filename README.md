# Brightness-AI-Image-Classification-
High school science fair project exploring how brightness affects AI image recognition's abilities 

Overview:
This project explores how artificial intelligence models perform image classification under varying brightness conditions. The goal is to evaluate how changes in     lighting affect model accuracy and reliability, and to analyze whether preprocessing techniques can improve performance in low-light or high-exposure images.

Research Question: 
How does the level of brightness affect the accuracy of an AI image recognition model?  

Hypothesis:
If the image is more distorted in terms of brightness, then the accuracy of an AI image recognition model will significantly decrease, especially when the brightness is lowered.  

Methodology: 
Procedure  

1) Create a main folder on the laptop labeled AI Distortion Project  

2) Within the main folder, create 10 subfolders each named brightness levels and the object name like pen(-100) and another subfolder named originals for a total of 11 subfolders 

3) Next, set up a clear consistent lighting source such as a desk lamp. Make sure lighting, angle the photo is taken, and distance from which photo is taken is the same throughout the data collection.  

4) Take 2 clear photos of the following objects (pencil, composition notebook, plastic spoon, plant, mug, iPad, eyewear, water bottle, shoes, and pen) to get a total of 20 images. 

5) Save and name each photo like pencil_01.jpg, pencil_02.jpg...pen_02.jpg and input all these into an Excel and save it to the originals folder.  

6) Open each original images on the iPhone 13 and use the phone editor to create 5 brightness levels for each photo and save all of these to the brightness folder of the respective object creating a total of 100 images. 

1st level – brightness of –100 

2nd level -  brightness of –50 

3rd level – brightness of 0 (original) 

4the level – brightness of 50 

5th level – brightness of 100  

7) Data augmentation is required to code the images to get 5 images of each original using rotations and reflections to get a total of 60 images to develop the model.  

8) Open Google Colab and start pre-processing the data, loading the libraries, and training the model of VGG16 base, VGG16 base + FFNN, and VGG16 base + FFNN + Data augumentation
9) Deploy the model using Hugging Face 
10) Input the images of the brightness distorted images and note whether the model classifies it correctly or not 
11) Calculate the accuracy of the model using the formula 
___________ (correctly identified) _____________ 
(Total number of trials at the respective brightness level for that object 
12) Record all the results in data tables  
13) Save the model and back up all images in USB drive for save storage

Results: 
- Model performance decreased as image brightness moved away from normal conditions.
- Low-light images produced the highest classification error rates.
- Preprocessing improved accuracy in several cases, especially in extreme lighting conditions.
-  As soon as the brightness was –50, the accuracy was roughly 70% and when the brightness was +50, the accuracy fell to 86%.
-  The accuracy of the model when the brightness was 100 was 80% while the accuracy when the brightness was 50 was 86%.
-  The model achieved the highest accuracy of 94% when the objects had the original brightness or the same brightness as the trained images. 
(See /figures folder or research paper for detailed graphs and charts)

Key Insights: 
- AI models are sensitive to lighting variation in image data.
- Data preprocessing can partially mitigate performance drops.
- Real-world image conditions (like poor lighting) significantly impact model reliability.

Tools and Technologies: 
- Python
- NumPy
- OpenCV
- TensorFlow
- Keras
- scikit-learn
- VGG16

Drawbacks: 
- Some objects were darker or lighter in colors
- Just 3 models were compared

Importance of these results: 
Understanding how brightness impacts the accuracy of an AI model has a significant impact on many fields such as medicine, self-driving cars, etc. For instance, when one is in the dark and tries to open their phone using the face ID, it wouldn’t recognize the image due to minimal lighting. However, if the same person is in a excessively bright area, the phone’s ability to recognize that person would be significantly higher. Another example is that medical diagnosis requires normal to greater amounts of brightness to reduce the chances of being misdiagnosed. So, MRI scans or X- ray scans require more light and would result in misdiagnosis or a disease
when the scans are captured in very minimal lightning. Misdiagnosis can happen even in ideal condition,but the chances of that would be very minute. These are just a few of the fields in which understanding the relationship between brightness and the accuracy of the AI model. Other fields include self-driving cars, surveillance, etc. Now in all fields listed above, improving the brightness conditions would result in higher accuracy even if the images are taken in differing lighting conditions. To sum it up, better brightness levels can positively impact AI models reliability, safety, and efficiency.

Future Improvements:
- Test more advanced models (CNN architectures or transformers)
- Expand dataset size and diversity


