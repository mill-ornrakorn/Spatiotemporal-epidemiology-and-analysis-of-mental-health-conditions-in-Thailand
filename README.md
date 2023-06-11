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
.

## Methods ⚙
**1. Descriptive Analytics**

**2. Cluster analysis**

1. ```Correlation Matrix```
     - The Spearman's Correlation Coefficient is a nonparametric measure of a non-linear and monotonic relationship between two ranked variables
        
2. ```Unsupervised Machine Learning```
     - K-Prototype Clustering is a cluster analysis method derived from the k-means and k-modes algorithms.  Therefore, the k-prototypes algorithm can cluster with mixed numerical and categorical values. K-means handle the numerical values, and k-modes handle the categorical values. These clustering algorithms are unsupervised learning, which is used with unlabeled data to find groups in the dataset. In this study, the algorithm is used to find groups among the disorders.

     - (Agglomerative) Hierarchical Clustering is a method of cluster analysis. There are two methods of hierarchical clustering, Agglomerative and divisive. In this study, we used the agglomerative hierarchical clustering method. In agglomerative hierarchical clustering, clusters are built from the bottom up. 

**3. Spatial pattern analysis**

1. ```Global Spatial Detection (Global Moran’s I)``` is used to determine whether the spatial correlation is positive or negative. It is shown as a clustered, fragmented, or random pattern
    
2. ```Local Spatial Detection (Local Moran’s I)``` is used to evaluate the autocorrelation within local neighborhoods at the local level.


## Results 📊
**1. Descriptive Analytics**

<p align="center">
<img src="https://github.com/mill-ornrakorn/Spatiotemporal-epidemiology-and-analysis-of-mental-health-conditions-in-Thailand/blob/main/pic%20for%20readme/line%20chart.gif?raw=true" alt= "linechart" height="400">
</br>
<b>Figure 1</b> The patients accessing mental health services rate in Thailand since 2015-2021 (per 100k population)
</p>


There are 9,496,342 cases in the patient data for 11 mental health services collected from the Department of Mental Health's data system between 2015 and 2021. As shown in Figure 1, the total number of cases is calculated per 100,000 population and displayed in line chart format. The graph's data can be displayed in two periods: The number of mental health services provided prior to the COVID-19 outbreak until COVID-19 was detected (2015-2019). The number of patients accessingmental health services for Depression, Autism, Alcoholism, and Drug addiction (excluding Amphetamine addiction) increased steadily until 2018 and then decreased. The COVID-19 period's alcohol-control measures are expected to reduce the number of alcoholism cases. The second section displays the number of patients accessing mental health services following the detection of COVID-19 (2020–2021), found that the number of patients Depression, Alcoholism, and Drug addiction are expected to rise slightly, in 2019


<p align="center">
<img src="https://github.com/mill-ornrakorn/Spatiotemporal-epidemiology-and-analysis-of-mental-health-conditions-in-Thailand/blob/main/pic%20for%20readme/2.jpg?raw=true" alt= "barchart" height="300">
</br>
<b>Figure 2</b> Total of the number of patients accessing services in Thailand since 2015-2021
(per 100k population).
</p>

Figure 2 depicts the percentage of the number of patients accessing mental health services in Thailand calculated per 100,000 population from 2015 to 2021. The total number of patients is 9,496,342 and is shown in bar chart format. Anxiety disorders, Schizophrenia, and Depression were the three disorders with the most mental health patients, with 2,259,434, 2,016,200, and 1,773,618 patients, respectively. Intellectual disabilities, Learning disabilities, and Self-harm were the three disorders with the fewest mental health patients, with 110,469, 118,088, and 147,807 patients, respectively.




- **Mapping**

<p align="center">
<img src="https://github.com/mill-ornrakorn/Spatiotemporal-epidemiology-and-analysis-of-mental-health-conditions-in-Thailand/blob/main/pic%20for%20readme/3.jpg?raw=true" alt= "map" height="400">
</br>
<b>Figure 3</b> The map Shows the location of mental health services rate at region, namely the provinces of Thailand, which has a total of 77 provinces.
</p>

