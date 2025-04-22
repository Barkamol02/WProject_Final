Movie Review Website
This is a Movie Review Website built using React for the frontend and Java (Spring Boot) for the backend. The application allows users to view movies and post reviews. The backend uses MongoDB as the database to store movie and review data.
Prerequisites
Before running the application, ensure you have the following installed:

Node.js (v16 or higher)
npm (v7 or higher)
Java (JDK 17)
Maven (for building the Java backend)
MongoDB (Local or Cloud instance, accessible via MongoDB Compass)
MongoDB Compass (optional, for database management)

Setup Instructions
1. Clone the Repository
git clone <repository-url>
cd movie-review-website

2. Backend Configuration (Java/Spring Boot)
a. Configure MongoDB

Open MongoDB Compass or your preferred MongoDB client.
Create a new database (e.g., movie_reviews_db) and note the database name and collection names (e.g., movies, reviews).
Update the MongoDB connection details in the application.properties file located in backend/src/main/resources/:

spring.data.mongodb.database=<your-database-name>
spring.data.mongodb.uri=<your-mongodb-uri>


Set the following environment variables on your system:
The name of your MongoDB database
A link to your MongoDB cluster



b. Build and Run the Backend

Build the project using Maven:

mvn clean install


Run the Spring Boot application:

mvn spring-boot:run

The backend will start on http://localhost:8080.
3. Frontend Configuration (React)
a. Install Dependencies

Navigate to the frontend directory:

cd movie-gold-v1-master


Install the required npm packages:

npm install

b. Run the Frontend

Start the React development server:

npm start

The frontend will start on http://localhost:3000 and automatically open in your default browser.
4. Database Configuration

Ensure the MongoDB database and collections are set up in MongoDB Compass or your MongoDB client.
Verify that the environment variables are correctly set to match your MongoDB setup.
If you customize collection names (e.g., movies, reviews), ensure they align with your backend code.

5. Using the Application

Open your browser and navigate to http://localhost:3000.
Browse the list of movies displayed on the homepage.
Click on a movie to view its details and post a review.
Reviews will be saved to the MongoDB database and displayed on the movie's page.

Project Structure
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

Troubleshooting

MongoDB Connection Issues: Verify the environment variables and ensure the MongoDB server is accessible.
Port Conflicts: If localhost:3000 or localhost:8080 is in use, change the ports in your code.
CORS Issues: Ensure the backend allows requests from http://localhost:3000 by configuring CORS in the Spring Boot application.
Environment Variables Not Loading: Ensure the environment variables are set correctly or use a library like dotenv in the backend to load them from a .env file.
SSL/TLS Handshake Error: Make sure your IP address is added to the IP Access List in MongoDB Compass.

Technologies Used

Frontend: React
Backend: Java, Spring Boot, Spring Data MongoDB
Database: MongoDB
Build Tools: npm, Maven

Contributing
Feel free to fork the repository and submit pull requests for improvements or bug fixes.
License
This project is licensed under the MIT License.

