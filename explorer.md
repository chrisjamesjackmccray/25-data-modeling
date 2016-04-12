# Instructions

In each section below, you'll have some data described to you. List the models you would create, the fields those models would have, the data type for each field and a description of what the field is for. For example, if I said I wanted to model a todo, I might write something like:

## Todo Model
1. item - string - the actual description of what they want to do
2. completed - boolean - the status of whether it's completed or not
3. user_id - integer - the id for the user who owns this todo
4. created_at - datetime - when the todo was created

NOTE! For all of these, assume you have a User model that represents the person logged into the website.



# Quest 1 - Medium Clone

Let's start with an easy one. I've provided you with the minimum number of models, you just need to provide the field information. If you can think of additional normalized data that needs another model, don't feel restricted by what's here.

You're creating a simple Medium clone where people can write blog posts and comment on other people's blog posts. You want to have enough information to show the latest blog posts, blog posts for specific authors, and blog posts for specific categories. Categories and Authors need to match exactly for us to do this, so we'll make them their own models.

## Blog Post Model
user_id - integer - id of user
URL - string - address of blog posts
image - string - image accompanying blog post

## Comment Model
user_id - integer - the id of the user
Comment - string - allows user to voice opinion about blog

## Author Model
User_id - integer - id of Author
health tips
positive thinking
Best Upcoming Tech
Game Reviews



## Category Model
User_id - integer - id of Author
health tips
positive thinking
Best Upcoming Tech
Game Reviews




# Quest 2 - Twitter Clone

You're creating a Twitter clone. People can create tweets, follow other people and have followers. Keep in mind, unlike the blog post example where a comment is a separate entity, tweets responding to other tweets are still just tweets. Also, think about how Twitter turns a tweet into useful information. Do you think they scan tweets for @mentions and hashtags, or are they storing that kind of thing as additional fields? What models do we need to recreate Twitter?

## Tweet
user_id - integer - id of user
URL - string - address of blog posts
image - string - image accompanying blog post

## User
First Name - String - first name of user
Last Name - String - last name of user

## Followers
user_id - integer - id of user
tweet_id - string - id of tweet

## Comments
User_id - integer - id of user
tweet_id - integer - id of tweet
comment - string - user comment

## Likes
User_id - integer - id of user
tweet_id - integer - id of tweet

## Shares
user_id - integer - id of user
tweet_id - integer - id of tweet

## Created at
id - When created

## Updated at
id - When Updated








# Quest 3 - Car Makes and Models

You're building a site that associates data with specific variations of specific cars. You need to break the data down from the manufacturer to the specific model. In other words, you need to model in such detail that the system knows that a 2007 Mustang and a 2013 Mustang are the _same_ thing (from the 5th Generation, 2005-2014), but that a 2015 Mustang is different from both of those. The car models should also know general information about the cars.

## Make / Manufacturer
Toyota - string - manufacturer - Toyota
Lexus - string - manufacturer - Toyota

## Model
2004 - Camry - 4th gen - string - car model
2003 - Corolla - 4th gen - string - car model
2007 - Corolla - 5th gen - string - car model
2008 - Prius -  5th gen - string - car model

## Generation
4th gen - integer - 2002-2005
5th gen - integer - 2005-2008













# Quest 4 - DC Comics

You've used the Marvel API quite a bit. Let's model a comic site of our own for DC. You'll need to think about the fact that there are characters (the superheroes), comics (the actual issues), series (the collections of issues), events (which consist of many issues), artists, writers, et cetera. This is an incredibly deep rabbit hole. Create at least 5 models that would be able to provide enough information for someone to build all of our Marvel apps, but in the DC universe.

## Superhero Name
Batman - string - Name
Superman - string - Name
Robin - String - Name
Flash - String - Name


## Comic Publications
Arrow: string - Comic Publication - integer - date - Jan 2013–Dec 2013

Batman: Arkham City - string - Comic Publication - integer - date - Jul - Oct 2011

Forever People: - string - Comic Publication - date - integer - Feb – Jul 1988

Four-Star Spectacular: - string - Comic Publication - date - integer - Mar/Apr 1976 – Jan/Feb 1977

## Artist
Jim Lee: string - Artist name

Mike Parobeck: String- Artist name

Greg Capullo: String - Artist name

Kelley Jones: String - Artist name

## Comic Book Series
Batman: String - Series
Superman: String - Series
Flash - String - Series
