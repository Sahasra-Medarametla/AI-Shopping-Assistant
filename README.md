**AI Shopping Assistant using Telegram & n8n**

**Introduction**

This project builds an AI Shopping Assistant that helps users find products quickly using Telegram.
The assistant understands user queries, searches products from Amazon, and returns the most relevant results with price and rating information.

Users can interact with the assistant using text messages or voice messages.

**Problem**

Online shopping often has several challenges:

-Too many search results

-Time spent comparing products

-No personalized suggestions

-This makes product searching slow and frustrating.

**Solution**

-The AI Shopping Assistant simplifies shopping by:

-Accepting text or voice queries

-Searching products from Amazon in real time

-Returning the top relevant products

-Providing quick responses inside Telegram

**Tools Used**

n8n – Workflow automation

Telegram Bot – User interaction

Google Gemini AI – Understands user queries

Scraper API – Fetches Amazon product data

Whisper API (Groq) – Converts voice to text

HTTP Request Node – Connects APIs in n8n

**Features**

-Text-based product search

-Voice message support

-Real-time Amazon product results

-Product details like price and ratings

-Fast responses inside Telegram

**Workflow Steps**
1. Telegram Trigger

The workflow starts when a user sends a message to the Telegram bot.

2. Message Type Check

The system checks whether the message is text or voice.

3. Voice Processing (if audio)

Download audio file from Telegram

Convert .oga file to .ogg

Use Whisper API to convert speech to text

4. AI Processing

The Gemini AI model understands the user request and prepares the product search query.

5. Product Search

The system uses Scraper API to fetch product information from Amazon.

6. Send Response

The assistant sends the top relevant products back to the user on Telegram.

**Workflow Architecture**

Telegram Message

↓

Check Message Type

↓

Text → AI Agent

Audio → Speech-to-Text → AI Agent

↓

Search Amazon Products

↓

Send Product Results to Telegram

**Example Query**
red dress under 2000

or voice message asking the same.

**Output**

The assistant returns:

Top product names

Price

Ratings

Product links

**Benefits**

-Faster product search

-Hands-free voice input

-Personalized product suggestions

-Simple shopping experience inside Telegram

**Future Improvements**

-Add personalized fashion recommendations

-Support multiple shopping websites

-Add image-based product search

-Include price comparison
