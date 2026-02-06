# PROJET TD-LOG — Event Management Application with QR Codes

## Overview

**PROJET TD-LOG** is a full-stack event management application designed for student associations.  
It provides secure participant management, QR code–based ticketing, and real-time access control via a mobile scanning interface.

**Tech stack**
- Frontend: Ionic, React, TypeScript  
- Backend: FastAPI (Python)

## Features

### User Management
- Creation and administration of users by authorized accounts
- Autocomplete-based search to quickly find participants

### Event Management
- Event creation via a back-office interface
- Assignment of participants to events
- Generation of a unique QR code per ticket

### QR Code Scanning
- Live QR code scanning from the Ionic mobile application
- Backend validation: valid ticket, already scanned ticket, or invalid ticket
- Automatic marking of scanned tickets to prevent duplicates

## Project Structure

The project is split into two independent Git repositories:

PROJET-TDLOG-BACKEND/  
PROJET-TDLOG-FRONTEND/

The frontend requires the backend to be running in order to function.

## Prerequisites

Backend:
- Python 3.10+
- Install dependencies: pip install -r requirements.txt

Frontend:
- Node.js 18+
- Install dependencies: npm install

## Environment Variables

Create a .env file with the following variables:

SUPERADMIN_EMAIL=admin@tdlog.local  
SUPERADMIN_PASSWORD=changeme  
SUPERADMIN_NAME=Super Admin  
VITE_BACKEND_URL=http://localhost:8000

VITE_BACKEND_URL must point to the running backend instance.

## Running the Project

Backend:
uvicorn main:app --reload

Backend available at:
http://localhost:8000

Frontend:
npm run dev