Figure 3 depicts the study region's geographical location, namely the provinces of Thailand, which has a total of 77 provinces. The number of patients accessing mental health services for all 11 mental health services from 2015 to 2021 was: Alcoholism, Drug addiction (excluding Amphetamine addiction), Schizophrenia, Depression, Anxiety disorder, Autistic disorder, Intellectual disabilities, Learning disabilities, Dementia, Self-harm, and Epilepsy. A geographical heat map was used to present the spatial distribution of the number of patients over a seven-year period, allowing the mapping to highlight the geographic distribution of disease-identifying mental disorders using different colors. The darker the color displayed in a province, the greater the amount of traffic in that province. The GEO package file in the Global Administrative Region Database (GADM) Version 3.6 was used to create all the maps.


**2. Cluster analysis**
- **Correlation matrix**
<p align="center">
<img src="https://github.com/mill-ornrakorn/Spatiotemporal-epidemiology-and-analysis-of-mental-health-conditions-in-Thailand/blob/main/pic%20for%20readme/8.jpg?raw=true" alt= "correlation" height="400">
</br>
<b>Figure 4</b> Total correlation of patients accessing mental health services in Thailand since 2015-2021 (per 100k population).
</p>

The correlation matrix shows 3 groups of disorders that have a positive linear relationship (correlate) with each other.
The first group includes Alcoholism and Drug addiction (excluding Amphetamine addiction). The second group includes
Schizophrenia, Depression and Anxiety disorder. The last group includes Intellectual Disabilities, Learning Disabilities, Autistic
disorder and Self-harm. Dementia and Epilepsy are not highly correlated with the rest of the disorders.

- **Unsupervised Machine Learning**

1. **K-Prototype** 

Below are the results of finding the optimal number of clusters using the Elbow method (Figure 5A) and the
Silhouette coefficient (Figure 5B). In the elbow method, we can see a bend where the graph looks like an elbow at K = 2 and K
= 3 in the left graph. In the right graph, it shows that the group of disorder is well-separated from other groups at K = 2 and K =
3 due to the higher silhouette coefficient than the other number of clusters (K). It indicates that 2 and 3 are the optimal number of clusters. 
<p align="center">
<img src="https://github.com/mill-ornrakorn/Spatiotemporal-epidemiology-and-analysis-of-mental-health-conditions-in-Thailand/blob/main/pic%20for%20readme/9.jpg?raw=true" alt= "K-Prototype" height="300">
</br>
<b>Figure 5</b> The results of (A) finding the optimal number of clusters for K-prototype clustering using Elbow method and (B)
Silhouette coefficient.
</p>

We applied K-Prototype to cluster the mental disorder. The algorithm clusters the disorders into groups based on the
similarity of the number of patients accessing mental health services (per 100,000 population in every province 2015-2021) and
the dissimilarity of the disorders’ names. When using K = 2, it divides 11 disorders into 2 groups. The first group includes
Schizophrenia, Depression and Anxiety disorder, and another group includes the rest. The result of the K-Prototype using K = 3
as represented in Figure 6 is quite similar to the correlation matrix, which also clusters disorders into 3 groups. In the correlation
matrix, Dementia and Epilepsy are not highly correlated with the rest of the disorders. For the K-prototype clustering result,
Dementia was assigned to the same group of Intellectual disabilities, Learning disabilities, Autistic disorder and Self-harm.
Epilepsy was assigned to the same group of Alcoholism and Drug addiction (excluding Amphetamine addiction). As we can see,
the first group using K = 2 and K = 3 has the exact same disorders. That means Schizophrenia, Depression and Anxiety disorder
are well-separated from other disorders and have a comparable number of patients accessing mental health services to each
other

<p align="center">
<img src="https://github.com/mill-ornrakorn/Spatiotemporal-epidemiology-and-analysis-of-mental-health-conditions-in-Thailand/blob/main/pic%20for%20readme/10.jpg?raw=true" alt= "clusterreult" height="150">
</br>
<b>Figure 6</b> The result of K-Prototype.

2. **Agglomerative hierarchical clustering**

We applied agglomerative hierarchical clustering and Ward's method to cluster the mental disorders. As a result, the
dendrogram in Figure 7 shows two major branches, A and B, by using a line cut-point to obtain clusters. We found three
clusters, represented in Figure 8. The first group includes Schizophrenia, Depression and Anxiety disorders. Subsequently, the
second group includes Dementia, Intellectual disabilities, Learning disabilities, Autistic disorder and Self-harm. The third group
includes Alcoholism, Drug addiction and Epilepsy.

