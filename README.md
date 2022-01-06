# Udacity Starbucks Capstone
Project in Data Scientist Nanodegree of [Udacity](https://www.udacity.com/)

You can read my Medium Blog Post in [Udacity Data Science Project](https://medium.com/@akikhoa/analyzing-starbucks-data-fc9cf89c1fe6).

## Installation
There should be no necessary libraries to run the code here beyond the *Anaconda* distribution of Python. The code should run with no issues using *Python versions 3.x*.
## Project Motivation
This project to complete udacity Data Scientist Nanodegree capstone project I've chosen Starbucks data that mimics customer behavior on the Starbucks rewards mobile app, and build a model to predict the preferred offer by the clients.

I'm interested to answer the following 6 questions:

*1. What is the Age Distribution of Starbucks Customers?*

*2. What is the Income Distribution of Starbucks Customers?*

*3. What is the Gender Distribution of Starbucks Customers?*

*4. How many customers enrolled yearly?*

*5. How long did the users become members?*

*6. Predict the preferred offer for the customer*
## File Descriptions
`Starbucks_Capstone_notebook.ipynb` - the notebook available here showcases work related to the above questions.

The data is contained in three files:

- `portfolio.json` - containing offer ids and meta data about each offer (duration, type, etc.)
- `profile.json` - demographic data for each customer
- `transcript.json` - records for transactions, offers received, offers viewed, and offers completed

Here is the schema and explanation of each variable in the files:

`portfolio.json`

- id (string) - offer id
- offer_type (string) - the type of offer ie BOGO, discount, informational
- difficulty (int) - the minimum required to spend to complete an offer
- reward (int) - the reward is given for completing an offer
- duration (int) - time for the offer to be open, in days
- channels (list of strings)

`profile.json`

- age (int) - age of the customer
- became_member_on (int) - the date when customer created an app account
- gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
- id (str) - customer id
- income (float) - customer's income

`transcript.json`

- event (str) - record description (ie transaction, offer received, offer viewed, etc.)
- person (str) - customer id
- time (int) - time in hours since the start of the test. The data begins at time t=0
- value - (dict of strings) - either an offer id or transaction amount depending on the record
## Results
The highest number of customers are between 50–60, aslo it’s a normal distribution.

The majority of the income is between 50000–70000 by average (65404), and it’s a right skewed distribution.

Men consume Starbucks products more than women.

Members of the Starbucks increased exponentially from 2013 and reached its highest in 2017(over 5000 members) which later declines steadily.

Average of days after which users can become members is 1781 days.

The highest of all models here was SVC by (0.89) for discount offer training. And the lowest of all models here was KNeighborsClassifier Model by (0.60) for bogo training.

Discount and BOGO increase the customer buy rating.
## Licensing, Authors, Acknowledgements
1. Udacity for providing such a complete Data Science Nanodegree Program
2. Starbucks for providing the datasets
