# 🏥 Medical Referral Appointment System

A full-stack MERN (MongoDB, Express, React, Node.js) application that enables seamless patient referrals, hospital management, and appointment scheduling.

<p align="center">
  <img src="Frontend/src/assets/logo.svg" alt="Banner" width="110" height="110">
</p>

---

## 📚 Table of Contents

- [✨ Features](#-features)
- [📸 Screenshots](#-screenshots)
- [📡 API Endpoints](#-api-endpoints)
- [🛠️ Tech Stack](#-tech-stack)
- [⚙️ Setup Instructions](#-setup-instructions)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

---

## ✨ Features

- 🧑‍⚕️ Role-based system for Admins, Doctors, and Patients
- 🏥 Manage hospitals and doctor availability
- 📅 Book, update, and cancel appointments
- 🔁 Refer patients between hospitals/doctors
- 🩺 View and upload medical records
- 🔒 JWT authentication with OTP email verification
- 📊 Admin dashboard for insights and stats

---

## 📸 Screenshots

### 🛠️ Admin Dashboard

_Manage hospitals and users_
[![Admin Screenshot](screenshots/admin-thumb.png)](screenshots/admin-dashboard.png)

---

### 🩺 Doctor Dashboard

_Create and view referrals and appointments_
[![Doctor Screenshot](screenshots/doctor-thumb.png)](screenshots/doctor-dashboard.png)

---

### 👤 Patient Dashboard

_Search doctors, view hospitals, and book appointments_
[![Patient Screenshot](screenshots/patient-thumb.png)](screenshots/patient-dashboard.png)

---

## 📡 API Endpoints

Click to expand full documentation:

<details>
<summary><strong>🔐 Authentication</strong></summary>

- `POST /api/auth/register` – Register a new user
- `POST /api/auth/login` – Login with email or username
- `POST /api/auth/verify` – Verify OTP
- `POST /api/auth/resend-otp` – Resend OTP
- `GET /api/auth/profile` – Get current profile
- `PUT /api/auth/profile` – Update profile
</details>

<details>
<summary><strong>👥 User Management (Admin)</strong></summary>

- `GET /api/users` – All users
- `GET /api/users/:id` – Single user
- `PUT /api/users/:id` – Update user
- `DELETE /api/users/:id` – Remove user
</details>

<details>
<summary><strong>🧑‍⚕️ Doctor</strong></summary>

- `POST /api/doctors` – Create profile
- `GET /api/doctors/profile` – My profile
- `PUT /api/doctors/profile` – Update profile
- `GET /api/doctors` – List all doctors
- `GET /api/doctors/:id` – Doctor by ID
- `GET /api/doctors/specialization/:specialization`
- `GET /api/doctors/hospital/:hospitalId`
</details>

<details>
<summary><strong>🧑‍🤝‍🧑 Patient</strong></summary>

- `POST /api/patients` – Create profile
- `GET /api/patients/profile` – My profile
- `PUT /api/patients/profile` – Update profile
- `GET /api/patients` – All patients (doctor/admin)
- `GET /api/patients/:id`
</details>

<details>
<summary><strong>🏥 Hospitals</strong></summary>

- `POST /api/hospitals` – Add hospital (admin)
- `GET /api/hospitals` – Public list
- `GET /api/hospitals/:id` – Hospital by ID
- `PUT /api/hospitals/:id` – Update (admin)
- `DELETE /api/hospitals/:id` – Remove (admin)
- `GET /api/hospitals/search?keyword=...`
</details>

<details>
<summary><strong>📅 Appointments</strong></summary>

- `POST /api/appointments` – Book appointment
- `GET /api/appointments/patient` – Patient view
- `GET /api/appointments/doctor` – Doctor view
- `GET /api/appointments/all` – Admin view
- `GET /api/appointments/:id` – Single view
- `PUT /api/appointments/:id/status` – Update status
- `PUT /api/appointments/:id/cancel` – Cancel appointment
</details>

<details>
<summary><strong>🔁 Referrals</strong></summary>

- `POST /api/referrals` – New referral
- `GET /api/referrals/patient`
- `GET /api/referrals/referring`
- `GET /api/referrals/referred`
- `GET /api/referrals/all`
- `GET /api/referrals/:id`
- `PUT /api/referrals/:id/status`
- `POST /api/referrals/:id/appointment`
</details>

<details>
<summary><strong>🧾 Medical Records</strong></summary>

- `POST /api/medical-records/upload`
- `GET /api/medical-records/patient/:patientId`
- `GET /api/medical-records/:id`
- `GET /api/medical-records/download/:id`
- `DELETE /api/medical-records/:id`
</details>

<details>
<summary><strong>🧑‍💼 Admin</strong></summary>

- `POST /api/admins`
- `GET /api/admins/profile`
- `PUT /api/admins/profile`
- `GET /api/admin/db-stats`
</details>

---

## 🛠️ Tech Stack

- **Frontend**: React, Tailwind CSS, Redux, Framer Motion
- **Backend**: Node.js, Express.js
- **Database**: MongoDB Atlas
- **Authentication**: JWT, OTP via email
- **Deployment**: Vercel

---

## ⚙️ Setup Instructions

### 1. Clone Repository

```bash
git clone https://github.com/its-Gray/medref.git
```

### 2. Install Dependencies

```bash
cd backend && npm install
cd ../frontend && yarn
```

### 3. Configure Environment Variables

Create .env files in both the backend and frontend directories with your environment-specific variables.

### 4. Run the Project

# Backend

```bash
cd backend
npm run dev
```

# Frontend

```bash
cd ../frontend
npm run dev
```

## 🤝 Contributing

We welcome all contributions! Follow these steps:

    Fork the repository

    Create a new branch: git checkout -b feature-name

    Make and commit your changes

    Push to your fork

    Submit a Pull Request

📄 License

This project is licensed under the MIT License.
