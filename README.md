# Accenture-Data-Analytics-and-Visualization-Virtual-Experience
As a Data Analyst in Accenture North America Data Analytics and Visualization Virtual Experience Program on Forage, I've analyzed our client 'Social Buzz's' app data to find out the most popular 5 content categories and derived business insights from it.

## Client: Social Buzz
Client name: Social Buzz

Client Industry Type: Social Media and Content Creation

Client Background: Social Buzz emphasizes content by keeping all users anonymous, only tracking user reactions on every piece of content. 
There are over 100 ways that users can react to content, spanning beyond the traditional reactions of likes, dislikes, and comments. 
This ensures that trending content, as opposed to individual users, is at the forefront of user feeds. 
Over the past 5 years, Social Buzz has reached over 500 million active users each month.
Every day over 100,000 pieces of content, ranging from text, images, videos and GIFs are posted. All of this data is highly unstructured and 
requires extremely sophisticated and expensive technology to manage and maintain.

They are expecting the following: 
- An analysis of their content categories that highlights the top 5 categories with the largest aggregate popularity.

## Datamodel:
The required and relevent datasets used in this project are:

Content  
ID: Unique ID of the content that was uploaded (automatically generated)  
User ID: Unique ID of a user that exists in the User table  
Type: A string detailing the type of content that was uploaded  
Category: A string detailing the category that this content is relevant to  
URL: Link to the location where this content is stored  

Reaction  
Content ID: Unique ID of a piece of content that was uploaded  
User ID: Unique ID of a user that exists in the User table who reacted to this piece of content  
Type: A string detailing the type of reaction this user gave  
Datetime: The date and time of this reaction  

ReactionTypes  
Type: A string detailing the type of reaction this user gave  
Sentiment: A string detailing whether this type of reaction is considered as positive, negative or neutral  
Score: This is a number calculated by Social Buzz that quantifies how “popular” each reaction is. A reaction type with a higher score  
should be considered as a more popular reaction

The brief carefully states that the client wanted to see “An analysis of their content categories showing the top 5 categories with the largest popularity”.  
As explained in the data model, popularity is quantified by the “Score” given to each reaction type.
We therefore need data showing the content ID, category, content type, reaction type, and reaction score.
So, to figure out popularity, we’ll have to add up which content categories have the largest score.

## Data Cleaning and Modeling

Datasets checked for missing values using Filter method in Excel and missing value rows deleted.  
Because we have Content ID common in all three datasets, removed unnecessary columns like: URL, User ID.  

To find Top 5 categories, I've merged the three datasets together using VLookUp function and used SumIf formula to aggregate the reaction type scores.  

## Conclusion and Insights

- Total number of unique content categories found: 16
- Most popular 5 content categories are:
  - Animals
  - Science 
  - Healthy eating
  - Technology 
  - Food   
  
![](https://user-images.githubusercontent.com/102014569/225896035-f44e8348-852f-43dc-a681-056f1bbbe23f.png)

- Maximum amount of content was posted in May 2021 with an increase of 12.4% from June 2020 which shows a steady growth.
- It is very interesting to see both food and healthy eating within the top 5, it really shows that food is a highly engaging content category. 
- Healthy eating ranks slightly higher than food, so perhaps user base may be skewed towards healthy eaters and health-conscious people.
- Finally, its also interesting to see science and technology too. This may suggest that people enjoy consuming factual content and snippets of content that they 
can learn something from.

## Skills 
Data Cleaning, Data Modeling, Data Analysing according to business needs, Data Visualization and Presentation, Advanced Excel.

## Completion Certificate
