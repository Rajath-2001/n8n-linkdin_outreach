 # LinkedIn Connection Request Automation (n8n + Browserflow + GeminiAi)

This automation project helps you send **personalized LinkedIn connection requests** automatically using **n8n**, **Browserflow**, **Google Sheets**, and **Gemini Ai API**.

---

##  Overview

The workflow performs the following steps:

1. **Trigger Setup:**  
   Uses a manual or scheduled trigger to start automation.

2. **Fetch Prospects from Google Sheet:**  
   - Pulls rows containing prospect names and LinkedIn URLs.  
   - Filters out entries where connection status = “Yes” (already sent).

3. **Check Connection Status (Browserflow):**  
   - Verifies whether you are already connected or pending with each profile.  
   - Only continues for profiles not yet connected.

4. **Profile Enrichment:**  
   - Retrieves LinkedIn data such as:
     - About/Bio  
     - Current Company  
     - Job Title  
     - Experience/Education  
   - This helps personalize your connection note.

5. **AI Message Generation :**  
   - Generates a personalized 150-character LinkedIn note using Gemini Ai.  

6. **Send Connection Request (Browserflow):**  
   - Sends connection requests automatically with the personalized note.

7. **Wait & Loop Logic:**  
   - Adds delay between requests to avoid LinkedIn restrictions.  
   - Loops for the next prospect.

8. **Update Google Sheet:**  
   - Marks the “Connection Sent” column as “Yes” once the request is sent successfully.

---

##  Tools Used

| Tool | Purpose |
|------|----------|
| **n8n** | Workflow automation engine |
| **Browserflow.io** | Extract and act on LinkedIn data safely |
| **Google Sheets** | Source list of prospects |
| **Gemini Ai API** | Generates personalized messages |
| **Cloud / MCP** | Fetches message templates dynamically |

---

## Key Features
- Fully automated connection process.  
- Uses AI for human-like personalization.  
- Safe cloud-side LinkedIn operations (no cookies).  
- Integrated Google Sheet update system.  
- Adjustable delays to comply with LinkedIn’s limits.

---


