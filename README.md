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

- R with packages: `shiny`, `plumber`, `dplyr`, `readr`, `httr2`, `jsonlite`, `knitr`
- LM Studio for local LLM hosting
- Bash shell (for `run.sh`)

### Installation & Setup

1. **Clone the repository**:
```bash
git clone https://github.com/foundations/tree/main/example_project
cd example_project
```

2. **Install R dependencies**:
```r
install.packages(c("shiny", "plumber", "dplyr", "readr", "httr2", "jsonlite", "knitr"))
```

3. **Install LM Studio** and download the `google/gemma-3-1b` model

### Running the System

Execute the main orchestration script in `git bash`.
```bash
./run.sh
```

This will:
1. Start the LLM service (LM Studio on port `1234`)
2. Launch the REST API (R Plumber on port `8000`)
3. Start the Shiny app (on port `8001`)

## 🔧 Component Details

### 1. Shiny App (`/app/app.R`)

**Purpose**: Interactive web interface for insulin pump data analysis

**Features**:
- Multi-select pump type interface
- Real-time data table display
- AI-generated summary analysis
- RESTful API integration

**Key Functions**:
- `api_data()`: Fetches data from the API
- `renderTable()`: Displays statistical summaries
- `renderText()`: Shows AI-generated insights

### 2. REST API (`/api/plumber.R`)

**Purpose**: Backend service for data processing and AI integration

**Endpoints**:
- `GET /summary?pumpid={ids}`: Returns statistical analysis and AI summary

**Key Functions**:
- `get_data(pumpid)`: Retrieves data from Google Sheets
- `get_stat(data)`: Calculates summary statistics
- `get_blurb(stat)`: Formats data as markdown
- `get_chat(blurb)`: Generates AI insights via LLM

### 3. Database (Google Sheets)

**Purpose**: Public data source containing insulin pump satisfaction surveys

**Data Structure**:
- `timestamp`: Survey submission time
- `type`: Pump model (Medtronic, Omnipod, Tandem)
- `satisfaction`: User satisfaction rating
- `failed`: Failure occurrence
- `date_failed`: Failure date

### 4. AI Agent (LM Studio)

**Purpose**: Intelligent data summarization and insights generation

**Configuration**:
- Model: `google/gemma-3-1b`
- System prompt: Specialized for insulin pump data analysis
- Temperature: 0.7 for balanced creativity/consistency

## 📊 Data Flow

1. **User Input**: Select pump types in Shiny app
2. **API Request**: App sends GET request to `/summary` endpoint
3. **Data Retrieval**: API fetches data from Google Sheets
4. **Statistical Analysis**: Calculate means, standard deviations, sample sizes
5. **AI Processing**: Send formatted data to LLM for summarization
6. **Response**: Return both statistical table and AI insights
7. **Display**: App renders results in interactive interface

## 🔍 Technical Highlights

- **Asynchronous Processing**: Non-blocking API calls
- **Modular Design**: Separated concerns across components
- **Scalable Architecture**: Easy to extend with additional endpoints
- **Production-Ready**: Proper logging and error management

## 🛠️ Development Notes

- The system uses a public Google Sheet as a database substitute
- LM Studio provides local LLM hosting for privacy and cost control
- All services run on different ports to avoid conflicts
- The orchestration script handles service startup sequencing

## 📈 Optional Enhancements

- Add additional credit cards
- Extra benefit tracking visualizations
- Add referal links
- Add cent per point values
- Add transfer partner cent per point values
