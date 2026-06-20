# Nexus AI - Customer Support Platform

Nexus AI is a full-stack AI-powered customer support platform that combines conversational AI, ticket management, order tracking, and human support workflows into a single application.

The platform enables customers to interact with an AI support agent capable of answering questions using FAQs, order information, and tracking data. When issues cannot be resolved automatically, the AI can escalate them into support tickets and assign them to human agents.

---

## Features

### Customer Features

* AI-powered customer support chat
* Order lookup and tracking updates
* FAQ-based question answering
* Ticket creation and escalation
* Ticket conversation history
* User profile management

### Support Agent Features

* View and manage assigned tickets
* Chat directly with customers
* Update ticket status and priority
* Generate AI-assisted responses
* Track ongoing conversations

### Admin Features

* FAQ management
* Order management
* Tracking update management
* Support agent account management

---

## AI Workflow

1. Customer sends a message to the AI agent.
2. AI determines the user's intent.
3. AI calls available tools such as:

   * FAQ retrieval
   * Order lookup
   * Tracking lookup
4. If the issue is resolved, the response is returned immediately.
5. If escalation is required:

   * AI creates a ticket
   * AI assigns category and priority
   * System automatically assigns the ticket to the support agent with the lowest workload
6. Customer and support agent communicate through the ticket.
7. Agent updates ticket status until resolution.
8. Once resolved, the ticket is closed and conversation is locked.

---

## System Architecture

### Frontend

* React
* TypeScript
* Tailwind CSS
* React Router
* Vite

### Backend

* FastAPI
* SQLModel / SQLAlchemy
* PostgreSQL
* Alembic
* JWT Authentication

### AI Layer

* Google Gemini
* Function Calling
* Tool-based Agent Workflow

---

## Technology Stack

| Layer          | Technologies                          |
| -------------- | ------------------------------------- |
| Frontend       | React, TypeScript, Tailwind CSS, Vite |
| Backend        | FastAPI, Python, SQLModel, SQLAlchemy |
| Database       | PostgreSQL                            |
| Authentication | JWT + Secure Cookies                  |
| AI             | Google Gemini                         |
| Migrations     | Alembic                               |

---

## Project Structure

```text
customer-support-agent/
│
├── frontend/
│   ├── src/
│   ├── components/
│   ├── pages/
│   ├── hooks/
│   └── utils/
│
├── backend/
│   ├── app/
│   │   ├── api/
│   │   ├── models/
│   │   ├── schemas/
│   │   ├── services/
│   │   └── utils/
│   ├── alembic/
│   └── main.py
│
└── README.md
```

---

## Core API Modules

### Authentication

* User signup/login
* Support agent signup/login
* Session management
* Profile updates

### Chat

* AI customer chat
* Chat history retrieval
* Message redaction

### Tickets

* Ticket creation
* Ticket assignment
* Ticket updates
* AI response generation

### Orders & Tracking

* Order management
* Shipment tracking
* Tracking updates

### FAQ

* FAQ storage and retrieval

---

## Local Development

### Backend

```bash
cd backend

python -m venv venv

# Windows
venv\Scripts\activate

# Linux/macOS
source venv/bin/activate

pip install -r requirements.txt

alembic upgrade head

uvicorn main:app --reload
```

Backend runs on:

```text
http://localhost:8000
```

API Documentation:

```text
http://localhost:8000/docs
```

---

### Frontend

```bash
cd frontend

npm install

npm run dev
```

Frontend runs on:

```text
http://localhost:5173
```

---

## Environment Variables

### Backend

```env
ASYNC_DB_URL=
SECRET_KEY=
ALGORITHM=HS256

ACCESS_TOKEN_EXPIRE_MINUTES=30
REFRESH_TOKEN_EXPIRE_DAYS=7

GEMINI_API_KEY=

FRONTEND_URL=http://localhost:5173
```

---

## Security Features

* JWT Authentication
* Cookie-based Sessions
* Password Verification
* CORS Protection
* Role-Based Access Control
* Secure Environment Variable Management

---

## Future Improvements

* Real-time WebSocket chat
* Ticket analytics dashboard
* Multi-language support
* Knowledge base management
* Automated sentiment analysis
* SLA monitoring
* Agent performance metrics

---

## License

This project was developed as part of the Nexus AI Customer Support Platform.
