
# Mitron Bank-Dashboard

### Dashboard Link : https://app.powerbi.com/links/QaJs83fSLb?ctid=9bb2360a-034c-4ecf-8228-aafe1a12b953&pbi_source=linkShare

## Problem Statement

This Dashboard helps the Mitron Bank is a legacy financial institution headquartered in Hyderabad. They want to introduce a new line of credit cards, aiming to broaden its product offerings and reach in the financial market.

This Dashboard helps the Mitron Bank to understand their target Customers Demographic, Income and Spending patterns so that they can design the Credit 
Card features as per their Customers requirements.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present.
- Step 5 :In the report view, under the view tab, theme was selected.
- Step 7 : Since the data contains various demographic information, thus in order to represent demographic, a new visual was added using the three ellipses in the visualizations pane in report view. 
- Step 8 : Visual filters (Slicers) were added for four fields named "Age Group", "Marital Status", "Gender" "City", "Month" & "Occupation".
- Step 9 : Three card visuals were added to the canvas,representing Total Customers, Male and Female Customers.
- Step 10 : A Donut chart was also added to the report design area representing the number of Married and Unmarried customers.
Three Clustured column chart were also added. One shows the Customers based on age group,city and by Occupation

- Step 11 : New measure was created to find total count of customers.

Following DAX expression was written for the same,
        
    Acive_Customer = COUNT(customer_id[customer_id])
        
A card visual was used to represent count of customers.

![image](https://github.com/Ambikapandey0821/Test/assets/162020155/a89705e8-fb0b-4ee4-90f5-0e598e65db1a)

- Step 12 : New measure was created to find total count of Male customers.

Following DAX expression was written for the same,
        
    Male_Customer = CALCULATE(COUNTA(customer_id[customer_id]),FILTER(dim_customers,dim_customers[gender]="Male"))
        
A card visual was used to represent count of Male customers.

![image](https://github.com/Ambikapandey0821/Test/assets/162020155/70653e14-a2a6-42d6-834c-bfb5c6b72a85)

- Step 13 : New measure was created to find total count of Female customers.

Following DAX expression was written for the same,
        
   Female_Customer = CALCULATE(COUNTA(customer_id[customer_id]),FILTER(dim_customers,dim_customers[gender]="Female"))
        
A card visual was used to represent count of Female customers.

![image](https://github.com/Ambikapandey0821/Test/assets/162020155/698bb78f-58c4-4675-9209-b7e0b37f71f1)

- Step 14 : New Page Created for Spend Analysis. In this page Four new cards added which shows the total Income, Total Spend, Average Income and Income utilisation percentage.

- Step 14 : New measure was created to find Income Utilisation percentage.

Following DAX expression was written for the same,
        
   Income utilisation% = DIVIDE(SUM(fact_spends[spend]),SUM(dim_customers[income]))
        
A card visual was used to represent Income Utilisation percentage.

![image](https://github.com/Ambikapandey0821/Test/assets/162020155/06a4771b-5b8f-4617-a18d-e6bd333da774)
        
- Step 14 : Seven New Line and Clustured column chart
added. Each charts shows the relationship between Income and Spend. Bar chart shows the Income and Spend whereas line shows the Income utilisation percentage.

- Step 15 : One Area chart added to show the spend based on the Months.


- Step 15 : One Area chart added to show the spend based on the Months.

A Area chart visual was used to represent spend based on Months.

![image](https://github.com/Ambikapandey0821/Test/assets/162020155/4b10d715-8f66-42e5-a6a7-d7931ed24962)

 - Step 14 : New Page Created for Income and spend Analysis . In this page one Matrix is added which shows the detailed relationship among all the varibales.
 and Three Scatter Chart added which shows the relationship between Income, Spend, City, Occupation and Age Group.

 A Scatter chart visual was used to represent relationship between Income, Spend, City, Occupation and Age Group.

 ![image](https://github.com/Ambikapandey0821/Test/assets/162020155/cbafb73e-e07c-4272-90cd-6d444e3fb07e)

  - Step 14 : Page Navigator and Slicers added at the bottom of all the pages. 


 - Step 18 : The report was then published to Power BI Service.
 
 
![image](https://github.com/Ambikapandey0821/Test/assets/162020155/8ff350cb-367f-4a77-9d33-dde5e06542b3)

# Snapshot of Dashboard (Power BI Service)

![image](https://github.com/Ambikapandey0821/Test/assets/162020155/555e0583-174a-4518-b26a-6b31e0bb8ff4)


 
 # Report Snapshot (Power BI DESKTOP)

![image](https://github.com/Ambikapandey0821/Test/assets/162020155/24765a76-2693-43c7-9b03-72cc83f24137)

![image](https://github.com/Ambikapandey0821/Test/assets/162020155/bd712400-9f09-4356-9a5f-275a041a3956)

![image](https://github.com/Ambikapandey0821/Test/assets/162020155/a6550a4e-e9bf-47be-8a23-a11241b42ce7)


# Insights

A Three page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

 ### Demographic Analysis

 Total Number of Customers - 4K

 Number of Customers (Male) - 2.6K

 Number of Customers (Female) - 1.4K
   
 Number of Married Customers - 3.14K (78.4%)

 Number of Unmarried Customers - 0.86K (21.6%)

 Thus, higher number of customers are Married and Male.
           
# Age Group 
    a) 25-34 - 1498
    b) 35-45 - 1273
    c) 21-24 - 691
    d) 45+ - 538

        Thus, higher number of customers are between the age of 25-34 and 35-45 Age Group.

# City 
    a) Mumbai - 1078
    b) Chennai - 834
    c) Bengaluru- 751
    d) Delhi NCR - 744
    e) Hyderabad - 593
  
        Here we can see that Mumbai has the largest customer base and Hyderabad has the lowest customer base.

# Occupation 
    a) Salaried IT Employees - 1294
    b) Salaried Other Employees - 893
    c) Freelancers- 784
    d) Business Owners - 630
    e) Government Employees - 399

      Here we can see that Salaried IT Employees are the largest customer base and Government Employees are the lowest customer base.

 ## [2] Utilisation percentage
 
 # Age Group
    a) 25-34 - 43.63%
    b) 35-45 - 46.74%
    c) 21-24 - 40.48%
    d) 45+ - 35.03%
 
         Thus, Age Group of 35-45 has the highest Income utilisation. And Age Group 45+ has the lowest.
 
 # City 
    a) Mumbai - 51%
    b) Chennai - 31%
    c) Bengaluru- 44%
    d) Delhi NCR - 58%
    e) Hyderabad - 36%
         Thus, maximum Income utilisation is from Mumbai city and lowest from Chennai.

