Website Chatbot - Google Gemini + Pinecone + Google Drive
=========================================================

An intelligent **AI-powered website chatbot** built using **Google Gemini**, **Pinecone**, and **Google Drive**, designed for **Noura Aesthetics Clinic**.This workflow allows the chatbot to automatically learn from uploaded Google Drive files and deliver smart, context-aware responses to website visitors in real time.

🚀 Features
-----------

*   🤖 **AI Chatbot (Google Gemini)** – Uses Gemini’s chat model for natural, human-like responses.
    
*   🧠 **Contextual Memory** – Maintains short-term chat context for smooth, continuous conversations.
    
*   📂 **Google Drive Integration** – Monitors a folder for new or updated files to refresh chatbot knowledge automatically.
    
*   🔍 **Vector Search (Pinecone)** – Embeds Drive content and retrieves relevant answers using semantic similarity.
    
*   ⚙️ **Automated Data Flow** – Files are processed, split into text chunks, embedded, and stored without manual steps.
    
*   💬 **Website Trigger** – Activates when a user sends a message through the website chat widget.
    

🧩 Workflow Overview
--------------------

1.  **Website Chat Message Received** → triggers the **AI Agent**.
    
2.  **AI Agent (Gemini)** → processes the user query using memory and the vector store.
    
3.  **Pinecone Vector Store** → retrieves the most relevant knowledge based on Drive documents.
    
4.  **Google Drive Trigger** → detects new or updated files and re-embeds them via **Gemini Embeddings**.
    
5.  **Default Data Loader + Text Splitter** → preprocesses content before vector storage.
    

🛠️ Tech Stack
--------------

*   **n8n** – Workflow automation
    
*   **Google Gemini (PaLM API)** – Chat model & embeddings
    
*   **Pinecone** – Vector database for semantic retrieval
    
*   **Google Drive API** – File storage and triggers
    
*   **LangChain** – AI pipeline orchestration
    

📁 Folder Automation
--------------------

The workflow monitors a specific Google Drive folder:

> Any new or updated files are automatically processed and embedded into Pinecone, keeping your chatbot’s knowledge up to date.

_(Make sure to set appropriate sharing permissions if the folder contains sensitive data.)_

🔒 Security Note
----------------

*   No API keys or credentials are stored in the exported JSON.
    
*   Credential references (like IDs) are local to your own n8n instance.
    
*   Safe to share or publish the workflow JSON publicly.
    

⚙️ Setup
--------

1.  Import the Website-Chatbot.json file into your **n8n** instance.
    
2.  Reconnect your credentials for:
    
    *   Google Drive OAuth2
        
    *   Google Gemini (PaLM API)
        
    *   Pinecone API
        
3.  Update your Pinecone index and namespace if needed.
    
4.  Deploy your website chat widget or trigger endpoint.
    

🧠 Example Use Case
-------------------

This chatbot can serve as an **AI assistant** for clinics, educational websites, or online businesses - answering visitor questions using up-to-date information stored in Google Drive.

📜 License
----------

Released under the **MIT License** – free to use, modify, and distribute with attribution.
