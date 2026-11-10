# Database Schema

## Overview

The project uses an n8n Data Table named `support_tickets` to store customer support tickets and their AI-generated analysis.

## Table: support_tickets

| Column | Data Type | Description |
|---|---|---|
| id | Default ID | Unique record identifier |
| ticket_id | String | Customer support ticket ID |
| message | String | Original customer message |
| category | String | AI-generated ticket category |
| priority | String | Ticket urgency |
| sentiment | String | Customer sentiment |
| summary | String | Short issue summary |
| suggested_action | String | Recommended support action |
| created_at | String | Record creation timestamp |
| createdAt | Default timestamp | n8n creation timestamp |
| updatedAt | Default timestamp | n8n update timestamp |

## Data Flow

1. The webhook receives the ticket.
2. The AI Agent analyses the customer message.
3. The Structured Output Parser validates the expected output structure.
4. The Data Table Insert Row operation stores the original message and analysis.
5. The webhook returns the AI-generated result.

## Storage Technology

The project currently uses n8n Data Tables rather than an external relational database such as PostgreSQL or MySQL.

## Future Improvements

A production version could migrate to PostgreSQL to support advanced queries, indexing, relationships, and larger data volumes.
