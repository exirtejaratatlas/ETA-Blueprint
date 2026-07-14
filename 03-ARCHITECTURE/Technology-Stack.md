---
document_id: ETA-ARCH-013
title: Technology Stack
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# ETA Technology Stack

## Purpose

This document defines the official technology stack of the ETA Enterprise Procurement Ecosystem.

Every implementation, integration, AI service, and deployment must follow these technology standards unless an Architecture Decision Record (ADR) approves an exception.

---

# Architecture Philosophy

ETA follows:

- Cloud Native
- API First
- AI Native
- Container First
- Open Standards
- Enterprise Ready
- Vendor Independent
- Domain Driven Design
- Clean Architecture

---

# Frontend

Framework

- Next.js

Language

- TypeScript

UI

- React
- Tailwind CSS
- shadcn/ui

State Management

- TanStack Query

Forms

- React Hook Form
- Zod

Charts

- Recharts

Icons

- Lucide

---

# Backend

Framework

- FastAPI

Language

- Python 3.12+

Validation

- Pydantic

ORM

- SQLAlchemy

Database Migration

- Alembic

API Documentation

- OpenAPI 3.1
- Swagger
- ReDoc

---

# Databases

Operational Database

- PostgreSQL

Vector Database

- Qdrant

Cache

- Redis

---

# AI Platform

Supported Models

- OpenAI
- Anthropic Claude
- Google Gemini
- Ollama
- vLLM

AI Components

- Model Router
- Prompt Engine
- Agent Orchestrator
- RAG Engine
- Enterprise Memory

---

# Object Storage

Supported

- MinIO
- AWS S3
- Cloudflare R2

Stores

- Documents
- Images
- Drawings
- Videos
- Certificates

---

# Authentication

Preferred

- Keycloak

Protocols

- OAuth2
- OpenID Connect

Tokens

- JWT
- Refresh Token

Future

- Microsoft Entra ID
- LDAP
- Active Directory

---

# API Standards

Architecture

- REST

Specification

- OpenAPI 3.1

Data Format

- JSON

Versioning

- Semantic Versioning

---

# DevOps

Containers

- Docker
- Docker Compose

CI/CD

- GitHub Actions

Reverse Proxy

- Nginx

Future

- Kubernetes
- ArgoCD

---

# Monitoring

Metrics

- Prometheus

Dashboards

- Grafana

Logs

- Loki

Tracing

- OpenTelemetry

---

# Documentation

Primary Format

- Markdown

Architecture Diagrams

- Mermaid

Knowledge Base

- Obsidian

API Documentation

- OpenAPI

Decision Records

- ADR

---

# Design Tools

UI Design

- Figma

Marketing Design

- Canva

Architecture Diagrams

- Mermaid

---

# Development Tools

IDE

- Visual Studio Code

Source Control

- Git

Repository

- GitHub

Package Manager

- pnpm

Monorepo

- Turborepo

---

# Testing

Backend

- Pytest

Frontend

- Playwright

API

- Postman
- OpenAPI Validation

Future

- Contract Testing

---

# Security

Authentication

- OAuth2

Encryption

- TLS 1.3

Secrets

- Environment Variables
- Secret Manager

Scanning

- Dependency Scanning
- Container Scanning

---

# Future Technologies

Planned Evaluation

- Kubernetes
- Kafka
- GraphQL Gateway
- Service Mesh
- Event Streaming
- Feature Store
- Knowledge Graph

---

# Technology Selection Principles

Every technology must be:

- Enterprise Grade
- Well Supported
- Open Standard
- Secure
- Scalable
- Maintainable
- AI Compatible

Technology choices are reviewed through Architecture Decision Records (ADRs).

---

# Long-Term Vision

ETA maintains a modern, enterprise-grade technology stack that supports intelligent procurement, AI-native workflows, scalable cloud and on-premise deployments, and long-term maintainability while minimizing vendor lock-in.