# Occupation  
    a) Salaried IT Employees - 51%
    b) Salaried Other Employees - 41%
    c) Freelancers- 46%
    d) Business Owners - 33%
    e) Government Employees - 29%
        Thus, maximum Income utilisation is from Salaried IT Employees - 51% and lowest from Government Employees - 29%.

# Gender
    a) Male - 45%
    b) Female - 40%
        Thus, maximum Income utilisation is from  Male - 45%.
 

# Marital Status
    a) Married - 42.74%
    b) Single - 43.34%
        Thus, maximum Income utilisation is from  Sigle - 43.34%.

# Category
    a) Bills - 19.94%
    b) Groceries - 16.08%
    c) Electronics - 14.99%
    d) Health & Wellness - 12.38%
    e) Travel - 11.16%
    f) Food - 8.25%
    g) Enternment - 7.17%
    h) Apparel - 6.46%
    i) Others - 3.03%
        Here we can see that Bills - 19.94% is the top most spend category followed by Groceries and Electronics.


# Transaction Payment Type
    a) Credit Card - 40.89%
    b) UPI - 26.26%
    c) Debit Card - 22.56%
    d) Net Banking - 10.29%
        Here We can say that Credit Card is the Most preferred Payment type. And Net Banking as the lowest preffered Payment type.

# Spend by Months in Millions
    a) May - 11.4 
    b) June - 13.7 
    c) July - 13.4 
    d) August - 16.7 
    e) September - 19.4
    f) October - 14.4
        Here we can say that maximum Spending is done on the month of September and least on May month.
