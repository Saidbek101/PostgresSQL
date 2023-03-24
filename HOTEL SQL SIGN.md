```SQL
CREATE TABLE hotels (
  id SERIAL PRIMARY KEY,
  name VARCHAR(255) NOT NULL,
  address VARCHAR(255) NOT NULL,
  phone VARCHAR(20) NOT NULL,
  email VARCHAR(255),
  website VARCHAR(255)
);

CREATE TABLE rooms (
  id SERIAL PRIMARY KEY,
  hotel_id INTEGER NOT NULL REFERENCES hotels(id),
  room_number INTEGER NOT NULL,
  room_type VARCHAR(50) NOT NULL,
  bed_type VARCHAR(50) NOT NULL,
  max_guests INTEGER NOT NULL,
  price_per_night NUMERIC(8,2) NOT NULL
);

CREATE TABLE bookings (
  id SERIAL PRIMARY KEY,
  room_id INTEGER NOT NULL REFERENCES rooms(id),
  guest_name VARCHAR(255) NOT NULL,
  guest_email VARCHAR(255) NOT NULL,
  check_in_date DATE NOT NULL,
  check_out_date DATE NOT NULL,
  num_guests INTEGER NOT NULL,
  total_price NUMERIC(8,2) NOT NULL
);

CREATE TABLE services (
  id SERIAL PRIMARY KEY,
  hotel_id INTEGER NOT NULL REFERENCES hotels(id),
  service_name VARCHAR(255) NOT NULL,
  service_description VARCHAR(500),
  price NUMERIC(8,2) NOT NULL
);

CREATE TABLE events (
  id SERIAL PRIMARY KEY,
  hotel_id INTEGER NOT NULL REFERENCES hotels(id),
  event_name VARCHAR(255) NOT NULL,
  event_description VARCHAR(500),
  start_date DATE NOT NULL,
  end_date DATE NOT NULL,
  price NUMERIC(8,2) NOT NULL
);

CREATE TABLE guests (
  id SERIAL PRIMARY KEY,
  first_name VARCHAR(255) NOT NULL,
  last_name VARCHAR(255) NOT NULL,
  email VARCHAR(255) NOT NULL,
  phone VARCHAR(20),
  address VARCHAR(255)
);

CREATE TABLE employees (
  id SERIAL PRIMARY KEY,
  hotel_id INTEGER NOT NULL REFERENCES hotels(id),
  first_name VARCHAR(255) NOT NULL,
  last_name VARCHAR(255) NOT NULL,
  email VARCHAR(255) NOT NULL,
  phone VARCHAR(20),
  job_title VARCHAR(255) NOT NULL,
  salary NUMERIC(8,2) NOT NULL
);

CREATE TABLE shifts (
  id SERIAL PRIMARY KEY,
  employee_id INTEGER NOT NULL REFERENCES employees(id),
  shift_date DATE NOT NULL,
  start_time TIME NOT NULL,
  end_time TIME NOT NULL
);

CREATE TABLE payments (
  id SERIAL PRIMARY KEY,
  booking_id INTEGER NOT NULL REFERENCES bookings(id),
  payment_date DATE NOT NULL,
  amount NUMERIC(8,2) NOT NULL
);

CREATE TABLE reviews (
  id SERIAL PRIMARY KEY,
  hotel_id INTEGER NOT NULL REFERENCES hotels(id),
  guest_id INTEGER NOT NULL REFERENCES guests(id),
  room_id INTEGER NOT NULL REFERENCES rooms(id),
  review_text TEXT,
  rating INTEGER NOT NULL
);

CREATE TABLE rooms (
  room_number SERIAL PRIMARY KEY,
  room_type VARCHAR(50) NOT NULL,
  max_occupancy INTEGER NOT NULL,
  price_per_night NUMERIC(10,2) NOT NULL,
  availability BOOLEAN NOT NULL
);

CREATE TABLE reservations (
  reservation_id SERIAL PRIMARY KEY,
  guest_id INTEGER REFERENCES guests(guest_id),
  room_number INTEGER REFERENCES rooms(room_number),
  check_in_date DATE NOT NULL,
  check_out_date DATE NOT NULL,
  num_of_guests INTEGER NOT NULL,
  payment_amount NUMERIC(10,2) NOT NULL
);
```
![image](https://user-images.githubusercontent.com/122611553/227434538-3ec03425-afb2-4d4d-8dce-49ed6410bb9f.png)

