# Datasheet: *FitBit Fitness Tracker Data*

Author: *Dhanya George Koottummel*

Organization: *School of Information, UC Berkeley*

## Motivation

*The questions in this section are primarily intended to encourage dataset creators to clearly articulate their reasons for creating the dataset and to promote transparency about funding interests.*

1. **For what purpose was the dataset created?** Was there a specific task in mind? Was there a specific gap that needed to be filled? Please provide a description.

	*The goal of creating the datasets was to create methods for remotely collecting data and establishing a link between self-reported survey responses and biometric data from consumer wearble devices, resulting in a de-identified and linked dataset*

2. **Who created this dataset (e.g. which team, research group) and on behalf of which entity (e.g. company, institution, organization)**?

	*The Fitbit datasets was part of a study done by Brinton J, Keating M, Ortiz, Evenson K, and Furberg R for a study titled "
Establishing Linkages Between Distributed Survey Responses and Consumer Wearable Device Datasets: A Pilot Protocol". This was done on behalf of RTI International which is a non-profit research organization.*

3. **What support was needed to make this dataset?** (e.g. who funded the creation of the dataset? If there is an associated grant, provide the name of the grantor and the grant name and number, or if it was supported by a company or government agency, give those details.)

	*The dataset was created for a study as mentioned above and the study was funded by iSHARE iinovation, research, and development project. Source: researchprotocols.org*

4. **Any other comments?**

	*The dataset was collected from a total of 30 people. They were recruited omn Mechanical Turk Prime and they were asked to complete a survey online. They were then asked to connect their personal Fitbit to a third party application called Fitabase to gather the data.*


## Composition

*Dataset creators should read through the questions in this section prior to any data collection and then provide answers once collection is complete. Most of these questions are intended to provide dataset consumers with the information they need to make informed decisions about using the dataset for specific tasks. The answers to some of these questions reveal information about compliance with the EU’s General Data Protection Regulation (GDPR) or comparable regulations in other jurisdictions.*

1. **What do the instances that comprise the dataset represent (e.g. documents, photos, people, countries)?** Are there multiple types of instances (e.g. movies, users, and ratings; people and interactions between them; nodes and edges)? Please provide a description.

	*The dataset is made up of different types of data in 11 different csv files. Each file maintains personal health information like daily activities, heartrate, calories, hourlt intensities, steps, sleep timings, and weight of the people who participated in the survey. *

2. **How many instances are there in total (of each type, if appropriate)?**

	*The number of instances per type is given below:
	daily activity - 458;
	heartrate per second merged -1048576;
	hourly calories merged - 24085;
	hourly intensity merged - 24085;
	hourly steps merged - 24085;
	minute calories narrow merged - 1048576;
	minute intensities narrow - 1048576;
	minute METs narrow merged - 1048576;
	minute sleep merged - 198560;
	minute steps narrow - 1048576;
	weight log info - 34*

3. **Does the dataset contain all possible instances or is it a sample (not necessarily random) of instances from a larger set?** If the dataset is a sample, then what is the larger set? Is the sample representative of the larger set (e.g. geographic coverage)? If so, please describe how this representativeness was validated/verified. If it is not representative of the larger set, please describe why not (e.g. to cover a more diverse range of instances, because instances were withheld or unavailable).

	*The dataset is not a sample of a larger dataset. This dataset was created for a study that target at establishing links between self-reported survey responses and consumer wearable device biometric data. For this 30 users were selected and data was collected only from them. The link could be successfully established with the 30 people.*

4. **What data does each instance consist of?** "Raw" data (e.g. unprocessed text or images) or features? In either case, please provide a description.

	*Each instance contains a fitbit recording of every activity that fitbit records. The dataset contains the following data for each instance - daily activities, steps covered, heartrate, calories, intensity, sleep information, and weight information. The collected data has been processed and has been organized into different csv files containing activity data, heartrate and sleep data.*

5. **Is there a label or target associated with each instance?** If so, please provide a description.

	*Each instance can be identified by a unique id that is associated with each entry. The id uniquely idenitifies the fitbit user.*

