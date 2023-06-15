# \# SISE2601 Project Code Replication Instructions:
Team name 7 - Nir Rahav, Shahar Oded and Guy Zagorski.

save the folder on your local machine while keeping the formation of the inner folders - data folder, proposel, final results.

Our final code is composed of 3 notebooks. 
The first - our proposal notebook, can be knitted directly, just update the links to the data extraction in the beginning of the codebook to fit your saved location

The Second - final results R notebook, "model", have all the imports and actions needed. Load the notebook and after importing the files in, start running the code block by block. Pay attantion to the data scaling block, no need to run it as it was found uninfluencial to the results. The statistic visualizations will appear as well, and you'll notice the data sampling preformed. In the end, you'll see how the K-Means model and viz are created. You can change the input feature in the final function to see the correlations for different features in compared to the target vriable.
Once you finish running this code, a "data_sample" file will be exported to your repository.

The Third - "Models" notebook in Python. To start, open this notebook in Collab or similar.Import "data_sample" file from R notebook output. Start running the code. You'll see the creation and testing of a regression tree model. Afterwards, you'll see a SHAP analysis on said tree.

And that's it!

# \# SISE2601 Project Data Description

This Markdown file describes the data folder structure and organization ...

CASEID (Case identification number) - Program generated case (record) identifier. A frequency distribution of this variable is not shown; each case has a unique value generated for identification purposes.

AGE - Calculated from date of birth and date of admission and categorized.

| Value |       Label        |
|:-----:|:------------------:|
|   1   |    12-14 years     |
|   2   |    15-17 years     |
|   3   |    18-20 years     |
|   4   |    21-24 years     |
|   5   |    25-29 years     |
|   6   |    30-34 years     |
|   7   |    35-39 years     |
|   8   |    40-44 years     |
|   9   |    45-49 years     |
|  10   |    50-54 years     |
|  11   |    55-64 years     |
|  12   | 65 years and older |

GENDER - This field identifies the client's biological sex

| Value | Label  |
|:-----:|:------:|
|   1   |  Male  |
|   2   | Female |

CALC_RACE - This field identifies the client's race:

-   Black or African American: A person having origins in any of the black racial groups of Africa.

-   White: A person having origins in any of the original people of Europe, the Middle East, or North Africa.

-   Other - Use this category for instances in which the client is not identified in any category above or whose origin group, because of area custom, is regarded as a racial class distinct from the above categories. This category includes the following types:

    -   Alaska Native (Aleut, Eskimo)

    -   American Indian

    -   Pacific Islander

    -   Asian

    -   Native Hawaiian

    -   Two or more races

| Value |           Label           |
|:-----:|:-------------------------:|
|   1   | Black or African American |
|   2   |           White           |
|   3   |        Other race         |

MARSTAT (Marital status) - This field describes the client's marital status. The following categories are compatible with categories used in the U.S. Census.

-   Never married: Includes clients who are single or whose only marriage was annulled.

-   Now married: Includes married couples, those living together as married, living with partners, or cohabiting.

-   Separated: Includes those legally separated or otherwise absent from spouse because of marital discord.

-   Divorced, widowed

| Value |       Label       |
|:-----:|:-----------------:|
|   1   |   Never married   |
|   2   |    Now married    |
|   3   |     Separated     |
|   4   | Divorced, widowed |

EDUC (Education) - This field specifies:

-   the highest school grade completed for adults or children not attending school

-   current school grade for school-age children (3-17 years old) attending school.

| Value |                                        Label                                         |
|:----------------:|:----------------------------------------------------:|
|   1   | Less than one school grade, no schooling, nursery school, or kindergarten to Grade 8 |
|   2   |                                    Grades 9 to 11                                    |
|   3   |                                  Grade 12 (or GED)                                   |
|   4   |                1-3 years of college, university, or vocational school                |
|   5   |       4 years of college, university, BA/BS, some postgraduate study, or more        |

