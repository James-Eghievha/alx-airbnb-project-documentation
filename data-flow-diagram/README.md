# Data Flow Diagram - Airbnb Clone

## Overview
This directory contains the Data Flow Diagram (DFD) for the Airbnb Clone project, illustrating how data moves through the system during key operations.

## Purpose
The DFD serves to:
- Visualize data movement between external entities, processes, and data stores
- Identify all inputs and outputs for each backend process
- Ensure complete data handling coverage for all user interactions
- Guide API endpoint design and database query optimization

## DFD Levels Included

### Context Level (Level 0)
Shows the entire system as a single process with external entities

### Level 1 DFD  
Breaks down core processes:
- User Registration & Authentication
- Property Management 
- Booking Management
- Payment Processing
- Review Management
- Communication Management

## Key Components

### External Entities
- **Guest** - Users who search and book properties
- **Host** - Users who list and manage properties  
- **Admin** - System administrators
- **Payment Gateway** - External payment processor (Stripe/PayPal)
- **Email Service** - External notification service

### Core Processes
1. **Authenticate User** - Handles login/logout operations
2. **Register User** - Processes new account creation
3. **Manage Properties** - Handles property CRUD operations
4. **Process Bookings** - Manages reservation lifecycle
5. **Handle Payments** - Processes payment transactions
6. **Manage Reviews** - Handles review creation and display
7. **Handle Communication** - Manages user messaging

### Data Stores
- **D1: Users** - User account information
- **D2: Properties** - Property listing details
- **D3: Bookings** - Reservation records
- **D4: Payments** - Payment transaction data
- **D5: Reviews** - User reviews and ratings
- **D6: Messages** - Communication records

## Data Flow Analysis

### Guest Booking Journey
1. Guest submits search criteria → Search Process
2. Search Process queries Properties database → Returns filtered results
3. Guest selects property → Booking Process validates availability
4. Booking Process creates reservation → Stores in Bookings database
5. Payment Process charges guest → Records in Payments database
6. Email Service sends confirmation → Guest receives notification

### Host Property Management
1. Host submits property details → Property Management Process
2. Process validates and stores → Properties database
3. Booking requests arrive → Host receives notifications
4. Host confirms/rejects → Updates Booking database
5. Payment processed → Host earnings recorded

## Nigerian Context Integration
The DFD incorporates Nigerian market considerations:
- Multi-currency payment processing (Naira, USD)
- Integration with local payment methods
- Regional property categorization
- Cultural preference handling in search algorithms

## Files
- `data-flow.png` - Complete Level 1 DFD diagram
- `README.md` - This documentation file

## Business Impact
This DFD ensures our Airbnb clone handles:
- Scalable data processing for Nigeria's growing tech market
- Secure payment flows meeting local banking regulations
- Efficient property search across diverse Nigerian locations
- Robust communication supporting multilingual interactions

---
*Created as part of ALX Backend Development Program*
*Author: James Eghievha*
*Date: 02 September 2025*
