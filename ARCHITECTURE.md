# Architecture Documentation: Health Habit Tracker

## Introduction
This document describes the architecture of Health Habit Tracker using the C4 model (Context, Container, Component, and Code diagrams). The system is designed as a scalable, cloud-native application that integrates with external fitness APIs to provide comprehensive nutrition and workout tracking.

---

## Domain
Health and Fitness Technology

The system supports individuals seeking to monitor and improve their health through structured fitness and nutrition planning.

## Problem Statement
Users require a centralized system to plan workouts, track meals, and monitor progress toward their health and fitness goals.

## Individual Scope

The system will consist of a web application, backend API services, and a database to store user data and activity logs.

## C4 Architecture
### Level 1 — System Context Diagram ###

Actors interacting with the system:
- User
- FitPlan System
- External Nutrition API (optional)
- Email Notification Service

### Level 2 — Container Diagram ###

Main containers inside the system:
- Web Application (Frontend)
- Backend API Server
- Database
- Notification Service

### Level 3 — Component Diagram (Backend) ###

Backend components:
API Server
│
- Authentication Service
- Workout Planner Service
- Nutrition Tracking Service
- Progress Analytics Service
- Notification Scheduler 