FRSTUSE_LEGAL (Age at first use - legal material) - The field goes over FRSTUSE1, FRSTUSE2 and FRSTUSE3 and check which age the client use for the first time in legal material (either alcohol or weed in legalized countries).

| Value |                     Label                     |
|:-----:|:---------------------------------------------:|
|   1   |            11 years old and under             |
|   2   |                  12-14 years                  |
|   3   |                  15-17 years                  |
|   4   |                  18-20 years                  |
|   5   |                  21-24 years                  |
|   6   |                  25-29 year                   |
|   7   |               30 year and older               |
|  -9   |          Not use/Missing/unknown/invalid      |
|  NA   | Not recorded (only illegal drug use records)  |

FRSTUSE_ILLEGAL (Age at first use - illegal material) - The field goes over FRSTUSE1, FRSTUSE2 and FRSTUSE3 and check which age the client use for the first time in illegal material.

| Value |                     Label                     |
|:-----:|:---------------------------------------------:|
|   1   |            11 years old and under             |
|   2   |                  12-14 years                  |
|   3   |                  15-17 years                  |
|   4   |                  18-20 years                  |
|   5   |                  21-24 years                  |
|   6   |                  25-29 year                   |
|   7   |               30 year and older               |
|  -9   |         Not use/Missing/unknown/invalid       |
|  NA   | Not recorded (only legal drug use records)    |

EMPLOY (Employment status) - This field identifies the client's employment status.

-   Full-time: Working 35 hours or more each week, including active duty members of the uniformed services.

-   Part-time: Working fewer than 35 hours each week.

-   Unemployed: Looking for work during the past 30 days or on layoff from a job.

-   Not in labor force: Not looking for work during the past 30 days or a student, homemaker, disabled, retired, or an inmate of an institution. Clients in this category are further defined in Detailed Not in Labor Force.

| Value |       Label        |
|:-----:|:------------------:|
|   1   |     Full-time      |
|   2   |     Part-time      |
|   3   |     Unemployed     |
|   4   | Not in labor force |

PREG (Pregnant at admission) - This field indicates whether a female client was pregnant at the time of admission. Missing values were counted as No.

| Value | Label |
|:-----:|:-----:|
|   1   |  Yes  |
|   2   |  No   |

VET (Veteran status) - This field indicates whether the client has served in the uniformed services (Army, Navy, Air Force, Marine Corps, Coast Guard, Public Health Service Commissioned Corps, Coast and Geodetic Survey, etc.). Missing values were counted as No.

| Value | Label |
|:-----:|:-----:|
|   1   |  Yes  |
|   2   |  No   |

STATE_PARTY - This field calculate by the last 10 elections and classifies the country according to its coloring on the political map

-   Democrat - States where in seven of the last ten elections the majority voted for the Democratic Party

-   Republican - States where in 7 of the last ten elections the majority voted for the Republican Party

-   Mitnadned - States where sometimes the majority votes for the Democratic Party and sometimes for the Republican Party

| Value | Label           |
|-------|-----------------|
| 0     | Republican      |
| 1     | Unstable / else |
| 2     | Democratic      |

LIVARAG (Living arrangements) - Identifies whether the client is homeless, a dependent (living with parents or in a supervised setting) or living independently on his or her own.

-   Homeless: Clients with no fixed address; includes homeless shelters.

-   Dependent living: Clients living in a supervised setting such as a residential institution, halfway house, or group home, and children (under age 18) living with parents, relatives, or guardians or (substance use clients only) in foster care.

-   Independent living: Clients living alone or with others in a private residence and capable of self-care. Includes adult children (age 18 and over) living with parents and adolescents living independently. Also, includes clients who live independently with case management or supported housing support.

| Value |      Label       |
|:-----:|:----------------:|
|   1   |     Homeless     |
|   2   | Dependent living |
|   3   |   Independent    |

