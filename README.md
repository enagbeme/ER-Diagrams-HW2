# Database Design Assignment

## Overview
This repository contains the database design for three selected systems:

- **Library Management System**
- **Hotel Booking System**
- **Sports Tournament Management System**

The project includes ER diagrams, relational schemas, and design justifications for each system.

## What is This Project?
This project showcases the creation of database designs using Entity-Relationship (ER) diagrams and relational schemas for various systems. The goal is to create a well-structured, normalized database system that can efficiently handle different types of data for a given application.

## Motivation
The motivation behind this project was to practice and improve my database design skills by translating real-world systems into well-structured databases. I aimed to showcase my understanding of database concepts such as entities, relationships, normalization, and system requirements.

## Project Description
This project features:

- ER diagrams in Chen notation and Crow's Foot notation
- Relational schemas for each system
- Assumptions and design choices made during the modeling process

The systems chosen for this project:

- **Library Management System**: Manages books, members, and loans.
- **Hotel Booking System**: Manages guests, rooms, and reservations.
- **Sports Tournament Management System**: Manages teams, players, and matches.

## Table of Contents
- [Library Management System](#library-management-system)
- [Hotel Booking System](#hotel-booking-system)
- [Sports Tournament Management System](#sports-tournament-management-system)
- [ER Diagrams](#er-diagrams)
- [Relational Schemas](#relational-schemas)
- [Assumptions and Design Choices](#assumptions-and-design-choices)
- [Setup Instructions](#setup-instructions)
- [Credits](#credits)
- [License](#license)

## Library Management System
**Entities:**
- Book (book_id, title, author)
- Member (member_id, name, membership_date)
- Loan (loan_id, loan_date, return_date, member_id, book_id)

## Hotel Booking System
**Entities:**
- Guest (guest_id, name, contact_info)
- Room (room_id, room_type, price)
- Reservation (res_id, check_in, check_out, guest_id, room_id)

## Sports Tournament Management System
**Entities:**
- Team (team_id, name, coach)
- Player (player_id, name, team_id)
- Match (match_id, date, location, team1_id, team2_id, winner_id)

## ER Diagrams
- **Chen Notation**: Located in `chen_diagrams/`
- **Crow's Foot Notation**: Located in `crows_foot_diagrams/`

## Relational Schemas
The relational schemas for each system are provided in the respective sections above. These schemas ensure proper normalization and referential integrity.

## Assumptions and Design Choices
- **Weak Entities**: Loans in the Library System depend on Books and Members.
- **Composite Attributes**: Names are stored as first and last names separately.
- **Multivalued Attributes**: Books can have multiple authors.
- **Relationships**: One-to-many and many-to-many relationships are properly defined.

## Setup Instructions
Clone this repository:

```bash
git clone <repo-link>
git add .
git commit -m "Updated ER diagrams and schemas"
git push origin main



