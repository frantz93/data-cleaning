# data-cleaning
Improving data quality

## Basic factors to take into account when preparing a data management plan
1. Data format: file type (ex. Text file, Excel sheet, Access DB, pandas df,...), field types
2. Naming and file structure: need a convention for naming files building directories 
    - meaningful name for the file and logical rules for directories
    - will allow to easily write code which refer to files by using the as less operation as possible
    - a look-up table may be useful for informing about different data tables
3. Access: refers to the privacy of the data files -> eventual restrictions to the data may be set
4. Storage and backup
    - choose of the place to store the data (ex. usb drive, hard drive, cloud,...)
    - who is responsible for managing the back up? 
    - what is the back up frequency?
5. Code: need to define the way that scripts will be managed
    - central repository for the codes? or each user has their own versions?
    - the method for sharing codes (end-to-end user sharing, github,...)
    - immutable code files or anyone can edit?
    - what language will be used (ex. Python, R)

## Documenting the data
Theses points need to be highlihted when documenting your data:
- The data origins (time-stamps, descriptions, context details)
- The description of which algorithms have been applied and with which criteria/thresholds, how data were cleaned etc.
- The data quality metrics and visualizations
- Instructions for importing and working with data (further processing, visualizing, and analysing)

## Data audit
Inspecting the way data are stored, documented and used. The audit must be :
- specifig and concrete
- focused on issues that can be addressed and how the can be addressed
- readable and comprensible by any person that could be interested to the data (summaries may be interesting for non expert)
- positive and make actionable suggestions

## Ensuring data quality before data collection
- Try to anticipate problems that may occur in the future with the data analyses : 
    ex. for ANOVA analyses, large different size between groups will lessen the power and accuracy of the test;
        for regression analyses, small variance in the independent variables will reduce the power of the model as well as the significantness of the estimated parameters
- Literature review: take profit of similar prior studies experience to avoid reproducing the same mistakes in data collection
- Consult with experienced people
- Run a pilot study (small-sample version of the study) and test if all the setup work

## Monitoring data during acquisition
- compute and inspect data quality metrics
- visualize the data
- update the quality metrics and visualizations when data come in
- if possible, solicit feedback fro, the participants of the study
NB. Do not run final analyses (ex. regressions, cluster analysis) on the data as while they are coming in

## Cleaning the data after data collection
- Use data quality metrics to identify and remove or correct bad data (missing, noisy, outliers)
- Do data normalization (data scaling)
NB. At this stage, challenging choice of algorithm or normalization method may have to be make. 
    In fact, picking thresholds for accepting or rejecting data is the most difficult part and carry out much uncertainty.

## Cleaning the data during analyses
This is when you go back cleaning the data after having looked at a surprinsing statistical result
NB. This is a very risky operation: high risk of bias, because the data analyst may be kind of imposing his personal beliefs and desired outcomes unto the data.
Better to avoid this method whenever possible, or have someone else clean the data without knowing the results. 
Third choice may be to pick an algorithm and threshold and apply blindly to all data in all groups/conditions, in order to remove the outliers for exemple.

## Two families of approach for cleaning the data
1- qualitative: visual inspection of the data
2- quantitative: use of algorithms to detect anormality in the data