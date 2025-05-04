# 🧠 Research Assistant

A full-stack productivity tool that combines a **Spring Boot API** and a **Chrome Extension** to help summarize and extend research notes using Google's Gemini API. The extension allows users to interact with AI directly in a side panel and receive relevant summaries or suggestions.

---

## 📦 Tech Stack

- **Backend**: Spring Boot (Java), WebClient, Jackson, Maven  
- **Frontend**: Chrome Extension (HTML/CSS/JS)  
- **AI Integration**: Gemini Pro API  
- **Build Tool**: Maven

---

## 📂 Project Structure

research-assistant/
├── research-assistant/ # Spring Boot backend
│ ├── src/main/java/com/research/assistant/
│ ├── src/main/resources/
│ └── pom.xml
├── research-assistant-ext/ # Chrome extension
│ ├── manifest.json
│ ├── background.js
│ ├── sidepanel.html
│ ├── sidepanel.js
│ └── sidepanel.css
└── .gitignore

---

## 🚀 How to Run the Spring Boot API

1. Navigate to the backend folder:
   ```bash
   cd research-assistant/research-assistant

2. Update application.properties with your Gemini API credentials:

properties
Copy code
gemini.api.url=https://generativelanguage.googleapis.com/v1beta/models/gemini-pro:generateContent?key=
gemini.api.key=YOUR_API_KEY_HERE

3. Run the app:
bash
Copy code
./mvnw spring-boot:run
The API will start on http://localhost:8080



**How to Load the Chrome Extension**
1. Open Chrome and go to chrome://extensions/

2. Enable Developer Mode (top-right toggle)

3. Click Load unpacked

4. Select the research-assistant-ext folder

5. Pin the extension and click to launch the side panel

🔗 API Endpoint
Method	Endpoint	Description
POST	/api/process-content	Accepts operation and content text

