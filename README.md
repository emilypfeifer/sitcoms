
# Determining Success of Sitcoms Using NLP on Pilot Script Data
## The Data
The data was compiled by me in October of 2019. The data includes roughly 50 sitcoms, half of which are "failed" and the half of which are "successful". The data also includes descriptive information about each sitcom such as the year it was released, number of episodes, etc., as well as a link to the script of the pilot episode of each show. 

All sitcoms included in this project were American-made, aired on a cable network, and were created in the last 30 years. This criteria meant excluding content from HBO, Netflix, or other platforms of the like. All programs were "situational comedies" and had an average runtime of about 22-minutes per episode. All failed sitcoms had Rotten Tomatoes scores below 45%, IMDB scores below 6.5, and were cancelled after one season. All successful sitcoms had Rotten Tomatoes scores above 60%, IMDB scores above 7, and had a mininmum of 3 seasons.

## Goal
The goal for this project was to develop a model that can correctly assess whether or not a sitcom was a fail or a success from the sitcom's pilot episode script.

## Notebook 1 - Obtaining and Cleaning the Data
I spend the bulk of the first notebook introducing the data that I collected, discussing why I collected it, and the criteria for which shows were included in the data. This notebook was also used to discuss possible confounding variables and how I went about making my project with the most scientific approach as possible. After explaining my method, I use the web-scraping API Selenium to generate a dataframe of scripts and then continue on to show how I optimized the dataframe for EDA and modeling.

## Notebook 2 - Exploratory Data Analysis
In my second notebook, I use a variety of visualizations to show what kind of content was included in my data as well as explore trends between programs. To better understand what sort of shows I choose, I generate numerical data and summary statistics, visualize distributions by class, and take a look at interactions between variables. The second part of my EDA revolves around the text data, for which I explore by creating word clouds as well as topic modeling using Latent Dirichlet Allocation (LDA). I finish the notebook with feature engineering from my text data.

## Notebook 3 - Classification
My third notebook is used for preprocessing my data and then running classifiers. The first run-through of my classifiers is completed on the TF-IDF vectorized script data alone. I then use Latent Semantic Analysis (LSA) to perform dimensionality reduction on my data and then I run my classifier set once more. My third classification run is completed on a combination dataframe of TF-IDF script data and the features that I generated in notebook 2, for which I used SciPy's Hstack function to unite. The fourth and final time I run my classifiers is on self-generated features alone. In the end, I compile all of the results into a single dataframe and compare models.

## Notebook 4 - Deep Learning
My fourth and final notebook makes use of deep learning techniques. The first step I take is to define an LSTM recurrent neural network with an embedding layer inside to generate word embeddings within the model. I then use K-Folds cross evaluation to validate my model's performance and generate visualizations to see the ins and outs of my model. In the second half of my notebook, I create word embeddings using pre-trained GloVe data and then build another neural network. I conclude my notebook and project with a discussion of my results as well as what plans and ideas I have for future work on the subject.



