QA Bot Setup Guide

Prerequisites

•⁠  ⁠Git installed on your machine
•⁠  ⁠Node.js and npm installed
•⁠  ⁠VS Code installed
•⁠  ⁠Postman (or any API testing tool)
•⁠  ⁠GROQ API key
•⁠  ⁠TestLeaf API key

Setup Instructions

1.⁠ ⁠Fork the Repository

1.⁠ ⁠Go to [https://github.com/Qeagle/qa-bot-langchain/](https://github.com/Qeagle/qa-bot-langchain/)
2.⁠ ⁠Click the *Fork* button in the top-right corner
3.⁠ ⁠Select your GitHub account to create the fork

2.⁠ ⁠Clone Your Forked Repository

Open your terminal and run:

git clone https://github.com/YOUR_USERNAME/qa-bot-langchain.git
cd qa-bot-langchain

Replace ⁠ YOUR_USERNAME ⁠ with your actual GitHub username.

3.⁠ ⁠Open in VS Code

open VS Code manually and select *File > Open Folder* and choose the ⁠ qa-bot-langchain ⁠ directory.

4.⁠ ⁠Switch to the Feature Branch

In the terminal within VS Code, run:

git checkout feature/custom-model

5.⁠ ⁠Configure Environment Variables

1.⁠ ⁠In the root directory, locate the ⁠ .env.example ⁠ file
2.⁠ ⁠Create a copy and rename it to ⁠ .env ⁠:

cp .env.example .env

3.⁠ ⁠Open the ⁠ .env ⁠ file and update the following keys:

GROQ_API_KEY=your_groq_api_key_here
TESTLEAF_API_KEY=your_testleaf_api_key_here

4.⁠ ⁠Save the file (⌘+S on macOS)

6.⁠ ⁠Install Dependencies and Run the Application

In the terminal, run:

npm install
npm run dev

The server should start on ⁠ http://localhost:8787 ⁠

7.⁠ ⁠Test the API with Postman

1.⁠ ⁠Open Postman
2.⁠ ⁠Create a new *POST* request
3.⁠ ⁠Set the URL to: ⁠ http://localhost:8787/search/document ⁠
4.⁠ ⁠Go to the *Body* tab
5.⁠ ⁠Select *raw* and *JSON* format
6.⁠ ⁠Enter the following request body:

{
    "question": "What is the main topic of this document?",
    "documentPath": "path/to/your/document.pdf"
}