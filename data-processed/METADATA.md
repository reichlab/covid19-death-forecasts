# Metadata file structure

Each model is required to have metadata in 
[yaml format](https://docs.ansible.com/ansible/latest/reference_appendices/YAMLSyntax.html), 
e.g. [see this metadata file](https://github.com/reichlab/covid19-forecast-hub/blob/master/data-processed/JHU_IDD-CovidSP/metadata-JHU_IDD-CovidSP.txt).
This file describes each of the variables (keys) in the yaml document.
Please order the variables in this order.


## Required variables

### team_name

The name of your team that is less than 50 characters.

### team_abbr

An abbreviated name for your team that is less than 15 alphanumeric characters and cannot 
inlucde a dash (-) or a whitespace. 

### model_name

The name of your model that is less than 50 characters.

### model_abbr

An abbreviated name for your model that is less than 15 alphanumeric characters and cannot
include a dash (-) or a whitespace.

### model_contributors

A list of all individuals involved in the forecasting effort
affiliations, and email address.
At least one contributor needs to have a valid email address. 
All email addresses provided will be added to 
an email distribution list for model contributors.

The syntax of this field should be 

    name1 (affiliation1) <user@address>, name2 (affiliation2) <user2@address2>

### website_url

(previously named `model_output`)

A url to a website that has additional data about your model. 
We encourage teams to submit the most user-friendly version of your 
model, e.g. a dashboard, or similar, that displays your model forecasts. 
If you have additionally a data repository
where you store forecasts and other model code, 
please include that in your methods section below. 
If you only have a more technical site, e.g. github repo, 
please include that link here.

### license

One of [these license keywords](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/licensing-a-repository) or "LICENSE.txt" (or 
"cc-by-nc-4.0"" which we expect to deprecate in the future).
(if none of these license keywords are appropriate).
We encourage teams to submit as a "cc-by-4.0" to allow the broadest possible uses
including private vaccine production 
(which would be excluded by the "cc-by-nc-4.0" license). 
If the value is "LICENSE.txt", 
then a LICENSE.txt file must exist within the folder and provide a license.

### team_model_designation 

Upon submission this field should be one of “primary”, “proposed” or “other”. 
For teams submitting only one model, this should be “primary”. 
For each team, one model can be designated as “primary”. 
Primary means the model will be ranked in evaluations and considered eligible 
for ensemble inclusion.

Other models can be designated as “proposed” or “other”. 
For models proposed as “proposed” the Hub team will determine whether the 
methodology is distinct enough that the model should be included in the ensemble 
(for as long as there are limits on the number of models per team in the 
ensemble). 
Models proposed as “other” will not be ranked in evaluations 
(they may still be listed, just not with a rank) and not eligible for inclusion 
in the ensemble.


### methods

A brief description of your forecasting methodology that is less than 200 
characters.


## Optional

### institional_affil

University or company names, if relevant. 

### team_funding 

Like an acknowledgement in a manuscript, you can acknowledge funding here.

### repo_url

(previously `model_repo`)

A github (or similar) repository url. 

### twitter_handles

One or more twitter handles (without the @) separated by commas.


### data_inputs

(previously `data_inputs_known` and `data_source_known`)

A description of the data sources used to inform the model, 
e.g. "NYTimes death data", "JHU CSSE case and death data", mobility data, etc. 


### this_model_is_an_ensemble

_**DEPRECATED**_: please remove from metadata file. 
In the future, inclusion of this field will be an error.

true/false indicating whether the model here is a combination of a set of other
models


### citation

A url (doi link preferred) to an extended description of your model,
e.g. blog post, website, preprint, or peer-reviewed manuscript. 



### methods_long

An extended description of the methods used in the model. 
If the model is modified, this field can be used to provide the date of the 
modification and a description of the change.
