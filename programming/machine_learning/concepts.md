# Concepts 

## Terminology

- **Supervised Learning:** The training data given to the algorithm has a desired solution and is paired with data as labels. 
    - **Includes:** Classification & Regression 

- **Unsupervised Learning:** The training data given has no desired solution as nno labels are provided. 
    - **Includes:** Clustering, Association, Visualization, Anomaly & Noveltly Detection 

- **Semisupervised Learning:** Algorithm is designed to handle labeled and unlabled data. Labelled data is unsed to classify unlabelled data. 
    - **Includes:** A combination of supervised and unsupervised algorithms

- **Reinforcement Leanring:** The algorithm chooses actions, based on this it receives rewards or penalties, the algorithm updates its logic based on this. 

- **Batch Learning:** Model needs to be trained on the whole dataset, if it needs to be re-trained it needs to be train again on the whole dataset and launched again. 

- **Online Learning:** "Incremental Learning" - Learning is incremental based on some learning rate, but needs to be monitored to ensure it does not deteriorate (ex: overfitting).

- **Instance Based Learning:** System memorizes samples and then generalizes between learned and new samples. 

- **Model Based Learning:** Selection and training of the model to make predictions
    - **Utility/Fitness Functions:** Measure of how good the model is. 
    - **Cost Function:** Measure of how bad the model is. 

## Data Quality
Typical issues with data to monitor: 
- **Insufficient Quantity**
- **Non-Representitive**
    - Sampling noise
    - Sampling bias 
- **Poor Data Quality**
- **Irrelevant Features**
- **Overfitting:** Model does not generalize well
    - Model is too complex reletive to data
    - Needs more training data 
    - Noise is skewing the model 
- **Underfitting:** Model is too simple reletive to data

### Testing/Validation 
Split data into training and testing data; typically 80% training and 20% testing.
Low training error + high test error => overfitting

**Validation Set:** A set of the training data that is used to test model candidates to determine which should be trained on the full dataset. 