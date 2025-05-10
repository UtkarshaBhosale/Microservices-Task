# 🥉 Microservices Task

This document helps you test multiple microservices — **User**, **Product**, **Order**, and **Gateway** — after running the `docker-compose` file. Each service exposes endpoints that can be verified using `curl` or directly in a browser.

---

## ✨ Services and Endpoints

### 👤 **User Service**

* **Base URL:** `http://localhost:3000`
* **Endpoints:**

  * **List Users:**

    ```bash
    curl http://localhost:3000/users
    ```

    <img src="https://github.com/user-attachments/assets/1de70369-7ec7-4f34-b31a-41d9833bf800" width="600" />

    🔗 Or open in your browser: [http://localhost:3000/users](http://localhost:3000/users) <img src="https://github.com/user-attachments/assets/f5c30de5-59fc-4606-b356-b0d9044341a5" width="600" />

---

### 🚙 **Product Service**

* **Base URL:** `http://localhost:3001`
* **Endpoints:**

  * **List Products:**

    ```bash
    curl http://localhost:3001/products
    ```

    <img src="https://github.com/user-attachments/assets/08f92f69-b838-402c-a3b7-b487b9c3debf" width="600" />

    🔗 Or open in your browser: [http://localhost:3001/products](http://localhost:3001/products) <img src="https://github.com/user-attachments/assets/0b2756a8-0366-4f42-a61c-41b682295bac" width="600" />

---

### 📦 **Order Service**

* **Base URL:** `http://localhost:3002`
* **Endpoints:**

  * **List Orders:**

    ```bash
    curl http://localhost:3002/orders
    ```

    <img src="https://github.com/user-attachments/assets/979e7844-71bb-44cc-a493-301cb62bd681" width="600" />

    🔗 Or open in your browser: [http://localhost:3002/orders](http://localhost:3002/orders) <img src="https://github.com/user-attachments/assets/5945ccfd-52cb-4c12-a0eb-d7021c32b338" width="600" /> <img src="https://github.com/user-attachments/assets/46147c8c-a57f-4704-93e4-928ecc7e6628" width="600" />

---

### 🌐 **Gateway Service**

* **Base URL:** `http://localhost:3003/api`
* **Endpoints:**

  * **Users:**

    ```bash
    curl http://localhost:3003/api/users
    ```

    <img src="https://github.com/user-attachments/assets/533b0137-8313-46c1-bef7-abc08879dbbd" width="600" />

  * **Products:**

    ```bash
    curl http://localhost:3003/api/products
    ```

    <img src="https://github.com/user-attachments/assets/861e5437-a066-4798-ad1b-c317f43777cf" width="600" />

  * **Orders:**

    ```bash
    curl http://localhost:3003/api/orders
    ```

    <img src="https://github.com/user-attachments/assets/6a5e84ba-542c-46f5-a5f9-5269530d9836" width="600" />

---

## 🛠️ Getting Started

1. 📦 **Start all services** using Docker Compose:

   ```bash
   docker-compose up
   ```

   <img src="https://github.com/user-attachments/assets/21726e6c-aa76-48fc-a880-285901ab7453" width="600" />

2. ✅ **Verify each service** using the `curl` commands or by visiting the browser URLs listed above.

---

## 🧰 Troubleshooting

* ❌ **Service not accessible?**

  * Ensure Docker is running.
  * Check container logs:

    ```bash
    docker-compose logs <service-name>
    ```

* ⚠️ **Port already in use?**

  * Stop other applications using the port or update the `docker-compose.yml` file to use different ports.

* 🐘 **Database connection issues?**

  * Make sure the database container is up and properly linked (if applicable).

* 🌐 **Gateway returns 404 or empty response?**

  * Confirm the internal service it's routing to is up and running.
  * Check `gateway` configuration files for routing paths.

---

## 🤝 Contributing

We welcome contributions! Here’s how you can help:

1. 🍝 Fork the repository.
2. 🌿 Create a new branch (`git checkout -b feature/my-feature`).
3. 💻 Make your changes and commit them (`git commit -m 'Add my feature'`).
4. 📤 Push to the branch (`git push origin feature/my-feature`).
5. ✅ Open a Pull Request.

---

## 🧪 IT Contribution

This setup supports:

* 🚀 Rapid local testing of microservices and their communication.
* ✅ Validating end-to-end integration across services using the API Gateway.
* 🔎 Isolating service behavior to test individual business logic.

---

## 🧯 Troubleshooting During IT Validation

* 🧪 Validate each microservice independently before checking through the gateway.
* 🔄 Restart individual containers if only one service is failing:

  ```bash
  docker-compose restart <service-name>
  ```
* 🔍 Inspect service logs or add logging statements for debugging internal failures.

---

## 🎉 Happy Testing!

Feel free to reach out or open issues for improvements, bugs, or ideas!
Together, we build better software. 🛠️🚀
