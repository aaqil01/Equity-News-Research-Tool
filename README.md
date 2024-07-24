# Equity-News-Research-Too

A web application powered by Streamlit and OpenAI's language model, designed for fetching, analyzing, and querying news articles based on user-provided URLs.

## Overview
This is a Streamlit-based web application designed to fetch news articles from user-provided URLs, process them, create embeddings, and allow users to query these articles using a question. The app utilizes various components of the LangChain library and integrates with OpenAI for language processing tasks.

## Features
Input: Users can input up to three URLs of news articles.
Processing: Articles are fetched, split into chunks, and embedded using OpenAI's language model.
Search: Users can ask questions related to the articles, and the app retrieves relevant answers from the stored embeddings.
Output: Displays the answer to the query and optionally, the sources cited for the answer.

## Setup and Usage
# Installation

Ensure Python 3.x is installed.
Install required packages using:
```
pip install streamlit langchain python-dotenv
```
## Configuration

Create a .env file in the project directory with your OpenAI API key:
makefile
```
OPENAI_API_KEY="your_openai_api_key_here"
```
## Running the App

Execute the Streamlit app:
arduino

```
streamlit run app.py
```
This will launch the app in your default web browser.

## Using the App

Input URLs of news articles in the sidebar.
Click "Process URLs" to fetch and process the articles.
Enter a question related to the articles in the main section and press Enter.
View the answer and cited sources (if available) displayed on the app.

## Components Used
Streamlit: For creating the web application interface.
LangChain: A library for building language processing pipelines.
UnstructuredURLLoader: Loads data from URLs.
RecursiveCharacterTextSplitter: Splits text into chunks for processing.
OpenAIEmbeddings: Generates embeddings using OpenAI's language model.
FAISS: A library for efficient similarity search and clustering of dense vectors.
OpenAI GPT-3.5: Provides the language model used for question answering.

## Files Included
app.py: The main Streamlit application code.
.env: Environment configuration file for storing API keys.
faiss_store_openai.pkl: Pickle file storing FAISS index of article embeddings.

## Dependencies
Python 3.x
Streamlit: 0.82.0
LangChain: Latest version compatible with Streamlit and OpenAI
Python-dotenv: For loading environment variables from .env file.
