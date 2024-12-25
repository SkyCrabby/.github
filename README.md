# SkyCrabby

SkyCrabby is a modern web application that bridges the gap between flights and rideshare services like Uber. It allows users to search for flights, book them, and seamlessly connect their transportation from the airport in a single platform. The frontend is built with React, the backend with Rust, and the data is managed in an SQL database.

---

## Features

- **Flight Search and Booking**: Users can browse and book flights from various airlines.
- **Rideshare Integration**: Automatically connects users with Uber rides from their destination airport.
- **All-in-One Platform**: Streamlines the process of booking flights and transportation.
- **Secure Transactions**: Ensures user data and payment information are secure.
- **User-Friendly Interface**: Intuitive design for a seamless booking experience.

---

## Tech Stack

### Frontend
- **React**
  - Framework for building the user interface.
  - Used for creating dynamic and responsive components.
  - State management with Context API or Redux (depending on complexity).

### Backend
- **Rust**
  - High-performance and secure backend logic.
  - Actix Web for building the API.
  - Handles authentication, API integration with flight and rideshare providers, and business logic.

### Database
- **SQL Database**
  - Used to store user data, flight information, and ride connections.
  - MySQL or PostgreSQL for relational data management.

---

## Setup and Installation

### Prerequisites
- **Node.js**: Required for running the React frontend.
- **Rust**: Required for building and running the backend.
- **SQL Database**: Ensure you have MySQL or PostgreSQL installed.

### Steps

1. **Clone the Repository**:
   git clone https://github.com/SkyCrabby/CrabbyFront.git
   git clone https://github.com/SkyCrabby/CrabbyBack.git

2. **Frontend Setup**:
   cd CrabbyFront
   npm install
   npm start

3. **Backend Setup**:
   cd CrabbyBack
   cargo build
   cargo run

4. **Database Setup**:
   - Create a database named `SkyCrabby`.
   - Run the provided SQL scripts in `/db` to initialize tables.

5. **Environment Variables**:
   - Create a `.env` file in both the frontend and backend directories with the following variables:
     
     **Frontend**:
     REACT_APP_API_URL=http://localhost:8000

     **Backend**:
     DATABASE_URL=postgres://user:password@localhost:5432/SkyCrabby
     API_KEY=your-flight-api-key
     API_SECRET=your-flight-api-secret

---

## API Endpoints

### Backend (Rust)
- **Flight Search**: `/api/flights`
  - GET: Search for flights.
  - Parameters: `origin`, `destination`, `date`, `passengers`.

- **Book Flight**: `/api/book`
  - POST: Book a flight.

- **Rideshare**: `/api/rideshare`
  - GET: Fetch available rides.
  - Parameters: `airport`, `arrival_time`.

---

## Contribution Guidelines

1. Fork the repository.
2. Create a feature branch:
   git checkout -b feature-name
3. Commit changes:
   git commit -m "Add your message here"
4. Push to the branch:
   git push origin feature-name
5. Create a pull request.

---

## License

SkyCrabby is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

---

## Contact
For questions, feedback, or support, please contact:
- **Email**: support@skycrabby.com
- **GitHub Issues**: [SkyCrabby Issues](https://github.com/SkyCrabby/CrabbyFront/issues)
