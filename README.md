# Regression Based Attribution

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

## What is Regression Based Attribution?

RBA is an econometric model based that provides media attribution and forecasting capabilities.

## Next Steps

Each notebook is part of a series to execute Regression-Based Attribution: 

*   Data import
*   [Data cleaning and feature selection](https://github.com/googlestaging/rba/blob/main/Data_Pre_Processing_%26_Feature_Selection.ipynb) 
*   Create the model
    * [BQML Linear Regression](https://github.com/googlestaging/rba/blob/main/RBA_Light_BQML.ipynb)
    * [OLS Linear Regression](https://github.com/googlestaging/rba/blob/main/RBA_Medium_OLS.ipynb)
    * [Bayesian Linear Regression](https://github.com/googlestaging/rba/blob/main/RBA_Heavy_Bayesian.ipynb)

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
