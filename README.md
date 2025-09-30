# Ansible: Declarative Automation at Scale  🚀

This project is a **mini CI/CD lab** built with **Docker, Ansible, and Jenkins**.  
It demonstrates how automation tools can be combined to provision infrastructure and deploy an application in a reproducible way.

---

## 🔹 What this project is about

- We create three containers using Docker Compose:
  - **Node1** → Ansible controller (the “master”)
  - **Node2 & Node3** → managed nodes that will serve a static HTML page

- Ansible is used to:
  - Install Apache web server on Node2 and Node3
  - Deploy a simple HTML page (`Hello from ansible-nodeX`)
  - Ensure the web server is running

- Jenkins is introduced to show how the same Ansible playbook can be executed automatically as part of a **CI/CD pipeline** instead of running it manually.

---

## 🔹 Why this is useful

- Understand the **Ansible architecture**: one controller managing multiple nodes.  
- Learn how to **orchestrate containers** with Docker Compose.  
- See how **infrastructure automation (Ansible)** can be integrated with **CI/CD (Jenkins)**.  
- End result: when you open your browser, each managed node serves its own webpage — deployed automatically.

---

## 🔹 Workflow Summary

1. **Setup the lab** using Docker Compose → brings up 3 containers.  
2. **Run the Ansible playbook** from Node1 → installs Apache and copies the HTML page to Node2 & Node3.  
3. **Access the result** in a browser:
   - Node2 → `http://localhost:9081`
   - Node3 → `http://localhost:9082`  
   Each will show “Hello from ansible-nodeX”.
4. **Automate with Jenkins** → pipeline runs the playbook inside a container, making deployment part of CI/CD.

---

## 🔹 Final Output

✅ Node2 webpage:  
![Node2 webpage](<img width="700" height="418" alt="image" src="https://github.com/user-attachments/assets/ed10b944-4d05-40ea-9024-c1682ebf79f7" />
)

✅ Node3 webpage:  
![Node3 webpage](<img width="692" height="431" alt="image" src="https://github.com/user-attachments/assets/604936bc-3d66-4496-b1d6-64314a903c90" />
)

✅ Jenkins pipeline showing successful build:  
![Jenkins pipeline](<img width="1898" height="477" alt="image" src="https://github.com/user-attachments/assets/31425f3c-b149-4803-b33e-9df6146064b0" />
)

---

## 📝 Author
👩‍💻 **Hitanshi N Patil**  
🔗 [GitHub Profile](https://github.com/Hitanshi-N-Patil)
