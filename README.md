# Web-Scraping-and-Semantic-Analysis-of-Scraped-Data using Gensim and BeatifulSoup and other python libraries
This repo consists of some code using python libraries for completing the Web scraping of the event details from various websites and after gathering the data checking the data and do analysis for removing the duplicate events on the same day at the same location.

In this project, I have curated the data from the 3 different websites which consists of the data of Event Name, Date or say on which event is going to happen, Location of the event, and the prize of a ticket for the event. And then I have used TF-IDF ( TF - term frequency, and IDF -  inverse document frequency ) for handling and checking the similarity for the various events with other events and it returns the matrix after calculating the same. 

Using the code we can scrap the data from the websites mentioned in the Jupyter Notebook.
Then we first gather the data in one Dataframe from different Dataframe of different websites. 
Then we append the location using 'AT' between location and event name.
After that, we append the date and month of the event for making it same format as day.
After that, we make a set of unique dates and then using loop we fetch one date and checking the similarity
of the particular events that are going to happen on that day itself only. 
And if the similarity index is more then 70% using the corpus of that events name and trained model using the corpus of data.

We first check if on that day if there is more than one event that only it will check similarity. If there is no more than one event it'll store the event and data in the new dataframe.
and if there is more than one event it'll go for checking the similarity of the events.

We use TF-IDF model from Gensim to find similarity of the Event names with other events and returns a matrix of numbers from 0.000000 to 1.000000 and if it's greater than 0.7 we are going to declare that as duplicate and storing the only one index from that events. and then storing the event name and date from that index to a dataframe we are using for making the final list of events.

And after doing the whole thing we print the final list of the events.

# Check the code for more information and suggest if any edits we can make to make it more accurate.
# This project is a demonstration purpose only. 
