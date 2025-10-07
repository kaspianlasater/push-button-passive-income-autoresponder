[README.txt](https://github.com/user-attachments/files/22740796/README.txt)
Ultimate AI Funnel PRO (Full) - README
========================================

What's included:
- public/index.html (signup form prefilled with name/email placeholders)
- public/success.html (thank-you page)
- server.js (backend: saves leads, sends Gmail alerts, pushes to Google Sheets, generates AI welcome emails)
- leads.json (local backup)
- .env (pre-filled with your Gmail + app password — KEEP THIS FILE PRIVATE)
- package.json (dependencies)

Quick local run:
1) Install Node.js (v16+)
2) In the project folder run:
   npm install
   npm start
3) Open http://localhost:3000 and test the form.

Google Sheets setup (optional):
1) Create a Google Cloud Project and enable the Google Sheets API.
2) Create a Service Account, generate a JSON key file, and download it to the project folder as "service-account-key.json".
3) Share your Google Sheet with the service account email (editor access).
4) Put the sheet ID in .env (GOOGLE_SHEET_ID). Set GOOGLE_SERVICE_ACCOUNT_KEY to the path of the downloaded JSON key file.

OpenAI (optional for better AI emails):
- Add your OpenAI API key to OPENAI_API_KEY in .env to let the server generate nicer AI-written welcomes.

Security notes:
- The .env in this package is pre-filled with your Gmail details as you requested. Keep the ZIP and repo private; DO NOT publish publicly.
- For production, it's best to set secrets directly in your host's environment variables rather than including .env in source control.

Deploy to Render:
- Create a private GitHub repo and push the unzipped files.
- Create a new Web Service on Render, connect the repo.
- Build command: npm install
- Start command: npm start
- For security, set GMAIL_USER and GMAIL_PASS in Render's environment variables instead of committing .env to the repo.

Enjoy!
