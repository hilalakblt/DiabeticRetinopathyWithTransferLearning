# Diabetic Retinopathy Detection Using Transfer Learning

Diabetic Retinopathy is the leading cause of blindness among the working-age adults (20-65). Because of diabetes, people’s eyes and their retinal blood vessels are damaged. Some symptoms of Diabetic Retinopathy include decreased distance and near vision, blurred and distorted vision. The number of patients who have Diabetic Retinopathy is predicted to increase 592 million in 2035.

The dataset is APTOS 2019 Retinal Images that was taken from Kaggle. There 3662 fundus images. The dataset has five levels of disease. (a)No DR, (b)Mild, (c)Moderate, (d)Severe and (e)Proliferative DR are categories of the disease. Their category distribution of images is 1805, 370, 999, 193, 295. Figure 2 shows the levels of diagnosis from No DR to Proliferative DR.

<img width="631" alt="Ekran Resmi 2023-02-28 23 18 44" src="https://user-images.githubusercontent.com/75835998/221968978-6fb80d0f-8c43-4eb3-9e8c-4dbe6968e547.png">

Because of the imbalance and low number of the dataset, the accuracy of train and validation was over 50%. So, the Random Over Sampling method was used to randomly duplicate examples in the minority class and it will also increase the number of total samples. After the Random Over Sampling method, the number of dataset images were increased to 9025 fundus images.

In addition, before the training step image processing techniques were applied by using OpenCV library. All of the images in the dataset were resized 250x250, histogram equalization[8] and median blur techniques were applied to images to pick out blood vessels. Also, in Figure 3 there is an histogram equalization. A colored retinal image had an uneven graph. After returning the image to a grayscale image from an RGB image, the histogram equalization technique was applied and the image had a more evenly distributed graph than the other.

<img width="356" alt="Ekran Resmi 2023-02-28 23 20 29" src="https://user-images.githubusercontent.com/75835998/221969293-f86675d8-a31e-4ac7-9336-ca9eec1f128c.png">

I trained the models with Adam optimizer because the Adam algorithm is a computationally efficient algorithm. For the activation function, Sigmoid function was used. I achieved the highest accuracy with 91% for EfficientNetB5 among all models and 82% accuracy for the validation dataset.

<img width="492" alt="Ekran Resmi 2023-02-28 23 22 37" src="https://user-images.githubusercontent.com/75835998/221969714-f18c6f9f-3088-4f28-ae63-b97cb5c846ed.png">


Also, you can read all documentation of the project from this link: https://docs.google.com/document/d/1QkEF7ps78nMqagXWxdMJ87k4QjEe3x8m/edit?usp=sharing&ouid=113027671940448470385&rtpof=true&sd=true
