# Udacity Starbucks Capstone
Project in Data Scientist Nanodegree of [Udacity](https://www.udacity.com/)

You can read my Medium Blog Post in [Udacity Data Science Project](https://medium.com/@akikhoa/analyzing-starbucks-data-fc9cf89c1fe6).

## Installation
There should be no necessary libraries to run the code here beyond the *Anaconda* distribution of Python. The code should run with no issues using *Python versions 3.x*.
## Project Motivation
The goal of this project is to combine transaction, demographic, and offer data to determine which demographic groups respond best to which offer type. This dataset is a simplified version of the real Starbucks app because the underlying simulator only has one product whereas Starbucks sells dozens of products.

The process of our analysis will be by the following step: Define our question, understanding the Datasets, Data preparation and wrangling, analyze the data, model the data, compare model performance, and finally selecting one model.

The problem statement I am aiming to answer are :

*1. What is the Age Distribution of Starbucks Customers?*

*2. What is the Income Distribution of Starbucks Customers?*

*3. What is the Gender Distribution of Starbucks Customers?*

*4. How many customers enrolled yearly?*

*5. How long did the users become members?*

*6. Predict the preferred offer for the customer*

Using the data provided (portfolio, profile, Transactional), I answer question 1~5 using charts and I answer the question 6 using 6 classification models.

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

## Analysis
Simple Analysis for the problem is provider in this [article](https://medium.com/@akikhoa/analyzing-starbucks-data-fc9cf89c1fe6).]

## Licensing, Authors, Acknowledgements
1. Udacity for providing such a complete Data Science Nanodegree Program
2. Starbucks for providing the datasets
