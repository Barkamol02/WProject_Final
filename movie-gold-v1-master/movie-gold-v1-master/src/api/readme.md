# 🌐 Connecting backed to frontend

This configuration sets up **Axios**, a promise-based HTTP client, to connect your frontend React application with the Spring Boot backend running at `http://localhost:8080`.

---

## 📄 Configuration File (axios.js)

```js
import axios from 'axios';

export default axios.create({
    baseURL: 'http://localhost:8080',
    headers: {
        "ngrok-skip-browser-warning": "true"
    }
});
```

---

## 🧩 Purpose

- `baseURL`: Specifies the root URL for all HTTP requests made using this Axios instance.
- `ngrok-skip-browser-warning`: This header bypasses ngrok's browser warning when testing APIs via a tunnel. It's safe to leave it during local development.

---

## 🚀 Usage

In your components or services, import the configured Axios instance:

```js
import api from './axios';

api.get('/movies')
   .then(response => console.log(response.data))
   .catch(error => console.error(error));
```

---

## 🛠 Notes

- Change the `baseURL` if your backend is hosted elsewhere (e.g., production URL or ngrok tunnel).
- For secure deployments, consider managing headers and base URLs via environment variables.

---

## 📦 Technologies

- Axios
- React
- Spring Boot (Backend)

---

## 📄 License

This snippet is part of the **Movieist Project** and licensed under the MIT License.

