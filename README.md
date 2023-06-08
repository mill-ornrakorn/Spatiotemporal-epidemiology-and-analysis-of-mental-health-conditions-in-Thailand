# Spatiotemporal epidemiology and analysis of mental health conditions in Thailand project ❤📊

This study aims to:

- Advocate **government policies** that allocate resources to regions where people seek mental health services.
- Help Thai people **realize the importance** of mental disorders.
- Provide an **overview of mental health** in Thailand.

This study is part of the course CPE 301: Work Integrated Learning, in the Health Data Science program at King Mongkut's University of Technology Thonburi, during the third semester of the academic year 2021. It involves practical training with professionals in a company, hospital, or other health-related organization for a minimum of six weeks during the summer.

### 🙋‍♀️Group (เกือบจะอ๋อ)
1. [Papin Thanutchapat](https://github.com/Jappapin)
2. [Chiraphat Phoncharoenwirote](https://github.com/Chiraphatt)
3. [Ornrakorn Mekchaiporn](https://github.com/mill-ornrakorn)

### 📚Advisor
1. **Asst. Prof. Dr. Chawarat Rotejanaprasert**; Department of Tropical Hygiene, Faculty of Tropical Medicine, Mahidol University
2. **Asst. Prof. Dr. Peerut Chienwichai**; Princess Srisavangavadhana College of Medicine, Chulabhorn Royal Academy
3. **Asst. Prof. Dr. Warut Aunjitsakul**; Division of Psychiatry, Faculty of Medicine, Prince of Songkla University


### 🏢Internship placement
Mahidol-Oxford Tropical Medicine Research Unit (MORU) Faculty of Tropical Medicine Mahidol University in Bangkok, Thailand

## Data source 📁

1. [Reported mental health service cases](https://dmh.go.th/report/datacenter/hdc/reds.asp) were  collected from the health data center (HDC), Department of Mental Health, Ministry of Public Health (MOPH). All the cases were aggregated yearly mental health service cases notified during the years 2015 to 2021 at the provincial level, classified into eighteen categories in the health data center, and only eleven categories were used in the study (Dementia, Alcoholism, Drug addiction (excluding Amphetamine addiction), Schizophrenia, Depression, Anxiety disorder, Intellectual disabilities, Learning disabilities, Autistic disorder, Self-harm, and Epilepsy). ICD-10 mental disorders were assigned the codes F00.X - F99.X. Case report data includes the year and province of diagnosis.

2. [Thailand’s mid-year population statistics](https://stat.bora.dopa.go.th/stat/statnew/statMONTH/statmonth/#/mainpage) were collected from official statistics registration systems. This study was conducted in Thailand, which collected data on a population of approximately 70 million people across 77 provinces with different geographies.

3. [The geographic coordinates and provincial boundary data (shapefile)](https://gadm.org/) are obtained from the GEO package file in the Global Administrative Region Database (GADM), a high-resolution territorial database containing provincial to subdistrict data for all countries across the world

**📍note that:** The details of the Data Preparation can be found in the
[Code](https://github.com/mill-ornrakorn/Spatiotemporal-epidemiology-and-analysis-of-mental-health-conditions-in-Thailand/blob/main/1-Data%20preparation.ipynb) 
,

## Methods ⚙
**1. Descriptive Analytics**

**2. Spatial pattern analysis**

1. ```Global Spatial Detection (Global Moran’s I)``` is used to determine whether the spatial correlation is positive or negative. It is shown as a clustered, fragmented, or random pattern
    
2. ```Local Spatial Detection (Local Moran’s I)``` is used to evaluate the autocorrelation within local neighborhoods at the local level.

**3. Cluster analysis**

1. ```Correlation Matrix```
     - The Spearman's Correlation Coefficient is a nonparametric measure of a non-linear and monotonic relationship between two ranked variables
        
2. ```Unsupervised Machine Learning```
     - K-Prototype Clustering is a cluster analysis method derived from the k-means and k-modes algorithms.  Therefore, the k-prototypes algorithm can cluster with mixed numerical and categorical values. K-means handle the numerical values, and k-modes handle the categorical values. These clustering algorithms are unsupervised learning, which is used with unlabeled data to find groups in the dataset. In this study, the algorithm is used to find groups among the disorders.

     - (Agglomerative) Hierarchical Clustering is a method of cluster analysis. There are two methods of hierarchical clustering, Agglomerative and divisive. In this study, we used the agglomerative hierarchical clustering method. In agglomerative hierarchical clustering, clusters are built from the bottom up. 

<!--
## Results 📊
**1. Descriptive Analytics**




There are 9,496,342 cases in the patient data for 11 mental health services collected from the Department of Mental
Health's data system between 2015 and 2021. As shown in Figure 1, the total number of cases is calculated per 100,000
population and displayed in line chart format. The graph's data can be displayed in two periods: The number of mental health
services provided prior to the COVID-19 outbreak until COVID-19 was detected (2015-2019). The number of patients accessing
mental health services for Depression, Autism, Alcoholism, and Drug addiction (excluding Amphetamine addiction) increased
steadily until 2018 and then decreased. The COVID-19 period's alcohol-control measures are expected to reduce the number of
alcoholism cases. The second section displays the number of patients accessing mental health services following the detection
of COVID-19 (2020–2021), found that the number of patients Depression, Alcoholism, and Drug addiction are expected to rise
slightly, in 2019


The graph below depicts the percentage of the number of patients accessing mental health services in Thailand
calculated per 100,000 population from 2015 to 2021. The total number of patients is 9,496,342 and is shown in bar chart
format. Anxiety disorders, Schizophrenia, and Depression were the three disorders with the most mental health patients, with
2,259,434, 2,016,200, and 1,773,618 patients, respectively. Intellectual disabilities, Learning disabilities, and Self-harm were the
three disorders with the fewest mental health patients, with 110,469, 118,088, and 147,807 patients, respectively.



- Mapping 


**2. Spatial pattern analysis**



**3. Cluster analysis**


## Conclusions 📄
The results of this study provided information about the spatiotemporal characteristics of mental disorders in Thailand
and also revealed the limitations of the data, which have an impact on the overall analysis and further applications. For more
accurate and interpretable results, such as geographic heat maps and associations between two disorders, the data used for
analysis should represent the real characteristics of each disorder, which can lead to change, such as mental health policy by
the government, attitudes and public interaction, and access to prevention and treatments.

>


<!--

ver. thai

# Spatiotemporal epidemiology and analysis of mental health conditions in Thailand project ❤📊

Spatiotemporal epidemiology and analysis of mental health conditions in Thailand เป็น การศึกษาที่เกี่ยวกับ การวิเคราะห์ทางระบาดวิทยาเชิงพื้นที่และเวลาของการเข้ารับบริการทางจิตเวชภายในประเทศไทย ซึ่งวิเคราะห์โดยใช้ Spatial pattern analysis และ Cluster analysis 

การศึกษานี้มีจุดมุ่งหมายเพื่อ
- นโยบายรัฐบาล: คาดว่าอาจจะสนับสนุนนโยบายของรัฐบาลไปในการจัดสรรทรัพยากรให้กับพื้นที่ที่มีผู้คนความต้องการเข้ารับบริการด้านสุขภาพจิต

- ตระหนักถึงความสำคัญ: 
ช่วยให้คนไทยได้ตระหนักถึงความสำคัญของความผิดปกติทางจิตว่าไม่ใช่เรื่องที่ไกลตัวเรา

- เห็นภาพรวมของสุขภาพจิตในประเทศไทย: 
ได้เห็นภาพรวมของสุขภาพจิตในประเทศไทย และอยากรู้ว่าทำไมในประเทศไทยถึงมีผู้ป่วยที่ผิดปกติจำนวนมาก และมีความสัมพันธ์อย่างไรในเชิงพื้นที่และเวลา

การศึกษานี้เป็นส่วนหนึ่งของรายวิชา CPE 301 บูรณาการการเรียนและการทำงาน (Work Integrated Learning) สาขาวิชาวิทยาศาสตร์ข้อมูลสุขภาพ มหาวิทยาลัยเทคโนโลยีพระจอมเกล้าธนบุรี ภาคเรียนที่ 3 ปีการศึกษา 2564 โดยเป็นการปฏิบัติงานในบริษัท โรงพยาบาล หรือ องค์กรทางด้านสุขภาพอื่น ๆ ระหว่างภาคฤดูร้อนไม่น้อยกว่า 6 สัปดาห์

### 🙋‍♀️Group: เกือบจะอ๋อ
1. [Papin Thanutchapat](https://github.com/Jappapin)
2. [Chiraphat Phoncharoenwirote](https://github.com/Chiraphatt)
3. [Ornrakorn Mekchaiporn](https://github.com/mill-ornrakorn)

### 📚Advisor
1. **Asst. Prof. Dr. Chawarat Rotejanaprasert**; Department of Tropical Hygiene, Faculty of Tropical Medicine, Mahidol University
2. **Asst. Prof. Dr. Peerut Chienwichai**; Princess Srisavangavadhana College of Medicine, Chulabhorn Royal Academy
3. **Asst. Prof. Dr. Warut Aunjitsakul**; Division of Psychiatry, Faculty of Medicine, Prince of Songkla University


### 🏢สถานที่ฝึกงาน
ภาควิชาสุขวิทยาเขตร้อน และหน่วยวิจัยโรคเขตร้อน มหิดล-ออกชฟอร์ด (Mahidol Oxford Tropical Medicine Research Unit; MORU) คณะเวชศาสตร์เขตร้อน มหาวิทยาลัยมหิดล

## Data source 📁
ข้อมูลที่ใช้ในการวิเคราะห์ ประกอบด้วย ดังนี้ 

1. [รายงานผู้ป่วยที่เข้ามาใช้บริการด้านจิตเวช](https://dmh.go.th/report/datacenter/hdc/reds.asp) ตั้งแต่ปีค.ศ. 2015 ถึง 2021 รวบรวมมาจาก กรมสุขภาพจิต กระทรวงสาธารณสุข 

2. [สถิติประชากรกลางปีของประเทศไทย](https://stat.bora.dopa.go.th/stat/statnew/statMONTH/statmonth/#/mainpage) รวบรวมมาจาก ระบบสถิติทางการทะเบียน

3. [พิกัดทางภูมิศาสตร์และข้อมูลเขตจังหวัดของประเทศไทย (shapefile)](https://gadm.org/) รวบรวมมาจาก Global Administrative Region
(GADM) ซึ่งเป็นฐานข้อมูลเชิงพื้นที่ของที่ตั้งเขตการปกกรองของทั่วโลก ละติจูด ลองจิจูด โดยในการศึกษานี้เราใช้ความละเอียดแบบจังหวัด (provincial boundaries (Level 1)) ในการวิเคราะห์

**📍note that:** รายละเอียดการทำ Data Preparation สามารถดูได้เพิ่มได้ใน 
[Code](https://github.com/mill-ornrakorn/Spatiotemporal-epidemiology-and-analysis-of-mental-health-conditions-in-Thailand/blob/main/1-Data%20preparation.ipynb) 
นะคะ

## Methods ⚙
**1. Descriptive Analytics**

**2. Spatial pattern analysis**

1. Global Spatial Detection (Global Moran’s I) เป็นการระบุว่า ความสัมพันธ์เชิงพื้นที่เป็นบวกหรือลบ และแสดงเป็นรูปแบบสุ่มหรือไม่
    
2. Local Spatial Detection (Local Moran’s I) ใช้ในการบอกบริเวณ และสัดส่วน ว่ามีการกระจายตัวเท่าไรของทั้งหมด

**3. Cluster analysis**

1. Correlation Matrix
     - The Spearman's Correlation Coefficient ใช้เพื่อให้เห็นความสัมพันธ์ระหว่างโรค
        
2. Unsupervised Machine Learning
    - K-Prototype Clustering เป็นอัลกอริทึมที่ต่อยอดมาจาก k-means โดยแก้ปัญหาเรื่องขอจำกัดที่สามารถคำนวณได้เฉพาะ numerical
     - (Agglomerative) Hierarchical Clustering


-->