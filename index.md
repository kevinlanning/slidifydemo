---

title: "Assessing skills in Computational Social Science"
author: "Kevin Lanning"
highlighter: highlight.js
output: pdf_document
job: null
knit: slidify::knit2slides
mode: selfcontained
hitheme: tomorrow
subtitle: A simple tool to illustrate Shiny Apps in R
framework: io2012
widgets: []
---

## The Venn Diagram model of Data Science
<div style='text-align: center;'>
    <img height='204' src='Data_Science_VD.png' />
</div>

In an early lecture, the Hopkins/Data Science team described Data Science in a Venn diagram as lying at the intersection of three domains of "Math and Statistics Knowledge", "Hacking Skills", and "Substantive Experience."
This model has substantial intuitive appeal and pedagogical value. But as a representation of the field of Data Science, it has important limitations.

---

## Two limitations of the model

The most important limitation of the model is that, work in data science can have no impact if it is not shared, hence,  *communication skills* (e.g., writing) are, together with hacking, statistics, and substance, critical for the Data Scientist.

A second limitation is that the model implicitly treats the requisite skills as discrete (present-absent), rather than *continuous dimensions* on which the skills of persons or teams might be assessed. 


---

## Data Science ~ (Math, Hacking, Substance, Writing)

If skills in math (M), hacking (H), substance (S), and writing (W) are continuous, and Data Science requires these and only these skills, then it is implied that expertise in Data Science is given by a function such as that specified above. 

It is beyond the scope of this assignment to empirically develop this equation, but its likely that it includes a non-additive component, as some minimum level of skill is needed in each of the four areas. Ignoring differential weights for the skills, a model which satisfies this rule might look something like the following:

```r
M <- 3; C <- 3; S <- 3; W <- 0; 
DataSci <- (.1*M*C*S*W) * (M+C+S+W)
```
Here, when one of the four skills is zero, so too is the estimated assessment of the project in Data Science:
DataSci = 0. But if W is changed from 0 to 1, the score for DataSci would increase to  2.7.

---

## Assessing skills in Computational Social Science

In the present application, I apply this logic (though not this exact equation) to a simple tool for assessing the capacities of individuals and teams in one area of Data Science, namely, Computational Social Science. The tool asks individuals to rate themselves on the four skills, then (a) plots the response and (b) provides an assessment/recommendation.

It is believed that tools such as this could ultimately help build effective teams of scholars and reviewers in Computational Social Science.  The code and application may be found at the links provided below:

https://github.com/kevinlanning/shinyapp1
https://kevinlanning.shinyapps.io/ComputationalSocialScienceRating
