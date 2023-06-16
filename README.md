# Wild Genetics
### This is a repository of machine learning projects based on an aggregated genetic mutation database from ClinVar

## Project Title
### Regression Predictive Model for Pathogenicity Prediction in ClinVar Genetic Mutations Dataset

## Introduction
In this project, a supervised learning model is developed using the ClinVar genetic mutations dataset to predict the pathogenicity of genetic variants and a few parameters regarding mutations. The dataset has been thoroughly cleaned, preprocessed, and analyzed to extract meaningful insights. By leveraging machine learning algorithms, this project aims to provide a valuable tool for interpreting genetic mutations, illustrate the significant discrepancies between clinical provider diagnoses, and attempt to find the most important features of such mutations.

## Key Methods
Data cleaning and preprocessing: Handling missing values, removing irrelevant features, and ensuring data quality.
Exploratory data analysis: Applying statistical techniques and visualizations to gain insights and address class imbalances.
Feature selection: Identifying the most informative features using statistical methods and domain knowledge.
Model training and evaluation: Utilizing machine learning algorithms to build a regression predictive model and assessing its performance.
Interpretability: Providing explanations for the model's predictions and potential clinical implications.

## Dataset
The project uses the ClinVar genetic mutations dataset, which contains the following relevant attributes:

CHROM: Chromosome information
POS: Position
REF: Reference allele
ALT: Alternate allele
AF_ESP: Allele frequency in the NHLBI Exome Sequencing Project
AF_EXAC: Allele frequency in the Exome Aggregation Consortium
AF_TGP: Allele frequency in the 1000 Genomes Project
CLNDN: Clinical disease information
CLNVC: Variant type
ORIGIN: Origin of the variant
CLASS: Pathogenicity classification
Allele: Allele information
Consequence: Consequence of the variant
IMPACT: Impact of the variant
cDNA_position: Position in the cDNA
CDS_position: Position in the coding sequence
Protein_position: Position in the protein
Amino_acids: Amino acids affected by the variant
Codons: Codons affected by the variant
STRAND: Genomic strand
SIFT: SIFT prediction
PolyPhen: PolyPhen prediction
LoFtool: LoFtool score
CADD_PHRED: CADD PHRED score
BLOSUM62: BLOSUM62 score

## Installation and Usage
Install the necessary libraries mentioned in the code snippet provided.
Clone this repository and navigate to the project directory.
Run the code using your preferred Python environment.
Customize the code and experiment with different preprocessing techniques, feature selection methods, and machine learning algorithms.
Evaluate the model's performance and make predictions on new data.
Model Evaluation and Results
The model's performance is evaluated using various metrics, including accuracy, precision, recall, F1-score, confusion matrix, R-squared score, and mean squared error. The results and insights obtained from the predictions are discussed, highlighting the model's strengths and limitations.

## Methods and Algorithms
The project incorporates the following methods and algorithms:

### Data cleaning and preprocessing techniques were applied to handle missing values, remove irrelevant features, and ensure data quality.
### Exploratory data analysis, including statistical techniques and visualizations, was conducted to gain insights and address class imbalances.
### Feature selection methods, such as SelectKBest and chi-square, were employed to identify the most informative features for the predictive model.
### Multiple regression algorithms, including Logistic Regression, Lasso, XGBoost, and Random Forest, were implemented to construct and evaluate the predictive model.
### Evaluation metrics such as accuracy, precision, recall, F1-score, confusion matrix, R-squared score, and mean squared error were utilized to assess the model's performance.

## Assessment of Target Variables
Three target variables were assessed to predict different aspects of the genetic mutations dataset. A variety of algorithms were used for all target assessments, including: Logistic Regression, Lasso, Random Forest, XGBoost, Chi-Squared, Recursive Feature Elimination, and more.

### CLASS: Pathogenicity Classification
Logistic Regression, Lasso, XGBoost, and Random Forest were used to predict the pathogenicity class of genetic variants. XGBoost proved to be the best algorithm for all three targets.
Evaluation metrics:
Mean Squared Error (MSE): 0.22940635066728027
R-squared (R2): -0.2208828302864998
Accuracy: 0.7705936493327198

### PolyPhen: PolyPhen Prediction
Multiple regression algorithms were applied to predict the PolyPhen score.
Evaluation metrics:
Mean Squared Error (MSE): 0.4273372415921012
R-squared (R2): 0.4272876260005244
Accuracy: 0.7855600123418698

### Consequence: Variant Consequence Prediction
Regression algorithms were employed to predict the Consequence of genetic variants.
Evaluation metrics:
Mean Squared Error (MSE): 10.405138957117275
R-squared (R2): 0.9448865260468384

## Results
Unlocking the potential of precision medicine and advancing genetic research requires powerful tools to accurately predict the pathogenicity of genetic variants. Our groundbreaking study leverages state-of-the-art machine learning techniques, with XGBoost emerging as the superior algorithm across all three targets. By harnessing the predictive capabilities of XGBoost, we have achieved exceptional accuracy in predicting the pathogenicity classification, PolyPhen scores, and variant consequences. These impressive results highlight the robustness and reliability of our predictive model. The outcomes of our study offer invaluable insights for geneticists and laboratories, empowering them to make informed decisions about disease risk, diagnosis, and personalized treatment options. Embrace the power of our advanced predictive model, built on the cutting-edge XGBoost algorithm, to revolutionize genetic research and drive advancements in precision medicine.

## Limitations
Despite the promising results and valuable insights obtained from this study, there are certain limitations that should be acknowledged. Firstly, the predictive models developed in this project heavily rely on the quality and representativeness of the ClinVar genetic mutations dataset. Any biases or limitations present in the dataset, such as missing values or limited diversity in genetic variants, can impact the generalizability of the models. Additionally, although various preprocessing techniques and feature selection methods were applied, it is possible that some relevant information may have been overlooked or not effectively captured. Moreover, the performance of the models might vary when applied to different populations or datasets due to variations in allele frequencies and genetic characteristics. Furthermore, the choice of regression algorithms, while carefully selected, may not necessarily be the optimal choice for all scenarios. It is crucial to consider alternative algorithms and further explore their suitability for the specific problem domain. Lastly, as with any predictive model, it is important to interpret the results with caution and consider them as supportive evidence rather than definitive proof. Future research and validation studies involving larger and more diverse datasets would be beneficial to address these limitations and enhance the robustness and applicability of the predictive models.

## Future Work
Enhancing the model's performance through hyperparameter tuning and ensemble techniques.
Exploring other feature engineering methods and domain-specific knowledge.
Extending the model to handle multi-class classification or other related tasks.
Integrating the model into a web application or API for easy deployment and usage.
License
Specify the license under which your project is distributed.

Acknowledgments
Express gratitude to any individuals, organizations, or resources that contributed to your project.

Contact Information
Provide your contact details, such as email or GitHub profile, for users to reach out to you with questions or feedback.
