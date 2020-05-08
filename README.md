# What is this repo?

This repo is the initial Date with Data (2020.04.29) and explores the dataset provided in a Kaggle repo. The Kaggle information is [here](https://www.kaggle.com/abcsds/pokemon) but the gist of the dataset is that this is a CSV containing base stats, types, and Pokedex indices for all 781 Pokemon.

# Requirements
Python via Anaconda

# What we did 2020.04.29
- Initial dataset finding on Kaggle

- Very rudimentary introduction to setting up a data science environment 
    - Update with links to tutorials to install Anaconda for Windows and Windows Subsystem for Linux
    
- Created Git repo
    - Link to GitHub
    
- Began writing README file for repo

- Began exploratory data analysis (EDA) with Jupyter Notebook (this notebook)

## Things We Noticed
- There are only 721 Unique Pokedex entries, but there are 800 Pokemon. Why?
    - There are duplicate entries due to alternate forms of Pokemon. These include Mega evolutions, but may also have Alolan, Galarian, and "Gigantamax" versions.
    
- There are going to be NaN or Null values for the second type for some/many Pokemon. How to handle the Null values?
    - In this case, we might be able to ignore them, but it depends on the use case for the data.
    
- We noticed the Sum of Stats, but are not yet sure if that is correct.
    - Suggest doing a simple sum of the stats in a new column to see whether or not the reported/given sum of stats column is correct. If not correct, see if we can do a pull request to update the source data so that it is fixed. 


## For next time
- What do we want to do with this data?
    - Suggest favorable/unfavorable matchups based on typing?
    - Suggest favorable/unfavorable matchups based on stats?
    - Or filter matchups based on typing and stat criteria
    
- Walkthrough setting up the GitHub repo
    - Terminal does not show in stream
    
- Why doesn't Terminal show up in stream?

- Generate a requirements.txt (pip) or a YAML (Conda) and upload to GitHub Repo


## What we did on 2020.05.07
- Created and linked local git to (GitHub repo)[https://github.com/AaronWChen/pokemon_kaggle_fun]

- Created the requirements.txt

- Calculated the sum of stats and compared them to the given sum. They are the same, but we wanted to do a simple fact check/verify

- Found a type chart (here)[https://pokemondb.net/type], maybe save the picture to the repo for easier reference
    - Saved the image to local repo
    - There is also a more complicated dual type chart (here)[https://pokemondb.net/type/dual]


## What we noticed
- Generation number is a categorical value here and should not be used as an integer

- In addition to Mega forms, there are the other designations for individual species. Eg, Confined, Unbound
    - Consider going through each name and seeing if the name is duplicated. If so, that means this has a alternate form that we might want to remove the record, or give it a better designation
        - When going through the Pokemon names, look for where capital letters are right after lowercase ones and split the string there

    - Make a new dataframe to hold all of the mega evolutions, legendaries, mythicals...anything with a stat total above a certain threshold 

    - Degrees of advantage and disadvantage
        - e.g., Normal vs Rock is at a disadvantage because Normal does half damage to Rock. But Rock does normal damage to Normal, so the disadvantage is not as severe as Fire vs Water. Fire vs Water is not as bad as dual type disadvantage say Dark/Steel vs Fighting. Plus there's zero damage scenarios like Ground vs Flying or Normal vs Ghost or Poison vs Steel

    - Make sub dataframes to simplify logic testing

## For next time
- Figure out logic to extract alternate forms and have them ready in another dataframe, if needed

- Figure out logic to depict type matchup advantage/disadvantage