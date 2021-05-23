---
layout: post
author: Tim Truty
title: Tru-torial- python and API data collection 
date: 2020-09-24
thumbnail: /assets/img/data-collect-post/data1.png
category: Trutorial
summary: A tutorial for data collection from API into SQL databasae
---

# Data Collection

This is a tutorial ( I am trying to brand this series as <i>Tru-torials</i>) how to collect data from a API and store that data into a SQL database. 
<hr />
There is a video associated with this tutorial. It assumes zero coding experience, but will be a great launching point to begin your data science or coding journey...

<hr />

<iframe width="560" height="315" src="https://www.youtube.com/embed/pF2k22vaSCo?rel=0&amp;controls=0&amp;showinfo=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen=""></iframe>

<hr />

## Overview

<b>
The 30,000 foot view of this project is: We will be pulling data from a server and populating database and getting data for a specific horse
</b>

![Sql 1]({{ "/assets/img/data-collect-post/sql1.png" | absolute_url }})

More specifically: We will be requesting horse and race data from a platform called [ZED Run](https://zed.run/) (An NFT based horse racing platform) and putting that data into a SQL database.

We will be using git, python, MySql to build this project. The end product will be a SQL database to perform queries on.

> Note: <b>QUERY</b>- is just a fancy way of saying "Give me certain data that matches what I am looking for". For example data on a specific horse in this tutorial.

This tutorial assumes no coding or CS experience so if you have some you can just grad the code and go. [Github repo](https://github.com/ttruty/ZedRunner)

Source: The original github repo that sparked this tutorial was from the user(with the unfortunate name) [KshitizGit](https://github.com/KshitizGIT/ZedRunner)

### Disclaimer
I am not a expert on Zed Run. I don't even use the platform, this was initial made for a friend that wanted some horse data. I just like data and tech and Zed Run seems to be a way to get data. Zed Run is a gambling platform with NFT and crypto so be careful. 

"Man, money ain't got no owners. Only spenders." - Omar Little (The Wire)

![Omar](https://media.giphy.com/media/OVtqvymKkkcTu/giphy.gif)


## Project Steps

View the video for the walk through, but I will break it down here.

0. If you do not have visual studio code installed [install it](https://code.visualstudio.com/download)


1. [Install git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

2. [Install python 3.8.5](https://www.python.org/downloads/release/python-385/)
    - Stick with specific version
    - Make sure to add to PATH, this allows command in terminal

3. pip install pipenv
    - use command `pip install pipenv`

4. Clone repositor with git 
    - use command `git clone https://github.com/ttruty/ZedRunner.git`

5. Now should be able to run the command to see API call
    - should be able to see api call
    - Data is not stored anywhere because we haven't made a MySQL server

6. Download and install MySQL Community 8.0.25
    -   MySql is from Oracle- [read about the hate for Oracle](https://www.reddit.com/r/linux/comments/2e2c1o/what_do_we_hate_oracle_for/)
    - Can leave all defaults and install... <b>BUT BE SURE TO MAKE A USER WITH THE CORRECT USERNAME AND PASSWORD</b>
    - This is not the root accounts, but a new user with username: zedrunner, and password: #ZedRunner@2021
    - Install can take a little bit

7. Run python codes again in this order wait for each one to complete... it will take some time:
    - run command `pipenv run python zed.py --type horse --force true`
    - `pipenv run python zed.py --type race --force true`
    - `pipenv run python zed.py --type stable --force true`

8. Now you should be able to query the database to see the data.    
    - Can read about [SQL](https://www.w3schools.com/sql/sql_intro.asp)
    - Click the 'create query button.
    - Enter a query and click the lightning bolt to run.

9. Get your horse data!
    - Can make a query to get your horse data

10. Now your data is in a database. This is only a local database on your system.

## WHATS NEXT?

Ok so now you have a local MySQL server running with the snapshot of data... great, right? This is not great. The data from the Zed Run platform keeps changing. Ideally you would want to set up this code to run on a schedule. The would be a [cron job](https://opensource.com/article/17/11/how-use-cron-linux) or a [scheduled task](https://datatofish.com/python-script-windows-scheduler/) on windows. But even then, you still only have a local database with all the data sitting on your machine.

The next step would be to turn this system into a web based system  to pull the data on a regular basis and structure queries to update a frontend application with the specific information you want.

If there is interest I will make the next <i>TRUtorial</i> to make a simple frontend website to use this data and database. That might be a little more involved because we will need to cover things like web hosting, server security, cloud basics as you would probably want to host on AWS, Azure, GCP, or a service like Digital Ocean.
