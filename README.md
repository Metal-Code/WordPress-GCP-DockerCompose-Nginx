# WordPress-GCP-DockerCompose-Nginx

## 📌 Aim
Deploy a WordPress site on **Google Cloud Platform (GCP)** using **Docker** and **Nginx**.

---

## 🛠 Steps & Commands

### 1️⃣ Create a VM Instance on GCP
1. Create a new VM instance (name it anything, e.g., `wordpress`).
2. Choose **Free Tier e2-micro** instance.
3. Change OS to **Ubuntu**.
4. Set disk size to **20 GB** or more.
5. Allow **HTTP** and **HTTPS** traffic.
6. Click **Create**.

---

### 2️⃣ Connect to VM via SSH
```bash
# Click on SSH in the GCP console for your instance
