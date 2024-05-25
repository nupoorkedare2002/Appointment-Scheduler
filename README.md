
# Appointment Scheduler for Career and Soft Skills Counseling

## Project Overview
This project focuses on developing the frontend of an Appointment Scheduler designed for students seeking career counseling, soft skills improvement (such as communication or grooming), and mental health support. The system facilitates booking sessions, managing schedules, and providing a user-friendly interface for both students and counselors.

### Key Objectives:
- Enable students to book sessions for career counseling, soft skills improvement, and mental health support.
- Provide a user-friendly dashboard for students to manage their appointments and profiles.
- Ensure timely notifications and confirmations through emails or in-app notifications.

## Features
- **User Registration and Login**: Secure user registration and authentication.
- **Dashboard**: A central hub for managing appointments, viewing upcoming sessions, and accessing profile settings.
- **Appointment Scheduling**: Easy booking process with real-time availability checks.
- **Notifications**: Automated email or in-app notifications for appointment confirmations and reminders.
- **Profile Management**: Users can update their personal information and manage their account settings.

## User Registration and Login Flow
1. User navigates to the registration page.
2. User fills in registration details (name, email, password, etc.).
3. System validates the information and creates a new user account.
4. Upon successful registration, user is redirected to the login page.
5. User logs in with their credentials.
6. System verifies the credentials and grants access to the dashboard.

## Dashboard Navigation
1. Upon logging in, user is presented with the dashboard.
2. User can see available options such as scheduling an appointment, viewing upcoming appointments, managing profile, etc.
3. User selects "Schedule Appointment" option.

## Appointment Scheduling Flow
1. User is directed to the appointment scheduling page.
2. User selects the type of counseling session (career, soft skills, or mental health).
3. User views available time slots based on counselor availability.
4. User selects a preferred time slot.
5. System prompts user to confirm the appointment.
6. User confirms the appointment.
7. System sends confirmation email or notification to user and counselor.

## Viewing Upcoming Appointments
1. User navigates to the "Upcoming Appointments" section in the dashboard.
2. User sees a list of their upcoming appointments.
3. User has the option to cancel or reschedule appointments if needed.

## Profile Management
1. User navigates to the "Profile" section in the dashboard.
2. User can update personal information, change password, etc.
3. User saves changes, and system updates the user profile accordingly.

## Logging Out
1. User clicks on the logout button in the dashboard.
2. System logs out the user and redirects to the login page.

## Data Models

### User Table
| Column Name | Data Type | Description |
| ----------- | --------- | ----------- |
| UserID      | INT       | Primary Key, Auto-increment |
| Username    | VARCHAR   | Username of the user |
| Email       | VARCHAR   | Email address of the user |
| Password    | VARCHAR   | Encrypted password |
| UserType    | ENUM      | Type of user (student, counselor, administrator, etc.) |

### Appointment Table
| Column Name       | Data Type | Description |
| ----------------- | --------- | ----------- |
| AppointmentID     | INT       | Primary Key, Auto-increment |
| UserID            | INT       | Foreign Key referencing User.UserID |
| CounselorID       | INT       | Foreign Key referencing Counselor.CounselorID |
| AppointmentDate   | DATE      | Date of the appointment |
| StartTime         | TIME      | Start time of the appointment |
| EndTime           | TIME      | End time of the appointment |
| AppointmentType   | ENUM      | Type of appointment (career counseling, soft skills improvement, mental health, etc.) |
| Status            | ENUM      | Status of the appointment (pending, confirmed, canceled, etc.) |

### Counselor Table
| Column Name | Data Type | Description |
| ----------- | --------- | ----------- |
| CounselorID | INT       | Primary Key, Auto-increment |
| Name        | VARCHAR   | Name of the counselor |
| Email       | VARCHAR   | Email address of the counselor |
| Specialization | VARCHAR | Area of specialization (career counseling, soft skills improvement, mental health, etc.) |

## Technologies Used
- Frontend: React.js , GSAP , Framer Motion , Figma
- CSS Framework: Bootstrap

## Installation and Setup
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/appointment-scheduler.git
