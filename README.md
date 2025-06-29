# Student--Teacher-Appointment

A web-based appointment and communication platform enabling students to book appointments with teachers and send them messages, while administrators can manage teachers and approve student registrations.

---

## Features

### Authentication
- Sign up/login system using Firebase Authentication
- Role-based redirection (Admin, Teacher, Student)

###  Admin Panel
- Add, update, or delete teacher information
- Approve pending student registrations

###  Teacher Dashboard *(Placeholder - implementation expected)*
- View and manage appointment requests from students
- Read messages sent by students

###  Student Dashboard
- Book appointments with teachers
- Send messages to teachers
- Logout securely

---

##  Tech Stack

| Layer       | Technology       |
|-------------|------------------|
| Frontend    | HTML, CSS, JavaScript |
| Backend     | Firebase Firestore |
| Auth        | Firebase Authentication |
| Hosting     | Firebase Hosting |

---

##  Project Setup

### 1. Clone the repository
```bash
git clone https://github.com/your-username/student-teacher-booking.git
cd student-teacher-booking
```

### 2. Firebase Configuration
Update the Firebase config object in all `.js` files:
- `index.html`
- `admin.dashboard.js`
- `student-dashboard.html`
- `teacher-dashboard.html`

### 3. Host via Firebase (optional)
```bash
firebase init
firebase deploy
```

Ensure your `firebase.json` includes:
```json
{
  "hosting": {
    "public": "demo",
    "rewrites": [{ "source": "**", "destination": "/index.html" }]
  }
}
```

---

## 📂 Project Structure

```
.
├── index.html                   # Login and Signup UI
├── admin-dashboard.html        # Admin dashboard UI
├── admin.dashboard.js          # Admin dashboard logic
├── student-dashboard.html      # Student dashboard
├── teacher-dashboard.html      # Teacher dashboard (UI placeholder)
├── firebase.json               # Firebase hosting config
```

---

##  Workflow

1. **User Registration**  
   - Admin, Teacher, or Student signs up
   - Students must be approved by Admin before accessing their dashboard

2. **Admin Dashboard**  
   - Manage teacher records
   - Approve new students

3. **Student Dashboard**  
   - Search teachers (by email)
   - Book appointment (with time, title, subject, department)
   - Send message to a teacher

4. **Teacher Dashboard** *(Implementation needed)*  
   - View incoming appointments
   - Accept/reject requests
   - View student messages

---

## ✅ Best Practices Followed

- Modular, maintainable JS code
- Cloud-based, portable deployment
- Secure Firebase integration
- Firebase Firestore used as a NoSQL database
- Basic logging via `console.log()` (can be extended using libraries)

---


## 📝 License

This project is open-source under the MIT License.
