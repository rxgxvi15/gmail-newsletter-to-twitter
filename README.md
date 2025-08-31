# Gmail Newsletter → Social Snippets Workflow

This repository contains an **n8n automation workflow** that transforms email newsletters into short social media snippets.  
It connects Gmail, Google Docs, and Twitter (X) to automatically publish snippets extracted from incoming newsletters.


## 🚀 Workflow Overview

1. **Gmail Trigger**  
   - Watches for new emails from a specific sender (e.g., `ragavisivanesans@gmail.com`).  
   - Runs every minute to check for new content.

2. **Google Docs (Insert)**  
   - Appends the email snippet into a designated Google Doc for archiving and reference.

3. **Google Docs (Get)**  
   - Retrieves the updated document content for processing.

4. **Code Node (Transform)**  
   - Splits the document text by newlines.  
   - Structures the data so that each line becomes an individual snippet ready for posting.

5. **Wait Node**  
   - Adds a delay to avoid hitting API rate limits before posting.

6. **Twitter (Create Tweet)**  
   - Publishes each snippet as a tweet.  
   - Tweets include the snippet text along with a timestamp.



## 🛠️ Tech Stack

- [n8n](https://n8n.io/) – Workflow automation tool
- Gmail – Email trigger
- Google Docs – Storage for snippets
- JavaScript (Code Node) – Data transformation
- Twitter (X) API – Publishing social media posts

