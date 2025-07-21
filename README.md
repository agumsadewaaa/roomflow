<!-- ROOMFLOW - README OVERVIEW -->
<h1>RoomFlow - Meeting Room Booking App</h1>

<p><strong>Tech Stack:</strong> Laravel 10 (backend, PostgreSQL), React + Vite + Tailwind (frontend)</p>

<hr/>
<h2>✨ FITUR</h2>
<ul>
  <li>User Register & Login (JWT Auth)</li>
  <li>Admin & User Role</li>
  <li>CRUD Ruangan (oleh Admin)</li>
  <li>CRUD Booking Ruangan (User)</li>
  <li>Calendar Booking View (via FullCalendar.js)</li>
  <li>Validasi jadwal bentrok</li>
</ul>

<hr/>
<h2>💡 STRUKTUR FOLDER</h2>
<pre>
roomflow/
├── client/             # React Vite Frontend
│   ├── public/
│   ├── src/
│   │   ├── components/     # FullCalendar, Form
│   │   ├── pages/          # Login, Register, Dashboard
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── tailwind.config.js
│
├── server/             # Laravel 10 Backend
│   ├── app/
│   │   ├── Models/         # User, Room, Booking
│   │   └── Http/Controllers
│   ├── routes/
│   │   └── api.php
│   ├── database/migrations/
│   └── .env.example
│
├── README.md
</pre>

<hr/>
<h2>🔄 API ROUTES</h2>
<p><strong>Auth:</strong></p>
<pre>
POST   /api/register
POST   /api/login
GET    /api/user
POST   /api/logout
</pre>
<p><strong>Room:</strong></p>
<pre>
GET    /api/rooms
POST   /api/rooms       (admin)
PUT    /api/rooms/{id}  (admin)
DELETE /api/rooms/{id}  (admin)
</pre>
<p><strong>Booking:</strong></p>
<pre>
GET    /api/bookings
POST   /api/bookings
PUT    /api/bookings/{id}
DELETE /api/bookings/{id}
</pre>

<hr/>
<h2>🚀 SETUP</h2>
<h3>Laravel (server/):</h3>
<pre>
cd server
cp .env.example .env
composer install
php artisan key:generate
php artisan migrate
php artisan serve
</pre>

<h3>React (client/):</h3>
<pre>
cd client
npm install
npm run dev
</pre>

<hr/>
