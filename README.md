# springboot-orders-api

# Orders API — Spring Boot 3
**Objetivo:** API CRUD de órdenes con filtros y Swagger.
## Stack
- Java 17, Spring Boot 3, Spring Web, Spring Data JPA
- H2 (dev) / MySQL (prod)
- Lombok, MapStruct (opcional)
- OpenAPI/Swagger UI
## Endpoints
- `GET /orders` — paginación, filtros por `status`, `dateFrom`, `dateTo`
- `POST /orders` — crear
- `PUT /orders/{id}` — actualizar
- `DELETE /orders/{id}` — borrar
## Cómo correr (dev)
```bash
./mvnw spring-boot:run -Dspring-boot.run.profiles=dev
```
## Config
```
application-dev.yml: H2
application-prod.yml: MySQL (usar env vars) 
```
## Tests
JUnit 5, Mockito — ejemplos en src/test
## Swagger
http://localhost:8080/swagger-ui/index.html
## **Estructura sugerida:**
```text
src/main/java/.../orders
├─ controller
├─ service
├─ repository
├─ model (entity/dto)
└─config
```
