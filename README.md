# TalentFlow - Mini Hiring Platform

> A modern, full-featured hiring platform built with React, featuring job management, candidate tracking, and dynamic assessments—all running entirely in the browser with no backend required.

[![Live Demo](https://img.shields.io/badge/demo-live-success?style=for-the-badge)](https://jobs-board-m996.vercel.app)
[![React](https://img.shields.io/badge/React-18.2-blue?style=for-the-badge&logo=react)](https://reactjs.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-4.1-38bdf8?style=for-the-badge&logo=tailwind-css)](https://tailwindcss.com/)
[![Dexie.js](https://img.shields.io/badge/Dexie.js-4.0-orange?style=for-the-badge)](https://dexie.org/)

---

## Table of Contents

- [Features](#features)
- [Live Demo Screenshots](#live-demo-screenshots)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Architecture](#architecture)
- [Key Features Breakdown](#key-features-breakdown)
- [Technical Decisions](#technical-decisions)
- [Challenges & Solutions](#challenges--solutions)
- [Project Structure](#project-structure)
- [API Simulation](#api-simulation)
- [Testing](#testing)
- [Deployment](#deployment)
- [Future Enhancements](#future-enhancements)

---

## Features

### Core Functionality

**Jobs Management**
- Create, edit, and archive jobs with validation
- Server-side pagination (10 jobs per page)
- Real-time search by job title
- Filter by status (active/archived) and tags
- Drag-and-drop reordering with optimistic updates
- Deep linking support (`/jobs/:jobId`)

**Candidates System**
- Virtualized list rendering (1000+ candidates)
- Client-side search (name/email)
- Server-side filtering by stage
- Kanban board with drag-and-drop stage transitions
- Detailed candidate profiles with activity timeline
- Add notes with @mentions and markdown support

**Assessment Builder**
- Dynamic form builder per job
- 6 question types: single-choice, multi-choice, short text, long text, numeric, file upload
- Live preview pane showing candidate view
- Form validation (required fields, numeric ranges, max length)
- Conditional question logic
- Persistent storage (survives page refreshes)

**Data Management**
- Auto-seeding: 25 jobs, 1000 candidates, 5 assessments
- IndexedDB persistence via Dexie.js
- MirageJS for API simulation (200-1200ms latency)
- 5-10% artificial error rate for resilience testing
- Optimistic UI updates with rollback on failure

---

## Live Demo Screenshots

### 1. Jobs Board
![Jobs Board](attachments/Job-Board.png)

### 2. Candidates Kanban Board
![Candidates Kanban](attachments/Candidate-List.png)

### 3. Candidate Profile & Timeline
![Candidate Profile](attachments/Candidate-Profile.png)

### 4. Assessment Builder
![Assessment Builder](attachments/Assesment-Builder.png)

---

## Tech Stack

### Frontend
- React 18.2
- React Router 6
- Tailwind CSS 4.1
- @dnd-kit
- @tanstack/react-virtual

### State & Data
- Dexie.js 4.0
- MirageJS 0.1
- Faker.js 8.0

### Build Tools
- Vite 5.2
- PostCSS & Autoprefixer

### Deployment
- Vercel

---

## Getting Started

### Prerequisites
- npm 8+

### Installation

```bash
git clone https://github.com/yourusername/talentflow-mini.git
cd talentflow-mini
npm install
npm run dev
