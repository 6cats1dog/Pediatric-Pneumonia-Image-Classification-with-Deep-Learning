![pnuemonia](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.news-medical.net%2Fnews%2F20201218%2FTransfer-learning-exploits-chest-Xray-to-diagnose-COVID-19-pneumonia.aspx&psig=AOvVaw3JAvBsyFEfYo5LEeNeb8yv&ust=1621698450950000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCLDY7NOP2_ACFQAAAAAdAAAAABAD)

# Pediatric Pneumonia Image Classification with Deep Learning

# Business Problem

In this project, the aim is to to build a deep neural network that trains on a large dataset for classification. In this case, we are using x-ray images of pediatric patients to identify whether or not they have pneumonia. The dataset comes from Kermany et al. on Mendeley.

#Context for Project

Pediatric pneumonia is responsible for the deaths of more than 800,000 young children worldwide each year, according to the United Nations Children's Fund (UNICEF).  These deaths occur almost exclusively in children with underlying conditions, such as chronic lung disease of prematurity, congenital heart disease, and immunosuppression. Although most fatalities occur in developing countries, pneumonia (see the image below) remains a significant cause of morbidity in industrialized nations.

#Dataset

The dataset of images ones from the Large Dataset of Labeled Optical Coherence Tomography (OCT) and Chest X-Ray Images published on 01/06/2018 by contributors Daniel Kermany,Kang Zhang, and Michael Goldbaum. This dataset contains thousands of validated OCT and Chest X-Ray images  described and analyzed in a larger article: "Identifying Medical Diagnoses and Treatable Diseases by Image-Based Deep Learning". The images are split into a training set and a testing set of independent patients.

# Method Used - CNN

CNN is a type of deep learning model for processing data that has a grid pattern, such as images, and designed to automatically and adaptively learn spatial hierarchies of features, from low- to high-level patterns. 

CNN is a mathematical construct that is typically composed of three types of layers (or building blocks): 
- convolution
- pooling,
- fully connected layers. 

The first two, convolution and pooling layers, perform feature extraction, whereas the third, a fully connected layer, maps the extracted features into final output, such as classification. A convolution layer plays a key role in CNN, which is composed of a stack of mathematical operations, such as convolution, a specialized type of linear operation. In digital images, pixel values are stored in a two-dimensional (2D) grid, i.e., an array of numbers, and a small grid of parameters called kernel, an optimizable feature extractor, is applied at each image position, which makes CNNs highly efficient for image processing, since a feature may occur anywhere in the image. As one layer feeds its output into the next layer, extracted features can hierarchically and progressively become more complex. The process of optimizing parameters such as kernels is called training, which is performed so as to minimize the difference between outputs and ground truth labels through an optimization algorithm called backpropagation and gradient descent, among others.

# Conclusion

Our model has 91.6% accuracy and has some error of approximately 8.33%. This means that there were some instances when the patient had pneumonia but was diagnosed as healthy. It was helpful to grayscale and limit the epochs by using early stopping to prevent overfitting of the model.

# Future Work

It is important to consider that there may be a potential for human error as well, which would be seen as a misdiagnosis. Work with cross-validating with a team of radiologist and/or pulmonologist would be helpful in making sure that our images where labeled correctly.

Future work would benefit from utilizing more data from populations such as adults and the elderly as well as from different parts of the world. This would allow us to generalize the data and increase the accuracy of diagnosis.

This model may be helpful as a primary screening test for patients. Since it has usable accuracy, this could flag a physician to examine the models determination and make the final confirmatory call on the diagnosis.
