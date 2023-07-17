# Machine Learning and Genetic Variations: Insights into Disease Classification and Regression Modeling

### This is a repository of a machine learning project based on an aggregated genetic mutation database from ClinVar extracted from Kaggle.

## Abstract:

This study aimed to elucidate the relationship between the pathogenicity of genetic mutations and the classification of the resulting diseases, utilizing the ClinVar database. An intensive data cleaning process was performed, including handling missing values, detecting outliers, and eliminating irrelevant columns. During this phase, a critical observation was made: the allele frequencies for genetic mutations varied significantly across different databases. This discrepancy poses a significant challenge in the field of genomics, as it could potentially lead to misleading interpretations and outcomes in genetic disease classification. Despite this obstacle, various machine learning models were deployed on the refined dataset. Initial models, however, struggled due to the imbalanced 'CLASS' target variable, achieving a less than ideal accuracy of 76% and an R-squared of -0.25. Nevertheless, the exploration of the PolyPhen variable and 'Consequence' column yielded more promising results. The XGBoost model, when applied to the PolyPhen variable, reached an accuracy of 78.8% and an R-squared of 0.21. Further, the model targeted towards the 'Consequence' column resulted in an impressive accuracy of 93.4% and an R-squared of 0.957, indicating a strong model fit. In conclusion, our study underscores the complexities involved in genetic mutation classifications, including significant variances in allele frequencies across databases. Despite early challenges, our research demonstrated the robust potential of machine learning in decoding these intricacies and provided a solid foundation for future research in genetic disease classification.

## Original Dataset
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

## Results and Target Variables
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

## Conclusion
The research project sought to examine the relationship between the pathogenicity of genetic mutations and the classification of genetic diseases using the ClinVar database. We embarked on a rigorous data cleaning process, handling missing values, identifying outliers, and removing redundant or irrelevant columns. A keen focus on the dataset's allele frequency measures (AF_ESP, AF_EXAC, and AF_TGP) revealed differing counts of null values and potential collinearity issues, leading us to engineer a new feature to capture to mean of all columns considering they represent the same theoretical value. We applied various machine learning models, including Chi-Squared, PCA Reduction, Lasso Regression, Recursive Feature Elimination, Logistic Regression, Random Forest, and XGBoost to our refined dataset. Initial results produced an accuracy of 0.76 and an R-square value of -0.25. The error scores were less than optimal due in part to the imbalanced binary nature of the 'CLASS' variable. However, subsequent analysis of the PolyPhen variable, which categorizes the projected implications of genetic variations on protein structure and functionality, yielded more promising results. Our XGBoost model achieved an accuracy of 78.8% for this target and an R-squared value of 0.21. 

Analysis of the 'Consequence' column, detailing the specific types of mutations, further enhanced our understanding of genetic mutation classifications. A final model built using the 'Consequence' column as a target, achieved an impressive accuracy of 93.4%. The R-squared value of 0.957 signified that the model could explain 95.7% of the variance in the dependent variable, while the low MSE value of 0.505 pointed to a close fit between the model predictions and actual results. In conclusion, our findings underscore the complexity of genetic mutation classifications and the potential of machine learning to enhance our understanding of these variations. While initial results were challenging, subsequent analyses of different variables provided promising insights, laying the groundwork for future research in genetic disease classification.

## Limitations
Despite the promising results and valuable insights obtained from this study, there are certain limitations that should be acknowledged. Firstly, the predictive models developed in this project heavily rely on the quality and representativeness of the ClinVar genetic mutations dataset. Any biases or limitations present in the dataset, such as missing values or limited diversity in genetic variants, can impact the generalizability of the models. Additionally, although various preprocessing techniques and feature selection methods were applied, it is possible that some relevant information may have been overlooked or not effectively captured. Moreover, the performance of the models might vary when applied to different populations or datasets due to variations in allele frequencies and genetic characteristics. Furthermore, the choice of regression algorithms, while carefully selected, may not necessarily be the optimal choice for all scenarios. It is crucial to consider alternative algorithms and further explore their suitability for the specific problem domain. Lastly, as with any predictive model, it is important to interpret the results with caution and consider them as supportive evidence rather than definitive proof. Future research and validation studies involving larger and more diverse datasets would be beneficial to address these limitations and enhance the robustness and applicability of the predictive models.

## Future Work
Enhancing the model's performance through hyperparameter tuning and ensemble techniques.
Exploring other feature engineering methods and domain-specific knowledge.
Extending the model to handle multi-class classification or other related tasks.
Integrating the model into a web application or API for easy deployment and usage.
Create new project based on significant differences between Allele Frequency databases
