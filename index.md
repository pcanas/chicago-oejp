---
layout: page
title: "Chicago: is your food safe?"
subtitle: A study on food security in the city, based on level of income per area and restaurant model.
use-site-title: true
---

<div style="text-align: justify" markdown="1">

# Title

A study on Food Security in Chicago

# Abstract


## Data-set
We used the [Chicago Food Inspections dataset](https://www.kaggle.com/chicago/chicago-food-inspections) dataset containing a list of the inspections of food establishments in Chicago from January 1, 2010 to the present.

Each line of the dataset represents an inspection and gives us information about the establishment itself, the result of the inspection, the violations detected and others.

Below is an example with only the more relevant columns kept:

|__Name__: _Chipotle Mexican Grill_|
|---|
|__Facility Type__: Restaurant|
|__Zip__: 60657|
|__Results__: Pass w/ Conditions|
|__Violations__: |
| 16. food-contact surfaces: cleaned & sanitized - comments: noted a very thick black and slimy substance inside the upper compartment of ice machine dripping onto the ice. Instructed management not to use ice machine until equipment is detail cleaned and sanitize. Priority foundation #7-38-005 | 
| 37. Food properly labeled; original container - comments: noted bulk food items stored inside containers at the dry storage not properly labeled. Instructed management that all bulk and working food ingredient containers must be labeled with contents name. | 
| 47. Food & non-food contact surfaces cleanable, properly designed, constructed & used - comments: noted foil paper used to line shelves. Instructed to clean and remove all foil paper to prevent hiding places for pest. | 
| 55. Physical facilities installed, maintained & clean - comments: noted cracks on floor at the basement dry storage area. Instructed to seal and resurface crack on floor to make them smooth and easily cleanable. | 
| 55. Physical facilities installed, maintained & clean - comments: noted stained tiles on walls and ceiling by the 3 compartment sink. Instructed to detail clean and maintain.  | 
| 58. Allergen training as required - comments: noted certified food managers on duty with no allergen training certification. Instructed management that all food service managers are required to have the allergen training certification.|


<img src="img/results_distribution_stacked_bar.png"
     alt="Result Distribution"
     style="float: right; margin-right: 20px; width:200px;" />


As can be seen most of the data is has results that are either: __Pass__, __Pass w/ Conditions__ or __Fail__. We will only be basing ourselves off that data.

<div style="clear: both;"> </div>

There are many different establishment types:
- Restaurants make up __67%__ of the data.
- Grocery stores make up __13%__ of the data.
- The rest of the data is __20%__ of the data.

For the purpose of this work we look more closely at the restaurants.

## Part 1: Is richer safer ?

We have compared inspections based on the [income for each zip code](https://towardsdatascience.com/getting-census-data-in-5-easy-steps-a08eeb63995d)

<img src="img/income_map.png"
     alt="Income map"
     style="float: left; margin-right: 20px; width:350px;" />
<img src="img/failRate_map.png"
     alt="Fail Rate map"
     style="float: right; margin-left: 20px; width:350px;" />

<div style="clear: both;"> </div>

From the maps it is easy to see that the few areas of high income seem to have a lower fail rate than the others.

There could be many ways this data is biased, for one the inspectors might be biased against restaurants in low income areas. To get a deeper look into this we looked at the actual violations that occurred. We saw the most noticeable difference for violation 18: “No evidence of rodent or insect outer openings protected/rodent proofed, a written log shall be maintained available to the inspectors”

#### Are poorer areas more targeted by inspections?

All establishments get assigned to a risk group. There are three groups:
- __High risk__ 
- __Medium risk__
- __Low risk__ 

We will not look at the low risk group because they are so uncommon that we don't have enough data on them.

<img src="img/scatter_inspectionFreq.png"
     alt="Inspection rates"
     style="float: left; margin-right: 20px; width:350px;" />

On the graph beside we see the average time between inspection per establishment for every zip code.
There doesn't seem to be any clear bias visible.

<div style="clear: both;"> </div>

<img src="img/scatter_oob.png"
     alt="Inspection rates"
     style="float: left; margin-right: 20px; width:350px;" />
<div style="clear: both;"> </div>

But we still see that areas with a lower income have a higher rate of going out of business.
WHY DO WE CARE? TEXT

<div style="clear: both;"> </div> 

#### Checking the specific violations:

<img src="img/violationDistribution_important.png"
     alt="Important violations"
     style="float: right; margin-right: 20px; width:350px;" />

In the graph beside we have the violations which show the most differences.
ADD SOME TEXT TO TALK ABOUT THIS

<div style="clear: both;"> </div>

Let's analyse the most common words from the violations:


<img src="img/low_income_areas_wc.png"
     title="Low income areas"
     alt="Important violations"
     style="float: left; margin-right: 20px; width:350px;" />

<img src="img/high_income_areas_wc.png"
     title="High income areas"
     alt="Important violations"
     style="float: right; margin-right: 20px; width:350px;" />

<div style="clear: both;"> </div>

TEXT ON WORD CLOUDS


## Part 2: Chains vs Businesses





































