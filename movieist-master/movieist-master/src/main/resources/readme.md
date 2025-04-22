#### Configure MongoDB

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

