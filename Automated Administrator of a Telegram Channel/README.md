# Automated Administrator of a Telgram Channel

## Overview
The goal of this project is to create a system capable of:
1. Doing Web Scrapping in order to get the latest article from the https://www.deeplearning.ai/the-batch/ and summarize it into few paragraphs.
2. Speak with human (for example, owner of the telegram channel) to get instructions about summarized text (make it shorter, delete some of the paragraphs, etc.)
3. Post approved paragraphs to the telegram channel.

## 1. Web Scrapping
Web scrapping is done by first finding the number of the latest article on the main page of the website. After that, from the web page of the latest article a content is gathered. Then, it is summarized by a Google Gemini model and sent to the administator of the channel by telegram bot + save paragraphs to the google sheets.

## 2. Interacting with human
After the web scrapping, a human is able to give the instructions to an AI Agent powered by the Google Gemini model throught interacting with telegram bot API to make changes in the summarized text (for example, delete some of the sentences or make it shorter). AI agent saves changes in the Google Sheets.

## 3. Posting content
After the message of approval from the human, the system posts the corrected text to the Telegram Channel.
