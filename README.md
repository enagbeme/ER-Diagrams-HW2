# ER Diagrams Design Assignment

## Overview
This repository contains the database design for three selected systems:

- **Library Management System**
- **Hotel Booking System**
- **Sports Tournament Management System**

The project includes ER diagrams, relational schemas, and design justifications for each system.
s
## What is This Project?
This project showcases the creation of database designs using Entity-Relationship (ER) diagrams and relational schemas for various systems. The goal is to create a well-structured, normalized database system that can efficiently handle different types of data for a given application.

## Motivation
The motivation behind this project was to practice and improve my database design skills by translating real-world systems into well-structured databases aimed to showcase our understanding of database concepts such as entities, relationships, normalization, and system requirements.

## Project Description
This project features:

- ER diagrams in Chen notation and Crow's Foot notation
- Relational schemas for each system
- Assumptions and design choices made during the modeling process

The systems chosen for this project:

- **Real Estate Listing System**: Manages properties, clients, and agents.
- **Hotel Booking System**: Manages guests, rooms, and reservations.
- **Sports Tournament Management System**: Manages teams, players, and matches.

## Table of Contents
- [Real Estate Listing System](#real-estate-listing-system)
- [Hotel Booking System](#hotel-booking-system)
- [Sports Tournament Management System](#sports-tournament-management-system)
- [ER Diagrams](#er-diagrams)
- [Relational Schemas](#relational-schemas)
- [Assumptions and Design Choices](#assumptions-and-design-choices)
- [Setup Instructions](#setup-instructions)
- [Credits](#credits)
- [License](#license)

## Real Estate Listing System
**Entities:**

- **Property** (PropertyID(PK), Address, ListingPrice, Bedrooms, Bathrooms, YearBuilt, AgentID(FK), IsAvailable)
- **Agent** (AgentID(PK), Name, ContactInfo, IsActive, HireDate, OfficeLocation)
- **Client** (ClientID(PK), Name, ContactInfo, Budget, PreferredLocation, Status)
- **PropertyClient** (PropertyClientID(PK), PropertyID(FK), ClientID(FK), InterestLevel, DateInterested, ActionTaken)

## Hotel Booking System
**Entities:**

- **Room** (RoomNumber(PK), RoomType, Rate, IsAvailable, Floor, MaxOccupancy)
- **Guest** (GuestID(PK), Name, ContactInfo, IsActive, Nationality, DateOfBirth)
- **Booking** (BookingID(PK), CheckInDate, CheckOutDate, GuestID(FK), RoomNumber(FK))

## Sports Tournament Management System
**Entities:**

- **Team** (TeamID(PK), Name, CoachID(FK), HomeCity, LogURL)
- **Player** (PlayerID(PK), Name, TeamID(FK), Position, Nationality, DateOfBirth)
- **Match** (MatchID(PK), Date, Location, Team1ID(FK), Team2ID(FK), WinnerID,RefereeID(FK))
- **Coach** (CoachID(PK), Name, CertificationLevel, Country, ExperienceYears)
- **Referee** (RefereeID(PK), Name, Country, CertificationLevel, ExperienceYears,MatchesOfficiated)

## ER Diagrams
The ER diagrams include:
- **Chen Notation** 
- **Crow's Foot Notation**
- The diagrams are available in **report.html** / **report.pdf** files

## Relational Schemas
The relational schemas for each system are provided in the respective sections above. These schemas ensure proper normalization and referential integrity.

## Assumptions and Design Choices
- **Weak Entities**: The PropertyClient entity is a weak entity as it relies on both Property and Client for its existence also The MatchTeam entity is a weak entity as it relies on both Match and Team for its existence.
- **Composite Attributes**: Names are kept simple; first and last names are stored as a single attribute.
- **Multivalued Attributes**: No multivalues attributes 
- **Relationships**: One-to-many and many-to-many relationships are properly defined.

## Setup Instructions
Clone this repository:

```bash
git clone <repo-link>
git add .
git commit -m "Updated ER diagrams and schemas report"
git push origin main