PRIMINIC (Source of income/support) - This field identifies the client's principal source of financial support. For children younger than 18 years old, report the primary parental source of income/support.

| Value |                 Label                 |
|:-----:|:-------------------------------------:|
|   1   |             Wages/salary              |
|   2   |           Public assistance           |
|   3   |    Retirement/pension, disability     |
|   4   |                 Other                 |
|   5   |                 None                  |
|  -9   | Missing/unknown/not collected/invalid |

ARRESTS (Arrests in past 30 days) - Indicates the number of arrests in the 30 days prior to the reference date (i.e., date of admission or date of discharge). This field is intended to capture the number of times the client was arrested (not the number of charges) for any cause during the reference period. Any formal arrest should be counted, regardless of whether incarceration or conviction resulted. Missing values were counted as None.

| Value |      Label       |
|:-----:|:----------------:|
|   0   |       None       |
|   1   |       Once       |
|   2   | Two or more time |

PSOURCE (Referral source) - This field describes the person or agency referring the client to treatment:

-   Individual (includes self-referral): Includes the client, a family member, friend, or any other individual who would not be included in any of the following categories; includes self-referral due to pending DWI/DUI.

-   Alcohol/drug use care provider: Any program, clinic, or other health care provider whose principal objective is treating clients with substance use diagnosis, or a program whose activities are related to alcohol or other drug use prevention, education, or treatment.

-   Other health care provider: A physician, psychiatrist, or other licensed health care professional; or general hospital, psychiatric hospital, mental health program, or nursing home.

-   School (educational): A school principal, counselor, or teacher; or a student assistance program (SAP), the school system, or an educational agency.

-   Employer/EAP: A supervisor or an employee counselor.

-   Other community referral: Community or religious organization or any federal, state, or local agency that provides aid in the areas of poverty relief, unemployment, shelter, or social welfare. This category also includes defense attorneys and self-help groups such as Alcoholics Anonymous (AA), Al-Anon, and Narcotics Anonymous (NA).

-   Court/criminal justice referral/DUI/DWI: Any police official, judge, prosecutor, probation officer or other person affiliated with a federal, state, or county judicial system. Includes referral by a court for DWI/DUI, clients referred in lieu of or for deferred prosecution, or during pre-trial release, or before or after official adjudication. Includes clients on pre-parole, pre-release, work or home furlough or TASC. Client need not be officially designated as "on parole." Includes clients referred through civil commitment. Clients in this category are further defined in Detailed Criminal Justice Referral

| Value |                  Label                  |
|:-----:|:---------------------------------------:|
|   1   |   Individual (includes self-referral)   |
|   2   |     Alcohol/drug use care provider      |
|   3   |       Other health care provider        |
|   4   |          School (educational)           |
|   5   |              Employer/EAP               |
|   6   |        Other community referral         |
|   7   | Court/criminal justice referral/DUI/DWI |

DSMCRIT (DSM diagnosis) - Client's diagnosis is used to identify the substance use problem that provides the reason for client encounter or treatment. This can be reported by using either the Diagnostic and Statistical Manual of Mental Disorders (DSM) from the American Psychiatric Association or the International Classification of Diseases (ICD), from the World Health Organization.

The discrete diagnosis codes have been recoded into categories related to use of and dependence on specific substances, mental health conditions, and other conditions. Diagnoses reported by states using either standard classification of mental disorders have been combined.

| Value |                             Label                              |
|:-----:|:--------------------------------------------------------------:|
|   1   |                    Alcohol-induced disorder                    |
|   2   |                   Substance-induced disorder                   |
|   3   |                      Alcohol intoxication                      |
|   4   |                       Alcohol dependence                       |
|   5   |                       Opioid dependence                        |
|   6   |                       Cocaine dependece                        |
|   7   |                      Cannabis dependence                       |
|   8   |                   Other substance dependence                   |
|   9   |                         Alcohol abuse                          |
|  10   |                         Cannabis abuse                         |
|  11   |                     Other substance abuse                      |
|  12   |                          Opioid abuse                          |
|  13   |                         Cocaine abuse                          |
|  14   |                       Anxiety disorders                        |
|  15   |                      Depressive disorders                      |
|  16   |            Schizophrenia/other psychotic disorders             |
|  17   |                       Bipolar disorders                        |
|  18   |        Attention deficit/disruptive behavior disorders         |
|  19   |                  Other mental health condtion                  |
|  -9   | Missing/unknown/not collected/invalid/no or deferred diagnosis |

