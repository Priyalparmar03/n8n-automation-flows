**Smart Real Estate Bot – n8n Automation**

**Project Overview**

Smart Real Estate Bot is an AI-powered real estate automation built using n8n that enables intelligent property search and lead management through Telegram.

The bot understands natural language messages, identifies user intent, collects property requirements (BHK, location, property type), searches listings, and delivers results via chat and email. It also stores leads, tracks conversation stages, and supports automated follow-ups.

This project demonstrates real-world automation skills combining AI, workflows, databases, and messaging platforms.

**Project Goals**

This project was built to:

Showcase advanced n8n workflow design

Demonstrate AI-powered intent classification

Build a real-world business automation use case

Practice lead management and data persistence

Create a portfolio-ready automation projects.

**How the Workflow Works**

1. Telegram Trigger

Listens for incoming messages from users

Filters out bot messages and empty inputs

2️. Message Parsing

Extracts structured data from user messages:

Name

Chat ID

Email (if provided)

BHK

Location

Property type

This allows free-text messages like:

“2 BHK apartment in Mumbai”

3️. AI Intent Classification

Uses an LLM (Groq – LLaMA models) to classify intent:

Greeting

Property search

Providing email

Email consent

Questions or other messages

The intent controls the entire conversation flow.

4️. Conversation Flow Control

A Switch node routes users based on intent

The bot:

Greets new users

Asks only for missing information

Avoids repeating questions

Maintains conversation context

5️. Property Requirement Collection

If information is missing:

The bot intelligently asks for one detail at a time

Keeps the conversation short and natural

6️. Property Search Automation

Once requirements are complete:

The bot searches property listings stored in Google Sheets

Filters by BHK and City

7️. Results Handling

If properties are found:

Formats results clearly with emojis

Shows them in Telegram

Asks for email consent

If no properties are found:

Sends an empathetic response

Offers email alerts for future availability

8️. Email Automation

Uses Gmail integration to:

Send property details

Send follow-up notifications

Emails are sent only after user consent

9️. Data Storage & Lead Management

Airtable

Stores user details

Tracks conversation stage

Maintains lead history

Google Sheets

Stores property listings

Logs shared property results

All records are upserted to avoid duplication.

 
 **Key Features**

AI-based intent understanding

Stateful conversation handling

Automated property matching

Email notifications with consent

Lead storage and updates

Scalable and reusable workflow design

No hardcoded credentials

**Tech Stack**

n8n – Automation platform

Telegram Bot API – User interaction

Groq (LLaMA 3.x) – AI intent classification & responses

Google Sheets – Property data & logs

Airtable – Lead management

Gmail API – Email notifications

JavaScript – Custom logic via Code nodes