<p align="center">
<img src="https://github.com/mill-ornrakorn/Spatiotemporal-epidemiology-and-analysis-of-mental-health-conditions-in-Thailand/blob/main/pic%20for%20readme/11.jpg?raw=true" alt= "hierarchical" height="400">
</br>
<b>Figure 7</b> The Dendrogram of mental disorder shows two major branches: A and B by using line cut-point to obtain three
clusters.
</p>


<p align="center">
<img src="https://github.com/mill-ornrakorn/Spatiotemporal-epidemiology-and-analysis-of-mental-health-conditions-in-Thailand/blob/main/pic%20for%20readme/10.jpg?raw=true" alt= "clusterreult" height="150">
</br>
<b>Figure 8</b> The result of Agglomerative hierarchical clustering.

**3. Spatial pattern analysis**
- **Global Spatial Detection**

<p align="center">
<img src="https://github.com/mill-ornrakorn/Spatiotemporal-epidemiology-and-analysis-of-mental-health-conditions-in-Thailand/blob/main/pic%20for%20readme/7.jpg?raw=true" alt= "tableglobal" height="300">
</br>
<b>Table 1</b> The value and p-value of Moran’s I hypothesis test of patients accessing mental health services in Thailand
during 2015-2021 (per 100k population).
</p>

According to the description, Global Moran's I is a statistic used to measure variable spatial autocorrelation. The table
below shows the value and p-value of Moran's I hypothesis test of mental health services accession in Thailand over a 7-year
period from 2015 to 2021, calculated per 100,000 population. The GEO package file in the Global Administrative Region
Database (GADM) Version 3.6 was used to create this analysis. According to Table 1's interpretation, there are 9 disorders with a
p-value of 0.05 (significant), indicating that we can find the pattern of cluster or location in neighboring positions that tend to
cluster but were unable to clearly identify the area.


However, there is a slight difference when looking at the yearly calculated p-value data. That is, the yearly p-value
has an interesting cluster pattern and exceeds several years in only 8 disorders: Alcoholism, Drug addiction (excluding
Amphetamine addiction), Schizophrenia, Depression, Anxiety disorder, Autistic disorder, Intellectual disabilities, and Learning
disabilities. It is divided into three subgroups: addiction, mood disorder, and brain disorder. This is why the researchers decided
to investigate the relationship by calculating the correlation coefficient between seven disorder pairs, as shown in Figure 10.

- **Local Spatial Detection**

This map was created using the LISA cluster technique and analysis. It was used to assess the autocorrelation within
local neighborhoods at the local level. Local measures can be used to identify spatial clusters and spatial outliers of each
disorder. The interpretation of the defined color results is described in the method's section 2.2.3 Local Spatial Detection (Local
Moran's I). The GEO package file in the Global Administrative Region Database (GADM) Version 3.6 was used to create all the
maps.

Figure 9 shows a cluster pattern of detectable mental health services for each disorder in Thailand. For spatial
interpretation, it was found that most clusters in the northern region had access to all 7 disorders, namely Depression, Anxiety
disorder, Intellectual disabilities, Learning disabilities, Autistic disorder, Self-harm and Epilepsy. In the northeast region, there
were clusters of the number of patients using mental health services for all 4 disorders, namely Alcoholism, Drug addiction,
Depression and Schizophrenia. In the central region, there was a cluster of patients accessing mental health services for all 2
disorders, namely Dementia and Self harm. For the cluster, there were 2 clusters of patients accessing mental health services in
the southern region: Anxiety disorder and Learning disabilities. In the eastern region, there is also a cluster of patients accessing
mental health services for 2 disorders: Autistic disorder and Epilepsy. The last area, the western region, had a cluster of patients
accessing mental health services only for learning disabilities. As shown in Figure 9,

<p align="center">
<img src="https://github.com/mill-ornrakorn/Spatiotemporal-epidemiology-and-analysis-of-mental-health-conditions-in-Thailand/blob/main/pic%20for%20readme/5.jpg?raw=true" alt= "mapLocal" height="400">
</br>
<b>Figure 9</b> Maps showing 11 clusters of disorders of the number of patients accessing mental health services in Thailand at the provincial level using Local Moran’s I statistic (LISA) used for a total of 7 years from 2015 to 2021.
</br>
<b>Note: </b>
For interpreting clusters, High-High were labeled by red, High-Low were labeled by yellow, Low-High were labeled by sky
blue, Low-Low were labeled by blue and Not significant were labeled by gray.
</p>

