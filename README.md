# Personalized-Cancer-Diagnosis

Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/

Data: Memorial Sloan Kettering Cancer Center (MSKCC)

Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/discussion/35336#198462

Problem statement :
    Classify the given genetic variations/mutations based on evidence from text-based clinical literature.

1.2. Source/Useful Links
    Some articles and reference blogs about the problem statement

    https://www.forbes.com/sites/matthewherper/2017/06/03/a-new-cancer-drug-helped-almost-everyone-who-took-it-almost-heres-what-it-teaches-us/#2a44ee2f6b25
    https://www.youtube.com/watch?v=UwbuW7oK8rk
    https://www.youtube.com/watch?v=qxXRKVompI8

1.3. Real-world/Business objectives and constraints.
    No low-latency requirement.
    Interpretability is important.
    Errors can be very costly.
    Probability of a data-point belonging to each class is needed.


1.4 STEPS FOLLOWED FOR SOLVING THE CASE STUDY:
    FIRSTLY,WE STARTED WITH LOADING DATA USING PANDAS LIBRARY.
    DID CLEANING,PREPROCESSING OF DATA USING VARIOUS NLP TECHNIQUES.
    DID EDA FOR UNDERSTANDING THE UNDERLYING PATTERN AND DISTRIBUTION OF DATA.
    CHECKED WHETHER EACH FEATURE IS IMPORTANT FOR FURTHER ANALYSIS USING UNIVARIATE ANALYSIS.
    CHECKED DISTRIBUTION OF CLASS LABEL AMONG TRAIN ,TEST, CV DATASET.
    BUILD A RANDOM MODEL TO FIND THE UPPERLIMIT OF THE LOGLOSS(== 2.5).
    GENERATED 9 CLASS PROBABILITIES RANDOMLY AND ENSURED THAT THEY SUM TO 1.
    USED ONE-HOT-ENCODING AND RESPONSE CODING FOR FEATURIZATION OF CATEGORICAL DATA.
    ON TEXT FEATURE WE USED BOW AND TFIDF AS FEATURIZATION TECHNIQUES AND TOOK ONLY TOP 1K FEATURES.
    BUILT MODEL ON EACH AND EVERY FEATURE TO ENSURE THAT THEY ARE USEFUL OR NOT.
    WE STARTED WITH NB AS OUR BASELINEMODEL AND THEN TRIED VARIOUS MODELS LIKE LOGISTIC REGRESSION,SVM,RF,STACKING,KNN ETC.
    SHOWED LOGLOSS FOR TRAIN,TEST,CV,MISCLASSIFICATION ERROR,CONFUSION MATRIX,PRECISION AND RECALL MATRIX FOR EACH MODEL .
    GAVE INTERPRETATION FOR EACH MODEL.
    DID FEATURE ENGINEERING BY COMBINING GIVEN FEATURE(GENE,VARIATION AND TEXT ) AS A NEW FEATURE.
    FINALLY GOT A LOGLOSS OF < 1.
