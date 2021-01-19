---
title: "Consuming Twitter API With Tweepy"
date: 2020-05-26T19:29:35-04:00
type: posts
tags: ['twitter']
layout: post
---

## Background

Twitter is a veritable source of social media data. It is unhindered by the same privacy concerns as Facebook because of its cavalier attitude towards social networking and less intrusive data collection. Twitter has become quite popular amongst journalists since its inception, as well as politicians and other figures with political power. I am interested in the interactions journalists have on Twitter. There are two classes of users, blue checkmarks and non checkmarked. Twitter uses the blue checkmark as a status symbol. The overwhelming majority of blue checkmark users are corporations, politicians, and journalists. It mirrors the power structure of U.S. society.

Twitter has a public facing API with which one could pull data for free, at a free rate. If I assume journalists follow each other on Twitter, I could use the connections of one journalist to find all of them.

## Tools

I intend to use [tweepy](http://docs.tweepy.org/en/latest/index.html) API wrapper to collect data from Twitter. The following [tutorial](https://realpython.com/twitter-bot-python-tweepy/#hello-tweepy) may help as well. Let's get down to business by first looking at what Twitter offers.

```python
import json
import tweepy
import os

# Authenticate to Twitter
# I saved my keys as environment variables
consumer_key = os.environ['TWITTER_CONSUMER_API_KEY']
consumer_secret = os.environ['TWITTER_CONSUMER_API_SECRET']

# I use OAuth v2 since I am using read-only access
auth = tweepy.AppAuthHandler(consumer_key, consumer_secret)

# Create API object
api = tweepy.API(auth)

# Lets seed the list of members I wish to plug
seedlist = ["sashaperigo","hacks4pancakes","StefanEtienne","sarahjeong","katienotopoulos"]

# For the time being, lets grab everything we can get
for seed in seedlists:
    seed_user = api.get_user(seed)
    with open(f'{seed_user.screen_name}.json','w') as fp:
        # the API provides a convenient _json object which is actually a
        # python dictionary representing the API endpoint 
        # https://api.twitter.com/1.1/users/show.json
        json.dump(obj=seed_user._json,fp=fp)
    # the following will iterate over each seedlist user's friends
    # and save what Twitter calls the User obj
    # see here https://developer.twitter.com/en/docs/tweets/data-dictionary/overview/user-object
    friends = [user for user in api.friends(seed)]
    for friend in friends:
        with open(f'{friend.screen_name}.json','w') as fp:
            json.dump(obj=friend._json,fp=f)
```

## Next Steps

Now that I have accumulated some data, I will need to pick it over and keep only the relevant bits. Twitter is simple enough to break down into concepts. The user creates tweets and can friend other users, who in turn can follow that user. I wish to analyze the friend network of journalists in an effort to determine how much overlap there is with other institutions with massive political power.
