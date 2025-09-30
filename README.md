# Ansible: Declarative Automation at Scale 🚀

This project is a **mini CI/CD lab** built with **Docker, Ansible, and Jenkins**.  
It demonstrates how automation tools can be combined to provision infrastructure and deploy an application in a reproducible, automated way.

---

## 🔹 What this project is about

- Three containers are created using Docker Compose:
  - **Node1** → Ansible controller (the “master”)
  - **Node2 & Node3** → managed nodes that will serve a static HTML page

- **Ansible** is used to:
  - Install the Apache web server on Node2 and Node3  
  - Deploy a simple HTML page (`Hello from ansible-nodeX`)  
  - Ensure the web server is running  

- **Jenkins** is used to demonstrate how the same Ansible playbook can be executed automatically as part of a **CI/CD pipeline** instead of being run manually.

---

## 🔹 Why this is useful

- Understand the **Ansible architecture**: one controller managing multiple nodes  
- Learn how to **orchestrate containers** with Docker Compose  
- See how **infrastructure automation (Ansible)** integrates with **CI/CD (Jenkins)**  
- End result → each managed node serves its own webpage, deployed automatically  

---

## 🔹 Workflow Summary

1. **Set up the lab** using Docker Compose → brings up 3 containers  
2. **Run the Ansible playbook** from Node1 → installs Apache and deploys the HTML page on Node2 & Node3  
3. **Access the results** in a browser:
   - Node2 → `http://localhost:9081`
   - Node3 → `http://localhost:9082`  
   Each displays “Hello from ansible-nodeX”  
4. **Automate with Jenkins** → pipeline executes the playbook in a container, making deployment part of CI/CD  

---

## 🔹 Final Output

✅ Node2 webpage:  
![Node2 webpage](https://github.com/user-attachments/assets/1b381827-bc2e-4905-91cb-d256d40cc89e)

✅ Node3 webpage:  
![Node3 webpage](https://github.com/user-attachments/assets/b32fa7d3-e377-41ce-ab02-b12054184371)

✅ Jenkins pipeline showing successful build:  
![Jenkins pipeline](https://github.com/user-attachments/assets/dd5e966a-075c-4b6a-a696-d0a307ba978c)

---

## 📝 Author

👩‍💻 **Hitanshi N Patil**  
🔗 [GitHub Profile](https://github.com/Hitanshi-N-Patil)
