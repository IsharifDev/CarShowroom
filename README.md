# CarShowroom

A full-stack car showroom management system for browsing vehicle inventory, scheduling test drives, and managing sales operations, backed by automated end-to-end tests.

## Tech Stack

- **Frontend:** React, TypeScript, Node.js
- **Backend:** Python, FastAPI
- **Database:** PostgreSQL
- **Testing & Automation:** Playwright, Selenium

## Features

- **Vehicle Inventory:** Browse, search, and filter vehicles by make, model, year, fuel type, and price.
- **Test Drive Scheduling:** Book and manage customer test drive appointments.
- **Sales & Inquiries:** Track customer inquiries, vehicle availability status, and sales records.
- **End-to-End Test Automation:** Automated browser and flow tests using Playwright and Selenium.

## Project Structure

- `CarShowroom/`
  - `backend/` — FastAPI app, models, schemas, routes, and PostgreSQL config
  - `frontend/` — React + TypeScript user interface
  - `tests/` — Automated test suites
    - `playwright/` — Playwright end-to-end tests
    - `selenium/` — Selenium browser tests
  - `.gitignore`
  - `README.md`

## Getting Started

### Prerequisites

- **Node.js** (v18 or higher)
- **Python** (3.10 or higher)
- **PostgreSQL** (14 or higher)

### 1. Clone the Repository

    git clone https://github.com/IsharifDev/CarShowroom.git
    cd CarShowroom

### 2. Backend Setup (FastAPI + PostgreSQL)

    cd backend
    python -m venv .venv
    source .venv/bin/activate
    pip install -r requirements.txt

*(Note: On Windows PowerShell, activate the environment with `.venv\Scripts\Activate.ps1`)*

Create a `.env` file inside `backend/` with your database credentials:

    DATABASE_URL=postgresql://postgres:your_password@localhost:5432/carshowroom
    SECRET_KEY=change_this_to_a_strong_secret_key

Start the FastAPI server:

    uvicorn app.main:app --reload

### 3. Frontend Setup (React + TypeScript)

Open a new terminal and run:

    cd frontend
    npm install
    npm run dev

### 4. Running Automated Tests

**Playwright:**

    cd tests/playwright
    npm install
    npx playwright install
    npx playwright test

**Selenium:**

    cd tests/selenium
    pip install -r requirements.txt
    pytest

## License

This project is currently unlicensed. Add a `LICENSE` file or configure one in GitHub repository settings to define usage terms.