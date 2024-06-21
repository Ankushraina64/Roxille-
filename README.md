# MERN Stack Coding Challenge

This project is a MERN stack application that interacts with a third-party API to fetch, store, and display product transaction data. It includes APIs for various data operations and visualizations, as well as a frontend to present the data in tables and charts.

## Table of Contents

- [Project Overview](#project-overview)
- [Installation](#installation)
- [Backend](#backend)
  - [APIs](#apis)
- [Frontend](#frontend)
  - [Features](#features)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

The application consists of two main parts:

1. **Backend**: A Node.js/Express server with MongoDB for data storage. The server fetches transaction data from a third-party API and provides endpoints for data operations and visualizations.
2. **Frontend**: A React application that interacts with the backend APIs to display transaction data in a table and various charts.

## Installation

### Prerequisites

- Node.js
- MongoDB
- npm or yarn

### Backend

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/mern-coding-challenge.git
    cd mern-coding-challenge
    ```

2. Install backend dependencies:

    ```bash
    cd backend
    npm install
    ```

3. Create a `.env` file in the `backend` directory and add your MongoDB URI:

    ```env
    MONGO_URI=your_mongodb_uri
    ```

4. Start the backend server:

    ```bash
    npm start
    ```

### Frontend

1. Install frontend dependencies:

    ```bash
    cd ../frontend
    npm install
    ```

2. Start the frontend development server:

    ```bash
    npm start
    ```

## Backend

### APIs

The backend provides the following APIs:

#### Initialize Database

- **Endpoint**: `/api/init`
- **Method**: GET
- **Description**: Fetches JSON data from the third-party API and initializes the database with seed data.

#### List Transactions

- **Endpoint**: `/api/transactions`
- **Method**: GET
- **Description**: Lists all transactions. Supports search and pagination.
- **Parameters**:
  - `month`: Month to filter transactions (January to December).
  - `search`: Search text for product title/description/price.
  - `page`: Page number for pagination.
  - `perPage`: Number of items per page.

#### Statistics

- **Endpoint**: `/api/statistics`
- **Method**: GET
- **Description**: Provides statistics for the selected month.
- **Parameters**:
  - `month`: Month to filter transactions (January to December).

#### Bar Chart

- **Endpoint**: `/api/bar-chart`
- **Method**: GET
- **Description**: Provides data for a bar chart showing price ranges and the number of items in each range.
- **Parameters**:
  - `month`: Month to filter transactions (January to December).

#### Pie Chart

- **Endpoint**: `/api/pie-chart`
- **Method**: GET
- **Description**: Provides data for a pie chart showing unique categories and the number of items in each category.
- **Parameters**:
  - `month`: Month to filter transactions (January to December).

#### Combined Data

- **Endpoint**: `/api/combined`
- **Method**: GET
- **Description**: Combines data from the Statistics, Bar Chart, and Pie Chart APIs.
- **Parameters**:
  - `month`: Month to filter transactions (January to December).

## Frontend

### Features

- **Transactions Table**: Displays a list of transactions with search and pagination functionalities.
- **Statistics**: Shows total sales amount, total sold items, and total unsold items for the selected month.
- **Bar Chart**: Displays the number of items in various price ranges for the selected month.
- **Pie Chart**: Shows the number of items in unique categories for the selected month.

## Usage

1. Start the backend server.
2. Start the frontend development server.
3. Open `http://localhost:3000` in your browser to view the application.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request.


