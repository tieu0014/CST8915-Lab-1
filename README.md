# CST8915 Lab 1: Algonquin Pet Store on Azure VM

**Student Name**: Eric Tieu
**Student ID**: 041273376
**Course**: CST8915 Full-stack Cloud-native Development
**Semester**: Fall 2026

---

## Demo Video

🎥 [Watch Demo Video](https://www.youtube.com/watch?v=4za2wbY-_yg)

---

## Technical Explanations

### Order Service (Node.js)

Order service utilizes 'express' a minimal Node.js framework to parse incoming data, in this case in the form of JSON and CORS to allow API request from different origins, the front end. It responds to orders sent from the front end, 'Store Front' on port 3000 and sends it to RABBITMQ.

### Product Service (Rust)

Product service utilizes CORS to allow access from any origin, specifically the frontend running on another server. The product service server also restricts requests to only GET requests. Once a request is made it sends an JSON array of product objects. It listens for these requests on port 3030.

### Store Front (Vue.js)

The store front displays the front end, it uses a script to fetch product information from the Product Service using a REST API on port 3030.
