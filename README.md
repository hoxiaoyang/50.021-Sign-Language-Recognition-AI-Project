# 50.021-Sign-Language-Recognition-AI-Project
Approximately 5% of the global population—over 360 million individuals—
 suffers from disabling hearing loss1. These individuals often face substantial
 challenges, ranging from communication barriers in daily interactions to expe
riences of social exclusion and discrimination.

Sign language recognition (SLR) is an important research area situated at the
 intersection of computer vision and natural language processing. It focuses on
 translating visual-gestural communication into structured linguistic representa
tions. In particular, isolated sign language recognition targets the identification
 of individual signs or phrases from discrete video sequences, without assuming
 grammatical or temporal continuity between consecutive signs.
 
 In this project, we decompose the broader objective of sign language trans
lation into two core components:

# Code Usage Guide
Before running our training and evaluation code, download the following datasets
 from the Kaggle competition page and place them in the input folder:
- **Complete dataset with csv, parquet, and json files:** https://www.
 kaggle.com/competitions/asl-signs
-  **Dataset in tfrecord format, split into 4 folds:** https://www.kaggle.
 com/datasets/hoyso48/islr-5fold
 To run our main preprocessing and training script, run all the cells in
 main_training_ script.ipynb from top to bottom in Kaggle. You can specify the model type that you want to train, in the second-last cell, by changing
 the model_type integer argument in get_model():
 - 1: cnn_transformers_model
 - 2: cnn_lstm_model
 - 3: cnn_gru_model 
 - 4: cnn_model
 - 5: transformers_model
 - 6: cnn_lintransformers_model
   
 To evaluate trained models (with .h5 file weights stored in our results folder),
 upload it to the Kaggle input folder and specify the path to the trained .h5
 model weights.
 
# Running the GUI
Before running our GUI, download the above mentioned datasets in a Kaggle
 notebook, placing them in the input folder. Upload the weights for the best
performing CNN + Transformer model. Go to https://dashboard.ngrok.com,
 and navigate to ”Your Authtoken” to fetch your personal authtoken. This is used by the ngrok agent to log into your account when a tunnel is started to host
 the UI online. To run our GUI, follow the instructions in the ui_for_demo.ipynb file. Run all the cells in a Kaggle notebook to host the interactive UI on ngrok with streamlit, using your personal ngrok token. Once the last cell is run, there should be a link that leads to the website UI.
 
# Project Overview
```
root/
│
├── eda.ipynb
├── Initial_Model     
│   ├── intial-bi-gru.ipynb
│   ├── intitial-cnn-lstm.ipynb
│   └── initial-gru.ipynb
│   └── intial_BLT.ipynb
├── results/
├── ui_for_demo.ipynb
├── main_training_notebook.ipynb
├── preprocessing_augmentations_walkthrough.ipynb
├── .gitignore
└── README.md
 
```

- `eda.ipynb:` Dataset analysis and visualization.
- `Initial_Model:` Directory containing initial model implementations.
  - `intial-bi-gru.ipynb:` Bidirectional GRU model.
  - `intitial-cnn-lstm.ipynb:` CNN-LSTM model.
  - `initial-gru.ipynb:` Basic GRU model.
  - `intial_BLT.ipynb:` Transformer-based model.
- `results:` Directory for storing model outputs.
- `ui_for_demo.ipynb:` Notebook for hosting the project UI.
- `main_training_notebook.ipynb:` Core training script.
- `preprocessing_augmentations_walkthrough.ipynb:` Data preprocessing guide.
- `.gitignore:` File specifying items to ignore in Git tracking.
- `README.md:` Project overview and instructions.



 

