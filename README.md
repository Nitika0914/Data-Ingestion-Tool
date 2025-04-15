Bidirectional ClickHouse & Flat File Data Ingestion Tool
--------------------------------------

Assignment Objective:

This project is a part of the Integration Assignment, where the goal was to build a web-based tool that facilitates bidirectional data ingestion between a ClickHouse database and Flat File (CSV). The application supports both ingestion flows, allows column selection, uses JWT-based authentication, and reports the total number of records processed after ingestion.

--------------------------------------
Features Implemented:

1. Bidirectional Ingestion:
   - ClickHouse → Flat File
   - Flat File → ClickHouse

2. Frontend (React + CSS):
   - Source/target selection (ClickHouse or CSV)
   - ClickHouse connection form
   - CSV config input
   - Table and column discovery with checkbox selection
   - Start ingestion with real-time status updates

3. Backend (FastAPI - Python):
   - Secure ClickHouse connection using JWT tokens
   - Schema and column discovery for both sources
   - Data extraction and insertion logic with batching
   - Record count summary displayed after ingestion

4. Error Handling:
   - Handles connection, authentication, ingestion, and schema errors
   - Displays user-friendly error messages in UI

--------------------------------------
Bonus Features Implemented:

- Multi-table join for ClickHouse source
- Column selection from source
- Progress bar

--------------------------------------
Tech Stack Used:

- Frontend: React, CSS
- Backend: FastAPI (Python)
- Database: ClickHouse (Dockerized for local use)
- File Handling: CSV via Pandas
- Auth: JWT Token-based for ClickHouse

--------------------------------------
How to Run:

1. Clone the repository.

--- Backend (FastAPI) ---
- Go to backend folder:
    cd backend
- Install dependencies:
    pip install -r requirements.txt
- Run the FastAPI server:
    uvicorn main:app --reload

--- Frontend (React) ---
- Go to frontend folder:
    cd frontend
- Install dependencies:
    npm install
- Start the app:
    npm start

--------------------------------------
Folder Structure:

project-root/
│
├── backend/
│   ├── main.py
│   ├── services/
│   ├── utils/
│
├── frontend/
│   ├── public/
│   ├── src/
│
├── prompts.txt
├── README.txt
└── requirements.txt

--------------------------------------
Test Cases Covered:

1. ClickHouse → Flat File (selected columns)
2. Flat File → ClickHouse (selected columns)
3. Join of ClickHouse tables → Flat File
4. Authentication & connection failure cases
5. Data preview

--------------------------------------
Recorded prompts are included in `prompts.txt`.

--------------------------------------
