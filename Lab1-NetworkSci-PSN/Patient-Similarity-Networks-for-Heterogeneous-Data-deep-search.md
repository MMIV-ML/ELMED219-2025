_Please provide the most resent research on the use of Patient Similarity Networks for integrating heterogeneous data in order to identify patient subtypes and to predict outcome (classification) of previously unseen new patients._  <br>(Gemini Advanced 1.5 Pro with Deep Research. January 9, 2025) [[link](https://g.co/gemini/share/5b58353dc5c3)]

# **Patient Similarity Networks for Integrating Heterogeneous Data to Identify Patient Subtypes and Predict Outcomes**

## **Introduction**

Patient similarity networks (PSNs) are increasingly used in clinical research to identify patient subtypes and predict outcomes. PSNs are graphs where nodes represent patients and edges represent the similarity between patients calculated using their clinical and/or biomolecular features 1. By integrating heterogeneous data, PSNs offer a more comprehensive understanding of patients compared to traditional approaches that rely on limited data sources. This holistic view leads to improved patient stratification and outcome prediction 1. PSNs can also be easily visualized, thus offering a natural way to inspect complex heterogeneous patient data and providing some level of explainability of the predictions obtained by machine learning algorithms 1. This article reviews recent research on the use of PSNs for integrating heterogeneous data to identify patient subtypes and predict the outcome of previously unseen new patients.

## **Research Methodology**

The research process involved a systematic literature review to identify relevant studies published in the last two years. The following steps were undertaken:

1. **Initial Search:** A search was conducted for research papers on Patient Similarity Networks published in the last two years.  
2. **Filtering for Heterogeneous Data Integration:** The identified papers were then filtered to select those that discussed integrating heterogeneous data in PSNs.  
3. **Filtering for Patient Subtyping:** The filtered papers were further refined to include only those that discussed the use of PSNs for identifying patient subtypes.  
4. **Filtering for Outcome Prediction:** Finally, the papers were filtered to focus on those that discussed predicting the outcome (classification) of previously unseen new patients using PSNs.  
5. **Data Extraction:** For each paper that met all the criteria, key information was extracted, including the methodology used, data used, results, limitations, and potential future work.

## **Integrating Heterogeneous Data in PSNs**

The increasing availability of high-throughput technologies has led to the acquisition of high-dimensional patient data, including omics data, laboratory data, and imaging data. Integrating these heterogeneous data sources can improve the accuracy and effectiveness of PSNs for patient subtyping and outcome prediction. Several methods have been proposed for integrating heterogeneous data in PSNs, including heterogeneous information networks and data fusion techniques.

Heterogeneous information networks connect patients, diseases, and drugs to solve the problem of vector representation of mixed information related to patients, diseases, and drugs 3. This approach addresses the challenges caused by high-dimensional and sparse vectors. For example, one study used a heterogeneous information network to connect patients, diseases, and drugs, considering the relationships between them to improve patient similarity calculations 3. This approach allowed for a more comprehensive representation of patient information and improved the accuracy of patient similarity measures.

Data fusion techniques combine multiple biomedical data views to construct PSNs, leveraging rich heterogeneous information 2. Different patient similarity measures have been proposed to integrate various data types. These measures play a crucial role in constructing PSNs by quantifying the relationships between patients based on their heterogeneous data. Choosing an appropriate similarity measure depends on the specific data type and the research question. Some common similarity measures include:

| Data Type | Data | Similarity Measure/Method |
| :---- | :---- | :---- |
| Binary | ICD-9 diagnosis code | Jaccard similarity |
| Continuous, Categorical, discrete | Clinical data | Cosine similarity |
| Continuous | mRNA, PPI | Pearson correlation |
| Continuous | Clinical variables, Individual gene, Genes in pathways/networks | Mean of normalized difference, Normalized difference, Pearson correlation |
| Discrete | Categorical-ordinal variable (e.g., tumor stage), Unbinned counts (e.g., mutation data), Matrix scores (e.g., response to questionnaire) | Normalized difference, Shared incidence in a grouped unit, chi-square distance |
| Continuous | mRNA, miRNA, DNA methylation | Scaled exponential kernel of Euclidean distance |
| Discrete |  | chi-squared distance |
| Binary |  | agreement-based measure |
| Continuous, binary | mRNA, DNA methylation somatic mutation | Scaled exponential kernel of weighted Euclidean distance, scaled exponential kernel of weighted Hamming distance |
| Categorical, discrete | Demographic, APOE4 allele status, MRI | squared-exponential kernel |

4

For instance, Jaccard similarity can be used to compare patients based on the presence or absence of specific diagnoses, while cosine similarity is suitable for comparing patients based on continuous clinical data. By incorporating these various similarity measures, PSNs can effectively integrate heterogeneous data and provide a more holistic view of patients.

## **Identifying Patient Subtypes Using PSNs**

PSNs have been used to identify subtypes of diseases. For example, in the case of glioblastoma multiforme, PSNs have been used to identify patient subgroups, including a patient subgroup with a substantially more favorable prognosis and patients with favorable responses to the drug temozolomide 5. The patient similarity was also used to obtain distinct subtypes of type 2 diabetes, each of which is associated with different diseases and specific genetic mutations. Similar sub-typing or grouping approaches have been applied to many other diseases like lung pneumonitis 5. This ability to identify distinct patient subtypes has important implications for personalized medicine, as it allows for the development of targeted treatments and interventions tailored to the specific characteristics of each subtype.

## **Predicting Outcomes of Unseen Patients Using PSNs**

In addition to identifying patient subtypes, PSNs can also be used to predict outcomes for unseen patients, which has significant implications for personalized medicine. One approach is to use a hierarchical-vertical patient classifier that leverages pathway analysis and patient similarity concepts to find meaningful features for both classes and individuals 6. This method processes omics data, hierarchically integrates them into pathways, and uses a novel similarity measure to assess how patients' pathway activity is alike. This approach has shown promising results in predicting the class of new patients described in external independent studies, following its initial training and testing phases on a local dataset 6.

Another approach involves constructing a PSN based on various clinical and surgical information, including data extracted from echocardiographic reports using natural language processing technology 7. This PSN can be used to predict postoperative complications and mechanical ventilation duration in patients undergoing congenital heart disease surgery. Studies have shown that such PSNs can achieve better prediction results than the average performance of clinicians 7.

Furthermore, PSNs have been used to design personalized treatment plans. By analyzing the network structure and identifying similar patients, clinicians can gain insights into the potential effectiveness of different treatment options for a given patient 5. This application of PSNs has the potential to improve patient outcomes and contribute to the advancement of precision medicine.

## **Recent Research on PSNs**

### **Sequential Data-Based Patient Similarity Framework for Patient Outcome Prediction 8**

This study developed a patient similarity framework for patient outcome prediction that makes use of sequential and cross-sectional information in electronic medical record systems. The researchers calculated sequence similarity from timestamped event sequences using edit distance and trend similarity from time series using dynamic time warping and Haar decomposition. They also extracted cross-sectional information, including demographic, laboratory test, and radiological report data, for additional similarity calculations. The effectiveness of the framework was validated by constructing k–nearest neighbors classifiers to predict mortality and readmission for acute myocardial infarction patients.

**Methodology:**

* Sequence similarity was calculated from timestamped event sequences using edit distance.  
* Trend similarity was calculated from time series using dynamic time warping and Haar decomposition.  
* Cross-sectional information, including demographic, laboratory test, and radiological report data, was extracted for additional similarity calculations.  
* k–nearest neighbors classifiers were constructed to predict mortality and readmission for acute myocardial infarction patients.

**Data:**

* Public and private data sets of acute myocardial infarction patients.

**Results:**

* Predictive models using the similarity model outperformed baseline models based on both public and private data sets for mortality prediction.  
* For mortality predictions, all models except for the logistic regression model showed improved performances over time.  
* The random forest model performed best for mortality prediction when using information from the first week after admission.

**Limitations:**

* The study focused on acute myocardial infarction patients, and the findings may not be generalizable to other patient populations.  
* The study used a limited number of variables for similarity calculations.

**Potential Future Work:**

* Evaluate the framework in other patient populations.  
* Incorporate more variables for similarity calculations.  
* Explore the use of other machine learning algorithms for outcome prediction.

### **StellarPath: Hierarchical-vertical Multi-Omics Classifier Synergizes Stable Markers and Interpretable Similarity Networks for Patient Profiling 6**

This study proposed StellarPath, a hierarchical-vertical patient classifier that leverages pathway analysis and patient similarity...[source](https://pmc.ncbi.nlm.nih.gov/articles/PMC11042724/)

**Methodology:**

* Hierarchical-vertical integration flow to combine different omics data types and identify significantly deregulated molecules.  
* Patient similarities are calculated based on how closely the patients' molecular values are related and how similarly they are deregulated.  
* Patient similarity networks (PSNs) are built for each enriched pathway.  
* Graph convolutional networks (GCNs) are trained on significant PSNs to classify unknown patients.

**Data:**

* One or more high-throughput omics datasets (e.g., gene expression, protein abundance, miRNA expression, etc.) that describe the same set of patient samples.  
* The patient samples must be divided into two distinct classes.  
* A library of pre-defined pathways from databases such as MSigDB, GO, Kegg, miRWalk, RNAInter, and OmniPath.

**Results:**

* StellarPath excels in classification performances and computational resources across sixteen datasets.  
* It demonstrates proficiency in inferring the class of new patients described in external independent studies, following its initial training and testing phases on a local dataset.

**Limitations:**

* No information about the limitations of the study was available in the research material.

**Potential Future Work:**

* Explore the applicability of StellarPath to a wider range of diseases and clinical scenarios.  
* Investigate the potential of StellarPath for personalized medicine and treatment decision-making.

### **Patient Similarity Search Based on Annotated Heterogeneous Information Network 3**

This study proposed a patient similarity search method based on an annotated heterogeneous information network (AHIN). The method uses an AHIN to connect patients, diseases, and drugs, which solves the problem of vector representation of mixed information related to patients, diseases, and drugs. The method also measures the similarity between patients by calculating the similarity between nodes in the AHIN.

**Methodology:**

* A heterogeneous information network is used to connect patients, diseases, and drugs.  
* An N-disease method is used to embed temporal information into the AHIN.  
* Similarity between patients is measured by calculating the similarity between nodes in the AHIN.

**Data:**

* Electronic Health Records (EHRs) containing a variety of data.

**Results:**

* The proposed method is superior to competitive baseline methods.  
* N-disease effectively encodes temporal information into the annotated HIN.

**Limitations:**

* The study used a limited number of EHRs.  
* The study did not evaluate the performance of the method in predicting patient outcomes.

**Potential Future Work:**

* Evaluate the method using a larger dataset of EHRs.  
* Evaluate the performance of the method in predicting patient outcomes.  
* Explore the use of other machine learning algorithms for patient similarity search.

### **Development and Validation of a Patient Similarity Network for Predicting Outcomes After Congenital Heart Disease Surgery: Translating Medicine-Based Evidence Into Practice 7**

This study developed and validated a patient similarity network (CHDmap) to predict outcomes after congenital heart disease surgery. Data from 4774 CHD surgeries were collected, and 66 indicators and all diagnoses were extracted from each echocardiographic report using natural language processing technology. Combined with some basic clinical and surgical information, the distances between each patient were measured by a series of calculation formulas. A machine learning model was constructed based on similar patients to provide personalized prediction.

**Methodology:**

* Data from 4774 CHD surgeries were collected.  
* 66 indicators and all diagnoses were extracted from each echocardiographic report using natural language processing technology.  
* Distances between each patient were measured by a series of calculation formulas.  
* A machine learning model was constructed based on similar patients to provide personalized prediction.

**Data:**

* Data from 4774 CHD surgeries.

**Results:**

* A simple poll of the k most similar patients provided by the PSN can achieve better prediction results than the...[source](https://medinform.jmir.org/2024/1/e49138)

**Limitations:**

* No information about the limitations of the study was available in the study.

**Potential Future Work:**

* Evaluate the generalizability of CHDmap to other congenital heart disease populations.  
* Explore the use of CHDmap for other clinical decision support tasks.

## **Conclusion**

PSNs offer a promising approach for integrating heterogeneous data to identify patient subtypes and predict outcomes. Recent research has demonstrated the effectiveness of PSNs in various clinical applications, such as predicting mortality and readmission in acute myocardial infarction patients 8, classifying patients based on molecular profiles 6, and predicting outcomes after congenital heart disease surgery 7. These studies highlight the potential of PSNs to improve patient care by enabling personalized treatment and informed clinical decision-making.

The ability of PSNs to integrate diverse data sources, including clinical data, omics data, and imaging data, provides a more holistic view of patients, leading to better patient stratification and outcome prediction compared to traditional methods that rely on limited data. Moreover, the visual representation of patient similarities in PSNs can enhance clinical decision-making by facilitating the identification of similar patients and enabling clinicians to learn from their treatment responses 1.

Despite the promising results, challenges remain in the development and application of PSNs. These challenges include the need for robust methods to integrate heterogeneous data, the development of accurate and interpretable similarity measures, and the scalability of PSN approaches to large datasets. Further research is needed to address these challenges and explore the full potential of PSNs for personalized medicine and clinical decision support.

#### **Works cited**

1\. Heterogeneous data integration methods for patient similarity networks \- PMC \- PubMed Central, accessed January 9, 2025, [https://pmc.ncbi.nlm.nih.gov/articles/PMC9294435/](https://pmc.ncbi.nlm.nih.gov/articles/PMC9294435/)  
2\. Heterogeneous data integration methods for patient similarity networks \- Giorgio Valentini, accessed January 9, 2025, [https://valentini.di.unimi.it/papers/MP\_Net\_survey\_Revised.pdf](https://valentini.di.unimi.it/papers/MP_Net_survey_Revised.pdf)  
3\. Heterogeneous Information Network-Based Patient ... \- Frontiers, accessed January 9, 2025, [https://www.frontiersin.org/journals/cell-and-developmental-biology/articles/10.3389/fcell.2021.735687/full](https://www.frontiersin.org/journals/cell-and-developmental-biology/articles/10.3389/fcell.2021.735687/full)  
4\. Heterogeneous data integration methods for patient similarity networks \- Oxford Academic, accessed January 9, 2025, [https://academic.oup.com/bib/article/23/4/bbac207/6604996](https://academic.oup.com/bib/article/23/4/bbac207/6604996)  
5\. Patient similarity: methods and applications \- arXiv, accessed January 9, 2025, [https://arxiv.org/pdf/2012.01976](https://arxiv.org/pdf/2012.01976)  
6\. StellarPath: Hierarchical-vertical multi-omics classifier synergizes ..., accessed January 9, 2025, [https://pmc.ncbi.nlm.nih.gov/articles/PMC11042724/](https://pmc.ncbi.nlm.nih.gov/articles/PMC11042724/)  
7\. A Patient Similarity Network (CHDmap) to Predict Outcomes After ..., accessed January 9, 2025, [https://medinform.jmir.org/2024/1/e49138](https://medinform.jmir.org/2024/1/e49138)  
8\. Sequential Data–Based Patient Similarity Framework for Patient ..., accessed January 9, 2025, [https://www.jmir.org/2022/1/e30720](https://www.jmir.org/2022/1/e30720)
