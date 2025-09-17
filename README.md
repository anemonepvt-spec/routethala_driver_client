# Routethala Driver App 🚍

![Flutter](https://img.shields.io/badge/Flutter-%2302569B.svg?style=for-the-badge&logo=Flutter&logoColor=white)

A Flutter application for bus drivers to share their live location with the server during a trip. This app is the driver-side client for the Routethala public transport tracking system.

---

## 📱 App Screens

A quick visual overview of the application's user interface.

| Login Screen | Route Selection | Live Ride |
| :----------: | :---------------: | :---------: |
|  |  |  |

---

## ✨ Key Features

* **Secure Driver Authentication**: Drivers log in using their unique vehicle ID and password.
* **Bus Route Selection**: A simple interface for the driver to select their designated route before starting a trip.
* **Real-time GPS Tracking**: Utilizes WebSockets to efficiently send live location coordinates to the server.
* **Ride Management**: Clear functionality to start and end a ride, changing the driver's status on the network.

---

## 📂 Project Structure

A brief overview of the key files in this project:

* `pubspec.yaml`: Defines project dependencies like `supabase_flutter`.
* `lib/main.dart`: The entry point of the application. Handles the initialization of the Supabase client.
* `lib/login_screen.dart`: Contains the UI and logic for the driver sign-in screen, including authentication calls.
* `lib/route_selection_screen.dart`: The UI and logic for selecting a bus route before a trip begins.
* `lib/live_ride_screen.dart`: The UI for the main ride screen, showing the selected route and live tracking status.

---

## 🔧 API Specification

This section outlines the API endpoints and data structures the Flutter app uses to communicate with the backend.

### 1. Driver Authentication

Authenticates the driver and retrieves a session token (JWT) for subsequent authenticated requests.

* **Endpoint**: `POST /api/v1/driver/auth/login`

#### Request Body

```json
{
  "vehicle_id": "TN09BE5678",
  "password": "driver_password_123"
}
