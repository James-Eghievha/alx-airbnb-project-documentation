# Use Case Diagram - Airbnb Clone Backend

## Overview
This document presents the use case diagram for the Airbnb Clone backend system, illustrating the interactions between different actors and the system's core functionalities.

## Purpose
The use case diagram serves to:
- Identify all system actors and their roles
- Map out key functionalities accessible to each actor
- Visualize system boundaries and interactions
- Provide a foundation for detailed system requirements

## Actors Definition

### Primary Actors
**Guest**
- Role: End-user seeking accommodation
- Goal: Find and book suitable properties
- Key Interactions: Search, book, pay, review properties

**Host**
- Role: Property owner/manager listing accommodations
- Goal: List properties and manage bookings
- Key Interactions: Create listings, manage availability, receive payments

**Admin**
- Role: Platform administrator
- Goal: Maintain platform integrity and user satisfaction
- Key Interactions: User management, content moderation, system monitoring

### Secondary Actors
**Payment Gateway**
- Role: External payment processing system
- Interaction: Process payments and refunds

**Email Service**
- Role: External email notification service
- Interaction: Send confirmation emails and notifications

**SMS Service**
- Role: External SMS notification service
- Interaction: Send text message notifications

## Use Cases by Actor

### Guest Use Cases
1. **Register Account** - Create new guest account
2. **Login** - Access existing account
3. **Search Properties** - Find accommodations by criteria
4. **Filter Search Results** - Refine search by amenities, price, location
5. **View Property Details** - See comprehensive property information
6. **Check Availability** - Verify dates and guest capacity
7. **Book Property** - Make reservation for selected dates
8. **Make Payment** - Pay for confirmed booking
9. **Cancel Booking** - Cancel reservation within policy
10. **Leave Review** - Rate and review stayed properties
11. **Send Messages** - Communicate with hosts
12. **Manage Profile** - Update personal information
13. **View Booking History** - See past and upcoming bookings

### Host Use Cases
1. **Register as Host** - Create host account with verification
2. **Login** - Access host dashboard
3. **Create Property Listing** - Add new property to platform
4. **Upload Photos** - Add property images and virtual tours
5. **Set Pricing** - Define rates and pricing strategies
6. **Manage Availability** - Update calendar and blocked dates
7. **Review Booking Requests** - Accept or decline reservations
8. **Communicate with Guests** - Send messages to potential/confirmed guests
9. **Update Property Details** - Modify listing information
10. **View Earnings** - Monitor income and payout schedules
11. **Respond to Reviews** - Reply to guest feedback
12. **Generate Reports** - Access booking and performance analytics

### Admin Use Cases
1. **Admin Login** - Access administrative dashboard
2. **Manage Users** - Oversee guest and host accounts
3. **Verify Host Identity** - Approve host registration and documentation
4. **Monitor Listings** - Review and moderate property listings
5. **Handle Disputes** - Resolve conflicts between users
6. **Process Refunds** - Manage payment disputes and refunds
7. **Generate System Reports** - Create platform analytics and insights
8. **Manage Platform Settings** - Configure system parameters
9. **Content Moderation** - Review and moderate user-generated content
10. **Security Monitoring** - Oversee platform security and fraud detection

## System Interactions

### Guest-System Interactions
- Guest initiates property search → System returns filtered results
- Guest makes booking request → System validates availability and processes
- Guest makes payment → System coordinates with Payment Gateway
- Guest receives confirmation → System triggers Email/SMS services

### Host-System Interactions
- Host creates listing → System validates and publishes property
- Host receives booking notification → System alerts via Email/SMS
- Host manages calendar → System updates availability in real-time
- Host receives payment → System coordinates payout via Payment Gateway

### Admin-System Interactions
- Admin monitors platform → System provides real-time analytics
- Admin moderates content → System flags and manages reported content
- Admin handles disputes → System provides tools and data for resolution

## System Boundaries
The Airbnb Clone system encompasses:

**Internal Functions:**
- User authentication and authorization
- Property listing management
- Booking and reservation processing
- Review and rating system
- Internal messaging system
- Admin dashboard and tools

**External Integrations:**
- Payment processing (Stripe, PayPal)
- Email notifications (SendGrid, Mailgun)
- SMS services (Twilio)
- File storage (AWS S3, Cloudinary)
- Maps and location services

## Business Rules Captured
1. Only verified hosts can create property listings
2. Guests must be logged in to make bookings
3. Payments are processed only after booking confirmation
4. Reviews can only be left by guests who completed their stay
5. Admins have override capabilities for dispute resolution
6. All financial transactions require external gateway validation

## Future Considerations
- Integration with calendar applications (Google Calendar, Outlook)
- Mobile app-specific use cases
- Advanced analytics and machine learning features
- Multi-language and localization support
- Advanced host tools and automation features
