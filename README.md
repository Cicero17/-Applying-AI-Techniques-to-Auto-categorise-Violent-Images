This project is based on the "Violent Scenes Dataset 2014", which is not publically available and should be obtaine by submitting a request to InterDigital (details at https://www.interdigital.com/data_sets/violent-scenes-dataset). The dataset contains features of scenes from Hollywood movies and Youtube video clips, which are annoated for the pressence of violence and other audio and vizual related concepts, such as screams and fire. The dataset is partitioned into 3 sets: dev (training), test and generalized (containing the Youtube clips).

This project consists of 2 jupyter notebooks: Utils and Main and an archive containing the models.

Utils contains functions used for: 
  saving (of the form save_, which also deal with data cleaning and making all the data arrays to be indexed per frame) and retrieving the data (of the form get_); 
  developing statistics (print_stats);
  extracting violence intervals from independent frame classification; 
  evaluation methods: k-fold-cross-validation, classic validation, MAP2014 metric (details at https://link.springer.com/article/10.1007/s11042-014-1984-4); 
  pre-processing methods: extracting pca vectors, standardization, one-hot-encoding compress; 
  post-processing methods: smooth, merge, decompress;
  models: saving, developing class weights;
  
Main contains the code for: manipulating the data, building the models, evaluating the models. The models presentd are: Decision Tree, Logistic Regression, Naive Bayes Classifier, Neural Networks. A general technique displayed in the context of the neural networks is the multi-task learning.

Requirements: tensorflow 2, scikit-learn, numpy, matplotlib, h5py, pickle.
