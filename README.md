This project demonstrates a reverse proxy setup using Docker Compose with Nginx routing to two backend services.





- Two backend services (`service1` in Go, `service2` in Python/Flask) each running on separate ports.
- An Nginx reverse proxy routes:
  - `/service1/*` → Go backend (port 8001)
  - `/service2/*` → Flask backend (port 8002)
- All services run on Docker using a **single exposed port**: `localhost:8080`.


| Route             | Target Container | Description              |
| ----------------- | ---------------- | ------------------------ |
| `/service1/ping`  | `service1`       | Health/status check      |
| `/service1/hello` | `service1`       | Greeting message (Go)    |
| `/service2/ping`  | `service2`       | Health/status check      |
| `/service2/hello` | `service2`       | Greeting message (Flask) |



Features 
- Nginx reverse proxy via Dockre container
- Path prefix routing (/service1,service2)
- JSON reponses from both services
- Health checks for both services
  
