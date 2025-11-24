# 📝 Guestbook App - Docker & Kubernetes Deployment

## ⚡ Tech Stack

![Go](https://img.shields.io/badge/Go-00ADD8?logo=go&logoColor=white) 
![Docker](https://img.shields.io/badge/Docker-blue?logo=docker&logoColor=white) 
![Kubernetes](https://img.shields.io/badge/Kubernetes-blue?logo=kubernetes&logoColor=white) 
![OpenShift](https://img.shields.io/badge/OpenShift-red?logo=redhat&logoColor=white) 
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white) 
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white) 
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black) 
![GitHub](https://img.shields.io/badge/GitHub-black?logo=github&logoColor=white) 
![IBM Cloud](https://img.shields.io/badge/IBM%20Cloud-0072C6?logo=ibm&logoColor=white) 
![CI/CD](https://img.shields.io/badge/CI/CD-blueviolet) 
![API](https://img.shields.io/badge/API-gray?logo=swagger&logoColor=white)

---

## About

This Guestbook application is a simple web-based app that allows users to submit entries and view them in real-time.  
It is part of **IBM Skills Network: Introduction to Containers with Docker, Kubernetes & OpenShift**.  

** The project demonstrates:**

- Building a **multi-stage Docker image**  
- Deploying to **Kubernetes**  
- Autoscaling using **Horizontal Pod Autoscaler (HPA)**  
- Performing **Rolling Updates and Rollbacks**  
- Deployment on **OpenShift clusters**

---

## Project Structure
```
v1/guestbook/
      ├─ Dockerfile
      ├─ deployment.yml
      ├─ main.go
      └─ public/
      ├─ index.html
      ├─ script.js
      ├─ style.css
      └─ jquery.min.js
```

---

## 🚀 Features

- **Frontend**: Web-based guestbook interface  
- **Backend**: Go (Golang) application  
- **Containerization**: Docker multi-stage build  
- **Deployment**: Kubernetes Deployment & Pods  
- **Scaling**: Horizontal Pod Autoscaler  
- **Versioning**: Rollouts and Rollbacks  

---

## 🛠️ Usage

1. **Build Docker Image**  

```bash
export MY_NAMESPACE=sn-labs-$USERNAME
docker build -t us.icr.io/$MY_NAMESPACE/guestbook:v1 .
docker push us.icr.io/$MY_NAMESPACE/guestbook:v1
```
2. **Deploy to Kubernetes**
```bash
kubectl apply -f deployment.yml
kubectl port-forward deployment.apps/guestbook 3000:3000
```

3. **Access Application**
Open browser at: [http://localhost:3000](http://localhost:3000)

---

## 🧩 Contributing

Contributions are welcome!
To contribute:

- Fork the repository

- Create your feature branch: git checkout -b feature-name

- Commit your changes: git commit -m "Add some feature"

- Push to the branch: git push origin feature-name

- Open a Pull Request

---

## 👤 Author

**Umme Sanjeda**  
🔗 GitHub: [https://github.com/usan-here](https://github.com/usan-here)  

---

## 📄 License

This project is licensed under the Apache License 2.0.
See LICENSE
 for details.

Built as part of IBM Skills Network Labs for learning containerization and orchestration technologies.
