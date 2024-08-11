# Bank-Loan
![image](https://github.com/egm3/Bank-Loan/assets/37548107/42ffe897-71d6-4172-9250-c4060a9be612)

## 1. Description
This a beginner machine learning project that uses decision trees to decide if a bank should or not grant a loan to a costumer. The primary aim of this project is to conduct an Exploratory Data Analysis (EDA) on a dataset pertaining to Loan Status. The ultimate goal is to leverage machine learning techniques to predict whether to approve or deny a loan application for a client. Through comprehensive data exploration and sophisticated modeling, the project seeks to uncover insights that will inform the decision-making process in lending, ensuring optimal outcomes for both the financial institution and its clientele.

## 2. Tools
This project was completely made in Python(**Pandas, Numpy, Matplotlib, Seaborn, Scikit-Learn**), Jupyter Notebook(anaconda) and Git/Github.

## 3. Introduction to the problem
Interest on loans is a fundamental aspect of how banks make money and is a significant contributor to their revenue streams. When a bank lends money to individuals, businesses, or other entities, it charges interest on the principal amount borrowed. This interest is essentially the cost of borrowing money and is expressed as a percentage of the loan amount. Therefore, predicting loan status is crucial for banks.

With a good loan prediction the bank can improve in several aspects. As following:

**Risk Management**: By accurately predicting loan status, banks can assess the level of risk associated with each loan application. This allows them to make informed decisions about whether to approve or deny a loan, thereby minimizing the risk of default and potential losses.

**Profitability**: Predicting loan status enables banks to optimize their lending practices to maximize profitability. By identifying low-risk borrowers, banks can offer them more favorable loan terms, such as lower interest rates, while charging higher rates to high-risk borrowers. This helps banks to maintain healthy profit margins while attracting reliable customers.

**Compliance**: Banks are subject to regulatory requirements that mandate responsible lending practices. Predicting loan status helps banks ensure compliance with these regulations by assessing the creditworthiness of borrowers and avoiding lending to individuals or businesses that are unlikely to repay their loans.

**Customer Satisfaction**: Accurate loan status prediction allows banks to offer better customer service by providing timely loan approvals or rejections. This enhances the overall customer experience and fosters goodwill towards the bank, leading to higher customer satisfaction and loyalty.

**Portfolio Management**: Understanding the predicted status of loans in their portfolio enables banks to manage their assets more effectively. By identifying potential problem loans early on, banks can take proactive measures to mitigate risk, such as restructuring loans or setting aside reserves for potential losses.

**Competitive Advantage**: Banks that can effectively predict loan status gain a competitive edge in the market. They can attract more customers by offering competitive loan products and better terms, while simultaneously minimizing their exposure to risky borrowers. This strengthens the bank's position in the industry and enhances its reputation as a reliable financial institution.

## 4. Insights from the Exploratory Data Analysis
EDA is primarily used to see what data can reveal beyond the formal modeling or hypothesis testing task and provides a provides a better understanding of data set variables and the relationships between them. It can also help determine if the statistical techniques you are considering for data analysis are appropriate.

**4.1** Most part of the applicants are men, do not have any dependent, are graduate, not self employed and have a credit history.
![image](https://github.com/egm3/Bank-Loan/assets/37548107/e3764776-f9ce-4a21-ad28-d6ba0c614754)
**4.2** The applicant income mean is about 3.5k and the loan amount requested mean is about 105k
![image](https://github.com/egm3/Bank-Loan/assets/37548107/3bc3ed03-8d98-47f9-b2b9-7518f97e5bc9)
**4.3** Seems there is no correlation between the applicant income and the loan amount requested.
![image](https://github.com/egm3/Bank-Loan/assets/37548107/8da899d7-b7ea-4c4c-ba78-ca2074eae3a9)
**4.4** If you are not married, you are more likely to not recieve a loan.
![image](https://github.com/egm3/Bank-Loan/assets/37548107/c63fc346-6547-43cf-8300-273428bc1f65)


**4.5** If you do not have a credit history, is extremely unlikely that you recieve a loan.
![image](https://github.com/egm3/Bank-Loan/assets/37548107/789d12b9-d84d-47fd-89bd-5155c2a43da1)


**4.6** Womem seems to have a lower income, but it does not influence to get or not a loan.
![image](https://github.com/egm3/Bank-Loan/assets/37548107/4422dad9-4119-4bca-8756-e48c60ed3e8b)
**4.7** People whit tree or more dependents request a higher loan
![image](https://github.com/egm3/Bank-Loan/assets/37548107/447cfbf8-0670-4135-bf65-33d04f21dc0a)

## 5. Modeling

**5.1 Preprocessing:** Preprocessing is a crucial step in preparing data for modeling. It involves cleaning, transforming, and organizing raw data into a format that can be easily and effectively used by machine learning models. 
- Handling Missing Values
  -  Removal: Delete rows or columns with a high proportion of missing values.
-  Data Transformation
  - Encoding Categorical Variables
-Data Splitting
  - Train-Test Split: Divide the dataset into training and testing sets to evaluate the model’s performance on unseen data.
  - Cross-Validation: Further split the data into k-folds for a more robust evaluation process.

Final Considerations:
Data Quality: Ensure the data is accurate, consistent, and relevant to the problem at hand.
Reproducibility: Document the preprocessing steps to ensure that the process can be replicated in future iterations or on different datasets.

**5.2 Build a Tree and optimize it**

A decision tree is a tool we use to make predictions based on data. Think of it like a flowchart, where each question we ask splits the data into different paths, leading us closer to the final decision. For example, if we're predicting whether a customer will buy a product, the tree might ask questions like "Is the customer under 30?" or "Has the customer bought from us before?"

- Asking the Right Questions: We start by asking questions that help us best separate the data into groups that are as clear as possible. For instance, we might ask if a customer is younger or older than 30 because that could tell us something about their buying habits. Then we build a preliminary tree.

After that, we are ready to opitimize this tree.
- Simplifying the Tree: After building the tree, we might notice that some branches are too complex or not very helpful. We can trim these branches to make the tree simpler and more focused, which often leads to better predictions.
- Better Predictions: By carefully building and refining the decision tree, we make sure that our predictions are as accurate as possible. This means we can better understand customer behavior, make more informed decisions, and ultimately improve business outcomes.

As final result, we got the following:
![image](https://github.com/user-attachments/assets/3c6409fe-27e1-4654-995e-5aecfa449c44)


It means that our Decision Tree Model can predict with a high accuracy when we should concive a loan(100% accuracy in true labels), but not that great when we shouldn't. 
