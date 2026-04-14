# 🌦️ RTO Weather Advisor

An AI-powered agent that analyzes weather forecasts to determine the most comfortable 3 days to commute, ensuring you avoid rain, snow, and freezing temperatures while adhering to corporate scheduling policies.

## 📸 Example Email Report
![Agent Output](RTOScreenshot.png)

## 🌟 Features
1. Fetches a 10-day forecast from Open-Meteo API
2. Scores each day using a custom penalty system (freezing rain, 
   rain, snow, cold) with extra penalty on commute hours (8AM / 4PM)
3. Finds the optimal 3-day combo that includes either Monday or Friday (company policy)
4. Uses Google Gemini AI to generate a natural, personalized explanation
5. Sends an HTML email summary every week
6. Designed for Google Cloud Run (serverless)

## Tech Stack
- **Python** — core logic
- **Google Cloud Run** — serverless deployment + scheduled trigger
- **Gemini AI (Gemma 4)** — natural language explanation
- **Open-Meteo API** — free weather data
- **Gmail SMTP** — email delivery
- **Google Cloud Run** – Deployment

## Setup

### Prerequisites
- Python 3.11+
- A Google Cloud project with Cloud Run enabled
- A Gmail account with an App Password

### Requirement.txt
- requests
- pandas
- google-genai
- python-dotenv

### Environment Variables
- RECEIVER_EMAIL=your-email@example.com
- SENDER_EMAIL=your-sender@gmail.com
- SENDER_APP_PASSWORD=your-gmail-app-password
- GOOGLE_API_KEY=your-gemini-api-key

## Development
The notebook (`rto-weather-agent.py`) contains the development process, including code cells for creating and testing the agent in Google Colab.

## About
Built by Daniel Young as a portfolio project to showcase applied data science skills in multi-source API integration, data processing, and LLM-driven automation, using a Python-based agent to deliver daily weather and RTO day selectio recommendations for improving commute life.
