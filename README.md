# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) College Tests Outcomes across Geographically Areas in California

# Table of Contents

* [Problem Statement](#problem-statement)
  * [Questions](#questions)
* [Datasets](#datasets)
  * [Data Dictionary](#data-dictionary)
    * [ACT Dataset](#act-dataset)
    * [SAT Dataset](#sat-dataset)
* [Findings](#findings)
* [Key Takeaways](#key-takeaways)
* [Recommendations](#recommendations)

# Problem Statement
Quantify the overall college test performance and participation for 12th graders in rural, suburban, and urban areas in California

## Questions
Which counties have SAT or ACT scores that are below the national average?
Is there a difference between English vs Math?
What is the student participation rate in ACT and SAT tests?

# Datasets

* ACT Data for California 12th graders for 2019
* [`act_2019_ca.csv`](./data/act_2019_ca.csv): 2019 ACT Scores in California by School ([source](https://www.cde.ca.gov/ds/sp/ai/) | [data dictionary](https://www.cde.ca.gov/ds/sp/ai/reclayoutact19.asp))
* SAT Data for California 12th graders for 2019
* [`sat_2019_ca.csv`](./data/sat_2019_ca.csv): 2019 SAT Scores in California by School ([source](https://www.cde.ca.gov/ds/sp/ai/) | [data dictionary](https://www.cde.ca.gov/ds/sp/ai/reclayoutsat19.asp))
* 57 counties included in the analysis
* 1646 schools included in the analysis



## Data Dictionary

### ACT Dataset

|Feature|Type|Dataset|Description|
|---|---|---|---|
|code|object|ACT|The county, district, or school code|
|county_code|object|ACT|The county code|
|district_code|object|ACT|The district code|
|school_code|object|ACT|The school code|  
|record_type|object|ACT|The record type C=County, D=District, S=School, X=State|
|school_name|object|ACT|The school name, N/A = County or District Level Record|
|district_name|object|ACT|The district name, N/A = County or District Level Record|
|county_name|object|ACT|The county name|
|enrollment|int|ACT|Enrollment of grade 12|
|test_takers|int|ACT|This is the number of ACT test takers|
|avg_scr_read|int|ACT|Average ACT  Reading Score, an asterisk is displayed  for schools with 14 or fewer students taking the ACT in order to preserve the anonymity of the students. An N/A is displayed if there were no ACT test takers and the grade 12 enrollment is equal to or greater than 15|
|avg_scr_eng|int|ACT|Average ACT  English Score, an asterisk is displayed  for schools with 14 or fewer students taking the ACT in order to preserve the anonymity of the students. An N/A is displayed if there were no ACT test takers and the grade 12 enrollment is equal to or greater than 15|
|avg_scr_sci|int|ACT|Average ACT Science Score, an asterisk is displayed  for schools with 14 or fewer students taking the ACT in order to preserve the anonymity of the students. An N/A is displayed if there were no ACT test takers and the grade 12 enrollment is equal to or greater than 15|
|avg_scr_math|int|ACT|Average ACT Math Score, an asterisk is displayed  for schools with 14 or fewer students taking the ACT in order to preserve the anonymity of the students. An N/A is displayed if there were no ACT test takers and the grade 12 enrollment is equal to or greater than 15|
|tst_takers_scr>21|int|ACT|Number of Test Takers Whose ACT Composite Scores Are Greater or Equal to 21. An asterisk is displayed for schools with 14 or fewer students taking the ACT in order to preserve the anonymity of the students. An N/A is displayed if there were no ACT test takers and the grade 12 enrollment is equal to or greater than 15|
|tst_takers%_scr>21|float|ACT|Percent of Test Takers Whose ACT Composite Scores Are Greater or Equal to 21.An asterisk is displayed for schools with 14 or fewer students taking the ACT in order to preserve the anonymity of the students. An N/A is displayed if there were no ACT test takers and the grade 12 enrollment is equal to or greater than 15.|
|year|object|ACT|The ACT test administration year: 2018-19|


### SAT Dataset

|Feature|Type|Dataset|Description|
|---|---|---|---|
|code|object|SAT|The county, district, or school code|
|county_code|object|SAT|The county code|
|district_code|object|SAT|The district code|
|school_code|object|SAT|The school code|  
|record_type|object|SAT|The record type C=County, D=District, S=School, X=State|
|school_name|object|SAT|The school name, N/A = County or District Level Record|
|district_name|object|SAT|The district name, N/A = County or District Level Record|
|county_name|object|SAT|The county name|
|12grade_enrollment|int|SAT|Enrollment of grade 12|
|12grade_test_takers|int|SAT|This is the number of SAT test takers in 12th grade|
|12graders_passing_ERW|int|SAT|The number meeting the Evidence-Based Reading & Writing (ERW) benchmark established by the College Board based on the New 2016 SAT test format as of March 2016 for Grade 12|
|12graders%_passing_ERW|float|SAT|The percent of students meeting the Evidence-Based Reading & Writing (ERW) benchmark established by the College Board based on the New 2016 SAT test format as of March 2016 for Grade 12|
|12graders_passing_Math|int|SAT|The number of students who met or exceeded the benchmark for the New SAT Math test format as of March 2016 for Grade 12|
|12graders%_passing_Math|float|SAT|The percent of students who met or exceeded the benchmark for SAT Math test for Grade 12|
|11grade_enrollment|int|SAT|Enrollment of grade 11|
|11grade_test_takers|int|SAT|This is the number of SAT test takers in 11th grade|
|11graders_passing_ERW|int|SAT|The number meeting the Evidence-Based Reading & Writing (ERW) benchmark established by the College Board based on the New 2016 SAT test format as of March 2016 for Grade 11|
|11graders%_passing_ERW|float|SAT|The percent of students who met or exceeded the benchmark for Evidence-Based Reading & Writing (ERW) test for Grade 11.|
|11graders_passing_Math|int|SAT|or the New SAT Math test format as of March 2016 for Grade 11.|
|11graders%_passing_Math|float|SAT|The percent of students who met or exceeded the benchmark for SAT Math test for Grade 11.|
|12graders_passing_both_tst|int|SAT|The total number of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 12.|
|12graders%_passing_both_tst|float|SAT|The percent of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 12.|
|11graders_passing_both_tst|int|SAT|The total number of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 11.|
|11graders%_passing_both_tst|float|SAT|The percent of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 11.|
|year|object|SAT|The SAT test administration year: 2018-19|

# Findings

A data analysis was conducted using Python. See data sets and complete analysis in College_Test_Outcomes_CA.ipynb attached and supporting CSV files.

The following were the findings from the EDA and Data Visualization:

1. The average number of students in rural counties having a passing score in the SAT or ACT is considerably lower than the average number of students having a good score in urban and suburban counties.
2. There is strong correlation in test scores for ACT across all test categories.
3. There is a strong correlation for number of students who pass the SAT Engligh/Reading/Writing section and number of students who pass the SAT Math section
4. For the SAT, the average number of students having a passing score is greater for English/Reading/Writing than Math.
5. Student participation rate in ACT is less than 20%
6. Student participation rate in SAT is less than 40%
7. Student in rural areas have the lowest average of number of students passing the ACT test
8. The distributions for number of students passing the English/Reading/Writing is different across rural, suburban, and urban counties.
9. For English/Reading/Writing, rural counties have the lowest number of students with a passing score.
10. For Math, rural counties also have the lowest number of students with a passing score
11. The box plots show a slight higher number of students passing SAT ERW over Math tests.
12. The data for number of students passing the SAT has outliers for urban, suburban, and rural areas, as well as for ERW and Math. These outliers represent a higher number of students passing the specific test section in comparison to the average number of students.


# Key Takeaways
1. The average number of students in rural counties having a good score in the SAT or ACT is considerably lower than the average number of students having a good score in urban and suburban counties.
2. There is no much difference in the average of scores across the test categories in the ACT. For the SAT, the average number of students having a passing score is greater for English/Reading/Writing than Math.
3. Student participation rate in ACT and SAT testing is the same across rural, suburban, and urban areas across California

# Recommendations
1. The low test performance in rural counties is a red flag. Need to evaluate this further by analyzing the data of other school performance metrics for students (ideally across all grades) in rural counties and compare this with the data from suburban and urban school metrics.
2. Analyze what factors can be affecting testing performance in rural counties such as school funding, school programs, and teacher qualifications.
3. Investigate and determine the needs of students in rural counties interested in taking the ACT or SAT.
