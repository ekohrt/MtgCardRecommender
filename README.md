# Mtg Card Recommender

A simple project that takes a card name as input and finds other cards that often appear together with that card.

Click into 'CardRecommender.ipynb' to see it in action.

### Summary:

This program uses a file derived from ~10,000 modern decks made by users on deckstats.net. For every card 'x', a count was kept of every other card 'y' that occurred in the same deck as 'x'. Then, all counts were divided by the total number of decks containining card 'x': this results in the percent of decks containing card 'x' that also contained card 'y'. The resuting JSON file is a dictionary containing an entry for every card; each card's entry is a dictionary of card co-occurrences.

This technique can be used as a tool to assist deckbuilding, or as a rudimentary deck generator (by starting with some card, keeping 4x of each top result, adding 24 lands, etc.).

Note: the dataset was collected on December 27 2021, so cards from sets released after this date are not recognized. Also, cards that are not commonly used in the Modern format might register as invalid because they did not occur in the dataset. Card names are case-sensitive.

Thanks for checking out this project!