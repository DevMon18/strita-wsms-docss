---
{"dg-publish":true,"permalink":"/st-rita-mission-station-wsms/","tags":["gardenEntry"]}
---

# St. Rita Mission Station - Wedding Schedule Management System (WSMS)


#### Source code: https://drive.google.com/file/d/109_9Phq-QmK48abxwaTgJzCFmxl1NuVC/view?usp=sharing

![Pasted image 20241217221356.png](/img/user/Pasted%20image%2020241217221356.png)

  

## System Overview

The *St. Rita Mission Station - Church Wedding Hall Schedule System* is a web-based platform designed to streamline the scheduling and management of church weddings.

  
### **Objective**:

- Simplify the booking process for clients.
- Provide a centralized system for administrators to manage schedules and validate wedding requirements.

  

  

### **Core Features**:

- Clients can register, log in, and submit detailed wedding forms.
- Calendar integration ensures conflict-free wedding scheduling.
- Admin can approve bookings, verify uploaded documents, and manage wedding schedules.

### **Workflow**:

1. **Step 1**: Client submits the wedding application, selects a date, and uploads required documents.
2. **Step 2**: Admin reviews the application, checks date availability, and validates documents.
3. **Step 3**: Approval status is updated, and the client receives a confirmation email along with a waiver.
### **Technology Stack**:  
- **Frontend**: JavaScript (FullCalendar.js, Parsley.js, Dropzone.js, SweetAlert2, jQuery AJAX).
- **Backend**: PHP and MySQL for processing and storing data.
### **Expected Outcomes**:
- A user-friendly platform for clients to book wedding schedules efficiently.
- A reliable backend for the admin to manage bookings, calendars, and document verification.

## Key Components

### **Frontend Components**
1. **Calendar Component**: FullCalendar.js for selecting and displaying unavailable wedding dates.
2. **Form Validation**: Parsley.js to ensure required fields and file uploads are validated on the client side.
3. **File Upload Component**: Dropzone.js for user-friendly drag-and-drop document uploads.
4. **Notifications/Alerts**: SweetAlert2 for displaying success, error, and confirmation messages.
5. **Dynamic Data Loading**: jQuery AJAX to load content dynamically without reloading the page.
### **Backend Components**

1. **Programming Language**: PHP
2. **Database**: MySQL (for managing user details, bookings, and uploaded files)
3. **Authentication**: PHP sessions or JSON Web Tokens (JWT) for secure user and admin login.
4. **File Storage**: Local storage on the server (organized by user IDs) or cloud storage (e.g., AWS S3 or Google Drive API).

### **System Components Overview**:

1. **Landing Page**: Overview of services, login, and registration buttons for clients and admin.
2. **Client Dashboard**: Form submission for bride/groom details, file uploads, calendar for selecting wedding dates, and booking status updates.
3. **Admin Dashboard**: Admin controls for reviewing and managing bookings, verifying documents, and updating status.
4. **Calendar Management**: Dynamic calendar with availability and non-availability indicators.
5. **File Management**: System for uploading, validating, and organizing wedding-related documents.
6. **Notifications**: Email notifications to clients when their booking is approved.


### **Email Notification**:

After the admin approves the booking, the system sends an email notification to the client, confirming the booking and providing the waiver link.

## Frameworks and Libraries

1. **Frontend**:
   - FullCalendar.js (for date selection)
   - Parsley.js (for form validation)
   - Dropzone.js (for file uploads)
   - SweetAlert2 (for notifications)
   - jQuery AJAX (for dynamic content loading)


2. **Backend**:
   - PHP (for backend logic)
   - MySQL (for database management)

3. **Email Notification**:

   - PHPMailer (for sending email notifications)
## I. User Interface Enhancements

### 1. Main Navigation Bar:
- **About Us**: Add a section with detailed information about St. Rita Mission Station's history, mission, and vision.
- **Services**: Include a list of services like baptisms, community events, etc.
- **Visual Design**: Use wedding-themed colors and fonts, with elegant icons and clear navigation.

### 2. Hero Section :
- Add a carousel of beautiful wedding photos.
- **Call-to-Action Button**: "Book Your Wedding Now" — This button will scroll smoothly to the login/register section or the booking form if the user is logged in.

### 3. Login & Register (Aside Section):
- **Social Media Login**: Provide Google and Facebook login options to simplify the registration and login process.

### 4. Contact Us Page:
- **Google Map Integration**: Pinpoint the church's exact location for easy directions.
- **Feedback Form**: Allow users to submit comments or inquiries.
- **Accessibility Features**:
  - Dark Mode Toggle for improved usability.
  - Screen reader support to ensure accessibility for visually impaired users.

## II. Client Side - UI Enhancements

### 1. Forms:
- **Auto-Save Draft**: Allow users to save their progress while filling out forms and return to it later.
- **Real-Time Form Validation**: Immediate feedback if required fields are missing or incorrect.

### 2. Wedding Calendar Integration:
- Use a calendar plugin (FullCalendar) to display available and reserved wedding dates.
- **Highlight Peak Seasons**: Show holidays or busy wedding dates in distinct colors.
- **Blocked Dates**: Display dates blocked for church maintenance or events.

### 3. Booking Status Dashboard:
- **Progress Tracker**: Show the booking status as "Pending → Approved → Completed."
- **Download Waiver**: Allow clients to download a PDF waiver once their booking is approved.
- **Notifications**: Send alerts (SMS/Email) on booking status updates.