- **Disorder pairs**

The correlation coefficient was calculated at a national level. The results are shown in Figure 4. In addition to
arranging the disorders with similar correlation coefficients into the same cluster together. If determined using correlation data
and pattern finding data calculated from global Moran's I analysis together, it is interesting to carry out a further study to find
the correlation between pairs of disorders by calculating correlation detailed at the provincial level and using 7-year cumulative
patients accessing mental health services data from 2015 to 2021. For interpretation, if a dark area is found in any province, it
means these disorder pairs have a similar number of patients accessing mental health services that were continued for many
years in such provinces. In other words, a relationship was found between these disorder pairs. Which found a total of 7
relationships with interest from 8 disorders as shown in Figure 10: Alcoholism and Drug addiction (excluding Amphetamine
addiction) with a national correlation coefficient of 0.69. The second pair is Schizophrenia and Depression, with a correlation
coefficient of 0.19. The third pair is Schizophrenia and Anxiety disorder, a correlation coefficient of 0.62. The fourth pair is
Depression and Anxiety disorder with correlation coefficient of 0.32. The fifth pair is Autistic disorder and Intellectual disabilities
with correlation coefficient of 0.67. The sixth pair is Autistic disorder and Learning disabilities with correlation coefficient of 0.37,
and last disorder pairs is Intellectual disabilities and Learning disabilities, with a correlation coefficient of 0.39.

In terms of interpreting spatial outcomes for interrelated disorder pairs when calculating correlation at province level.
It was found that most provinces in the northern region were related to Alcoholism and Drug addiction, Schizophrenia and
Anxiety disorder. In addition, Autistic disorder, Intellectual disabilities and Learning disabilities that are the part of brain-related
disorders were also found. In most provinces in the Northeast, there was a relationship between Alcoholism and Drug addiction,
Schizophrenia and Anxiety disorder. The central and southern regions found the same pairs of disorders, namely, brain-related
disorders (Autistic disorder, Intellectual disabilities and Learning disabilities). For the western ans eastern region, it was found a
relationship of disorder pairs; Schizophrenia and Depression and the second pair is Depression and Anxiety disorder are shown
in Figure 10.

<p align="center">
<img src="https://github.com/mill-ornrakorn/Spatiotemporal-epidemiology-and-analysis-of-mental-health-conditions-in-Thailand/blob/main/pic%20for%20readme/6.jpg?raw=true" alt= "mapdisorderpairs" height="250">
</br>
<b>Figure 10</b> Map of Spearman’s correlation of disorder pairs of the number of patients accessing mental health services in
Thailand at the provincial level for a total of 7 years (2015-2021)
</p>


## Discussion 🔍

