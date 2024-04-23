---
toc: true
comments: True
layout: post
title: Data Structure Blog test
description: 
type: plans
courses: { compsci: {week: 28} }
image: images/erfef.webp
---

# Unique Collection/Table Display with SQLite3 Editor

![Codeimage](https://media.discordapp.net/attachments/1219822341719068672/1230716807275614208/Screenshot_2024-04-18_at_11.30.36_AM.png?ex=66345558&is=6621e058&hm=7017fdd993c59dff0d2a1d577fe41500c8ee797e20e8c307c81b0d322c075c56&=&format=webp&quality=lossless&width=1688&height=1306)

The image stored in this database is sent to the frontend. The frontend uses the data to create a song "box" for each unique song, each with it's own properties defined by the database. 

## Table Initialization and Test Data Creation

![Codeimage](https://media.discordapp.net/attachments/1219822341719068672/1230725881480085509/Screenshot_2024-04-18_at_8.45.10_PM.png?ex=66345dcb&is=6621e8cb&hm=6cfa98d0b01ccaceb4fd185a72c45359e9f834e84d01224d92129e2b02f41147&=&format=webp&quality=lossless&width=1350&height=732)

I initialize the database (the image above) by first defining different parameters of each song, defining the id, name, url, etc. of the song, and then I actually intialize the database by assigning each column of the database to a variable so that I can actually use it later in the code. 

## List Extracted from Database as Python Objects

![Codeimage](https://media.discordapp.net/attachments/1219822341719068672/1230716807652970496/Screenshot_2024-04-18_at_11.43.01_AM.png?ex=6627cf18&is=66267d98&hm=c87b619b26b031a2241f63b8d7328e58aed5961ae6c7d0fd9b78e3ecb1f30c21&=&format=webp&quality=lossless&width=1536&height=1306)

After I set an endpoint in debugger to where the code returns all song data in JSON format, so we can see that the database is correctly setup and that the information is actually being used. 

## Example Dictionaries

![Codeimage](https://media.discordapp.net/attachments/1219822341719068672/1230716807275614208/Screenshot_2024-04-18_at_11.30.36_AM.png?ex=66345558&is=6621e058&hm=7017fdd993c59dff0d2a1d577fe41500c8ee797e20e8c307c81b0d322c075c56&=&format=webp&quality=lossless&width=1688&height=1306)
Song Database with unique attributes to be used in frontend to create unique song boxes. 
![Codeimage](https://media.discordapp.net/attachments/1219822341719068672/1230718653755031582/Screenshot_2024-04-18_at_8.16.28_PM.png?ex=66345710&is=6621e210&hm=ae3845c910d124b5a2c7e15b960be88d9cdd0abd511d0dbe982a1f2424b22520&=&format=webp&quality=lossless&width=1350&height=448)
Game database with a unique points system, that updates whenever the user wins a game of any game in our catalog. 
## Python API Code for Request and Response Handling

![Codeimage](https://media.discordapp.net/attachments/1219822341719068672/1230716806927355924/Screenshot_2024-04-18_at_11.31.32_AM.png?ex=66345558&is=6621e058&hm=8311832965fb7e1d0761a5988b59753b0c4957f5cbe86bca62d32e418237d3ae&=&format=webp&quality=lossless&width=1350&height=636)

In the get request, the code identifies if there is an ID provided. If there is, the code will retrieve the song with that ID from the database and returns its details as JSON. 


## URL Request and Body Requirements in Postman

![Codeimage](https://media.discordapp.net/attachments/1219822341719068672/1230719611058782238/Screenshot_2024-04-18_at_8.20.14_PM.png?ex=663457f4&is=6621e2f4&hm=24ba75e1fd6525852e7ccbe376c4178b427701561ef383c6ba652a17ae9777ae&=&format=webp&quality=lossless&width=1350&height=992)

The get request is working, and all songs and data stored in database can be correctly retrieved in JSON format to be utilized by frontend. 

## JSON response data for 200 success conditions on GET, POST, and UPDATE methods, and JSON response for error for 404 when providing an unknown user ID to an UPDATE request.

![Codeimage](https://media.discordapp.net/attachments/1219822341719068672/1230716806646468709/Screenshot_2024-04-18_at_12.07.03_PM.png?ex=66345558&is=6621e058&hm=f70f89057cf46c97695324daa6f29db0dbc3a1cb92eada306f174b495d6b571b&=&format=webp&quality=lossless&width=1350&height=354)

For our delete function, which allows the user to delete a song from the database, two messages will be sent out, a 200 message for successful deletion, and a 404 error if the song that is trying to be deleted is not found. 
## Demo of Obtaining an Array of JSON Objects in Chrome Browser

![Codeimage](https://media.discordapp.net/attachments/1219822341719068672/1230716808256815205/Screenshot_2024-04-18_at_12.15.09_PM.png?ex=66345558&is=6621e058&hm=8e4a0fa3d5517f82dcf9f2938c191d9b815df23a1d6dd928a575d452cdcbbe53&=&format=webp&quality=lossless&width=1350&height=814)

Data is correctly fetched from backend. If backend was not running or broken, there would be no music boxes on the screen. 
## JavaScript Code for Fetching and Handling Data

![Codeimage](https://media.discordapp.net/attachments/1219822341719068672/1230716808798146561/Screenshot_2024-04-18_at_12.17.18_PM.png?ex=6627cf18&is=66267d98&hm=6b0aa5ecdffb493f564188ebc057bd96281b6327ed7b1b5eeb852412b0f55bcc&=&format=webp&quality=lossless&width=2664&height=1300)


Code fetches from the backend and gets specific song data. With success, the code will use the createItemBlock function to create a visual block for the song using the information provided, and display that block on the website. The code will give an "error fetchign data" error message if there is an error encountered. 

## Understanding Linear Regression Algorithms

Many different datapoints with multiple parameters not limited to x,y,z are plotted on a 3-D graph using computer algorithms. Then, a regression line is plotted. Decisions are usually made where a new point inputted by the user is plotted on the graph. Different sides of the regression line can decide what the outcome is. The regression line is somewhat of a cutoff, or a line that separates different outcomes. 

## Understanding Decision Tree Analysis Algorithms

The algorithm consists of many nodes and branches, where each node is a feature, and each branch is the outcome of that decision, which decides the next node. Tree starts at the top. Different criteria/rules of each node will change the next node, which will eventually change the answer..
