# 💬 Arunav AI WhatsApp Bot

[![Node.js](https://img.shields.io/badge/Node.js-18.x-brightgreen?logo=node.js)](https://nodejs.org/)
[![Baileys](https://img.shields.io/badge/Baileys-WhiskeySockets-blue?logo=whatsapp)](https://github.com/WhiskeySockets/Baileys)
[![OpenAI](https://img.shields.io/badge/OpenAI-GPT--3.5/4-purple?logo=openai)](https://openai.com/)
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Made with ❤️ in India](https://img.shields.io/badge/Made%20in-%E2%9D%A4%EF%B8%8F%20India-orange)](https://thebrothing.com)

This is a WhatsApp chatbot powered by OpenAI GPT and Baileys, trained to reply like Arunav Gupta an elite Indian dating coach.  
It speaks like a confident elder brother: flirty, practical, respectful, and masculine.

---

📸 Demo

_(Insert GIF or screenshot here)_

---

## ⚙️ Features

- ✅ Smart WhatsApp chatbot using OpenAI
- 👨‍🏫 Custom personality: talks like Arunav from The Bro Thing
- 📱 Handles both personal & group messages (configurable)
- 🔁 Auto-reconnect if WhatsApp disconnects
- 💾 Remembers message logs & chat context
- ✏️ Simple file-based setup (no DB needed)

---

## 📁 Folder Structure

arunav-ai-bot/
│
├── data/ # Chat history & context
│ ├── messages.json
│ └── context.json
│
├── src/ # Main logic
│ ├── index.js # WhatsApp bot starter
│ ├── openai.js # Handles GPT replies
│ ├── logger.js # Logs messages
│ └── groupHandler.js # (Optional) extra logic for groups
│
├── training/ # Custom bot personality
│ └── knowledge_base.txt
│
├── .env # Environment config
├── package.json
├── README.md

---

🚀 Getting Started

1. Clone the repo

git clone https://github.com/yourusername/arunav-ai-bot.git
cd arunav-ai-bot

2. Install dependencies
   npm install

3. Add environment variables
   Create a .env file in root:

OPENAI_API_KEY=your-openai-key-here
SESSION_AUTH_PATH=./auth_info
REPLY_IN_GROUPS=true
REPLY_IN_PERSONAL=false

4. Customize bot voice
   Edit training/knowledge_base.txt:

vbnet
Copy
Edit
You are Arunav, an elite dating coach who speaks like a confident elder brother.
Your replies are flirty, practical, respectful, and masculine.

Examples:

Q: I matched a girl, what should I say?
A: Start with something on her profile. Keep it playful: “Your travel pics made me jealous. Planning your next trip already?”

Q: She hasn’t replied in 2 days, what now?
A: Don’t chase. Post a story, show your life is full. Then later send: “Guess you got busy being cute somewhere else.”

Always reply short, smart, and human. Don’t sound robotic. Avoid generic advice. 5. Run the bot
bash
Copy
Edit
node src/index.js
Scan the QR code in terminal with WhatsApp.

🔄 Changing WhatsApp Number
If you want to use a new number:

bash
Copy
Edit
rm -rf auth_info
node src/index.js
Then scan again with the new number.

🔧 Configuration Guide
Variable Description Example
OPENAI_API_KEY Your OpenAI API key sk-...
SESSION_AUTH_PATH Path to store WhatsApp auth session ./auth_info
REPLY_IN_GROUPS Reply in groups (true/false) true
REPLY_IN_PERSONAL Reply to personal chats (true/false) false

🧠 GPT Message Flow
json
Copy
Edit
[
{ "role": "system", "content": "Prompt from knowledge_base.txt" },
{ "role": "user", "content": "Actual WhatsApp message" }
]
Bot then replies like a smooth, emotionally calibrated human (not like ChatGPT).

🛠️ Troubleshooting
Problem: OpenAI key not found
Solution:
Make sure .env exists in project root and you run from root:

bash
Copy
Edit
node src/index.js
If inside src/, use:

js
Copy
Edit
require("dotenv").config({ path: "../.env" });
📜 License
This project is licensed under the MIT License.

👑 Made by @TheBroThing
Want a bot like this for your brand, startup, or influencer persona?
DM us — we build custom AI bots that sound like you and sell for you.
