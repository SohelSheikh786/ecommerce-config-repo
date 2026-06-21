# Ecommerce Config Repo

This repository stores centralized configuration files for the **Ecommerce Microservices Project**.  
All microservices fetch their configuration from this repo via the **Spring Cloud Config Server**.

## 📂 Structure
Each microservice has its own YAML file:
- `user-service.yml`
- `product-service.yml`
- `order-service.yml`
- `payment-service.yml`
- `cart-service.yml`
- `notification-service.yml`

## ⚙️ Usage
1. Start the **Config Server** (port `8888`).
2. Each microservice includes the following in its `bootstrap.yml`:
   ```yaml
   spring:
     cloud:
       config:
         uri: http://localhost:8888
