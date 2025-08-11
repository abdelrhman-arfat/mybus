# MyBus API Documentation

This document provides an overview of the API routes for the MyBus project.
This document provides an overview of the API routes for the [MyBus project](https://abdelrhman-arfat.github.io/mybus/).


## API Routes ⚙️



### Authentication Routes 🔑

The authentication module handles user authentication, OTP verification, and user profile management.

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/{url}/auth/send-otp` | Send OTP to user's phone number |
| POST | `/{url}/auth/verify-otp` | Verify the OTP sent to user |
| POST | `/{url}/auth/resend-otp` | Resend OTP if not received |
| POST | `/{url}/auth/logout` | Logout user from the system |
| GET | `/{url}/auth/profile` | Get user profile information |



### Trip Management Routes ✈️

These routes handle trip creation, management, and lifecycle operations.

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/{url}/trips` | Create a new trip |
| GET | `/{url}/trips` | Get all trips |
| GET | `/{url}/trips/{id}` | Get trip by ID |
| PUT | `/{url}/trips/{id}` | Update trip data |
| POST | `/{url}/trips/{id}/start` | Start the trip |
| POST | `/{url}/trips/{id}/complete` | Complete the trip |
| POST | `/{url}/trips/{id}/cancel` | Cancel the trip |




### Trip Seat Management Routes 💺

These routes manage seat information and reservations within a trip.
| Method | Endpoint                             | Description                |
| ------ | ------------------------------------ | -------------------------- |
| GET    | `/trips/{trip}/seats`                | Get all seats for a trip   |
| GET    | `/trips/{trip}/seats/layout`         | Get seat layout for a trip |
| GET    | `/trips/{trip}/seats/available`      | Get available seats        |
| GET    | `/trips/{trip}/seats/statistics`     | Get seat statistics        |
| GET    | `/trips/{trip}/seats/{seat}`         | Get seat by ID             |
| PUT    | `/trips/{trip}/seats/{seat}`         | Update seat assignment     |
| POST   | `/trips/{trip}/seats/{seat}/reserve` | Reserve a seat             |
| POST   | `/trips/{trip}/seats/{seat}/release` | Release a reserved seat    |
| POST   | `/trips/{trip}/seats/{seat}/disable` | Disable a seat             |
| POST   | `/trips/{trip}/seats/{seat}/enable`  | Enable a seat              |


### Passenger Routes 🚶

These routes handle passenger-related operations within a trip.

| Method | Endpoint                                        | Description                   |
| ------ | ----------------------------------------------- | ----------------------------- |
| GET    | `/trips/{trip}/passengers`                      | Get all passengers for a trip |
| POST   | `/trips/{trip}/passengers`                      | Add a new passenger           |
| GET    | `/trips/{trip}/passengers/statistics`           | Get passenger statistics      |
| GET    | `/trips/{trip}/passengers/{passenger}`          | Get passenger by ID           |
| PUT    | `/trips/{trip}/passengers/{passenger}`          | Update passenger              |
| DELETE | `/trips/{trip}/passengers/{passenger}`          | Delete passenger              |
| POST   | `/trips/{trip}/passengers/{passenger}/board`    | Mark passenger as boarded     |
| POST   | `/trips/{trip}/passengers/{passenger}/complete` | Mark passenger as completed   |



### Driver Routes 🧑‍✈️

These routes manage driver profiles and statistics.
| Method | Endpoint             | Description                       |
| ------ | -------------------- | --------------------------------- |
| GET    | `/driver/profile`    | Get driver profile information    |
| POST   | `/driver/profile`    | Update driver profile information |
| GET    | `/driver/statistics` | Get driver statistics             |

### Driver Vehicle Routes 🚗

| Method | Endpoint                     | Description                     |
| ------ | ---------------------------- | ------------------------------- |
| GET    | `/driver/vehicles`           | Get all vehicles for the driver |
| POST   | `/driver/vehicles`           | Add a new vehicle               |
| GET    | `/driver/vehicles/{vehicle}` | Get vehicle by ID               |
| PUT    | `/driver/vehicles/{vehicle}` | Update vehicle data             |
| DELETE | `/driver/vehicles/{vehicle}` | Delete a vehicle                |

Google Gemini API – Image Data Extraction 🧠📷
The GeminiApiHandler is used to extract structured JSON data from various documents (National ID, Driver’s License, Vehicle Registration, etc.) using Google’s Gemini 2.0 Flash API.
