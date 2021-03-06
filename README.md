# Card Recommender and Deck Generator for Magic: the Gathering

A simple program that takes a card name as input and finds other cards that often appear together with that card. This technique can be used as a tool to help in deckbuilding, or modified into a simple deck generator.

Click into 'CardRecommender.ipynb' to see the jupyter notebook. (If it doesn't load, you can view the notebook here: https://nbviewer.jupyter.org/github/ekohrt/MtgCardRecommender/blob/main/CardRecommender.ipynb)

### Summary:

This program uses a file derived from ~10,000 modern decks made by users on deckstats.net. For every card 'x', a count was kept of every other card 'y' that occurred in the same deck as 'x'. Then, all counts were divided by the total number of decks containining card 'x': this results in the percent of decks containing card 'x' that also contained card 'y'. The resuting JSON file is a dictionary containing an entry for every card; each card's entry is a dictionary of card co-occurrences.

This technique can be used as a tool to assist deckbuilding by recommending cards frequently used by other players, or as a rudimentary deck generator (by starting with some card, keeping 4x of each top result, adding 24 lands, etc.).

Note: the dataset was collected on December 27, 2021, so cards from sets released after this date are not recognized. Also, cards that are not commonly used in the Modern format might register as invalid because they did not occur in the dataset. Card names are case-sensitive.

Thanks for checking out this project!
