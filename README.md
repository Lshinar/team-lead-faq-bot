# team-lead-faq-bot
Team Lead FAQ Bot for employees
<!-- This is the markdown template for the final project of the Building AI course, 
created by Reaktor Innovations and University of Helsinki. 
Copy the template, paste it to your GitHub README and edit! -->

# Project Title

Final project for the Building AI course - Team Lead FAQ Bot

## Summary

This project aims to create a bot that can sit natively in Slack or Whatsapp and offer employees within a team or department a quick way to have questions answered as though they have come from a team leader/mananger. 


## Background

Which problems does your idea solve? How common or frequent is this problem? What is your personal motivation? Why is this topic important or interesting?

This project seeks to solve the following problems:
* Time wasted by repetitive or excessive employee questions.
* Streamline quiery processes by creating pools of general departmental knowledge.
* Highlights what information or services are most needed from a department both internally and from other departments.

These problems are faced by almost all team leaders, who need to support their employees while still attending to their own workload. Often employee questions (especially from outsdie the team/department) are repetitive and frequent, suggesting that the implementation of such a solution has a user base waiting for it already. 

This project is an opportunity to leverage AI tools to improve productivity and focus in the workplace, by diminihsing the likelihood tangental tasks cropping up in the workday such as answeing relatively common department related questions.


## How is it used?

Users will interact with a bot on Slack or Whatsapp (named "Marketing FAQ Bot" for example) and ask their question. From there the bot will search its database of questions and answers (as inputted by the team leader/manager) and find an answer of best fit, delivering it to the user. If no such answer exists or the user is dissatified with the response and automatic alert is sent to the team leader/manager in question with the original question and name of user to allow them to interact directly. Additionally, in such a case the team leader/manager is prompted to add the answer to the user question to the database for future use.

## Images
[Whatsapp Demo] (https://github.com/Lshinar/team-lead-faq-bot/blob/main/ChatGPT%20Image%20Aug%2017%2C%202025%2C%2005_58_57%20PM.png)
[Slack Demo] (https://github.com/Lshinar/team-lead-faq-bot/blob/main/ChatGPT%20Image%20Aug%2017%2C%202025%2C%2005_56_12%20PM.png)

## Data sources and AI methods
Where does your data come from? Do you collect it yourself or do you use data collected by someone else?
Data will be either manually inputted by the user, or the user will be given an option for their communications to be scraped and for an AI to pick out FAQs that arise from past conversations.

## Challenges

What does your project _not_ solve?
This project does not solve the human interaction problem entirely, it cannot. At a certain point someone will need to interact with either a question or the adding of additional data. But it does significantly reduce instances where time would be wasted on questions that have already been answered multiple times.

## Suggested AI Methods

Retrieval-Augmented Generation
Hybrid Search
Intent Classification

## Tech Stack Suggestion
Backend: Python (FastAPI)

Embeddings/LLM: OpenAI GPT-4o-mini for generation; text-embedding-3-large for retrieval (or local Llama 3 + bge for on-prem).

Vector store: pgvector (cheap, easy) → upgrade to Pinecone later.

Orchestration: LangChain or LlamaIndex (optional; keep it simple first).

Integrations: Slack Bolt SDK; WhatsApp Business (Cloud API) in phase 2.

Storage: Postgres for FAQs/metadata; S3/GCS for documents.

Auth/RBAC: Slack user profile → role mapping table.

Which limitations and ethical considerations should be taken into account when deploying a solution like this?

One must take into account the data privacy entailed in this project. Considering this is a work-oriented tool, sensitive internal communications would be handled and therefore the storage of all data would need to be secure to maintain company integrity. One way that this could be done is to host the data and/or AI agent on the client company's servers, allowing the company to keep their data within their hands. However, this would still require a backdoor for project engineers to manipulate the AI when needed.

## What next?

How could your project grow and become something even more? What kind of skills, what kind of assistance would you  need to move on? 


## Acknowledgments
