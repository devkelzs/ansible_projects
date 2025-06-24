# Project : Install and Configure a Web Server Using Ansible

## ✅ Objective

Use Ansible to automate the installation and configuration of a web server (Apache or Nginx). The server should display a custom homepage with your name.

---

## 📦 Requirements

- Install **Apache** or **Nginx** on the target machine.
- Create a homepage at `/var/www/html/index.html` with the following content:

```

Welcome to \[Your Name]'s server, managed by Ansible!

`

- Ensure the web server is **started** and **enabled** on boot.

- Target system: **Ubuntu/Debian** (using `apt`).



## 📁 Project Structure

```

ansible\_webserver/
├── files/
│   └── index.html            
├── inventory.ini            
├── playbook.yml              
└── README.md                 



---

## 🧾 Inventory File (`inventory.ini`)

Make sure you configure your inventory with the correct IPs, username, and private key:


[webservers]
```ur-server-ip> ansible_user=ubuntu ansible_ssh_private_key_file=~/.ssh/your-key.pem```
```ur-server-ip> ansible_user=ubuntu ansible_ssh_private_key_file=~/.ssh/your-ke.pem```

**USE ANSIBLE PING TO VERIFY CONNECTTION TO MANAGE NODES**

![Ping](images/Screenshot%20(161).png)
---


---

## 🚀 How to Run

From your project directory, run:

```bash
ansible-playbook -i inventory.ini playbook.yml
```

![DISPLAY](images/Screenshot%20(162).png)
---

## ✅ Test It

Open your browser and visit:

```
http://<your-server-ip>
```

You should see your custom welcome message.

![HOMEPAGE](images/Screenshot%20(160).png)

---

## 🔒 Notes

* Ensure SSH access to your remote machines is working.
* Port 22 (SSH) and port 80 (HTTP) should be open in your security group.
* Works on Ubuntu 20.04/22.04/24.04. For CentOS, replace `apt` with `yum` and `apache2` with `httpd`.

---