FREQ_ATND_SELF_HELP (Attendance at substance use self-help groups in past 30 days) - This field indicates the frequency of attendance at a substance use self-help group in the 30 days prior to the reference date (the date of admission or date of discharge). It includes attendance at Alcoholics Anonymous (AA), Narcotics Anonymous (NA), and other self-help/mutual support groups focused on recovery from substance use and dependence.

| Value |                 Label                 |
|:-----:|:-------------------------------------:|
|   1   |            Not attendance             |
|   2   |      1-3 times in the past month      |
|   3   |      4-7 times in the past month      |
|   4   |     8-30 times in the past month      |
|   5   |  Some attendance, frequency unknown   |
|  -9   | Missing/unknown/not collected/invalid |

UNDER_INFLUENCE - This field describe if the client arrive under any influence of drugs or alcohol to the admission.

| Value | Label |
|:-----:|:-----:|
|   0   | False |
|   1   | True  |

SUBSTANCE - This field describe the addiction of each person according to his statements in SUB1, SUB2 and SUB3. The field use function that check if the addiction is to legal drugs (include alcohol) or not and classify them. If person use legal drug (include alcohol) and illegal drug we classify it according to the illegal drug. If a person was classified as user of 2 illegal drugs of different type, the record was ommited in the filter.

-   Stimulant - Bitter drugs

-   Depressant - depressant or "down" drugs

-   legal in state - Legal drugs, according to the states.

-   Over the counter / other - Medicines that are available in pharmacies and are consumed excessively or other

The values are ordered by severity.

| Value |          Label           |
|:-----:|:------------------------:|
|   0   |      legal in state      |
|   1   | Over the counter / other |
|   2   |        Stimulant         |
|   3   |        Depressant        |

: ADDICTIV_LEVEL - This field describe the patient's level of addiction. It's take the addictions and with the help of a function calculates the level of addiction. The field refers to the patient's most addictive drug.

-   Non addictive / Unknown - not addictive

-   Low - low level addictive

-   High - medium level addictive

-   Very high - High level addictive

| Value |          Label           |
|:-----:|:------------------------:|
|   1   | Non addictive / Unknown  |
|   2   |           Low            |
|   3   |           High           |
|   4   |        Very high         |

: FREQ (Frequency of use) - Specifies the frequency of use of the substances. The field uses a function that calculates the material that is consumed at the highest level and which it displays.

| Value |                 Label                 |
|:-----:|:-------------------------------------:|
|   1   |       No use in the past month        |
|   2   |               Some use                |
|   3   |               Daily use               |
|  -9   | Missing/unknown/not collected/invalid |

: PSYPROB (Co-occurring mental and substance use disorders) - Indicates whether the client has co-occurring mental and substance use disorders

| Value | Label |
|:-----:|:-----:|
|   1   |  Yes  |
|   2   |  No   |

NOPRIOR (Previous substance use treatment episodes) - Indicates the number of previous treatment episodes the client has received in any substance use treatment program. Changes in service for the same episode (transfers) should not be counted as separate prior episodes.

| Value |                 Label                 |
|:-----:|:-------------------------------------:|
|   0   |      No prior treatment episodes      |
|   1   |     One prior treatment episodes      |
|   2   |     Two prior treatment episodes      |
|   3   |    Three prior treatment episodes     |
|   4   |     Four prior treatment episodes     |
|   5   | Five or more prior treatment episodes |