## III. Admin Side - UI Enhancements

### 1. Dashboard:
- **Key Metrics**: Display:
  - Total bookings
  - Pending requests
  - Upcoming weddings
- **Calendar View**: Integrate FullCalendar to display all wedding bookings.
- **Tasks Section**: A list of pending tasks (e.g., pending approval requests).

### 2. Client Management:
- **Search & Filter**: Allow admins to search clients by name, status, or date.
- **Edit Booking Details**: Enable admins to modify booking details upon client request.

### 3. Reports & Analytics:
- **Charts and Data Export**: Use libraries like Chart.js to display wedding statistics (e.g., number of weddings by month) and allow data export to CSV/PDF for reporting purposes.

### 4. Admin Profile Settings:
- Admins can update their profile information, change passwords, and upload a profile picture.

## IV. System-Wide Features

### 1. Logging & Monitoring:
- **Audit Log**: Track all actions taken by admins, including booking edits, status changes, and settings modifications.

### 2. Backup System:
- **Database Backups**: Automated daily/weekly backups of the database to prevent data loss.

### 3. Enhanced Security:
- **Two-Factor Authentication (2FA)**: Add 2FA for admins to improve login security.
- **Input Validation**: Validate inputs both on the client-side (JavaScript) and server-side (PHP).

### 4. Localization (Optional):
- **Language Support**: Add support for multiple languages (e.g., English, Filipino) based on user preference.

## V. Features for Clients After Login

### 1. Client Dashboard:
- **Welcome Message**: Display the client's name (e.g., "Welcome, [Client Name]").
- **Booking Status Card**: Show the booking status: Pending, Approved, Completed.
- **Booking Form**: A multi-step form:
  - Step 1: Bride details
  - Step 2: Groom details
  - Step 3: Document upload
  - Step 4: Wedding date selection

### 2. Notifications:
- **Booking Updates**: Clients receive notifications (via email and/or SMS) when their booking status changes.

## VI. Database Structure

### 1. Admins Table (For Super Admin and Sub Admins):
- **superadmin**: Username: `admin`, Password: `admin` (no hashing)
- **subadmin**: Limited access (view, manage bookings, and settings only).
- **Tables**:
  - `admins` (superadmin, subadmin)
  - `users` (clients)
  - `bookings`
  - `services`

**Example Structure**:

```sql
CREATE TABLE admins (
    admin_id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL,
    role ENUM('superadmin', 'subadmin') DEFAULT 'subadmin',
    full_name VARCHAR(100),
    email VARCHAR(100) NOT NULL UNIQUE,
    profile_picture VARCHAR(255) DEFAULT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

CREATE TABLE users (
    user_id INT AUTO_INCREMENT PRIMARY KEY,
    full_name VARCHAR(100),
    email VARCHAR(100) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL,
    phone VARCHAR(15),
    wedding_date DATE,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

CREATE TABLE bookings (
    booking_id INT AUTO_INCREMENT PRIMARY KEY,
    user_id INT,
    status ENUM('Pending', 'Approved', 'Completed') DEFAULT 'Pending',
    date DATE,
    documents JSON,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (user_id) REFERENCES users(user_id)
);

CREATE TABLE services (
    service_id INT AUTO_INCREMENT PRIMARY KEY,
    service_name VARCHAR(100),
    description TEXT,
    price DECIMAL(10, 2)
);
```

## VII. Additional Navigation Features

### 1. Announcements Section:
- Admin can post updates about church events, holidays, etc.

### 2. FAQ Section:
- A list of common queries about the wedding process, requirements, and packages.

### 3. Testimonials Section:
- Display reviews or testimonials from couples who've used the service.

### 4. Help & Support:
- A dedicated page for user support, FAQs, and contact details.

## VIII. Task Management for Admin

### 1. Task Reminders:
- Admins will receive reminders for tasks such as:
  - Pending approval
  - Upcoming weddings
  - Follow-up emails

### 2. Manage Wedding Packages:
- Admins can manage the different wedding packages offered by the church.

### 3. Custom Notifications:
- Admins can set custom notification messages for different booking statuses.

## IX. Implementation Plan

### Frontend:
- **HTML/CSS/Bootstrap**:
  - Use Bootstrap's grid system for responsiveness.
  - Implement custom CSS for unique wedding-themed designs (soft colors, elegant typography).
  - JavaScript Libraries for enhanced functionality like FullCalendar (for date selection), SweetAlert (for confirmation popups), and PHPMailer (for email notifications).
  - Implement **responsive design** to ensure compatibility across mobile and desktop devices.

### Backend:
- **PHP (Server-Side Logic)**:
  - Handle authentication, form submissions, and user requests.
  - Ensure secure login using email/password, as well as social media logins (Google/Facebook).
  - Use **bcrypt** for password hashing when adding users, but for admin (superadmin/subadmin), you may skip hashing as per your requirement.



  

- **/assets**: Contains static assets like CSS, JavaScript, and images.

  

- **/includes**: Includes configuration and helper files like database connection and email logic.

  

- **/views**: Contains the PHP files for different views (landing page, dashboards, forms).

  

- **/uploads**: Stores uploaded documents and waivers.

  

- **index.php**: Main entry point for the application.

  

  

---

  

## Conclusion

This system is designed to manage wedding hall bookings effectively while offering a seamless user experience for both clients and administrators. With dynamic calendar features, easy document uploads, and email notifications, this platform ensures an efficient booking process for church weddings.


-----