In the discussion of spatial outcomes, it was found that the clusters of spatial autocorrelation patterns occurred in
various regions. For example, the major clusters of spatial autocorrelation depression were discovered in several northern
provinces where the Mind organization provided information on Seasonal Affective Disorder (SAD). SAD is a type of depression
that occurs during specific seasons or times of year. Depression is characterized by a persistently low mood that interferes with
daily activities. If you have SAD, you will experience depression during certain seasons or due to certain types of weather or
temperature. It is available in both winter and summer [(50)](https://www.mind.org.uk/information-support/types-of-mental-health-problems/seasonal-affective-disorder-sad/about-sad/). That is why the North has a large number of patient depressive
services compared to other regions. The second disorder is drug addiction. According to an analysis of the current drug situation
in 2017, most of the northern regions, especially the fringe areas, are conducive to the smuggling of drugs from neighboring
countries that produce drugs, namely countries. Laos, Myanmar, and Cambodia [(51)](https://so03.tci-thaijo.org/index.php/rdirmu/article/view/209737). As a result, it may be the cause of the drug
epidemic and a large number of patients seeking drug addiction services in the north. Then there was the cluster of spatial
autocorrelation anxiety disorders, which were mostly found in the Northeast. It's a very hot climate. A description of cortisol: it's
a hormone secreted by stress or anxiety. Cortisol levels are higher in the summer than in the winter [(52)](https://www.stylist.co.uk/life/summer-anxiety-makes-worse-heat-wave-social-causes-symptoms-advice/219735). The northeastern
region of Thailand has the highest average temperature. A rise in temperature can also cause agitation, palpitations, nausea, and
fatigue, which is a common anxiety symptom. There are other disorders that were not discussed because there is limited
information.

From all the methods we used (correlation matrix, K-prototype clustering, and agglomerative hierarchical clustering),
there are three groups of disorders that cluster based on characteristics of the number of patients accessing mental health
services in every province from 2015-2021.
The first group includes Alcoholism, Drug addiction (excluding Amphetamine addiction), and Epilepsy. These disorders
are highly correlated due to the fact that abusing alcohol has a potential risk of other substance use, such as marijuana,
cocaine, and heroin (at least one) [(53)](https://www.alcoholrehabguide.org/alcohol/drinking-drugs/). For the association between Alcoholic and Epilepsy, the available evidence suggests
that the prevalence of epilepsy among alcoholics is at least triple that in the general population, and that alcoholism may be
more prevalent among epileptic patients than in the general population [(54)](http://dx.doi.org/10.1111/j.1528-1157.1985.tb05658.x).

The second group includes Schizophrenia, Depression and Anxiety disorder. From the result of the correlation, it was
found that Schizophrenia and Anxiety disorder are more highly correlated than Schizophrenia and Depression. In this research,
the prevalence of anxiety disorders was studied. The incidence of anxiety disorders was 45.16% in schizophrenia compared to
controls. The research findings show that anxiety disorders are higher in schizophrenia than in the general population. It is also
said that symptoms of anxiety tend to precede symptoms of schizophrenia [(55)](http://dx.doi.org/10.4103/0972-6748.196045). Likewise, the Conrad and Chapman study
found that anxiety disorders are one of the early causes of schizophrenia [(56)](http://dx.doi.org/10.1155/2018/5917475). On the other hand, anxiety disorders may occur
after treatment for schizophrenia due to concerns in daily life. The stress of being judged because of admission for
schizophrenia is not widely accepted by society. This is reason enough to explain the relationship between schizophrenia and
anxiety disorders. There was also a relationship between schizophrenia and depression. which had lower correlation values
compared to schizophrenia and anxiety disorders. Therefore, when diagnosed with this type of disorder, it is less likely to be
identified as schizophrenia [(57)](http://dx.doi.org/10.1016/j.schres.2013.05.028). But when diagnosed with schizophrenia, depression may also be present. Therefore, the
correlation calculation showed that the correlation was low.

The last group includes Intellectual disabilities, Learning disabilities, Autistic disorder, Self-harm and Dementia. The
correlation coefficient between Autistic disorder and Intellectual disabilities is higher than the correlation coefficient between
Autistic disorder and Learning disabilities because Intellectual disabilities are the most common co-occurring disorder with
Autistic disorder, and the greater severity of one of these two disorders appears to have effects on the other disorder [(58)](http://dx.doi.org/10.1016/j.ridd.2009.06.003).
Dementia correlates with Autistic disorder and also correlates with Intellectual Disabilities. Vivanti et al. used US medical
insurance records for 1.2 million individuals aged 30–64 years. The prevalence was highest among people with intellectual
disability alone (7.10%), but was also considerably higher among people with ASD (4.04%) and people with ASD and intellectual
disability (5.22%) than among the healthy population (0.97%) [(59)](http://dx.doi.org/10.1002/aur.2590). For the association with Self-harm, the study of Blanchard et
al. shows that Autistic disorder was associated with a substantially increased risk of self-injurious behaviors and suicidality, and
people with Autistic disorder had 2.26-times higher odds of self-harm than those without ASD [(60)](http://dx.doi.org/10.1001/jamanetworkopen.2021.30272).

There are several limitations to this study. First, the data source was a mental health accessed services report and
stigmatization of mental disorders may prevent patients from seeking treatment. Therefore, the number of patients accessing
mental health services may not be the same as the actual number of patients that occur. Furthermore, the number and
location of mental health services in each province may affect the difficulty of accessing the service and may explain why the
number of patients accessing mental health services is low. Another limitation is that Bangkok Metropolis's mental health
accessed services data was missing in 2017. Missing data can reduce the efficiency of statistical analysis [(61)](http://dx.doi.org/10.4097/kjae.2013.64.5.402). Moreover, many
people may have more than one mental health diagnosis [(62)](https://www.constellationbehavioralhealth.com/blog/the-importance-of-a-complete-diagnosis-managing-multiple-mental-illnesses/). All of the above limitations can cause bias in the data. As for the
future work, we desired to reduce the limitations to the least.



## Conclusions 📄
The results of this study provided information about the spatiotemporal characteristics of mental disorders in Thailand and also revealed the limitations of the data, which have an impact on the overall analysis and further applications. For more accurate and interpretable results, such as geographic heat maps and associations between two disorders, the data used for analysis should represent the real characteristics of each disorder, which can lead to change, such as mental health policy by the government, attitudes and public interaction, and access to prevention and treatments.


## References 📖

50. What is seasonal affective disorder (SAD)? [Internet]. [cited 2022 Jul 24]. Available from:
https://www.mind.org.uk/information-support/types-of-mental-health-problems/seasonal-affective-disorder-sad/about-sad/

51. Jandeang B. Analysis of Current Drug Situation Problem [Internet]. Journal of Research and Development Institute,Rajabhat Maha Sarakham University. 2017;4(2):37–56. Available from: https://so03.tci-thaijo.org/index.php/rdirmu/article/view/209737

52. Geall L, Crockett M. You’re not imagining it: hot weather really can make anxiety worse – here’s how to deal with it 27 [Internet]. Stylist. The Stylist Group; 2022 [cited 2022 Jul 24]. Available from: https://www.stylist.co.uk/life/summer-anxiety-makes-worse-heat-wave-social-causes-symptoms-advice/219735

53. Galbicsek C. Drinking And Drugs [Internet]. Alcohol Rehab Guide. [cited 2022 Jul 19]. Available from:
https://www.alcoholrehabguide.org/alcohol/drinking-drugs/

54. Chan AWK. Alcoholism and Epilepsy [Internet]. Vol. 26, Epilepsia. 1985. p. 323–33. Available from:
http://dx.doi.org/10.1111/j.1528-1157.1985.tb05658.x

55. Chaudhury S, Kiran C. Prevalence of comorbid anxiety disorders in schizophrenia [Internet]. Vol. 25, Industrial Psychiatry
Journal. 2016. p. 35. Available from: http://dx.doi.org/10.4103/0972-6748.196045

56. Grillo L. A Possible Link between Anxiety and Schizophrenia and a Possible Role of Anhedonia [Internet]. Vol. 2018,
Schizophrenia Research and Treatment. 2018. p. 1–8. Available from: http://dx.doi.org/10.1155/2018/5917475

57. Tandon R, Gaebel W, Barch DM, Bustillo J, Gur RE, Heckers S, et al. Definition and description of schizophrenia in the
DSM-5. Schizophr Res [Internet]. 2013 Oct;150(1):3–10. Available from: http://dx.doi.org/10.1016/j.schres.2013.05.028

58. Matson JL, Shoemaker M. Intellectual disability and its relationship to autism spectrum disorders [Internet]. Vol. 30,
Research in Developmental Disabilities. 2009. p. 1107–14. Available from: http://dx.doi.org/10.1016/j.ridd.2009.06.003

59. Vivanti G, Tao S, Lyall K, Robins DL, Shea LL. The prevalence and incidence of early-onset dementia among adults with
autism spectrum disorder. Autism Res [Internet]. 2021 Oct;14(10):2189–99. Available from:
http://dx.doi.org/10.1002/aur.2590

60. Blanchard A, Chihuri S, DiGuiseppi CG, Li G. Risk of Self-harm in Children and Adults With Autism Spectrum Disorder: A
Systematic Review and Meta-analysis. JAMA Netw Open [Internet]. 2021 Oct 1;4(10):e2130272. Available from:
http://dx.doi.org/10.1001/jamanetworkopen.2021.30272

61. Kang H. The prevention and handling of the missing data [Internet]. Vol. 64, Korean Journal of Anesthesiology. 2013. p. 402. Available from: http://dx.doi.org/10.4097/kjae.2013.64.5.402

62. Ellis ME. The importance of a complete diagnosis: Managing multiple mental illnesses [Internet]. Constellation Behavioral Health. [cited 2022 Jul 18]. Available from:
https://www.constellationbehavioralhealth.com/blog/the-importance-of-a-complete-diagnosis-managing-multiple-mental-illnesses/



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