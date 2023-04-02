# Spatiotemporal epidemiology and analysis of mental health conditions in Thailand project ❤📊

Spatiotemporal epidemiology and analysis of mental health conditions in Thailand เป็น การศึกษาที่เกี่ยวกับ การวิเคราะห์ทางระบาดวิทยาเชิงพื้นที่และเวลาของการเข้ารับบริการทางจิตเวชภายในประเทศไทย โดยได้วิเคราะห์โดยใช้ Spatial pattern analysis และ Cluster analysis 

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
1. Asst. Prof. Dr. Chawarat Rotejanaprasert
2. Asst. Prof. Dr. Peerut Chienwichai


### 🏢สถานที่ฝึกงาน
ภาควิชาสุขวิทยาเขตร้อน และหน่วยวิจัยโรคเขตร้อน มหิดล-ออกชฟอร์ด (Mahidol Oxford Tropical Medicine Research Unit; MORU) คณะเวชศาสตร์เขตร้อน มหาวิทยาลัยมหิดล

### 📁Data source
ข้อมูลที่ใช้ในการวิเคราะห์ ประกอบด้วย ดังนี้ 

1. [รายงานผู้ป่วยที่เข้ามาใช้บริการด้านจิตเวช](https://dmh.go.th/report/datacenter/hdc/reds.asp) ตั้งแต่ปีค.ศ. 2015 ถึง 2021 รวบรวมมาจาก กรมสุขภาพจิต กระทรวงสาธารณสุข 

2. [สถิติประชากรกลางปีของประเทศไทย](https://stat.bora.dopa.go.th/stat/statnew/statMONTH/statmonth/#/mainpage) รวบรวมมาจาก ระบบสถิติทางการทะเบียน

3. [พิกัดทางภูมิศาสตร์และข้อมูลเขตจังหวัดของประเทศไทย (shapefile)](https://gadm.org/) รวบรวมมาจาก Global Administrative Region
(GADM) ซึ่งเป็นฐานข้อมูลเชิงพื้นที่ของที่ตั้งเขตการปกกรองของทั่วโลก ละติจูด ลองจิจูด โดยในการศึกษานี้เราใช้ความละเอียดแบบจังหวัด (provincial boundaries (Level 1)) ในการวิเคราะห์

**📍note that:** รายละเอียดการทำ Data Preparation สามารถดูได้เพิ่มได้ใน 
[Code](https://github.com/mill-ornrakorn/Spatiotemporal-epidemiology-and-analysis-of-mental-health-conditions-in-Thailand/blob/main/1-Data%20preparation.ipynb) 
นะคะ

### ⚙ Methods
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
