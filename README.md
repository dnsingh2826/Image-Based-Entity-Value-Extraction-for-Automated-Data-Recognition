### Image-Based-Entity-Value-Extraction-for-Automated-Data-Recognition

This project focuses on automating the process of extracting entity values, such as weight, volume, dimensions, and voltage, from product images. The goal is to develop a machine learning pipeline capable of recognizing these key data points for structured output, enabling more efficient and accurate data processing across various industries, such as e-commerce and logistics.

#### Key Technologies

EasyOCR: Used for text recognition within images to extract entity values directly from product labels and packaging.
Google Cloud Vision API: Utilized for detecting entities in images with high accuracy, helping in label detection and extraction of complex values.
Python: Core programming language used for integrating machine learning models and APIs.
Machine Learning: Applied classification and regression models to predict the extracted entity values.
Computer Vision: Techniques used to preprocess images, detect areas of interest, and enhance feature extraction.

#### Approach

1. Data Collection
The project began with gathering a diverse dataset of product images that included visible entity values such as dimensions, weight, and other relevant specifications. Images were sourced from various product categories to ensure model robustness across different product types.

2. Preprocessing
Images were preprocessed using techniques such as resizing, grayscale conversion, and contrast enhancement to ensure optimal text and feature extraction.
Specific regions of interest (ROI) in the images, such as areas likely containing product labels, were identified and segmented for further analysis.

4. Text Extraction with EasyOCR
EasyOCR was employed to extract text from the product images, focusing on labels that mentioned key entities.
The OCR output was then cleaned and filtered to retain only relevant values such as dimensions and units (e.g., cm, kg, ml).

5. Entity Detection with Google Cloud Vision API
For images where text extraction alone wasn't sufficient, Google Cloud Vision API was used to detect and extract complex entities from product visuals.
The API's label detection feature helped identify specific elements like weight or volume, which were then mapped to corresponding values.

6. Feature Extraction and Validation
Custom algorithms were developed to validate and ensure the accuracy of the extracted values.
This included checking for unit consistency, eliminating noisy data, and predicting missing values where applicable using machine learning techniques.

7. Model Training and Value Prediction
Machine learning models were applied to classify and predict the entity values based on the extracted features.
These models were trained using a portion of the dataset, with a separate validation set to ensure the accuracy and generalization of predictions.

8. Output Generation
The final system was designed to generate structured output in a JSON or CSV format, with the extracted and predicted values organized by product.
This structured format ensures that the data can be easily integrated into downstream systems, such as inventory management or e-commerce platforms.
