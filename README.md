# Cookieless Regression Based Attribution

Copyright 2021 Google LLC
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

https://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

This solution, including any related sample code or data, is made available 
on an “as is,” “as available,” and “with all faults” basis, solely for 
illustrative purposes, and without warranty or representation of any kind. 
This solution is experimental, unsupported and provided solely for your 
convenience. Your use of it is subject to your agreements with Google, as 
applicable, and may constitute a beta feature as defined under those 
agreements.  To the extent that you make any data available to Google in 
connection with your use of the solution, you represent and warrant that you 
have all necessary and appropriate rights, consents and permissions to permit 
Google to use and process that data.  By using any portion of this solution, 
you acknowledge, assume and accept all risks, known and unknown, associated 
with its usage, including with respect to your deployment of any portion of 
this solution in your systems, or usage in connection with your business, 
if at all.

This is not an officially supported Google product.

## What is Attribution?

In marketing, attribution refers to the evaluation of all marketing touchpoints a user encounters during their path to conversion. Assigning credits or weights to various touch points uncovers which channels or combinations of channels attributed the greatest impact/s on conversion. 
Attribution is used by advertisers to optimize marketing channels at a granular level and to support their understanding of their individual audiences and market as a whole.

Attribution lets you assign credit to each marketing channel and will allow you to observe how they contribute to conversions, for example online sales. 

## What is Regression Based Attribution?

RBA is an approach to measuring digital media performance via econometric models built in open source code (SQL, Python, R). This methodology does not utilize user level data, thus making it privacy safe and durable through 3P cookie deprecation.

RBA can answer questions including:

- What channel and sub-channel impression weights will generate the maximum return for a given line of business?
- Within each channel, what media partners and environments have the greatest impact on intended outcomes?
- Does buying methodology (Direct IO versus Programmatic) influence the impact of their respective channels?

## Requirements

### Technical Skills

RBA models are built using SQL or Python code.

### Data

- Media data can be collected through Campaign Manager and/or Search Ads 360. Desired frequency of data is daily, however weekly or monthly data can be used as long as the industry standard of 10-20 observations per feature in the model is met. At least one year's worth of data is preferred for the model to gain a sufficient read of media signals.

Campaign Manager: 
   - Download daily data from the campaign manager UI for the past 12 months. 
   - Navigate to Reporting & Attribution > Report Builder > Offline Reporting > New Offline Report > Standard > Basic. 
   - Pull the following columns:
      - Advertiser
      - Placement
      - Placement ID
      - Date 

Search Ads 360:
   - Download daily data from the Search Ads 360 UI
   - Pull the following columns:
      - From (start date)
      - To (end date)
      - Device segment
      - Engine
      - Account
      - Campaign
      - Ad group
      - Clicks
      - Any other metrics you would like to utilize to segment your variables

Sales Data:
    - Pull the following columns:
      - Date
      - Sales (Conversions, Revenue, or other KPI)
      - Zip Code
      - Region



## RBA Framework

Step 1: Gather aggregated data

Step 2: Train model

Step 3: Interpret model results

Step 4: Optimize media strategy


## Next Steps

After aggregating data in BigQuery or Google Sheets, execute the following notebooks for data cleaning and modeling: 

*   [Data cleaning and feature selection](https://github.com/googlestaging/rba/blob/main/Data%20Pre-Processing%20%26%20Feature%20Selection.ipynb)
      - Pulls in data from BigQuery, performs exploratory data analysis, cleaning, and feature reduction
*   Modeling
    * [BQML Linear Regression](https://github.com/googlestaging/rba/blob/main/BQML%20Model.ipynb)
    * [OLS Linear Regression](https://github.com/googlestaging/rba/blob/main/OLS%20Model.ipynb)
    * [Bayesian Linear Regression](https://github.com/googlestaging/rba/blob/main/Bayesian%20Model.ipynb)
    * Vector Autoregression

## How to clone this repository

``` shell
git clone https://github.com/google/rba
mkdir my-new-thing
cd my-new-thing
git init
cp -r ../rba/* ../rba/.github .
git add *
git commit -a -m 'Applying RBA Code'
```
