# Diabetic Retinopathy
Diabetic retinopathy (DR), also known as diabetic eye disease, is a medical condition in which damage occurs to the retina due to diabetes mellitus. It is a leading cause of blindness. Diabetic retinopathy affects up to 80 percent of those who have had diabetes for 20 years or more. Diabetic retinopathy often has no early warning signs. Retinal (fundus) photography with manual interpretation is a widely accepted screening tool for diabetic retinopathy, with performance that can exceed that of in-person dilated eye examinations.

The below figure shows an example of a healthy patient and a patient with diabetic retinopathy as viewed by fundus photography (source):
![image](https://github.com/user-attachments/assets/618a7254-2f30-487d-b753-9cd7b79e85c5)





An automated tool for grading severity of diabetic retinopathy would be very useful for accerelating detection and treatment. Recently, there have been a number of attempts to utilize deep learning to diagnose DR and automatically grade diabetic retinopathy. This includes this competition and work by Google. Even one deep-learning based system is FDA approved.

Clearly, this dataset and deep learning problem is quite well-characterized.

A look at the data:
## Data description from the competition:

You are provided with a large set of high-resolution retina images taken under a variety of imaging conditions. A left and right field is provided for every subject. >Images are labeled with a subject id as well as either left or right (e.g. 1_left.jpeg is the left eye of patient id 1).

A clinician has rated the presence of diabetic retinopathy in each image on a scale of 0 to 4, according to the following scale:

0 - No DR

1 - Mild

2 - Moderate

3 - Severe

4 - Proliferative DR

Your task is to create an automated analysis system capable of assigning a score based on this scale.

...

Like any real-world data set, you will encounter noise in both the images and labels. Images may contain artifacts, be out of focus, underexposed, or overexposed. A major aim of this competition is to develop robust algorithms that can function in the presence of noise and variation.

# A minor problem!

Due to the large image file size, there are only 1000 files with labels and one csv file with the labels of all the images in the directory available in the kernel, as demonstrated below. The actual competition had on the order of 35,000 files so this is clearly a very small subset of the data. In addition, this is a highly imbalanced dataset.

Originally, I had aimed to create a model that would be close to the SOTA, but clearly, with only 1000 images that's not possible.

# AIM OF KERNEL: I will utilize transfer learning, oversampling, and progressive resizing on this small, imbalanced dataset. Given that many real-world datasets are also small and imbalanced, it will be interesting to see how far these techniques will take us.