6. **Is any information missing from individual instances?** If so, please provide a description, explaining why this information is missing (e.g. because it was unavailable). This does not include intentionally removed information, but might include, e.g. redacted text.

	*Hourly steps and hourly calories are missing from certain instances and these have been logged as 0.*

7. **Are relationships between individual instances made explicit (e.g. users' movie ratings, social network links)?** If so, please describe how these relationships are made explicit.

	*Yes, the relationship between individual instances have been made explicit by using their IDs. Each instance has an ID that uniquely identifies the fitbit user. All the data associated with a particular user have the same unique ID.*

8. **Are there recommended data splits (e.g. training, development/validation, testing)?** If so, please provide a description of these splits, explaining the rationale behind them.

	*Yes, the data has already been split into physical activity, heart rate and sleep monitoring.*

9. **Are there any errors, sources of noise, or redundancies in the dataset?** If so, please provide a description.

	*No there are no error, sources of noise or redundancies in the data.*

10. **Is the dataset self-contained, or does it link to or otherwise rely on external resources (e.g. websites, tweets, other datasets)?** If it links to or relies on external resources, a) are there guarantees that they will exist, and remain constant, over time; b) are there official archival versions of the complete dataset (i.e., including the external resources as they existed at the time the dataset was created); c) are there any restrictions (e.g. licenses, fees) associated with any of the external resources that might apply to a future user? Please provide descriptions of all external resources and any restrictions associated with them, as well as links or other access points, as appropriate.

	*The data is not self-contained. This original complete dataset was uploaded to Zenodo by Robert Furberg, Julia Brinton, Michael Keating, Alexa Ortiz on 05/31/2016 and it was dicided into two folders each folder contains roughly one month's worth of user-submitted data:
mturkfitbitexport4.12.16-5.12.16.zip - (1 month’s prospective data)
mturkfitbitexport3.12.16-4.11.16.zip - (1 month’s retrospective)* 

*The dataset uploaded to Kaggle by Möbius is only the first folder named (mturkfitbitexport4.12.16-5.12.16.zip), which contains data from 12/04/2016 to 12/05/2016, and this dataset contains the retrospective data (mturkfitbitexport3.12.16-4.11.16.zip).*

*Souce: Crowd-sourced Fitbit datasets, kaggle.com*

