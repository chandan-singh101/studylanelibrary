# Study Lane Library - Payment & Services System

A modern web application for library services management with integrated
payment processing.

## Overview

This project consists of two main components:

-   **Service Page (`service.html`)** - Library services interface with
    cart functionality\
-   **Payment Page (`payment.html`)** - Secure payment processing with
    Razorpay integration

## Features

### Service Page

-   **Service Categories:** Beverages, Stationery, Printing services\
-   **Shopping Cart:** Add items, manage quantities, view total\
-   **User Management:** Collect user details (name, phone, seat
    number)\
-   **Complaint System:** Quick complaint submission\
-   **Responsive Design:** Works on desktop and mobile devices\
-   **Modal System:** Contact, feedback, about us, and privacy policy
    modals

### Payment Page

-   **Razorpay Integration:** Secure payment processing\
-   **Auto-redirect:** Automatically opens payment modal on page load\
-   **Payment Status Handling:** Success, failure, and cancellation
    states\
-   **User Information Display:** Shows user details during payment\
-   **Database Recording:** Stores payment transactions (requires
    backend implementation)

## Setup Instructions

### Prerequisites

-   Razorpay account for payment processing\
-   Web server to host the files\
-   Backend API endpoints (as referenced in the code)

### Installation

1.  Clone or download the project files\
2.  Update the Razorpay key in `payment.html`:
    `javascript     const options = {         "key": "your_razorpay_key_here", // Replace with your actual key         // ... other options     };`
3.  Deploy to a web server\
4.  Set up backend APIs for:
    -   `/api/services` - Fetch available services\
    -   `/api/record-payment` - Store payment records\
    -   `/api/quick-complaint` - Handle complaints\
    -   `/api/contact` - Process contact forms\
    -   `/feedback` - Handle feedback submissions

## File Structure

    /
    ├── service.html          # Main services page with cart
    ├── payment.html          # Payment processing page
    └── (Backend APIs needed) # Server-side endpoints

## Usage

### For Library Staff

-   Set up services through the backend database\
-   Monitor payments through Razorpay dashboard\
-   Manage user complaints and feedback

### For Users

-   Browse available services on the service page\
-   Add items to cart with desired quantities\
-   Provide user details when placing order\
-   Complete payment through Razorpay gateway\
-   Submit complaints or feedback as needed

## Technology Stack

-   **Frontend:** HTML5, CSS3, JavaScript (ES6+)\
-   **Payment Gateway:** Razorpay\
-   **Icons:** Font Awesome 6.4.0\
-   **Styling:** Custom CSS with responsive design\
-   **Fonts:** Segoe UI system font stack

## Configuration

### Required Backend Endpoints

-   `GET /api/services` - Returns JSON array of services and items\
-   `POST /api/record-payment` - Stores payment transaction data\
-   `POST /api/quick-complaint` - Processes quick complaints\
-   `POST /api/contact` - Handles contact form submissions\
-   `POST /feedback` - Processes user feedback

### Razorpay Configuration

-   Replace test key with live key for production\
-   Configure webhooks for payment status updates\
-   Set up proper success/cancel URLs

## Browser Support

-   Chrome (recommended)\
-   Firefox\
-   Safari\
-   Edge

## Security Notes

-   Always use HTTPS in production\
-   Validate all user inputs on server side\
-   Keep Razorpay API keys secure\
-   Implement proper CORS policies for APIs

## License

© 2023 Study Lane Library. All rights reserved.
