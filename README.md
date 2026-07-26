# news-sentiment-stock-chatbot
LLM-powered financial chatbot combining FinBERT sentiment analysis, historical financial news, and live Yahoo Finance data for sentiment-driven stock forecasting using Groq and OpenRouter.

# News Sentiment-Driven Stock Prediction Chatbot

An LLM-powered financial chatbot that combines **FinBERT sentiment analysis**, historical financial news, and live Yahoo Finance market data to generate sentiment-driven stock forecasts. The project also compares **Groq** and **OpenRouter** as inference backends for the same Llama 3.3 70B model.

## Overview

This project uses financial news headlines to estimate short-term stock movements through a sentiment-based prediction pipeline. Rather than training a machine learning forecasting model, it computes historical average next-day returns from sentiment bands and presents the results through an LLM-powered conversational interface.

Two implementations are included:

- **Groq** (Llama 3.3 70B)
- **OpenRouter** (Llama 3.3 70B)

Both use the same prediction pipeline and differ only in the LLM inference backend.

## Dataset

- **Historical News:** `analyst_ratings_processed.csv`
- **Period:** 2009–2020
- **Live Market Data:** Yahoo Finance (`yfinance`)
- **Sentiment Model:** ProsusAI/FinBERT
- **LLM:** Llama 3.3 70B (Groq / OpenRouter)

## Features

- Financial news sentiment analysis using FinBERT
- Historical sentiment-band construction
- Live stock price and news retrieval
- Sentiment-driven price forecasting
- Conversational chatbot interface
- Groq and OpenRouter backend comparison
- Cached sentiment lookup tables for faster inference

## Key Takeaways

- Uses FinBERT to score financial news sentiment.
- Maps sentiment scores into historical return bands for stock forecasting.
- Integrates live Yahoo Finance data for real-time predictions.
- Produces identical prediction logic across Groq and OpenRouter, enabling a direct comparison of LLM inference backends.
