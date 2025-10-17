**1) Machine Learning Applications in Corporate Sustainability and Water Stewardship**

The main application of machine learning algorithms in the sustainability sphere centers around the prediction of the ESG score in relation to other indicators. Notably, Subrama-
niam, **R. K. et. al. (2024)** used ARIMA models and decision trees to capture the non-linear relationships through which CSR committees and ESG initiatives affect corporate 
sustainability. The analysis has revealed the top eight environmental score factors, having disclosure scores in the lead, followed by ESG funds, risk scores, green innovation, and recycling. **Lin,
H., Hsu, B. (2022)** set out to predict the ESG score of non-financial companies in Taiwan using 27 financial metrics and global governance indicators. A collection of the following
models was used to achieve this goal: random forest (RF), Extreme Learning Machines (ELM), support vector machine (SVM), and eXtreme Gradient Boosting (XGBoost).
The machine learning applications in the literature for water sustainability center around technical aspects in the catchment level, especially Water Quality Prediction. For instance,
**Durgun, Y. (2024)** has worked on the enabling of AI techniques to measure water quality in smart urban water systems. Agriculture is a very important sector to consider when it comes to water management, as it uses 70 percent of freshwater worldwide. **Hussein, E. E.
et. al, (2024)** have worked on groundwater quality assessment and Irrigation Water Quality Index (IWQI) prediction using machine learning algorithms. It had been identified that here has been a peak in 2023 in the literature discussing Machine Learning applications:
in addressing the wastewater management challenge, especially for performing tasks such as
modeling, prediction, and optimization Zhong, **S. et. al (2021)**.
Leaning closer into the water context in the corporate world, we see that the literature is
very scant. One of the key research, **Tian, M., Adriaens, P. (2025)**, used audited financial
accounting metrics to build econometric and machine learning models: Random Forest and
AdaBoost (Adaptive Boosting) for predicting water intensity indicators for growth companies
across eleven industries listed on the SP 500 index. In this study, water intensity is considered
as an efficiency measure relative to sales, operating income, and fixed asset investment;
hence, the use of financial data as predictors in modelling. The analysis can help inform
about operational efficiency with respect to water use or the risk that can affect production
facilities due to draining water resources.

**2) Machine Learning : CatBoost Model**
In the traditional Machine Learning methods, the usual way of dealing with categorical variables is through One-Hot Encoding or Label Encoding. In our case, the majority of the
dataframe features are categorical, which means that using the techniques above would result in a sparse matrix, increasing the risk of overfitting and reducing the scalability **Liang,
Z., (2025)**. CatBoost was introduced as a new gradient boosting toolkit to introduce an innovative way of dealing with categorical variables, accomplished through an implementation of ordered boosting. It also seeks to address the prediction shift issue we find in the
regular boosting algorithms. The major way through which CatBoost deals with categorical variables is through target statistics, where a feature is replaced by a numeric feature
corresponding to some target statistics (TS). Another functionality that makes this gradient boosting toolkit is its ability to capture feature combinations and high-order dependencies
between categorical variables. It has been demonstrated that empirically, CatBoost outperforms the traditional GBDT: Gradient Boosting Decision Trees packages. Prokhorenkova,
L. et al., **(2018; Dorogush, A. V. et al., 2018)**. Caboost is primarily an extension of the gradient boosting technique, where it combines
multiple weak learns to create a strong predictive model. Essentially, it is an ensemble learning method where the error rate of the constructed tree is evaluated and consequently
the next tree rectify it in the next iteration. We have implemented the model in Python through the package catboost, specifically its two modules CatBoostClassifier and Pool. As the primary research question is the study of
what leads corporations to be prone to drastic water-related outcomes, we have chosen as the target variable: ’w21 experienced water impacts’, which is an abbreviation of the
original question: W2.1 Has your organization experienced any detrimental water-related
impacts? From the Business Impacts part of the questionnaire. The variable takes two values either Yes/No. The modelling needs three important variables: (1) Iterations:
Number of trees to build, (2) Learning Rate: measures the contribution of each new model with smaller values, a smaller contribution of each tree, and vice versa. (3) Depth:
the size of each individual tree. The choice of variables depended on the most prominent factors determining water stewardship. We have detailed the categorical and numerical variables used for our analysis in
the table in the annex. As we are dealing with 52 variables, we examined feature importance using the method from the catboost get feature importance to include those with
a cumulative importance of 95 percent, which resulted in their reduction to 35. The feature selection renders many benefits: it can reduce the occurrence of overfitting as redundancy is
eliminated, it also increases accuracy of the modelling, and finally reduces the training time **Del Vitto, A.,et. al. (2023)**. The data that we are working with is suffering from class imbalance, where there is a
domination of Class 0: No Water Impacts have been observed. We first implemented the model without solving for the class imbalance, then we tested different class balancing tech-
niques to make for improvements in the model: using compute class weight from the sklearn.utils.class weight package, testing different class weights, and upsampling of the
minority category. We have concluded that the latter technique was the most effective. 