11. **Does the dataset contain data that might be considered confidential (e.g. data that is protected by legal privilege or by doctor-patient confidentiality, data that includes the content of individuals' non-public communications)?** If so, please provide a description.

	*The dataset contains personal health, physical activity information of the users. Collection of the data need to be approved by the users. All the participants in the study were 18 years of above, and was willing to give the research team access to their fitbit data for the previous month and the upcoming month. Data was collected only after the electronic consent form was signed.*

12. **Does the dataset contain data that, if viewed directly, might be offensive, insulting, threatening, or might otherwise cause anxiety?** If so, please describe why.

	*No*

13. **Does the dataset relate to people?** If not, you may skip the remaining questions in this section.

	*Yes, the dataset contains physical activity, heart rate, and sleep hours of 30 people.*

14. **Does the dataset identify any subpopulations (e.g. by age, gender)?** If so, please describe how these subpopulations are identified and provide a description of their respective distributions within the dataset.

	*No, the dataset does not identify subpopulations.*

15. **Is it possible to identify individuals (i.e., one or more natural persons), either directly or indirectly (i.e., in combination with other data) from the dataset?** If so, please describe how.

	*Individuals cannot be identified using the data collected as only details like steps, heart rate, sleep hours etc. are collected.*

16. **Does the dataset contain data that might be considered sensitive in any way (e.g. data that reveals racial or ethnic origins, sexual orientations, religious beliefs, political opinions or union memberships, or locations; financial or health data; biometric or genetic data; forms of government identification, such as social security numbers; criminal history)?** If so, please provide a description.

	*Personally identifiable data has not been collected.*

17. **Any other comments?**

	*N/A*


## Collection

*As with the previous section, dataset creators should read through these questions prior to any data collection to flag potential issues and then provide answers once collection is complete. In addition to the goals of the prior section, the answers to questions here may provide information that allow others to reconstruct the dataset without access to it.*

1. **How was the data associated with each instance acquired?** Was the data directly observable (e.g. raw text, movie ratings), reported by subjects (e.g. survey responses), or indirectly inferred/derived from other data (e.g. part-of-speech tags, model-based guesses for age or language)? If data was reported by subjects or indirectly inferred/derived from other data, was the data validated/verified? If so, please describe how.

	*The dataset was collected through a wearble device (Fitbit). The data collected is not directly observable. Each person part of the study was required to  keep track of their own weight, diet, or exercise routine or keep track of their own blood pressure, blood sugar, sleep patterns, headaches, or some other health-related indicator. Since the data is recorded by the fitness device the data does not need to be validated.*

2. **What mechanisms or procedures were used to collect the data (e.g. hardware apparatus or sensor, manual human curation, software program, software API)?** How were these mechanisms or procedures validated?

	*To create the data, each of the 30 users (MTurkers via Amazon's Mechanical Turk platform) was required to have a wearable device - fitbit which monitored steps, physical activity, herat rate, and sleep hours. Participants were initially required to read a short task description and compensation information on Mturk's research studies advertisement page. Interested participants were asked to click on a link directing them to a series of eligibility questions. The participants were asked to complete an electronic consent form and then given a unique participant ID. A health questionnaire was to be filled and at the end of the questionnaire willingness to allow researchers to download the Fitbit data was asked. Upon consent participants were routed to a third party data service provider called Fitabase LLC, which can access and aggregate self-tracker data. A unique Fitabase link was provided for each participant. Fitabase provided the required data to the researchers.*

3. **If the dataset is a sample from a larger set, what was the sampling strategy (e.g. deterministic, probabilistic with specific sampling probabilities)?**

	*Fitabase provided both raw and aggregate data and hence separate sampling strategy was not required.*

4. **Who was involved in the data collection process (e.g. students, crowdworkers, contractors) and how were they compensated (e.g. how much were crowdworkers paid)?**

	*The data was collected from 30 participants (Mturkerrs) via Amazon's Mechanical Turk Platform. Mturkers are a workforce of individuals willing to participate in online research studies in exchange for money deposited into their Amazon.com personal account. An eligible Mturker must also be at least 18 years of age, regularly wear a Fitbit, and be willing to give the research team access to their Fitbit data for the previous month and the upcoming month from the date of sign-up. Upon completion of the Fitabase sign-up, participants will be given $10 via Mturk Prime’s customer service team.*
	*Source: Establishing Linkages Between Distributed Survey Responses and Consumer Wearable Device Datasets: A Pilot Protocol, researchprotocols.com*

5. **Over what timeframe was the data collected?** Does this timeframe match the creation timeframe of the data associated with the instances (e.g. recent crawl of old news articles)? If not, please describe the timeframe in which the data associated with the instances was created. Finally, list when the dataset was first published.

	*The Crowd-sourced Fitbit datasets was collected from 03.12.2016 to 05.12.2016 and was part of a study done by Brinton J, Keating M, Ortiz A, Evenson K, Furberg R for a study titled: Establishing Linkages Between Distributed Survey Responses and Consumer Wearable Device Datasets: A Pilot Protocol. The original complete data is uploaded to Zenodo by Furberg, Robert; Brinton, Julia; Keating, Michael ; Ortiz, Alexa, on 05.12.2016. This timeframe matches the creation timeframe of the data associated with the instances.*

7. **Were any ethical review processes conducted (e.g. by an institutional review board)?** If so, please provide a description of these review processes, including the outcomes, as well as a link or other access point to any supporting documentation.

	*Yes, the dataset was created as part of a study and the study was reviewed and approved by the RTI International Institutional review board.*

8. **Does the dataset relate to people?** If not, you may skip the remainder of the questions in this section.

	*Yes*

9. **Did you collect the data from the individuals in question directly, or obtain it via third parties or other sources (e.g. websites)?**

	*The dataset was obtained via the third party system kaggle.com. The original complete data is uploaded to Zenodo by Furberg, Robert; Brinton, Julia; Keating, Michael ; Ortiz, Alexa, on 05.12.2016.*

10. **Were the individuals in question notified about the data collection?** If so, please describe (or show with screenshots or other information) how notice was provided, and provide a link or other access point to, or otherwise reproduce, the exact language of the notification itself.

	*Data was collected from the participants after receiving signed electronic consent forms.*

11. **Did the individuals in question consent to the collection and use of their data?** If so, please describe (or show with screenshots or other information) how consent was requested and provided, and provide a link or other access point to, or otherwise reproduce, the exact language to which the individuals consented.

	*Consent was obtained from the individuals before they could participate in the study. The interested participants were asked to click on a link from Mturk's research advertisement page. The link directed them to a series of eligibility questions. Once eligibility was established, the participants completed an electronic consent and became a part of the data collection panel. The participants were asked to complete a halth questionnaire and queries for their willingness to allow researchers to download their fitbit data. Upon consent the participants were routed to a third party data collection platform for data collection. Participants had the right to refuse to participate or cancel their registration anytime.*

12. **If consent was obtained, were the consenting individuals provided with a mechanism to revoke their consent in the future or for certain uses?** If so, please provide a description, as well as a link or other access point to the mechanism (if appropriate).

	*The users were given an opportunity to cancel their registration in Fitabase while participating in the dataset collection. There is no mechanism to cancel the registration or revoke the data once the dataset is published.*

13. **Has an analysis of the potential impact of the dataset and its use on data subjects (e.g. a data protection impact analysis) been conducted?** If so, please provide a description of this analysis, including the outcomes, as well as a link or other access point to any supporting documentation.

	*To my knowledge no such impact analysis was done on the use of the data on the subjects.*

14. **Any other comments?**

	*N/A*


## Preprocessing / Cleaning / Labeling

*Dataset creators should read through these questions prior to any pre-processing, cleaning, or labeling and then provide answers once these tasks are complete. The questions in this section are intended to provide dataset consumers with the information they need to determine whether the “raw” data has been processed in ways that are compatible with their chosen tasks. For example, text that has been converted into a “bag-of-words” is not suitable for tasks involving word order.*

1. **Was any preprocessing/cleaning/labeling of the data done (e.g. discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values)?** If so, please provide a description. If not, you may skip the remainder of the questions in this section.

	*Yes, the dataset was cleaned and uploaded on Zenodo. The data was divided into 2 folders, each containing data collected over one month. The first folder contains retrospective data and the second folder contains prospective data. The folders contain separate csv files with each file having physical activities, heart rate, and sleep hours data.*

2. **Was the "raw" data saved in addition to the preprocessed/cleaned/labeled data (e.g. to support unanticipated future uses)?** If so, please provide a link or other access point to the "raw" data.

	*The data that is collected from Fitabase is cleaned and labeled. This data can however be used for future uses as no data has been removed.*

3. **Is the software used to preprocess/clean/label the instances available?** If so, please provide a link or other access point.

	*The entire data is available from Fitabase and no additional cleaning was required.*

4. **Any other comments?**

	*N/A*


## Uses

*These questions are intended to encourage dataset creators to reflect on the tasks  for  which  the  dataset  should  and  should  not  be  used.  By  explicitly highlighting these tasks, dataset creators can help dataset consumers to make informed decisions, thereby avoiding potential risks or harms.*

1. **Has the dataset been used for any tasks already?** If so, please provide a description.

	*Yes, the dataset was collected for a purpose. This has already been used for the study Establishing Linkages Between Distributed Survey Responses and Consumer Wearable Device Datasets: A Pilot Protocol by Furberg, Robert; Brinton, Julia; Keating, Michael ; Ortiz, Alexa*

2. **Is there a repository that links to any or all papers or systems that use the dataset?** If so, please provide a link or other access point.

	*There is no repository that links all the papers that use this dataset. However a few studies that were conducted using this dataset can be found on kaggle.som. The studies are Bellabet case study -Julen Aranguren: https://www.kaggle.com/julenaranguren/bellabeat-case-study
Bellabet Case Study with R -Anastasiia Chebotina: https://www.kaggle.com/chebotinaa/bellabeat-case-study-with-r*

3. **What (other) tasks could the dataset be used for?**

	*The data set contains physical activity details and details like heart rate, sleep hours etc. Hence tha dataset can be used for studies dealing with sleep such as sleep pattern of people, REM sleep cycles, routine analysis, human behavioral analysis etc.*

4. **Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses?** For example, is there anything that a future user might need to know to avoid uses that could result in unfair treatment of individuals or groups (e.g. stereotyping, quality of service issues) or other undesirable harms (e.g. financial harms, legal risks) If so, please provide a description. Is there anything a future user could do to mitigate these undesirable harms?

	*The dataset does not identify the gender, age, or any other personally identifiable details of the users. Hence my assumption is that this dataset will not result in unfair treatment of individuals or groups.*

5. **Are there tasks for which the dataset should not be used?** If so, please provide a description.

	*N/A*

6. **Any other comments?**

	*N/A*


## Distribution

*Dataset creators should provide answers to these questions prior to distributing the dataset either internally within the entity on behalf of which the dataset was created or externally to third parties.*

1. **Will the dataset be distributed to third parties outside of the entity (e.g. company, institution, organization) on behalf of which the dataset was created?** If so, please provide a description.

	*Yes, the dataset was created on behalf of of RTI International which is a non-profit research organization. It was originally uploaded on Zenodo. This is already distributed to a third party application Kaggle by Mobius.*

2. **How will the dataset will be distributed (e.g. tarball on website, API, GitHub)?** Does the dataset have a digital object identifier (DOI)?

	*DOI- 10.5281/zenodo.53894*

3. **When will the dataset be distributed?**

	*Unknown*

4. **Will the dataset be distributed under a copyright or other intellectual property (IP) license, and/or under applicable terms of use (ToU)?** If so, please describe this license and/or ToU, and provide a link or other access point to, or otherwise reproduce, any relevant licensing terms or ToU, as well as any fees associated with these restrictions.

	*Unknown*

5. **Have any third parties imposed IP-based or other restrictions on the data associated with the instances?** If so, please describe these restrictions, and provide a link or other access point to, or otherwise reproduce, any relevant licensing terms, as well as any fees associated with these restrictions.

	*Not to my knowledge*

6. **Do any export controls or other regulatory restrictions apply to the dataset or to individual instances?** If so, please describe these restrictions, and provide a link or other access point to, or otherwise reproduce, any supporting documentation.

	*Unknown*


## Maintenance

*As with the previous section, dataset creators should provide answers to these questions prior to distributing the dataset. These questions are intended to encourage dataset creators to plan for dataset maintenance and communicate this plan with dataset consumers.*

1. **Who is supporting/hosting/maintaining the dataset?**

	*The dataset is hosted by kaggle.*

2. **How can the owner/curator/manager of the dataset be contacted (e.g. email address)?**

	*Unknown. No data has been specified related to contacting the owners.*

3. **Is there an erratum?** If so, please provide a link or other access point.

	*No. To my knowledge, the creators have not published any list of corrections or errors in Fitbit Dataset.*

4. **Will the dataset be updated (e.g. to correct labeling errors, add new instances, delete instances)?** If so, please describe how often, by whom, and how updates will be communicated to users (e.g. mailing list, GitHub)?

	*As far as I know, corrections, updates, and deletions will not happen on the dataset.Communication channels have not been established with users for notifying the users about updates.*

5. **If the dataset relates to people, are there applicable limits on the retention of the data associated with the instances (e.g. were individuals in question told that their data would be retained for a fixed period of time and then deleted)?** If so, please describe these limits and explain how they will be enforced.

	*Unknown. The users were asked to sign an electronic conset form before the collection of the data. No data is available on the time period for which the data will be retained.*

6. **Will older versions of the dataset continue to be supported/hosted/maintained?** If so, please describe how. If not, please describe how its obsolescence will be communicated to users.

	*No communication channels have been set up with the users. The dataset is hosted on Kaggle.com. No further updates have been done on the data.*

7. **If others want to extend/augment/build on/contribute to the dataset, is there a mechanism for them to do so?** If so, please provide a description. Will these contributions be validated/verified? If so, please describe how. If not, why not? Is there a process for communicating/distributing these contributions to other users? If so, please provide a description.

	*N/A. The data cannot be updated.*

8. **Any other comments?**

	*Your Answer Here*
