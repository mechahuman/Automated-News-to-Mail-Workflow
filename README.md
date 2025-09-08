#  News Update on Email — n8n Workflow

This project contains an **n8n workflow** that fetches the latest news from multiple sources every morning and sends a daily digest email.

The workflow is exported from [n8n](https://n8n.io) and can be imported into your own instance.

---

##  Features
-  **Schedule Trigger** — runs automatically at 8:00 AM.
-  **RSS Feeds** — pulls headlines from:
   - ESPN (Sports)
   - TechCrunch (Technology)
   - Times of India (Top Stories from India)
-  **Merge + Code Nodes** — extracts the **top 3 news articles** from each source and formats them into a digest.
-  **Gmail Node** — sends the compiled digest to your chosen email.

---

##  How to Use

### 1. Import into n8n
- Download [workflow](main.html)
  

### 2. Configure Gmail Node
The workflow uses a Gmail node to send the digest.

- In the JSON, the placeholder recipient is:
examplemail@gmail.com

Replace this with your own destination email.


- Reconnect the Gmail **credentials** inside n8n:
- Go to **Credentials → New → Gmail OAuth2 API**.
- Authenticate with your Google account.
- Select that credential inside the **Send a message** node.

⚠️ **Your personal email/credentials are never included** in this repo. You must configure them yourself after import.


### 3. Run & Test
- Enable the workflow in n8n.
- Trigger manually or wait until **8:00 AM**.
- You should receive a digest email with top headlines grouped by category.


---

##  License
MIT License — [LICENSE](LICENSE)

---

##  Credits
Built with [n8n](https://n8n.io).  
News sources: [ESPN](https://www.espn.com/), [TechCrunch](https://techcrunch.com/), [Times of India](https://timesofindia.indiatimes.com/).



