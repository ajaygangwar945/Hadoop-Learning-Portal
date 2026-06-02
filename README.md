 <img src="hadoop_banner.png" alt="Hadoop Learning Portal Banner" width="100%" height="200" style="object-fit: contain; background: #0d1117; border-radius: 8px;" />

<h1 align="center"> Hadoop Learning Portal</h1>

<p align="center">
  <a href="https://ajaygangwar945.github.io/Hadoop-Learning-Portal/">
    <img src="https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-FFD700?style=for-the-badge&logo=github&logoColor=black" alt="Live Demo" />
  </a>
  <a href="https://hub.docker.com/r/ajaygangwar945/hadoop-learning-portal">
    <img src="https://img.shields.io/badge/Docker%20Hub-Repository-0db7ed?style=for-the-badge&logo=docker&logoColor=white" alt="Docker Hub" />
  </a>
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" />
  <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white" alt="Nginx" />
</p>

---

## 🌟 Overview

The **Hadoop Learning Portal** is a sleek, modern, and interactive single-page educational application designed to help developers, students, and big data enthusiasts learn the fundamentals and advanced ecosystems of Apache Hadoop.

This repository contains everything from conceptual explanations of Big Data and core Hadoop architecture to practical code snippets for Apache Hive, HBase, Cassandra, and standard Java utility programs. It is built as a highly responsive web application, packaged with Docker, and deployed via standard automated CI/CD workflows.

🔗 **Explore the Live App:** [Hadoop Learning Portal Live](https://ajaygangwar945.github.io/Hadoop-Learning-Portal/)

---

## 🚀 Key Features

* **Introduction to Big Data:** Clear breakdown of Structured, Semi-Structured, and Unstructured data, as well as the **5 V's of Big Data** (Volume, Velocity, Variety, Veracity, Value).
* **Hadoop Core Architecture:** Detail-rich explanations of major core components:
  * **NameNode & DataNode** (Storage)
  * **JobTracker & TaskTracker** (MapReduce Processing)
  * **YARN Architecture** (Resource Manager, Node Manager, Application Master, Containers)
* **Hands-on Command Guide:** Ready-to-use commands for **HDFS**, **MapReduce**, and database systems.
* **Java Programming Snippets:** Practical implementations for general arithmetic and algorithmic tasks (Factorial, Palindrome, Armstrong numbers, Sum of Evens).
* **Multi-Database Ecosystem Coverage:**
  * **Apache Hive:** HiveQL operations, partitioning, and bucketing.
  * **Apache HBase:** Column family management, NoSQL querying, and prefix filters.
  * **Apache Cassandra:** Key-space creation, replication strategies, and query styling.
* **Interactive FAQs:** Expandable accordion system addressing the most common big data technical questions.
* **Premium Dark UI/UX:** Responsive interface featuring frosted glassmorphic card elements, custom neon highlight schemes, smooth animations, and code block formatting.

---

## 🛠️ Tech Stack & Structure

* **Frontend:** Pure HTML5 & Vanilla CSS3 (highly responsive, responsive grid system, micro-animations, glassmorphic UI).
* **Server:** Nginx (Alpine-based light weight image).
* **Containerization:** Docker.
* **CI/CD:** GitHub Actions (automated builds and publishes to Docker Hub).

### Repository File Architecture

```text
├── .github/
│   └── workflows/
│       └── docker.yaml        # GitHub Actions workflow for building & pushing Docker image
├── Apache Hadoop.svg          # Official vector graphic/icon for Apache Hadoop
├── Dockerfile                 # Configuration to package the application with Nginx Alpine
├── index.html                 # The single-page responsive educational web application
├── hadoop_banner.png          # High-tech generated banner image
├── README.md                  # Visual guide and repository documentation (This File)
└── DOCUMENTATION.txt          # Technical specifications and comprehensive learning outline
```

---

## 🐳 Dockerization & Deployment

This project is fully containerized using **Nginx on Alpine Linux** to ensure high-performance static file serving and minimal memory footprint.

### Running Locally with Docker

1. **Build the Docker Image:**

    ```bash
    docker build -t hadoop-learning-portal .
    ```

2. **Run the Container:**

    ```bash
    docker run -d -p 8080:80 --name hadoop-portal-instance hadoop-learning-portal
    ```

3. **Access the Application:**
    Open your browser and navigate to `http://localhost:8080`.

---

## ⚙️ CI/CD Pipeline

The project features a fully automated deployment pipeline integrated with **GitHub Actions**:

* **Trigger:** Automated build on every push to the `main` branch.
* **Platform:** Runs on `ubuntu-latest`.
* **Action Flow:**
    1. Checkouts the source code.
    2. Logs into Docker Hub using encrypted secrets.
    3. Builds the production-ready Docker image.
    4. Tags the image with both the running build number and the `latest` tag.
    5. Pushes the built image tags to the public Docker Hub repository: `ajaygangwar945/hadoop-learning-portal`.

## 📝 Authors

* **Ajay Gangwar** - [ajaygangwar945](https://github.com/ajaygangwar945)
