# image-captioning
Dataset: https://www.kaggle.com/datasets/adityajn105/flickr8k

Building machine learning models to caption images

# Image Captioning Project
## Data Collection and Pre-processing:
The dataset consisted of 8091 images and the pickle file had 25000 captions. The images were pre-processed by making them 224x224 pixels for uniformity.

# Methodology:
## Model 1: VGG16 + LSTM 
Model Architecture:

<img width="393" alt="image" src="https://github.com/user-attachments/assets/cc40ef68-c6e7-4e70-bd0d-1181894c985f" />

Accuracy and Loss Scores:

![image](https://github.com/user-attachments/assets/dee81dda-8f16-43da-a089-c2a5fe9014de)

BLEU Score: The BLEU scores calculated for images were on average 0.008, with only one 
image having a score of 1 (perfect prediction).

Predictions with images from the internet:

![image](https://github.com/user-attachments/assets/beb9b0f1-eefb-419a-a028-b9ce5bb6f405)
![image](https://github.com/user-attachments/assets/0101b9a1-967d-45ad-8dc2-7525b7a1b443)
![image](https://github.com/user-attachments/assets/88d693a0-a61b-42a1-a892-26534ad3d17b)
![image](https://github.com/user-attachments/assets/86996628-53bd-4c0c-938b-c7769cf26b11)
![image](https://github.com/user-attachments/assets/a7b6f742-0afe-4568-b045-af13eedad86d)

## Model 2: Inception + LSTM 
Model Architecture:

<img width="357" alt="image" src="https://github.com/user-attachments/assets/7583b37c-94da-4cca-942c-316f0b061330" />

Accuracy and Loss Scores:

![image](https://github.com/user-attachments/assets/9d8ec05b-cc04-4b8e-9a25-addc0f631f4f)

Predictions with images from the internet:

![image](https://github.com/user-attachments/assets/1d830577-a062-432f-ac2a-7d47d9e4ecdb)

# Limitations:
- Lack of GPU accessibility. Runtimes took really long due to everything being 
processed solely by CPU.
- This meant that we could not make use of more LSTM layers in decoding the captions.
- This also meant that we could not make use of dropouts and L2 regularization.
- With more GPU processing, We could make the models more accurate.

# Inference:
- Both models are predicting captions for the images decently although they both have lower accuracy scores.
- Model 1 had a much shorter runtime compared to Model 2.
- Both models could be made better by making the architectures more complex while also making sure that they are not being overfit on the train dataset.
- Having a bigger dataset could also make the models better at predicting images from the internet.
