# OpenSource Taxi Booking

An open-source taxi booking platform designed with a robust backend and intuitive frontend. This project aims to provide a complete and scalable solution for building taxi booking applications with a focus on real-world use cases.

---

## Technologies Used

- **Backend**: Node.js, Express, TypeScript
- **Frontend**: Next.js, React
- **Mobile App**: Expo, React Native
- **Database**: MongoDB (for flexible data handling)

---

## Folder Structure

```
/backend        # Backend services (Node.js, Express, TypeScript)
/frontend       # Frontend application (Next.js)
/mobile         # Mobile app (Expo, React Native)
```

---

## API Architecture

The project is divided into three core sections, each handling specific responsibilities:

### 1. **Customer Routes**

| Endpoint                          | Method  | Description                                |
|-----------------------------------|---------|--------------------------------------------|
| `/customer/signup`                | POST    | Register a new customer                   |
| `/customer/login`                 | POST    | Login and receive JWT                     |
| `/customer/profile`               | GET     | View customer profile                     |
| `/customer/profile`               | PATCH   | Update customer profile                   |
| `/customer/rides/book`            | POST    | Book a new ride                           |
| `/customer/rides/estimate`        | POST    | Get fare estimate for a ride              |
| `/customer/rides/cancel/:id`      | PATCH   | Cancel a ride                             |
| `/customer/rides/:id`             | GET     | View specific ride details                |
| `/customer/rides/live/:id`        | GET     | Track live ride (via WebSockets/REST)     |
| `/customer/rides/history`         | GET     | Fetch past ride history                   |
| `/customer/wallet`                | GET     | View wallet balance and transactions      |
| `/customer/wallet/top-up`         | POST    | Add funds to wallet                       |
| `/customer/notifications`         | GET     | View notifications (e.g., ride updates)   |
| `/customer/support/ticket`        | POST    | Raise a support ticket                    |
| `/customer/support/ticket/:id`    | GET     | View support ticket details               |
| `/customer/ratings/:rideId`       | POST    | Rate a driver and provide feedback        |

### 2. **Driver Routes**

| Endpoint                          | Method  | Description                                |
|-----------------------------------|---------|--------------------------------------------|
| `/driver/signup`                  | POST    | Register a new driver                     |
| `/driver/login`                   | POST    | Login and receive JWT                     |
| `/driver/profile`                 | GET     | View driver profile                       |
| `/driver/profile`                 | PATCH   | Update driver profile                     |
| `/driver/documents/upload`        | POST    | Upload driver verification documents      |
| `/driver/documents/status`        | GET     | Check document verification status        |
| `/driver/rides/available`         | GET     | View available rides nearby               |
| `/driver/rides/:id/accept`        | PATCH   | Accept a ride request                     |
| `/driver/rides/:id/decline`       | PATCH   | Decline a ride request                    |
| `/driver/rides/:id/start`         | PATCH   | Mark ride as started                      |
| `/driver/rides/:id/complete`      | PATCH   | Mark ride as completed                    |
| `/driver/rides/live`              | PATCH   | Update driver’s live location             |
| `/driver/rides/history`           | GET     | Fetch past rides                          |
| `/driver/earnings`                | GET     | View earnings summary                     |
| `/driver/notifications`           | GET     | View notifications (e.g., ride updates)   |
| `/driver/support/ticket`          | POST    | Raise a support ticket                    |
| `/driver/support/ticket/:id`      | GET     | View support ticket details               |

### 3. **Admin Routes**

| Endpoint                          | Method  | Description                                |
|-----------------------------------|---------|--------------------------------------------|
| `/admin/login`                    | POST    | Admin login                               |
| `/admin/dashboard`                | GET     | View dashboard stats (active rides, users, etc.) |
| `/admin/customers`                | GET     | List all customers                        |
| `/admin/customers/:id`            | GET     | View a specific customer’s details        |
| `/admin/customers/:id/ban`        | PATCH   | Ban/unban a customer                      |
| `/admin/drivers`                  | GET     | List all drivers                          |
| `/admin/drivers/:id`              | GET     | View a specific driver’s details          |
| `/admin/drivers/:id/verify`       | PATCH   | Approve driver verification               |
| `/admin/drivers/:id/ban`          | PATCH   | Ban/unban a driver                        |
| `/admin/rides`                    | GET     | List all rides                            |
| `/admin/rides/:id`                | GET     | View ride details                         |
| `/admin/earnings`                 | GET     | View platform earnings                    |
| `/admin/dynamic-pricing`          | POST    | Set dynamic pricing rules                 |
| `/admin/support/tickets`          | GET     | View all support tickets                  |
| `/admin/support/tickets/:id`      | GET     | View a specific ticket’s details          |
| `/admin/notifications`            | POST    | Send notifications to customers or drivers|

---

## How to Contribute

We welcome all contributions to make this project more robust and scalable. If you're interested in contributing, please follow these steps:

### Steps to Contribute:

1. **Fork the Repository**  
   Fork this repository to your GitHub account.

2. **Clone the Repository**  
   Clone your forked repository locally:
   ```bash
   git clone https://github.com/your-username/opensource_taxi_booking.git
   cd opensource_taxi_booking
   ```

3. **Set Up the Development Environment**  
   Follow the instructions below for setting up the development environment for the backend, frontend, and mobile sections.

4. **Make Your Changes**  
   Create a new branch and make your changes:
   ```bash
   git checkout -b your-feature-branch
   ```

5. **Submit a Pull Request**  
   After making your changes, submit a pull request to the main repository.

---

## Getting Started

### Backend Setup

1. Navigate to the `/backend` folder:
   ```bash
   cd /backend
   ```

2. Install the dependencies:
   ```bash
   npm install
   ```

3. Run the backend server:
   ```bash
   npm run dev
   ```

### Frontend Setup

1. Navigate to the `/frontend` folder:
   ```bash
   cd /frontend
   ```

2. Install the dependencies:
   ```bash
   npm install
   ```

3. Run the frontend server:
   ```bash
   npm run dev
   ```

### Mobile Setup

1. Navigate to the `/mobile` folder:
   ```bash
   cd /mobile
   ```

2. Install the dependencies:
   ```bash
   npm install
   ```

3. Run the mobile app:
   ```bash
   expo start
   ```

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

We look forward to collaborating with developers around the world to build this open-source taxi booking platform! Feel free to open issues or create pull requests for new features, enhancements, or bug fixes.
