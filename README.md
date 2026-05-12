# 🤖 WhatsApp AI Secretary

An AI-powered WhatsApp automation bot that acts as your personal secretary - filtering spam, confirming payments, and prioritizing important messages automatically.

## 🎯 What it does

- ✅ **Payment Detection** - Automatically confirms payment messages
- 🚫 **Spam Filtering** - Blocks promotional and spam messages  
- 🔔 **Priority Messages** - Flags important contacts
- 💬 **Auto-replies** - Responds intelligently to queries
- 🕐 **Business Hours** - Only responds during work hours
- 🌐 **Multi-language** - Supports Hindi, English, Hinglish
- 📊 **Logs everything** - Records all messages to Google Sheets
- ⚡ **Rate Limiting** - Prevents spam abuse

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| n8n | Workflow automation |
| Google Gemini AI | Message classification |
| Meta WhatsApp Cloud API | WhatsApp integration |
| Google Sheets | Message logging |

## 🏗️ Architecture

Incoming WhatsApp Message
↓
Webhook (n8n)
↓
Message Type Filter
↓
Rate Limiter
↓
Business Hours Check
↓
AI Agent (Gemini)
↓
Google Sheets Logger
↓
Spam Loop Prevention
↓
Auto Reply via WhatsApp

## ✨ Features

### 1. Smart Message Classification
- PAYMENT → Auto confirms with receipt
- SPAM → Silently ignores
- IMPORTANT → Priority alert
- QUESTION → Helpful answer
- NORMAL → Friendly response

### 2. Business Hours Filter
- Only responds 9AM-6PM IST
- Outside hours → Closed message
- Customizable per client

### 3. Rate Limiting
- Max 3 messages per minute per contact
- Prevents API quota abuse
- Customizable limits

### 4. Google Sheets Logging
- Timestamp
- Phone number
- Message content
- AI response
- Auto-organized

### 5. Multi-language Support
- Detects message language automatically
- Replies in same language
- Supports Hindi, English, Hinglish

## 🚀 Setup Guide

### Prerequisites
- n8n account (free at n8n.io)
- Google account
- Meta WhatsApp Cloud API credentials
- Google Gemini API key (free at aistudio.google.com)

### Installation

**Step 1 — Import workflow:**
1. Download `workflow.json`
2. Go to n8n dashboard
3. Click "Import workflow"
4. Upload file

**Step 2 — Add credentials:**
1. Google Gemini API key
2. Google Sheets OAuth
3. WhatsApp API token

**Step 3 — Configure:**
1. Update webhook URL
2. Set business hours
3. Add VIP contacts
4. Update system message

**Step 4 — Deploy:**
1. Click Publish in n8n
2. Add webhook URL to WhatsApp API
3. Test with a message!

## 💰 Use Cases

| Business Type | Value |
|--------------|-------|
| Restaurants/Cafes | Order & booking management |
| Coaching Institutes | Student query handling |
| Freelancers/Consultants | Client communication |
| E-commerce sellers | Order confirmations |
| Real Estate | Lead filtering |

## 📸 Screenshots

*Coming soon*

## 🎥 Demo

*Coming soon*

## ⚠️ Disclaimer

This bot uses AI for automated responses. All messages are processed automatically. Not responsible for any miscommunication.

## 👨‍💻 Author

**Jatin**
- GitHub: [@your-username]
- Built with n8n + Google Gemini

## 📄 License

MIT License - feel free to use and modify!
