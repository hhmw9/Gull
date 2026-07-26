# Gull
We provide a best doctor and service for your health 
<form method="POST" action="/login">

<input
type="email"gulmedical
name="email"gmc
placeholder="Email"
class="form-control">

<br>

<input
type="password"aaa
name="password"
placeholder="Password"aaa
class="form-control">

<br>

<button class="btn btn-primary w-100">
Login
</button>

</form>
 <!DOCTYPE html>
<html>
<head>

<title>Gul Medical Center</title>

<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">

</head>

<body>

<div class="container mt-5">

<h2>Hospital Dashboard</h2>

<div class="row">

<div class="col-md-3">
<div class="card bg-primary text-white">
<div class="card-body">
<h4>Total Patients</h4>
<h2>200</h2>
</div>
</div>
</div>

<div class="col-md-3">
<div class="card bg-success text-white">
<div class="card-body">
<h4>Total Doctors</h4>
<h2>20</h2>
</div>
</div>
</div>

<div class="col-md-3">
<div class="card bg-warning text-dark">
<div class="card-body">
<h4>Today's Appointments</h4>
<h2>35</h2>
</div>
</div>
</div>

<div class="col-md-3">
<div class="card bg-danger text-white">
<div class="card-body">
<h4>Monthly Revenue</h4>
<h2>$18,500</h2>
</div>
</div>
</div>

</div>

</div>

</body>
</html> 
CREATE TABLE appointments(
id INT AUTO_INCREMENT PRIMARY KEY,
patient_id INT,
doctor_id INT,
appointment_date DATE,
appointment_time TIME,
status VARCHAR(20),
FOREIGN KEY(patient_id) REFERENCES patients(id),
FOREIGN KEY(doctor_id) REFERENCES doctors(id)
);
CREATE TABLE patients(
id INT AUTO_INCREMENT PRIMARY KEY,
patient_name VARCHAR(150),
gender VARCHAR(20),
age INT,
phone VARCHAR(20),
address TEXT,
blood_group VARCHAR(5),
created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
); 
CREATE TABLE users (
id INT AUTO_INCREMENT PRIMARY KEY,
name VARCHAR(100),
email VARCHAR(100) UNIQUE,
password VARCHAR(255),
role ENUM('Admin','Doctor','Receptionist','Pharmacist','Lab','Accountant'),
created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
