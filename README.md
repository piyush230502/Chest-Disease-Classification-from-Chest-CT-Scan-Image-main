### Chest Disease Classification from Chest CT Scan Images

**Overview**

The "Chest Disease Classification from Chest CT Scan Images" project leverages deep learning to analyze and classify chest CT scan images. Its primary goal is to provide an automated solution for detecting various chest diseases based on imaging data. By integrating machine learning pipelines with a user-friendly interface, this project aims to support medical professionals and enhance diagnostic accuracy. Below is a detailed exploration of the project’s components, workflow, and key features.

#### Key Features

1. **Automated Classification Pipeline**:
   - The project implements a machine learning pipeline for classifying chest CT scans.
   - The pipeline is encapsulated within a Python module and executed via the `PredictionPipeline` class, which processes input images and outputs predictions.

2. **Web Application**:
   - A Flask-based web application serves as the front-end interface.
   - Users can upload chest CT scan images and receive real-time classification results.

3. **Dockerized Deployment**:
   - A `docker-compose.yml` file ensures the application can run in a containerized environment, simplifying deployment and scalability.
   - The Docker setup includes port mapping for seamless integration with host systems.

4. **Environment Setup**:
   - The project specifies dependencies in a `requirements.txt` file.
   - Users can easily set up the environment using Conda and pip, ensuring reproducibility.

---

#### Workflow

The project’s workflow is divided into several stages:

1. **Configuration**:
   - Configuration files such as `config.yaml` and `params.yaml` define model parameters and data processing settings.
   - These configurations enable modularity and flexibility, allowing users to fine-tune the pipeline for different datasets or classification tasks.

2. **Data Preparation**:
   - External datasets, linked via the README, are preprocessed to align with the model’s requirements.
   - The preprocessing pipeline likely involves resizing, normalization, and augmentation of CT scan images.

3. **Model Training**:
   - Although the uploaded files focus on deployment, the project’s structure suggests an integrated training pipeline, defined within `src` modules.
   - The trained model is stored and utilized for inference in the `PredictionPipeline` class.

4. **Inference and Prediction**:
   - The Flask application facilitates image uploads, decodes the input, and passes it to the prediction pipeline.
   - Results are displayed to the user in a simple and intuitive format.

---

#### Implementation Details

1. **Flask Web Application (`app.py`)**:
   - The `app.py` script initializes the Flask app and integrates it with the prediction pipeline.
   - Key components:
     - **Image Decoding**: Handles image uploads and prepares them for prediction.
     - **Prediction Pipeline**: Loads the trained model and executes inference.
     - **Routing**: Provides endpoints for image upload and prediction, ensuring a seamless user experience.

2. **Logging (`demo.py`)**:
   - A simple logging mechanism records application events, aiding debugging and monitoring.

3. **Containerization (`docker-compose.yml`)**:
   - Defines the application’s container structure, enabling consistent deployment across environments.
   - Exposes the application on port 8080 for external access.

---

#### Setup Instructions

To replicate and deploy the project, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone [<repository_url>](https://github.com/piyush230502/Chest-Disease-Classification-from-Chest-CT-Scan-Image-main.git)
   cd Chest-Disease-Classification-from-Chest-CT-Scan-Image
   ```

2. **Set Up the Environment**:
   ```bash
   conda create -n chest python=3.8 -y
   conda activate chest
   pip install -r requirements.txt
   ```

3. **Run the Application**:
   ```bash
   python app.py
   ```

4. **Docker Deployment**:
   - Build and run the Docker container using the following command:
     ```bash
     docker-compose up --build
     ```

#### External Resources

1. **Dataset**:
   - The dataset for training and inference is linked in the README file. Users can download it from [Google Drive](https://drive.google.com/file/d/19odgbXzJEu5y-LeVg1h2-lpZl6hDOZ5i/view?usp=sharing).


#### Future Improvements

The project has significant potential for expansion:

1. **Enhanced Model Training**:
   - Integrate advanced deep learning architectures (e.g., ResNet, EfficientNet) for improved accuracy.
   - Implement transfer learning techniques to leverage pre-trained models.

2. **Real-Time Deployment**:
   - Deploy the application on cloud platforms (e.g., AWS, GCP) for real-time access.

3. **Comprehensive Logging**:
   - Extend the logging mechanism to capture detailed application metrics and usage statistics.

4. **User Interface Enhancements**:
   - Develop a more sophisticated front-end using frameworks like React or Angular.
   - Provide visual feedback, such as annotated CT images highlighting areas of concern.

---

### Conclusion

The "Chest Disease Classification from Chest CT Scan Images" project is a robust framework for medical image analysis. By combining machine learning pipelines, a user-friendly interface, and containerized deployment, it bridges the gap between technology and healthcare. While the current implementation demonstrates significant promise, future enhancements can further refine its performance and usability, paving the way for broader adoption in clinical settings.



 - [Data link](https://drive.google.com/file/d/19odgbXzJEu5y-LeVg1h2-lpZl6hDOZ5i/view?usp=sharing)

## Workflows

1. Update config.yaml
2. Update params.yaml
3. Update the entity
4. Update the configuration manager in src config
5. Update the components
6. Update the pipeline 
7. Update the main.py
8. Update the dvc.yaml 



## Git commands

```bash
git add .

git commit -m "Updated"

git push origin main
```

## How to run?

```bash
conda create -n chest python=3.8 -y
```

```bash
conda activate chest
```

```bash
pip install -r requirements.txt
```

```bash
python app.py
```

### Mlflow dagshub connection uri

```bash
MLFLOW_TRACKING_URI=https://dagshub.com/entbappy/Chest-Disease-Classification-from-Chest-CT-Scan-Image.mlflow \
MLFLOW_TRACKING_USERNAME=entbappy \
MLFLOW_TRACKING_PASSWORD=6824692c47a369aa6f9eac5b10041d5c8edbcef0 \
python script.py
```


### RUN from bash terminal

```bash
export MLFLOW_TRACKING_URI=https://dagshub.com/entbappy/Chest-Disease-Classification-from-Chest-CT-Scan-Image.mlflow

export MLFLOW_TRACKING_USERNAME=entbappy 

export MLFLOW_TRACKING_PASSWORD=6824692c47a369aa6f9eac5b10041d5c8edbcef0

```



### DVC cmd

1. dvc init
2. dvc repro
3. dvc dag
