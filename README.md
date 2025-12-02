# SYSEN-5151 Team 3 Project

Team 3 Systems Engineering graduate student group project demonstrating the integration of a **Shiny App**, **REST API**, **Database**, and **AI Agent** for analyzing Credit Card Benefit Tracker data.

## Problem Statement

According to a 2025 CreditCards.com survey, 23% of rewards cardholders haven’t redeemed any rewards over the past year.
- Reward credit card customers are missing out on “fee money” card issues providing for using their card
- 50% of American adults have 2+ credit cards
- Cardholders struggle to manage multiple credit cards and utilize all of the benefits offered

## Team Goal

To create a tool that helps users manage multiple credit cards to track and maximize rewards.

## 🎯 Project Overview

This project showcases a complete data science pipeline that:
- **App**: Interactive Credit Card Benefit Tracker web application for data visualization
- **API**: RESTful service built with R Plumber for data processing
- **Database**: Public Google Sheets as a data source (simulating a database)
- **AI Agent**: LLM integration for intelligent data summarization

## Solution/Objective

- **Single Rewards Tracker**: A mobile application that brings together rewards, perks, and offers from all the credit cards.
- **Unified Dashboard**: View and manage all credit card rewards, balances, and benefits in one easy-to-use interface.
- **AI Assistant**: AI-powered assistant that learns spending habits across multiple cards and the rewards marketplace to deliver tailored strategies for maximizing benefits.
- **Personalized Recommendations**: Get real-time guidance on the best card to use for each purchase category (travel, dining, groceries, and others).
- **Smart Reminders**: Stay on top of expiring rewards, rotating bonus categories, and limited-time offers with timely alerts.

## 🏗️ Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   CC Track App     │───▶│   REST API      │───▶│   Database      │───▶│   AI Agent      │
│   (Port 8001)   │    │   (Port 8000)   │    │   (Google Sheet)│    │   (Port 1234)   │
└─────────────────┘    └─────────────────┘    └─────────────────┘    └─────────────────┘
```

## 📁 Project Structure

### Core Files

- **need to add run sh reference** - Main orchestration script that starts all services
- [`README.md`] (README.md)- This documentation file

### App Directory (`/app`)

- **need to add app directory reference** - Shiny web application for insulin pump data visualization

### API Directory (`/api`)

- **add plumber reference** - REST API endpoints for data processing and AI integration
- **add r script reference** - API server startup script

## 🚀 Quick Start

### Prerequisites

- Make sure you have a figma accont or create one

### Installation & Setup

1. **Clone the repository**:
```bash
git clone [https://github.com/foundations/tree/main/example_project
cd example_project](https://github.com/alb473/SYSEN-5151-Team-3/edit/main/README.md)
```

2. **Access the website**:
```https://cat-coal-70641067.figma.site/welcome
```

3. **Access the code**
```[https://cat-coal-70641067.figma.site/welcome](https://www.figma.com/make/WmYF3xhMTaF3sQWs05wHM1/SYSEN5151?node-id=0-1&p=f&t=BZSpuWUKZYf59HoM-0)
```

## 🔧 Component Details

### 1. Website
```https://cat-coal-70641067.figma.site/welcome
```
**Purpose**: To give users the ability to track credit card benefits and rewards for multiple credit cards.

**Features**:
- Can select multiple credit cards to track
- AI generated recommendations
- Offer tracking

**Key Functions**:


### 2. REST API 

**Purpose**: 

**Endpoints**:
-

**Key Functions**:


### 3. Database

**Purpose**: 

**Data Structure**:


### 4. AI Agent

**Purpose**: 

**Configuration**:
- Model: `custom ML Model`
- System prompt: Specialized for credit card benefit tracking analysis

## 📊 Data Flow

1. **User Input**: Select card types
2. **API Request**: Secure OAuth or Plaid/Finicity API connection.
3. **Data Retrieval**: Real time reward data from APIs
4. **Statistical Analysis**: Calculate bonus totals, calculate bonuses, calculate best deals
5. **AI Processing**: Send formatted data to LLM for summarization
6. **Response**: Return insights and offers
7. **Display**: App renders card benefit tracking results in interactive interface

## 🔍 Technical Highlights



## 🛠️ Development Notes

- The system uses AI to track different offers
- User input including type of card details directs them to curated data

## 📈 Optional Enhancements

- Add additional credit cards
- Extra benefit tracking visualizations
- Add referal links
- Add cent per point values
- Add transfer partner cent per point values
