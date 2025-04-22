# 🎥 Movieist - Spring Boot Backend

This is a Spring Boot backend application for a movie-related service named **Movieist**. It includes a global **CORS (Cross-Origin Resource Sharing)** configuration to enable frontend applications to interact with the backend across different origins.

---

## 🚀 Getting Started

### 📦 Prerequisites

Make sure you have the following installed:

- Java JDK 17
- Maven
- Spring Boot CLI (optional, for running via CLI)
- An IDE like IntelliJ IDEA or VSCode

---

### ▶️ Running the Application

1. Clone the repository or copy the code.
2. Open the project in your IDE.
3. Run the `MovieistApplication` class as a Java application.

Or from terminal:

```bash
mvn spring-boot:run
```

The backend will be accessible at:  
**`http://localhost:8080`**

---

## 🔐 CORS Configuration

This application allows all origins, methods, and headers. It’s globally configured using a `WebMvcConfigurer` bean:

```java
registry.addMapping("/**")
        .allowedOrigins("*")
        .allowedMethods("*")
        .allowedHeaders("*")
        .allowCredentials(false)
        .maxAge(3600);
```

### ⚠️ Note

- In production, it's recommended to **restrict CORS** to specific origins and methods to ensure better security.
- Adjust the `.allowedOrigins()` and `.allowedMethods()` as needed.

---

## 🧰 Technologies Used

- Java 17
- Spring Boot
- Maven
- Spring Web MVC

---

## 📄 License

This project is licensed under the MIT License.

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

