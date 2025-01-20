# AI_vs_Real
Deepfake Detection CNN

Vanya Shrivastava
vanyashr@usc.edu 

Can you distinguish an AI-generated image from a real one? I created a CNN that can!

I found a dataset on Kaggle with over 3200 images of both AI-generated headshots and real. Please visit: https://www.kaggle.com/datasets/shahzaibshazoo/detect-ai-generated-faces-high-quality-dataset 

To preprocess the data, I rescaled all images identically. I also augmented the data further by incorporating variations such as rotated images and width and height adjustments. Furthermore, the dataset had not been divided into train, test, and split directories; its original directories were AI and real. So, I had to create directories for training and testing and split them among each. 

I used a simple CNN architecture and the binary entropy loss function for binary classification. I also used the pre-trained model VGG16, a CNN for image recognition, and customized it to apply to the deepfake detection situation. I used Adam optimization and binary-cross entropy for loss, and the metric for success was accuracy.  

Because of the compilation techniques I used, the model had a 97.8% test accuracy. This model could be equipped commercially for people to upload their images and determine whether they are AI-generated. Please visit: https://www.linkedin.com/posts/vanyashrivastavaa_ai-deepfakes-technology-activity-7286121286131412993-yWSu?utm_source=share&utm_medium=member_desktop

While uploading newly generated and hyperrealistic deepfakes, the model repeatedly classified them as real images. This could be due to the lack of diversity in the data set. Furthermore, deepfake technology is rapidly advancing and detection algorithms are trailing behind. 

To continue this project, I would implement a Grad-CAM to understand which features lead the CNN to conclude that certain images are real or AI. This can help us determine which features to look out for to determine whether something is AI-generated or not. 

OpenAI. "Development Assistance for AI Face Image Detector Code by ChatGPT, Large Language Model." OpenAI, 2025. https://chatgpt.com.
