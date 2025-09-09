# Loan Default Prediction Analysis For A Commercial Bank | Power BI

<img width="1000" height="500" alt="Cover project github" src="https://github.com/user-attachments/assets/06eaf0de-a23d-42b3-89ee-4c58978fc351" />

**Author:** Vu Bich Loan <br>
**Date:** September 2025 <br>
**Tool Used:** BI <br>

## Table of Contents
1. [📌Background & Overview](#background--overview)
2. [📂Dataset Overview](#dataset-overview)
3. [⚖️Hypothesis](#hypothesis)
4. [📊Visualizations & Key Insights](#visualizations--key-insights)
5. [🔎Final Conclusion](#final-conclusion)
6. [✅Recommendations](#recommendations)

---

## 📌Background & Overview
**📖 What is this project about?** <br>
This project aims to build a Power BI dashboard using the Loan Portfolio dataset to provide a comprehensive analysis of customer profile characteristics and risk factors that influence loan default likelihood. The goal is to provide senior managers with data-driven insights to: <br>
- Evaluate existing risk trends within the loan portfolio.
- Identify customer segments that require prioritized risk control.
- Provide a foundational understanding for developing appropriate loan approval and interest rate policies. <br>

**👤 Who is this project for?** <br>
- Board of Directors (CEO, CFO, CRO) 
- Personal Lending Department (Loan Officers, Portfolio Managers) 
- Risk Analysis and Control Department <br>

**❓Business Questions:** <br>
- What factors are most strongly correlated with loan default likelihood?
- Which customer segments have a higher-than-average risk? <br>

## 📂Dataset Overview
- **Total Records:** 255,347
- **Format:** CSV
- **Features:** 18
- **Key Columns:**
  - `LoanAmount`
  - `Income`
  - `CreditScore`, `NumCreditLines`, `HasMortgage`, - `LoanPurpose`
  - `DTIRatio`
  - `Age`, `EmploymentType`, `MonthsEmployed`, `Education`, `MaritalStatus`, `HasDependents`
  - `Default` (Target) <br>
    
## ⚖️Hypothesis
| **Hypothesis**| **Description**|
|----------|----------|
| **H1** | We hypothesize that a borrower's **income and employment profile** are key predictors of loan default risk. Specifically, we expect to see higher default rates among customers with: <br> - Low income <br> - A high debt-to-income (DTI) ratio (>51%) <br> - A limited or unstable employment history, including unemployment and a short duration of employment (under 1 year) |
| **H2** | We hypothesize that a borrower's **credit profile** is a key predictor of loan default risk. Specifically, we expect to see a significantly higher default rate among borrowers who have a very low credit score, possess a high number of credit lines, and lack a mortgage. |
| **H3** | We hypothesize that an unstable **demographic profile** is strongly correlated with higher loan default risk. Specifically, we expect to see a significantly higher default rate among younger borrowers (under 40) who are divorced, have no dependents, and possess a high school education level. |

## 📊Visualizations & Key Insights <br>
### 📍Page 1: Summary <br>

<img width="633" height="357" alt="image" src="https://github.com/user-attachments/assets/1032e002-3582-4f2f-9174-c3cd92c8b257" /> <br>

**🎯 Target:** Analyze Loan Portfolio Overview <br>
**💡Insights:** The bank approved 255.35K loan applications totaling $33 billion in loan amounts. Of the approved loans, good loans comprised 88.39%, while bad loans (or default loans) accounted for 11.61%. <br>
                                                                                                                                                                            
### 📍Page 2: Overview <br>

<img width="633" height="357" alt="image" src="https://github.com/user-attachments/assets/961d6788-45d2-45fd-beac-22d73f225313" /> <br>

**🎯Target:** Analyze the characteristics of existing customer profiles <br>
**💡Key visuals and Insights:** <br>
- **_Total Loan Applications by Education:_** <br>
  - Bachelor's degree holders take the most loans (64,366 applications) <br>
- **_Total Loan Amount by Loan Purpose_** <br>
  - Highest loan amount issued for home and business purposes <br>
- **_Median Loan Amount by Credit Score Category_** <br>
  - Low-credit-score customers have the highest median loan amounts <br>
- **_Average Loan Amount by Age Category_** <br>
  - Adults (26–39) take the largest loans on average <br>
- **_Average Income and Total Loan Applications by Employment Type_** <br>
  - Current borrowers are evenly distributed across various employment types (Unemployed, Part-time, Self-employed, Full-time) with incomes ranging from $82K to $83K USD. Full-time employees have the highest average income at $82,890K USD. <br>

**📝 Summary** <br>
  - Current borrowers are typically **adults between 26 and 39 years old** with a **bachelor's degree**. They are predominantly **full-time employees** with an average income of around **$82K USD**. The majority of loan applications are for **home and business purposes**, with these purposes also receiving the largest loan amounts. Notably, customers with low credit scores tend to receive the highest median loan amounts. <br>

### 📍Page 3: Analysis <br>
**1. Good and Bad Analysis** <br>
**🎯Target:** Comparing the characteristics of good loan and bad loan customers based on income, credit score, age, and purpose <br>

 <img width="633" height="356" alt="image" src="https://github.com/user-attachments/assets/03188ecf-c11b-4d65-9cec-1125c4f9cf2e" /> <br>
 
**💡Key visuals and Insights:** <br>
- **_Good and Bad Loan Rate by Income Category_** <br>
  - A very clear **inverse correlation** exists between income and the default rate. The default rate is highest among the **low-income** group at **17.96%**, while in the **high-income** group, this number is only **9.08%**. This indicates that income is a crucial indicator for predicting a borrower's ability to repay. <br>
- **_Applications by Credit Score_** <br>
  - The majority of approved loan applications are good loans. The number of loan applications increases significantly in higher credit score categories. While the number of applications in the **Very Low (0-400) ** and **Low (401-450) ** groups is the lowest, their proportion of bad-loan applications is very high. <br>
- **_Good and Bad Loan Rate by Age Group_** <br>
  - Age also has a strong correlation with risk. The youngest age group, **Teen (0-19) **, has the highest default rate at **22.14%**. This rate decreases as borrowers get older, showing that financial stability increases with age. <br>
- **_Good and Bad Loan Rate by Loan Purpose_** <br>
  - Loan purpose, with only minor differences between groups, appears to be a less significant risk factor compared to income, age, and credit score. <br>

**2. Bad Loan Details** 
**🎯Target:** Kiểm chứng từng hypothesis với biểu đồ trực quan <br>
**2.1 Risk 1** <br>

<img width="633" height="357" alt="image" src="https://github.com/user-attachments/assets/4da7f4c5-90c4-46a4-857f-2a56a81a166a" /> <br>

**💡Key visuals and Insights:** <br>
- **_Bad Loan Rate by Income Category_** <br>
  - There is a strong inverse correlation between income and the default rate: income is higher, default rate is lower. <br>
  - The default rate for the **low-income** customer group is the highest at **17.96%**, which is nearly twice the rate of the **high-income** group **(9.08%)**. This indicates that income is a crucial indicator for predicting a borrower's ability to repay. <br>
- **_Bad Loan Rate by Employment Duration and Employment Type_** <br>
  - Regarding **Employment Duration**, customers who have been employed for **less than 1 year** have a higher default rate than other groups. The longer the employment period, the lower the default rate.  <br>
  - Regarding **Employment Type**, **unemployed** individuals have the highest default risk regardless of their employment duration. The risk of default decreases from unemployed and part-time workers, to self-employed individuals, and finally to full-time employees. Job stability is a crucial factor affecting the ability to repay. <br>
- **_Bad Loan Rate by Loan Purpose and Income Category_** <br>
  - Although loan purpose has an impact on the default rate, the **income factor remains decisive**. Regardless of the loan purpose, the low-income customer group consistently has the highest default rate. <br>
  - The highest default rate is for loan applications with a **business purpose**. <br>
- **_Bad Loan Rate by Income Category and DTI_** <br>
  - The heatmap shows a clear inverse correlation between income and the default rate, and a positive correlation between DTI and the default rate. Specifically, customers with **low income and a high DTI** have the highest likelihood of default. Conversely, customers with **high income and a low DTI** show the lowest default risk. <br>

**2.2 Risk 2**

<img width="635" height="354" alt="image" src="https://github.com/user-attachments/assets/eb5a1918-59a4-4359-b508-c605f2289d81" /> <br>

**💡Key visuals and Insights:** <br>
- **_Bad Loan Rate by Credit Score Category_** <br>
  - A clear **inverse correlation** exists between credit score and the default rate. The lower the credit score, the higher the default rate, with the **very low credit score (<400)** group having the highest default rate at **13.34%**. <br>
- **_Bad Loan Rate by Credit Score Category and Has Mortgage_** <br>
  - The analysis reveals a crucial point: regardless of the credit score, borrowers **without a mortgage** consistently have a higher default rate. This indicates that having a mortgage helps mitigate default risk. <br>
- **_Bad Loan Rate by Credit Score Category and Number of Credit Lines_** <br>
  - The heatmap shows a clear inverse correlation between credit score and the default rate, as well as a **positive correlation** between the number of credit lines and the default rate. Specifically, customers with a **low credit score** and a **high number of credit lines** have the highest likelihood of default. Conversely, the group with a **high credit score** and a **low number of credit lines** shows the lowest default risk. <br>

**2.3 Risk 3**

<img width="633" height="352" alt="image" src="https://github.com/user-attachments/assets/0c748d61-5a34-467d-b2d8-fc474b7e8a94" /> <br>

**💡Key visuals and Insights:** <br>
- **_Bad Loan Rate by Age Category_** <br>
  - The default rate fluctuates between **5.13%** and **22.14%**. The highest default rate is **22.14%** for the **Teen (0-19)** customer group, which is more than **4 times** the rate of the lowest-risk group, Senior Citizens. <br>
  - The group of customers **under 40 years old**, which includes Teens and Adults (20-39), has a significantly higher default rate than all other age groups. <br>
- **_Bad Loan Rate by Marital Status and Has Dependents_** <br>
  - Divorced individuals with no dependents have the highest default rate. This suggests that a lack of personal stability and the financial burden following a divorce are key risk factors. <br>
- **_Bad Loan Rate by Education and Age Category_** <br>	
  - Education level is identified as a risk factor. Customers who possess only a **high school education** have the highest default rate, regardless of their age group. <br>

## 🔎Final Conclusion 
| **Aspect** | **Insight** |
|----------|----------|
| Income & Employment Profile| Higher default rates among customers with: <br> - Low income <br> - A high debt-to-income (DTI) ratio (>51%) <br> - A limited or unstable employment history, including unemployment and a short duration of employment (under 1 year) |
| Credit profile | Higher default rates among borrowers who <br> - have a very low credit score <br> - possess a high number of credit lines <br> -lack a mortgage |
## ✅Recommendations
**1. Tăng cường Đánh giá Rủi ro với Các Nhóm Khách hàng Nhạy cảm 📈** <br>
Ngân hàng nên áp dụng các tiêu chí xét duyệt nghiêm ngặt hơn cho những khách hàng thuộc nhóm rủi ro cao. Cần đặc biệt chú ý đến các hồ sơ có: <br>
- Tỷ lệ nợ trên thu nhập (DTI) cao (>51%). <br>
- Hồ sơ việc làm không ổn định (thất nghiệp hoặc thời gian làm việc ngắn dưới 1 năm). <br>
- Điểm tín dụng rất thấp. <br>
- Số lượng hạn mức tín dụng hiện có cao nhưng thiếu khoản vay thế chấp. <br>

**2. Điều chỉnh Chính sách Cho vay dựa trên Hồ sơ Nhân khẩu học 🎯** <br>
Thiết lập các điều kiện vay vốn linh hoạt hơn, phù hợp với từng đặc điểm nhân khẩu học. Ví dụ, với nhóm khách hàng trẻ tuổi (dưới 40 tuổi) có tình trạng hôn nhân không ổn định hoặc chỉ có trình độ học vấn trung học phổ thông, ngân hàng có thể cân nhắc: <br>
- Giảm số tiền vay tối đa để hạn chế rủi ro. <br>
- Yêu cầu thêm tài sản đảm bảo hoặc đồng vay. <br>

