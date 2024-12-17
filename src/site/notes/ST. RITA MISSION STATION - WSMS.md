---
{"dg-publish":true,"permalink":"/st-rita-mission-station-wsms/","tags":["gardenEntry"]}
---





## Landing Page - User Interface

	Nav
		- Home
			(When clicking the home navigation it will go back to the top part of the index (has smooth scrolling))
		- Gallery
			(When clicking the gallery navigation it will go to the gallery section below using smooth scrolling in index)
		- Contact Us
			(When clicking the Contact Us navigation it will go to the bottom part (before footer) has smooth scrolling)
	
	Section
		- Image Slide (Carousel)
			- Description About St. Rita Mission Station
	Aside
		Login 
			Email Address:
			Password:
			- Below Register
				- Register Form
					- First Name
					- Last Name
					- Password
					- Confirm Password
					- Email Address
					- Contact Number
			- Forgot Password?
				- Email Address
		
	Article
		  - lorem ipsum

### Footer
	- Lorem ipsum
## Client Side - UI (after logging in from Landing Page)

### Container
Fill-out Forms
	- Forms
		Inside the forms:
			- Name of the Bride ***Required**
					- Date of Birth
					- Birthplace
					- Mother's maiden name
					- Father's name
				Files to be uploaded: ***Required**
					- Baptismal Certificate
					- Confirmation Certificate
					- Permit to Marry
						If there is any: **Optional**
						(Files to be uploaded)
						- Marriage License if Civilly Married
						- Death Certificate - if Widowed (deceased spouse)
					Checkboxes **Required**
						- Already Interviewed for PRE-NUPTIAL or CANONICAL INTERVIEWER (Yes or No)
						- Has Seminar for PRE-CANA (Yes or No)
			- Name of the Groom
					- Date of Birth
					- Birthplace
					- Mother's maiden name
					- Father's name
				Files to be uploaded: ***Required**
					- Baptismal Certificate
					- Confirmation Certificate
					- Permit to Marry
						If there is any: **Optional**
						(Files to be uploaded)
						- Marriage License if Civilly Married
						- Death Certificate - if Widowed (deceased spouse)
					Checkboxes **Required**
						- Already Interviewed for PRE-NUPTIAL or CANONICAL INTERVER (Yes or No)
						- Has Seminar for PRE-CANA (Yes or No) 
				Below of the 2 forms there will be a calendar which the user can pick the date of their desired wedding date. If there is already taken dates by other user the date of calendar has description that indicates (Already Reserved)
	Buttons: Confirm & Cancel

