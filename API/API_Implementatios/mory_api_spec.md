# Memory Agent API Specification

This document serves as the official API specification for the Memory Agent. It defines the communication protocols, endpoints, and data formats for interaction with other agents and services within the system.

## Key Principles
* **Text-Based Communication:** The API operates on a text-in, text-out model. The Memory Agent is responsible for all internal logic, including embedding generation and vector search.
* **Single Source of Truth:** This API specification is the definitive contract for all communication with the Memory Agent.

## Base URL
* **Development:** `http://localhost:8000/api/memory`
* **Production:** `https://api.agentiiv.com/api/memory`

---

## Endpoints

### 1. Store Memory
This endpoint is used to ingest new memory items (e.g., grants, conversations, organizations) into the system.

**URL:** `POST /store`

**Input (Request Body):**
A JSON object containing the memory to be stored.

```json
{
  "type": "string",
  "unique_id": "string",
  "content": "string"
}
