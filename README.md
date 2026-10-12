<div align="center">

# ⚙️ Student Management : chaîne DevOps complète

**Application Spring Boot de gestion des étudiants, livrée par une chaîne CI/CD Jenkins avec analyse de qualité et supervision.**

![Java](https://img.shields.io/badge/Java-17-ED8B00?logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?logo=springboot&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?logo=jenkins&logoColor=white)
![SonarQube](https://img.shields.io/badge/SonarQube-4E9BCD?logo=sonarqube&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?logo=prometheus&logoColor=white)

</div>

## ✨ Contenu

- **Application** : API REST Spring Boot (étudiants, départements, cours, inscriptions) avec Spring Data JPA.
- **Intégration continue** : pipeline Jenkins (`Jenkinsfile`) qui récupère le code, compile avec Maven et lance l'analyse **SonarQube**.
- **Conteneurisation** : `Dockerfile` pour construire l'image de l'application.
- **Supervision** : Prometheus configuré via `monitoring/docker-compose.yaml`.

## 🔁 Pipeline

```
GitHub ──▶ Jenkins ──▶ mvn compile ──▶ SonarQube (qualité) ──▶ image Docker ──▶ supervision Prometheus
```

## 🚀 Lancer

```bash
./mvnw spring-boot:run
docker compose -f monitoring/docker-compose.yaml up -d
```

---
👩‍💻 Réalisé par **Maram Rzeigui** · [LinkedIn](https://www.linkedin.com/in/maram-rzeigui/)
