# AI Chat Assistant

A simple AI-powered chat assistant built with Node.js and the Anthropic Claude API, deployed as a serverless function on Vercel.

## Features
- Real-time chat interface (vanilla HTML/CSS/JS, no framework needed)
- Node.js serverless backend calling the Claude API
- Conversation history maintained client-side
- One-click deploy to Vercel

## Tech Stack
- Node.js (Vercel Serverless Functions)
- Anthropic Claude API
- HTML/CSS/JavaScript (frontend)

## Setup

1. Clone the repo and install dependencies:
   ```
   npm install
   ```

2. Get an API key from https://console.anthropic.com

3. Add it as an environment variable in your Vercel project:
   ```
   ANTHROPIC_API_KEY=your_key_here
   ```

4. Deploy:
   ```
   vercel deploy
   ```

## How it works
The frontend sends chat messages to `/api/chat`, a Vercel serverless function that forwards them to the Claude API and returns the model's reply. Conversation history is kept in the browser and resent with each request so the model has context.
