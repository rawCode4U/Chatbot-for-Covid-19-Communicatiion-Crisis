# Chot Bot for COVID Crisis Communications 
## Team Name
Dummy Varible
## Team members
1.Abhishek Kumar (Team Leader)
2.Shubham Kumar
3.Saurabh kumar

## Contents

1. [Overview](#overview)
2. [The idea](#the-idea)
3. [How it works](#how-it-works)
4. [Diagrams](#diagrams)
5. [Documents](#documents)
6. [Datasets](#datasets)
7. [Technology](#technology)
8. [Getting started](#getting-started)
9. [Resources](#resources)
10.[Thank you](#thank-you)

## Overview

### What's the problem?
In times of crisis, communications systems are often overwhelmed with people trying to find basic information about testing, symptoms, community response, and other resources. When communication lines get clogged, people who need real help can't get through.So, I am made this Chatbot help peoples giving information about Covid 19 Safety ,precautions, News and many more from trusted Sources.


## The idea

COVID-19 has citizens looking for answers about symptoms and testing sites as well as current status of schools, transportation, and other public services. Using Watson Assistant, this Call for Code Starter Kit has designed a virtual assistant pre-loaded to understand and respond to common questions about COVID-19, scan COVID-19 news articles using Watson Discovery and respond to COVID statistics inquires with data from trusted sources.

With this Watson Assistant powered Crisis Communications Starter Kit you can integrate a chatbot into your Call for Code solution in an IBM Cloud hosted web server, using a Slack integration or via a Node-RED Dashboard. 

It can:
- Respond by sharing consistent, accurate COVID-19 information
- Help citizens quickly and easily access the latest information through their channel of choice – voice, text or collaborative tool
- Free valuable resources by automating answers to common COVID-19 questions
- Dynamically update information with the latest developments and recommendations

The challenge for you is to build out from this framework to create a more complete solution.

## How it works
[Watch Chatbot Demo on Youtube](https://youtu.be/ImunXQ5j3EU)
## Diagrams

### Website integration with COVID-19 crisis communication chatbot

![Chatbot Architecture diagram](/images/Chatbot-Architecture.png)

1. User visits a website with the COVID-19 chatbot and asks a question.
2. Node.js web server calls the Watson Assistant service hosted in IBM Cloud.
3. Watson Assistant uses natural language understanding and machine learning to extract entities and intents of the user question.
4. Source COVID-19 FAQ information from trusted CDC data.
5. Watson Assistant invokes an OpenWhisk open source powered IBM Cloud Function.
6. IBM Cloud Function calls the Watson Discovery service running in IBM Cloud.
7. Watson Discovery scans news articles and responds with relevant articles.
8. Watson Assistant invokes an OpenWhisk open source powered IBM Cloud Function.
9. IBM Cloud Function calls the COVID-19 API to get statistics.
10. Watson Assistant replies to the user inquiry.
11. Node.js web server displays the chat answer to the user.


## Documents

### Trusted sources for COVID-19 information
- [CDC COVID-19 FAQ](https://www.cdc.gov/coronavirus/2019-ncov/faq.html)


## Datasets

- [covid19api](https://covid19api.com/)

## Technology

### IBM technology

- [IBM Watson Assistant](https://www.ibm.com/cloud/watson-assistant/)
- [Watson Discovery](https://www.ibm.com/cloud/watson-discovery)
- [IBM Cloud Functions](https://cloud.ibm.com/functions/)

### Open source technology

- [Node.js](https://nodejs.org/en/)
- [Apache OpenWhisk](https://openwhisk.apache.org/)

## Getting started

### Prerequisite

- Register for an [IBM Cloud](https://www.ibm.com/account/reg/us-en/signup?formid=urx-42793&eventid=cfc-2020?cm_mmc=OSocial_Blog-_-Audience+Developer_Developer+Conversation-_-WW_WW-_-cfc-2020-ghub-starterkit-communication_ov75914&cm_mmca1=000039JL&cm_mmca2=10008917) account.

### Set up an instance of Watson Assistant

Log in to IBM Cloud and provision a Watson Assistant instance.

**Step 1.** From the [IBM Cloud catalog](https://cloud.ibm.com/catalog/services/watson-assistant), provision an an instance of **Watson Assistant**.
  ![Watson Assistant Catalog](/Chatbot/assistant/WA-Photo1.png)

**Step 2.**  Launch the Watson Assistant service.

**Step 3.** Click **Create assistant** and follow [these detailed instructions](https://cloud.ibm.com/docs/assistant?topic=assistant-assistant-add) for how to create an assistant.
  ![Watson Assistant Photo2 ](/Chatbot/assistant/WA-Photo2.png)

**Step 4.** Name the Watson Assistant instance **COVID Crisis Communication**
  ![Watson Assistant Photo3 ](/Chatbot/assistant/WA-Photo3.png)

**Step 5.** Click **Add Dialog skill** to add this to your assistant. Follow [the documentation](https://cloud.ibm.com/docs/assistant?topic=assistant-skill-dialog-add) if you have questions.
  ![Watson Assistant Photo4 ](/Chatbot/assistant/WA-Photo4.png)

**Step 6.** Click **Import skill > Choose JSON file** and import the [`skill-CDC-COVID-FAQ.json`](./Chatbot/assistant/skill-CDC-COVID-FAQ.json) file.
  ![Watson Assistant Photo5 ](/Chatbot/assistant/WA-Photo5.png)

**Step 7.** Go back to the All Assistants page. From the action menu ( **`⋮`** ), open **Settings**.
  ![Watson Assistant Photo6 ](/Chatbot/assistant/WA-Photo6.png)

**Step 8.**  On the Settings tab, click **API Details** on the left and make a note of the `Assistant ID` and `Api Key` for future use.
  ![Watson Assistant Photo7 ](/Chatbot/assistant/WA-Photo7.png)

**Step 9.** Go back to the All Assistants page and click on the **Skills** link.
  ![Watson Assistant Skills ](/Chatbot/assistant/WA-Skills.png)

**Step 10.** On the Skill page, click on the action menu ( **`⋮`** ), open **View API Details**.
  ![Watson Assistant Skill Properties](/Chatbot/assistant/WA-SkillAPIProperties.png)

**Step 11.** On the Skill Details page, make note of the `Skill ID` for future use.
  ![Watson Assistant Skill Details](/Chatbot/assistant/WA-SkillDetails.png)

**Step 12.**  Go back to your dialog skill and click on the **Preview Link** button on the side to get a link to test and verify your assistant.
  ![Watson Assistant Photo9 ](/Chatbot/assistant/WA-Photo91.png)

**Step 13.** Ask the Watson Assistant chatbot some questions about COVID-19.
<p align="center">
<img width="50%" height="50%" src="https://raw.githubusercontent.com/Call-for-Code/Solution-Chatbot-Communication-2020/master/Chatbot/assistant/WA-Photo101.png">
</p>

### Embed your COVID-19 chatbot on a Node.js website

Finally, you can embed your COVID-19 crisis communication chatbot on a Node.js website.

## Sample questions you may like to know
1. Why is the disease being called corona virus disease 2019, COVID-19
2. Should my child wear a face mask?
3. Why is  Corona Virus (COVID-19) spreading between people?
4. Where do i need to disinfect?
5. Can a person test negative and later test positive for COVID-19?
6. What should I have my family do to keep from getting sick?
7. What should healthcare professionals and health departments do?
8. While school’s out, how can I help my child continue learning?
9. What should I do if someone in my house gets sick with COVID-19?
10. Why might someone blame or avoid individuals and groups (create stigma) because of COVID-19?
11. Will warm weather stop the outbreak of COVID-19?
12. Who is at higher risk for serious illness from COVID-19?


## Disclosures

This tool is intended to provide information based on currently available CDC and other public information to help you make decisions about seeking appropriate medical care. This system is not intended for the diagnosis or treatment of disease or other conditions, including COVID-19, and you should not provide any personally identifying or private health information.

This Watson Assistant bot is populated with data that is sourced from the following resources:

- Most static responses provide information found on the CDC's COVID FAQ Page: https://www.cdc.gov/coronavirus/2019-ncov/faq.html
- Dynamic infection and death counts are sourced from Johns Hopkins University via the following API: https://www.covid19api.com/
- Dynamic news stories are sourced from Watson Discovery's news feed. Additional information on that service can be found here: https://www.ibm.com/watson/services/discovery-news/

### Thank you!
  Hope this Chat bot helps you to clear you most of the quries regarding  covid 19.
  Go and explore Chatbot find your answer[Covid Chatbot](https:bit.ly/Covid-19bot)
