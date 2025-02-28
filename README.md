# Assignment 2: Support Agent Chatbot for CDP "How-to" Questions

This project implements a support agent chatbot that provides step-by-step "how-to" guidance for Customer Data Platforms (CDPs) such as Segment, mParticle, Lytics, and Zeotap. The chatbot uses a language model (via LangChain) to generate structured JSON responses, and it integrates various tools (web search, Wikipedia query, and file-saving) to gather and present information.

---

## Table of Contents

- [Project Structure](#project-structure)
- [Features](#features)
- [Requirements](#requirements)
- [Setup](#setup)
- [Usage](#usage)
- [Notes](#notes)
- [License](#license)

---

## Project Structure

The project is organized as follows:

assignment2/
├── main.py # Main Flask and LangChain application
├── tools.py # Definitions for search, Wikipedia query, and saving tools
├── requirements.txt # List of Python dependencies
├── README.md # This documentation file
├── .env # Environment file containing the API key (e.g., OPENAI_API_KEY)


---

## Features

- **CDP "How-to" Assistance:**  
  Answer questions about performing tasks or using features in popular CDPs — Segment, mParticle, Lytics, and Zeotap.

- **Structured JSON Output:**  
  The agent generates responses with a strict JSON format, including:
  - `topic`: A brief summary topic of the answer.
  - `summary`: Detailed step-by-step instructions or guidance.
  - `sources`: A list of source URLs or references used.
  - `tools_used`: A list of tools that were invoked (e.g., web search, Wikipedia).

- **Tool Integration:**  
  Three tools are available:
  - **Web Search:** Uses DuckDuckGo to search for relevant information.
  - **Wikipedia Query:** Retrieves concise data using Wikipedia.
  - **File Saving:** Saves output data to a text file.

- **Multiple Interfaces:**  
  You can run the chatbot in the command-line mode or use the provided web interface (via Flask) as needed.

---

## Requirements

- Python 3.8+
- The following Python packages (see [requirements.txt](requirements.txt)):
  - langchain
  - wikipedia
  - langchain-community
  - langchain-openai
  - langchain-anthropic
  - python-dotenv
  - pydantic
  - duckduckgo-search

---

## Setup

1. **Clone the Repository**

   Clone this repository (or download the project folder) and navigate into it:

2. **Install Dependencies**

Install the required packages using pip:

3. **Configure the API Key**

Create a file named `.env` in the project root with the following line (replace with your actual key):

## Usage

### Command-Line Mode

To run the chatbot in the terminal:
python main.py

Then, when prompted (e.g., "What can I help you research?"), type your CDP-related query such as:
- "How do I set up a new source in Segment?"
- "How can I integrate my data with Zeotap?"

The structured JSON response will be printed in the terminal.


