# Automated Chat Funnel

## Overview
The goal of this project is to create a system capable of:
1. Chatting with user 
2. Gathering information about user (name, phone number, annual income, country of residence)
3. Qualifying potential customer based on some threshold

## 1. Chatting with user
A Google Gemini model is used to interact with user through Telegram bot. The conversation memory of the LLM model is created with utilizing Google Sheets. 
Prompts from the user and answers of the AI are saved to the Google Sheets and all conversation memory is recalled and formatted to be input to the LLM after each trigger of the workflow.

## 2. Gathering information
The information from the user is obtained by asking related questions by LLM

## 3. Qualifying potential customer
For testing purposes I created a threshold of 100000 of annual income and that the user need to be placed in Ukraine. If the information provided by the user satisfies the threshold, information about this user is added to 
another Google Sheets (potential customer database). The process of analyzing the asnwers gained from user and adding information into Table is done by Text Classifier and AI Agent both powered by Google Gemini model.
