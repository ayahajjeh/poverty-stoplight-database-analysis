<style>h1,h2,h3,h4 { border-bottom: 0; } </style>

# <span style="color:Crimson">Cases to Explore</span>

<span style="color:Crimson; font-size: 10pt">_Poverty Stoplight Platform Database Analysis_</span>

<span style="color:blue">_Guidelines:_</span>
Below are the types of issues that were identified in the poverty stoplight platform database. For each issue, I provide 1) a descriptoin of the issue as it was provided to me by my supervisor, Alexis Risaldi, and then 2) how I identified the issues in the dataset, and 3) how I answered the analysis questions, along with screenshots of the results for the three database excel files I had (attached in the zip file). Additionally, all the results and analysis that you see below are exported into new excel files (attached in the zip file) that you are welcome to look over. You can generate similar exported excel files by replacing the input excel files and matching the new excel file names into the Python script provided. Lastly, when using the Python script provided, please make sure to download any necessary libraries on your local device, and if you don't have the right setup to run Jupyter Notebooks locally on your device, you can upload the notebook into a Google Colab file, and the you'll be able to run the script remotely. Feel free to reach out to me, Aya Hajjeh, at ayabaselhajjeh@gmail.com for any troubleshooting assistance needed.

## <span style="color:Navy">1. Surveys that are geographically misplaced</span>

To identify (latitude, lonitude) value pairs that are geographically misplaced, I used the libray global-land-mask (credit to Karin, Todd. Global Land Mask. October 5, 2020. https://doi.org/10.5281/zenodo.4066722) to flag the pair values that are in the ocean and not on land.

![geographically misplaced results](./analysis%20results/geographically%20misplaced%20results.png)

## <span style="color:Navy">2. Surveys that were taken in less than 3 months for the same person</span>

Over the months, Poverty Stoplight team have found follow-up surveys with differences in minutes or days. Follow-up surveys should have a minimum difference of 3 months to analyze if there were any changes in the indicators. Therefore, the Python script I created flag any survey follow-ups that were taken in less than 3 months for the same person.

![follow-up survey less than 3 months results](./analysis%20results/follow-up%20survey%20less%20than%203%20months%20results.png)

## <span style="color:Navy">3. Surveys that take less than 20 minutes to complete</span>

The average time to complete the surveys is 20 minutes, which typically includes around 25 socioeconomic questions and an average of 50 indicators. To identify the surveys where this isn't the case, the Python script flags the surveys that were taken in less than 20 minutes.

![total time less than 20 minutes results](./analysis%20results/total%20time%20less%20than%2020%20minutes%20results.png)

## <span style="color:Navy">4. Surveys that are answered by children under 14</span>

In the European Union, minors' personal data protection is regulated by the General Data Protection Regulation (GDPR). According to the GDPR, parental or legal guardian consent is required to process the personal data of minors under 14 years old. I identify all the surveys from minors under 14 years old and flag them in an exported excel file so we can take appropriate action.

![age under 14 results](./analysis%20results/age%20under%2014%20results.png)

## <span style="color:Navy">5. Invalid Snapshot Values</span>

Some data entries have invalid snapshot values and that could for either one of the following reasons: a missing snapshot value, a duplicated snapshot value, or a missing family id. I identified such invalid values, flagged them in an exported excel file, along with the reasons on why each survey had been flagged.

![invalid snapshot values results](./analysis%20results/invalid%20snapshot%20values%20results.png)

## <span style="color:Navy">6. Other Questions</span>

1. How many families have transitioned from yellow to green per indicator?

![yellow to green transition results 1](./analysis%20results/yellow%20to%20green%20transition%20results%201.png)

![yellow to green transition results 2](./analysis%20results/yellow%20to%20green%20transition%20results%202.png)

![yellow to green transition results 3](./analysis%20results/yellow%20to%20green%20transition%20results%203.png)

![yellow to green transition results 4](./analysis%20results/yellow%20to%20green%20transition%20results%204.png)

2. How many families have transitioned from red to green per indicator?

![red to green transition results 1](./analysis%20results/red%20to%20green%20transition%20results%201.png)

![red to green transition results 2](./analysis%20results/red%20to%20green%20transition%20results%202.png)

![red to green transition results 3](./analysis%20results/red%20to%20green%20transition%20results%203.png)

![red to green transition results 4](./analysis%20results/red%20to%20green%20transition%20results%204.png)

3. Which indicator had the most favorable changes from yellow to green?

![yellow to green most favorable indicator transition](./analysis%20results/yellow%20to%20green%20most%20favorable%20indicator%20transition.png)

4. Which indicator had the most favorable changes from red to green?

![red to green most favorable indicator transition](./analysis%20results/red%20to%20green%20most%20favorable%20indicator%20transition.png)

5. What is the average time between the baseline survey and the follow-up survey?

![average time taken between baseline and follow-up survey results](./analysis%20results/average%20time%20taken%20between%20baseline%20and%20follow-up%20survey%20results.png)
