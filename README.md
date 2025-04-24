# Event Management System in c++

## Overview
Event Management System is a console-based C++ application that allows users to create, manage, and participate in events. The system features user authentication, event creation with date/time validation, RSVPs, public and private events, and efficient date-based searches.

## Features
- **User Management**
  - Registration with unique usernames
  - Secure password input (masked during entry)
  - Session management with login/logout

- **Event Creation and Management**
  - Create events with titles, descriptions, and dates
  - Public and private event visibility options
  - Date and time validation
  - RSVP functionality

- **Searching and Browsing**
  - Search events by keywords in title or description
  - View upcoming events within a specified time range
  - Personal event dashboard for created and attended events

- **User Interface**
  - Clean, formatted console interface with tables and menus
  - Interactive navigation between views
  - Visual feedback for success/failure operations

## Technical Implementation
- Binary Search Tree (BST) for efficient date-based event retrieval
- Hash maps for O(1) lookups of users and events by ID
- Custom DateTime class with validation and comparison operators
- Object-oriented design with separation of concerns

## Getting Started

### Prerequisites
- C++ compiler with C++11 support
- POSIX-compatible terminal (for password masking)

### Compilation
```bash
g++ -std=c++11 event_manager.cpp -o event_manager
```

### Running the Application
```bash
./event_manager
```

## Usage Guide

### Main Menu
The application presents different options based on your login status:

**When not logged in:**
- Login
- Register
- Search Events
- View Upcoming Events
- Exit

**When logged in:**
- Logout
- Create New Event
- RSVP to Event
- View My Events
- Search Events
- View Upcoming Events
- Exit

### Creating an Event
1. Log in to your account
2. Select "Create New Event"
3. Enter event details:
   - Title
   - Date and time (format: YYYY-MM-DD HH:MM)
   - Public/Private setting
   - Description

### Searching for Events
1. Select "Search Events"
2. Enter search keywords (or leave empty to view all accessible events)
3. Select an event from results to view details

### RSVPing to Events
1. Log in to your account
2. Select "RSVP to Event"
3. Enter the event ID number

## Data Structures

### Binary Search Tree (BST)
- Used for organizing events by date/time
- Enables efficient range queries for upcoming events
- Each node can contain multiple events at the same time point

### Hash Maps
- Fast lookup for users by username
- Fast lookup for events by ID

## Security Considerations
- Password masking during input
- Access control for private events
- Input validation for dates and other fields

## Future Improvements
- Self-balancing BST implementation (AVL or Red-Black tree)
- Password hashing for enhanced security
- Event modification and deletion capabilities
- Recurring events
- Calendar view for upcoming events
- User profiles with additional information
- Event categories and tags

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
