# DevOps Internship Assessment

## 📋 Objective
Containerize and deploy a **Next.js** application using:
- Docker
- GitHub Actions
- GitHub Container Registry (GHCR)
- Kubernetes (Minikube)

---

## ⚙️ Setup Instructions

### 1️⃣ Run Locally
```bash
npm install
npm run dev
```
App runs on: http://localhost:3000

---

### 2️⃣ Build & Run with Docker
```bash
docker build -t nextjs-app .
docker run -p 3000:3000 nextjs-app
```
App runs on: http://localhost:3000

---

### 3️⃣ GitHub Actions CI/CD
On push to **main**, GitHub Actions:
- Builds Docker image
- Pushes image to **GitHub Container Registry (GHCR)**

---

### 4️⃣ Deploy to Minikube
Start Minikube:
```bash
minikube start
```
Apply manifests:
```bash
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
```
Access the app:
```bash
minikube service nextjs-service
```

---

## 🧠 Evaluation Focus
- Docker optimization
- GitHub Actions workflow correctness
- Kubernetes configuration quality
- Documentation clarity

---

## 👩‍💻 Author
Your Name  
[GitHub Profile](https://github.com/Sarabjeeth-kaur)
