# Demetra - Agricultural Platform

A comprehensive agricultural platform combining satellite data, weather analytics, and field management tools to help farmers make data-driven decisions.

## Overview

Demetra is a full-stack agricultural technology platform that provides:
- **Real-time weather data** and historical climate analysis
- **Field management** with geographic visualization
- **Satellite data integration** from climate data sources
- **User authentication** and multi-role support (farmers, agronomists)
- **Weather metrics** for crop planning and decision-making

## Architecture

The platform consists of three main components:

### Backend (Python/FastAPI)
- RESTful API built with FastAPI
- Integration with Copernicus Climate Data Store (CDS)
- Real-time and historical weather data services
- MongoDB for data persistence
- Endpoints for field management, weather metrics, and user authentication

### Frontend (React/TypeScript)
- Modern React application with TypeScript
- Interactive mapping and field visualization
- User dashboard for farmers and agronomists
- Responsive UI built with Tailwind CSS and shadcn/ui components

### Database
- MongoDB for storing user data, field information, and cached weather data
- Optimized for geospatial queries

## Tech Stack

**Backend:**
- Python 3
- FastAPI
- MongoDB
- Uvicorn

**Frontend:**
- React
- TypeScript
- Vite
- TanStack Query
- Tailwind CSS

**Infrastructure:**
- Docker & Docker Compose
- MongoDB


## API Endpoints

Key endpoints include:
- `POST /signup` - User registration
- `POST /login` - User authentication
- `POST /field-metrics` - Get current weather for a field
- `POST /field-metrics-historic` - Get historical weather data
- `POST /add_field` - Add a new field
- `POST /get_fields` - Retrieve user's fields
- `POST /delete_field` - Remove a field

Full API documentation is available at `/docs` when running the backend.

## Features

- **Field Management:** Create, view, and manage agricultural fields with geographic boundaries
- **Weather Analytics:** Real-time and historical weather data visualization
- **User Roles:** Support for farmers and agronomists with different access levels
- **Geospatial Queries:** Efficient location-based data retrieval
- **Responsive Design:** Works on desktop and mobile devices

## Project Structure

```
platform/
├── backend/                 # FastAPI backend
│   ├── sat_data/           # Satellite and climate data services
│   ├── live_data/          # Real-time weather services
│   ├── database/           # Database models and connections
│   └── main.py             # API entry point
├── demetra-front-end/      # React frontend
│   ├── client/src/         # Frontend source code
│   ├── server/             # Backend integration
│   └── shared/             # Shared schemas
└── docker-compose.yml      # Docker orchestration
```
