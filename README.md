# MyBus API Documentation

This document provides an overview of the API routes for the MyBus project.





## API Routes



### Authentication Routes

The authentication module handles user authentication, OTP verification, and user profile management.

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/{url}/auth/send-otp` | Send OTP to user's phone number |
| POST | `/{url}/auth/verify-otp` | Verify the OTP sent to user |
| POST | `/{url}/auth/resend-otp` | Resend OTP if not received |
| GET | `/{url}/auth/profile` | Get user profile information |
| POST | `/{url}/auth/logout` | Logout user from the system |



### Trip Management Routes

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




### Trip Seat Management Routes

These routes manage seat information and reservations within a trip.

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/{url}/trips/{id}/seats/{seat_id}` | Get seat information |
| PUT | `/{url}/trips/{id}/seats/{seat_id}` | Assign passenger to a seat |
| POST | `/{url}/trips/{id}/seats/{seat_id}/reserve` | Reserve a seat |
| POST | `/{url}/trips/{id}/seats/{seat_id}/release` | Release a reserved seat |
| GET | `/{url}/trips/{id}/seats` | Get all seats for a trip |



### Passenger Routes

These routes handle passenger-related operations within a trip.

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/{url}/trips/{id}/passengers` | Get all passengers for a trip |
| POST | `/{url}/trips/{id}/passengers` | Create a new passenger |



### Driver Routes

These routes manage driver profiles and statistics.

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/{url}/driver/profile` | Get driver profile information |
| POST | `/{url}/driver/profile` | Update driver profile information |
| GET | `/{url}/driver/statistics` | Get driver statistics |



### Driver Vehicle Routes

These routes manage vehicles associated with drivers.

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/{url}/driver/vehicles` | Get all vehicles for a driver |
| POST | `/{url}/driver/vehicles` | Add a new vehicle for a driver |
| PUT | `/{url}/driver/vehicles/{id}` | Update vehicle data |
| GET | `/{url}/driver/vehicles/{id}` | Delete a vehicle |




