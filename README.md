# Topic Modelling on Open Ended Survey Responses

This project was made as part of the final project for the Nashville Software School Data Science Bootcamp

## Goal

* Identify themes found in open ended survey responses of the Tennessee Educator Survey
* Quantify prevalence of topics 
* Using an exemplar comment, find other comments that are similar

## Notebooks

* initial_exploration_python.ipynb
     * Initial exploration of 2018 data using a number of NLP techniques
* preliminary_results.ipynb
     * Preliminary analysis of 2018 data and further exploration of NLP
* survey_2019_responses.ipynb
     * Cleaner exploration and initial exploration of 2019 data
* interactive_app_2019.ipynb
     * Interactivity added with ipywidgets
     * LDA vizualized with PyLDAvis
     * Ability to filter comments by district, gender, and years of experience
     * Further interpret topics by seeing any of the top 25 most representative comments in a selected topic
     * Find similar comments by typing a query or pasting a comment in the corpus
          * Uses cosine similarity to find similar comments
* interactive_app_2019_no_ldavis.ipynb
     * Same as interactive_app_2019, but with the LDAvis suppressed

## Background 

Each spring, a survey is sent out to all educators across the state of Tennessee, including teachers and administrators. This survey is used to inform policy going forward and assess effectiveness of policies looking back.

Most of the questions ask survey takers to score a statement on a Likert scale (e.g. to what extent you agree or disagree with a statement about your education experience in this school year). But there is one open ended question at the end. This year the question asked "What would you tell the Commissioner are the two most important things for her to concentrate on over the next five years"

Currently, there is no efficient way gather insights from the entirety of the comments. There are too many to read through every one, so that was the impetus for this project.

Quick Facts:
* ~ 75,000 surveys sent out each year
* ~ 45,000 people complete the survey
* ~ 25,000 open ended comments in the most recent survey

## Data Exploration

<img src="/../screenshots/cdf_word_counts.png" width="500" height="350" title="Word Count CDF"> 

* Mean (red): 53 words
* Cutoff for LDA (yellow): 20 words
    * Set a cutoff in order to provide LDA with enough substance for a topic model
    * About 60% (16,000) comments met the threshold

## Topics Found

* Identified 12 topics among the comments

1. **Testing** (testing, tn ready, eoc, much)
2. **Special Education** (special education, rti, general, regular, intervention)
3. **Teacher Evaluation** (evaluation, portfolio, kindergarten, developmentally appropriate)
4. **School Climate** (counselor, mental health, class size, staff)
5. **Planning Time** (planning time, spend, lesson, amount time, instructional time)
6. **Technology** (technology, art, professional development, choice, access)
7. **Salary** (pay, salary, increase, commissioner, raise)
8. **Standards** (grade level, skill, standard, basic)
9. **Charter Schools** (high school, public school, voucher, charter)
10. **Test Prep** (year, standardized testing, end year, every year, throughout)
11. **Instructional Materials** (resource, material, read, science, program, writing, book, unit)
12. **Behavior and Discipline** (parent, behavior, child, accountable, discipline, held accountable, consequence)

## Results

* Plotted topics by number of comments scoring highest and second highest in each topic 

<img src="/../screenshots/capstone_presentation.png" width="700" height="350" title="Two Plots in One">

Testing and School Climate are by far the most common primary topics. There is a tighter range for the secondary topics

* Assigned each comment to any topic for which the comment had a score above 0.2 for that topic

<img src="/../screenshots/percentage_slide.png" width="500" height="300" title="Two Plots in One">

Testing and School Climate are largely talked about in over half of open ended comments

