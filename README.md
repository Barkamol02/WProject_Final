# 🎮 Movie Review Website

This is a Movie Review Website built using **React** for the frontend and **Java (Spring Boot)** for the backend. It allows users to view movies and post reviews. The backend uses **MongoDB** to store movie and review data.

---

## 🛠 Prerequisites

Ensure the following are installed on your system:

- Node.js (v16 or higher)
- npm (v7 or higher)
- Java (JDK 17)
- Maven (for Java backend build)
- MongoDB (Local or Cloud instance)
- MongoDB Compass *(optional)*

---

## 🚀 Setup Instructions

### 1. Clone the Repository

```bash
git clone <repository-url>
cd movie-review-website
```

---

### 2. Backend Configuration (Spring Boot)

#### a. Configure MongoDB

- Open MongoDB Compass or your preferred MongoDB client.
- Create a new database (e.g., `movie_reviews_db`) and note the database name and collections (e.g., `movies`, `reviews`).
- Update the MongoDB connection details in `backend/src/main/resources/application.properties`:

```properties
spring.data.mongodb.database=your_db_name
spring.data.mongodb.uri=your_connection_uri
```

- Set the following environment variables on your system:
  - MongoDB database name
  - Connection URI to your cluster

#### b. Build and Run the Backend

```bash
cd backend
mvn clean install
mvn spring-boot:run
```

The backend will run on: [http://localhost:8080](http://localhost:8080)

---

### 3. Frontend Configuration (React)

#### a. Install Dependencies

```bash
cd frontend  # or movie-gold-v1-master if applicable
npm install
```

#### b. Run the Frontend

```bash
npm start
```

The frontend will run on: [http://localhost:3000](http://localhost:3000)

---

### 4. Database Configuration

- Ensure MongoDB database and collections are created (`movies`, `reviews`).
- Confirm environment variables match your MongoDB setup.
- If collection names are customized, make sure they match the backend code.

---

### 5. Using the Application

1. Open your browser and go to [http://localhost:3000](http://localhost:3000)
2. Browse the list of movies displayed on the homepage.
3. Click a movie to view details and post a review.
4. Reviews will be saved to MongoDB and shown on the movie's detail page.

---

## 📁 Project Structure

```
final/
├── backend/                    # Spring Boot backend
│   ├── src/
│   ├── pom.xml
│   └── src/main/resources/application.properties
├── frontend/                   # React frontend
│   ├── src/
│   ├── package.json
│   └── public/
└── README.md
```

---

## 🧹 Troubleshooting

- **MongoDB Connection Issues:** Ensure environment variables are set and MongoDB server is accessible.
- **Port Conflicts:** If `localhost:3000` or `localhost:8080` is in use, change the ports in your code.
- **CORS Issues:** Configure Spring Boot to allow requests from `http://localhost:3000`.
- **Environment Variables Not Loading:** Make sure they are correctly set, or use a library like `dotenv` in your backend.
- **SSL/TLS Handshake Error:** Add your IP to the IP Access List in MongoDB Compass.

---

## 🧰 Technologies Used

- **Frontend:** React
- **Backend:** Java, Spring Boot, Spring Data MongoDB
- **Database:** MongoDB
- **Build Tools:** npm, Maven

---

## 🤝 Contributing

Feel free to fork the repository and submit pull requests for improvements or bug fixes.

---

## 📜 License

This project is licensed under the **MIT License**.