*After confirming - There will be a pending status in the user dashboard that says
- Your booking is **pending** please wait for confirmation in less than 5 - 7 days.
- if the staff/admin approve its booking the pending status will be changed into APPROVED please check your email to get the view the waiver.
## Admin Side - UI
(Don't use hashing for Superadmin account = username: Admin password:Admin)

## Sidebar Dashboard - UI with hamburger icon
 - Profile Picture (rounded)
 - Name of the Administrator
 - Clients (Can manage clients CRUD)
	 - (When clicking the clients sidebar - The page will view the user who was registered and their pending status where the administrator can manage the status whether it is approved or cancelled and if the admin/staff approved it there will be an email notification sent to the registered client. 
		This is the email:
			---
			
			**Subject:** Wedding Request Approval
			
			Dear [Recipient's Name],
			
			We are pleased to inform you that your request to reserve the church hall for your wedding on [Date] has been approved.
			
			Please let us know if you need any further assistance or have specific arrangements in mind.
			
			Congratulations, and we look forward to celebrating this special occasion with you!
			
			Best regards,  
			[Your Name]  
			[Your Position]  
			[Church Name]  
			[Contact Information]
				 
 - 
	


# File Structure


WSMS/
├── assets/                          # Static files
│   ├── css/                         # Stylesheets
│   │   └── style.css                # Custom CSS for the system
│   ├── js/                          # JavaScript files
│   │   └── scripts.js               # Custom JavaScript
│   ├── images/                      # Images (logos, icons, etc.)
│   └── plugins/                     # Third-party plugins
├── includes/                        # Reusable PHP scripts
│   ├── header.php                   # Common header for all pages
│   ├── footer.php                   # Common footer for all pages
│   ├── navbar.php                   # Navigation bar
│   └── phpmailer/                   # PHPMailer for email notifications
├── templates/                       # Email templates
│   └── email_template.php           # Email notification template
├── admin/                           # Admin-related files
│   ├── index.php                    # Admin login page (superadmin & subadmin login)
│   ├── dashboard.php                # Superadmin Dashboard
│   ├── subadmin_dashboard.php       # Subadmin Dashboard (restricted)
│   ├── manage_bookings.php          # Booking management (for superadmin & subadmin)
│   ├── manage_users.php             # User management (only for superadmin)
│   ├── add_user.php                 # Add new user (superadmin only)
│   └── reports.php                  # Reports and analytics (for superadmin)
├── client/                          # Client-side files
│   ├── dashboard.php                # Client dashboard
│   ├── booking.php                  # Wedding booking form
│   └── profile.php                  # Client profile management
├── public/                          # Public-facing files
│   ├── index.php                    # Homepage
│   ├── login.php                    # User login page (client-side)
│   ├── register.php                 # User registration page
│   └── contact.php                  # Contact us page
├── uploads/                         # Uploaded files
│   └── bookings/                    # Folder for booking documents
├── config.php                       # Database configuration file
├── .htaccess                        # Apache routing configuration
├── README.md                        # Documentation


Here’s a structured approach to proceed with the development of the **St. Rita Mission Station Wedding Schedule Management System (WSMS)**. This includes user interface (UI) enhancements, database structure, functionality integration, and system features. Let’s break it down in a more organized way, using your requirements.

---

### **Project: St. Rita Mission Station - Wedding Schedule Management System (WSMS)**

---

### **I. User Interface Enhancements**

**1. Main Navigation Bar:**

- **About Us**: Add a section with detailed information about St. Rita Mission Station's history, mission, and vision.
- **Services**: Include a list of services like baptisms, community events, etc.
- **Visual Design**: Use wedding-themed colors and fonts, with elegant icons and clear navigation.

**2. Hero Section (Image Slider - Carousel):**

- Add a carousel of beautiful wedding photos.
- **Call-to-Action Button**: "Book Your Wedding Now" — This button will scroll smoothly to the login/register section or the booking form if the user is logged in.

**3. Login & Register (Aside Section):**

- **Social Media Login**: Provide Google and Facebook login options to simplify the registration and login process.

**4. Contact Us Page:**

- **Google Map Integration**: Pinpoint the church’s exact location for easy directions.
- **Feedback Form**: Allow users to submit comments or inquiries.
- **Accessibility Features**:
    - Dark Mode Toggle for improved usability.
    - Screen reader support to ensure accessibility for visually impaired users.

---

### **II. Client Side - UI Enhancements**

**1. Forms:**

- **Auto-Save Draft**: Allow users to save their progress while filling out forms and return to it later.
- **Real-Time Form Validation**: Immediate feedback if required fields are missing or incorrect.

**2. Wedding Calendar Integration:**

- Use a calendar plugin (FullCalendar) to display available and reserved wedding dates.
- **Highlight Peak Seasons**: Show holidays or busy wedding dates in distinct colors.
- **Blocked Dates**: Display dates blocked for church maintenance or events.

**3. Booking Status Dashboard:**

- **Progress Tracker**: Show the booking status as "Pending → Approved → Completed."
- **Download Waiver**: Allow clients to download a PDF waiver once their booking is approved.
- **Notifications**: Send alerts (SMS/Email) on booking status updates.

---

### **III. Admin Side - UI Enhancements**

**1. Dashboard:**

- **Key Metrics**: Display:
    - Total bookings
    - Pending requests
    - Upcoming weddings
- **Calendar View**: Integrate FullCalendar to display all wedding bookings.
- **Tasks Section**: A list of pending tasks (e.g., pending approval requests).

**2. Client Management:**

- **Search & Filter**: Allow admins to search clients by name, status, or date.
- **Edit Booking Details**: Enable admins to modify booking details upon client request.

**3. Reports & Analytics:**

- **Charts and Data Export**: Use libraries like Chart.js to display wedding statistics (e.g., number of weddings by month) and allow data export to CSV/PDF for reporting purposes.

**4. Admin Profile Settings:**

- Admins can update their profile information, change passwords, and upload a profile picture.

---

### **IV. System-Wide Features**

**1. Logging & Monitoring:**

- **Audit Log**: Track all actions taken by admins, including booking edits, status changes, and settings modifications.

**2. Backup System:**

- **Database Backups**: Automated daily/weekly backups of the database to prevent data loss.

**3. Enhanced Security:**

- **Two-Factor Authentication (2FA)**: Add 2FA for admins to improve login security.
- **Input Validation**: Validate inputs both on the client-side (JavaScript) and server-side (PHP).

**4. Localization (Optional):**

- **Language Support**: Add support for multiple languages (e.g., English, Filipino) based on user preference.

---

### **V. Features for Clients After Login**

**1. Client Dashboard:**

- **Welcome Message**: Display the client’s name (e.g., “Welcome, [Client Name]”).
- **Booking Status Card**: Show the booking status: Pending, Approved, Completed.
- **Booking Form**: A multi-step form:
    - Step 1: Bride details
    - Step 2: Groom details
    - Step 3: Document upload
    - Step 4: Wedding date selection

**2. Notifications:**

- **Booking Updates**: Clients receive notifications (via email and/or SMS) when their booking status changes.

---

### **VI. Database Structure**

#### **1. Admins Table (For Super Admin and Sub Admins)**

- **superadmin**: Username: `admin`, Password: `admin` (no hashing)
- **subadmin**: Limited access (view, manage bookings, and settings only).
- **Tables**:
    - `admins` (superadmin, subadmin)
    - `users` (clients)
    - `bookings`
    - `services`


Here’s a structured approach to proceed with the development of the **St. Rita Mission Station Wedding Schedule Management System (WSMS)**. This includes user interface (UI) enhancements, database structure, functionality integration, and system features. Let’s break it down in a more organized way, using your requirements.

---

### **Project: St. Rita Mission Station - Wedding Schedule Management System (WSMS)**

---

### **I. User Interface Enhancements**

**1. Main Navigation Bar:**

- **About Us**: Add a section with detailed information about St. Rita Mission Station's history, mission, and vision.
- **Services**: Include a list of services like baptisms, community events, etc.
- **Visual Design**: Use wedding-themed colors and fonts, with elegant icons and clear navigation.

**2. Hero Section (Image Slider - Carousel):**

- Add a carousel of beautiful wedding photos.
- **Call-to-Action Button**: "Book Your Wedding Now" — This button will scroll smoothly to the login/register section or the booking form if the user is logged in.

**3. Login & Register (Aside Section):**

- **Social Media Login**: Provide Google and Facebook login options to simplify the registration and login process.

**4. Contact Us Page:**

- **Google Map Integration**: Pinpoint the church’s exact location for easy directions.
- **Feedback Form**: Allow users to submit comments or inquiries.
- **Accessibility Features**:
    - Dark Mode Toggle for improved usability.
    - Screen reader support to ensure accessibility for visually impaired users.

---

### **II. Client Side - UI Enhancements**

**1. Forms:**

- **Auto-Save Draft**: Allow users to save their progress while filling out forms and return to it later.
- **Real-Time Form Validation**: Immediate feedback if required fields are missing or incorrect.

**2. Wedding Calendar Integration:**

- Use a calendar plugin (FullCalendar) to display available and reserved wedding dates.
- **Highlight Peak Seasons**: Show holidays or busy wedding dates in distinct colors.
- **Blocked Dates**: Display dates blocked for church maintenance or events.

**3. Booking Status Dashboard:**

- **Progress Tracker**: Show the booking status as "Pending → Approved → Completed."
- **Download Waiver**: Allow clients to download a PDF waiver once their booking is approved.
- **Notifications**: Send alerts (SMS/Email) on booking status updates.

---

### **III. Admin Side - UI Enhancements**

**1. Dashboard:**

- **Key Metrics**: Display:
    - Total bookings
    - Pending requests
    - Upcoming weddings
- **Calendar View**: Integrate FullCalendar to display all wedding bookings.
- **Tasks Section**: A list of pending tasks (e.g., pending approval requests).

**2. Client Management:**

- **Search & Filter**: Allow admins to search clients by name, status, or date.
- **Edit Booking Details**: Enable admins to modify booking details upon client request.

**3. Reports & Analytics:**

- **Charts and Data Export**: Use libraries like Chart.js to display wedding statistics (e.g., number of weddings by month) and allow data export to CSV/PDF for reporting purposes.

**4. Admin Profile Settings:**

- Admins can update their profile information, change passwords, and upload a profile picture.

---

### **IV. System-Wide Features**

**1. Logging & Monitoring:**

- **Audit Log**: Track all actions taken by admins, including booking edits, status changes, and settings modifications.

**2. Backup System:**

- **Database Backups**: Automated daily/weekly backups of the database to prevent data loss.

**3. Enhanced Security:**

- **Two-Factor Authentication (2FA)**: Add 2FA for admins to improve login security.
- **Input Validation**: Validate inputs both on the client-side (JavaScript) and server-side (PHP).

**4. Localization (Optional):**

- **Language Support**: Add support for multiple languages (e.g., English, Filipino) based on user preference.

---

### **V. Features for Clients After Login**

**1. Client Dashboard:**

- **Welcome Message**: Display the client’s name (e.g., “Welcome, [Client Name]”).
- **Booking Status Card**: Show the booking status: Pending, Approved, Completed.
- **Booking Form**: A multi-step form:
    - Step 1: Bride details
    - Step 2: Groom details
    - Step 3: Document upload
    - Step 4: Wedding date selection

**2. Notifications:**

- **Booking Updates**: Clients receive notifications (via email and/or SMS) when their booking status changes.

---

### **VI. Database Structure**

#### **1. Admins Table (For Super Admin and Sub Admins)**

- **superadmin**: Username: `admin`, Password: `admin` (no hashing)
- **subadmin**: Limited access (view, manage bookings, and settings only).
- **Tables**:
    - `admins` (superadmin, subadmin)
    - `users` (clients)
    - `bookings`
    - `services`

**Example Structure**:

sql

Copy code

`CREATE TABLE admins (     admin_id INT AUTO_INCREMENT PRIMARY KEY,     username VARCHAR(50) NOT NULL UNIQUE,     password VARCHAR(255) NOT NULL,     role ENUM('superadmin', 'subadmin') DEFAULT 'subadmin',     full_name VARCHAR(100),     email VARCHAR(100) NOT NULL UNIQUE,     profile_picture VARCHAR(255) DEFAULT NULL,     created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP );  CREATE TABLE users (     user_id INT AUTO_INCREMENT PRIMARY KEY,     full_name VARCHAR(100),     email VARCHAR(100) NOT NULL UNIQUE,     password VARCHAR(255) NOT NULL,     phone VARCHAR(15),     wedding_date DATE,     created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP );  CREATE TABLE bookings (     booking_id INT AUTO_INCREMENT PRIMARY KEY,     user_id INT,     status ENUM('Pending', 'Approved', 'Completed') DEFAULT 'Pending',     date DATE,     documents JSON,     created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,     FOREIGN KEY (user_id) REFERENCES users(user_id) );  CREATE TABLE services (     service_id INT AUTO_INCREMENT PRIMARY KEY,     service_name VARCHAR(100),     description TEXT,     price DECIMAL(10, 2) );`

---

### **VII. Additional Navigation Features**

**1. Announcements Section**:

- Admin can post updates about church events, holidays, etc.

**2. FAQ Section**:

- A list of common queries about the wedding process, requirements, and packages.

**3. Testimonials Section**:

- Display reviews or testimonials from couples who’ve used the service.

**4. Help & Support**:

- A dedicated page for user support, FAQs, and contact details.

---

### **VIII. Task Management for Admin**

**1. Task Reminders**:

- Admins will receive reminders for tasks such as:
    - Pending approval
    - Upcoming weddings
    - Follow-up emails

**2. Manage Wedding Packages**:

- Admins can manage the different wedding packages offered by the church.

**3. Custom Notifications**:

- Admins can set custom notification messages for different booking statuses.

---

### **IX. Implementation Plan**

#### **Frontend:**

- **HTML/CSS/Bootstrap**:
    - Use Bootstrap’s grid system for responsiveness.
    - Implement custom CSS for unique wedding-themed designs (soft colors, elegant typography).
    - JavaScript Libraries for enhanced functionality like FullCalendar (for date selection), SweetAlert (for confirmation popups), and PHPMailer (for email notifications).
    - Implement **responsive design** to ensure compatibility across mobile and desktop devices.

#### **Backend:**

- **PHP (Server-Side Logic)**:
    - Handle authentication, form submissions, and user requests.
    - Ensure secure login using email/password, as well as social media logins (Google/Facebook).
    - Use **bcrypt** for password hashing when adding users, but for admin (superadmin/subadmin), you may skip hashing as per your requirement.


