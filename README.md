# 📊 Telegram AI Personal Finance Tracker

An automated personal finance tracking system that captures expenses and income via Telegram messages, parses them using Google Gemini AI, and logs them into Google Sheets using Make.com.

---

## 🏗 Architecture & Workflow

1. **Input:** User sends a natural language prompt to the Telegram Bot (e.g., *"4€ coffee"* or *"Paid 200€ for freelance project"*).
2. **Processing:** Make.com forwards the text to **Google Gemini AI**.
3. **Parsing:** Gemini extracts structured JSON data containing `type`, `amount`, `category`, and `description`.
4. **Storage:** The parsed data is automatically appended as a new row in **Google Sheets** with a timestamp (`now`).

---

## 🛠 Tools & Technologies

* **Telegram Bot API:** Mobile interface for sending quick financial updates.
* **Make.com:** Automation platform (iPaaS) connecting all services.
* **Google Gemini AI (`gemini-3.6-flash`):** Natural Language Processing (NLP) to convert unstructured text into JSON.
* **Google Sheets:** Database and spreadsheet storage.

---

## 🚀 How to Replicate

1. **Clone/Download Repository:** Download the `make-scenario-blueprint.json` file.
2. **Import Blueprint:** Go to Make.com, create a new scenario, and select **Import Blueprint** from the bottom menu.
3. **Configure Connections:**
   * Link your **Telegram Bot Token** (via BotFather).
   * Link your **Google Gemini API Key** (via Google AI Studio).
   * Select your **Google Sheets** target file.
4. **Set System Instruction:** Pass the following instruction to Gemini:
   > Extract transaction details into JSON format with keys: `type` (Expense/Income), `amount` (numeric), `category`, `description`.
5. **Enable Automation:** Turn **SCHEDULING** to **ON** (Immediately as data arrives).

---

## 🔐 Security Notice
All API keys, bot tokens, and personal credentials have been removed from the exported blueprint file for security purposes.
