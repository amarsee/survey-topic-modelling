# Topic Modelling on Open Ended Survey Responses

This project was made as part of the final project for the Nashville Software School Data Science Bootcamp

## Goal

* Identify themes found in open ended survey responses of the Tennessee Educator Survey
* Quantify prevalence of topics 
* Using an exemplar comment, find other comments that are similar

## Background 

Each spring, a survey is sent out to all educators across the state of Tennessee, including teachers and administrators. This survey is used to inform policy going forward and assess effectiveness of policies looking back.

Most of the questions ask survey takers to score a statement on a Likert scale (e.g. to what extent you agree or disagree with a statement about your education experience in this school year). But there is one open ended question at the end. This year the question asked "What would you tell the Commissioner are the two most important things for her to concentrate on over the next five years"

Currently, there is no efficient way gather insights from the entirety of the comments. There are too many to read through every one, so that was the impetus for this project.

Quick Facts:
* ~ 75,000 surveys sent out each year
* ~ 45,000 people complete the survey
* ~ 25,000 open ended comments in the most recent survey

## Data Exploration

<img src="/../screenshots/cdf_word_counts.png" width="700" height="350" title="Word Count CDF"> 

* Mean (red): 53 words
* Cutoff for LDA (yellow): 20 words
    * Set a cutoff in order to provide LDA with enough substance for a topic model
    * About 60% (16,000) comments met the threshold
