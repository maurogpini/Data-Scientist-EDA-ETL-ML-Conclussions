<h1 align=center> MAURO GONZALO PINI
<h1 align=center> HENRY LABS - DATA SCIENCE COHORT 06
<h1 align=center> INDIVIDUAL PROJECT #2

## **Context**

The scenario simulates a request regarding a database with 346,479 rows and 22 columns containing various data related to the real estate market in the USA. You can read the detailed instructions in the CONSIGNA.md file, but in summary, the requirement was to create a Machine Learning model that can predict whether a property belongs to a category defined by a price range.

## **Documentation and Description of the Process**

Initially, I conducted an in-depth exploratory analysis and data transformation, which can be seen in detail in version 1 of the work, provided in the V1_EDA_ETL file. I was extremely meticulous in detecting and eliminating duplicate records, reducing their number from 346,479 to 63,297, which represents 18.26% of the initial total. I then decided to implement several supervised learning models but was unable to achieve an accuracy of over 80% when testing the model against a test dataset.

It was then that I hypothesized that training the model with a small number of records might have caused subsequent prediction problems. So, I created a completely different EDA (Exploratory Data Analysis) and ETL (Extract, Transform, Load) process, changing the criteria to be much more lenient, leaving 251,639 records in the dataset (72.62%).

To compare the results, I decided to focus on evaluating the performance of a decision tree model with predefined parameters applied to the same data column structure. In this case, I achieved an accuracy of 91% against the test dataset, representing a significant improvement. The third scenario is an intermediate one in which I worked with 147,404 records, representing 42.5% of the original data, and achieved an accuracy of 84%.

## **Conclusions**

At first glance, one might infer that the more data you have to analyze, the better the result. One would easily agree with that statement. However, several questions arise when reflecting on the matter. If a large portion of the sample space is biased or filled with inconsistencies, will my conclusions be accurate? If the nature of the question is to determine the price category of a property, is it beneficial for the model training to have records that repeat up to 380 times?

Much will depend on the nature of the question you want to answer and the type of information required. Beyond the specifics of this particular case, what these notebooks and their development demonstrate is that the analyst's criteria, the decisions they make, and the order in which they make them directly and significantly affect the final outcome. A specific decision in the ETL stage can determine the entire future of a project.
