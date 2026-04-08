# Day 6 — Vagrant and Linux Servers

## Key Focus
- VM creation using Vagrant
- Automating server setup (Nginx, WordPress)
- Multi-VM configuration
- Basics of system services using systemctl

---

## Topics Covered

### 1. Vagrant Virtual Machines
- Vagrant is used to create reproducible development environments  
- It uses a `Vagrantfile` to define VM configuration  

Basic commands:
```bash
vagrant init
vagrant up
vagrant ssh
```

---

### 2. VM Configuration (IP, RAM, CPU)

Example configuration in Vagrantfile:

```ruby
config.vm.network "private_network", ip: "192.168.33.10"

config.vm.provider "virtualbox" do |vb|
  vb.memory = "1024"
  vb.cpus = 2
end
```

---

### 3. Sync Directories
- Used to share files between host and VM  

```ruby
config.vm.synced_folder ".", "/vagrant"
```

---

### 4. Provisioning (VERY IMPORTANT)
- Provisioning automates setup of the VM  

Example:

```ruby
config.vm.provision "shell", inline: <<-SHELL
  sudo apt update
  sudo apt install -y nginx
SHELL
```

👉 This eliminates manual setup every time VM is created  

---

### 5. Website Setup (Nginx)
- Installed Nginx inside VM  
- Started service  

```bash
sudo systemctl start nginx
sudo systemctl enable nginx
```

---

### 6. WordPress Setup
- Learned basic steps to deploy WordPress  

Requires:
- Web server (Nginx/Apache)  
- Database (MySQL)  
- PHP  

---

### 7. Automation
- Automated website + WordPress setup using provisioning scripts  
- Similar to Infrastructure Automation (DevOps concept)  

---

### 8. Copilot AI
- Used AI (GitHub Copilot) to generate commands/scripts  
- Helps speed up DevOps tasks  

---

### 9. Multi VM Setup

Example:

```ruby
config.vm.define "web" do |web|
  web.vm.network "private_network", ip: "192.168.33.10"
end

config.vm.define "db" do |db|
  db.vm.network "private_network", ip: "192.168.33.11"
end
```

---

### 10. systemctl & Tomcat
- `systemctl` is used to manage services  

```bash
systemctl status nginx
systemctl start nginx
systemctl enable nginx
```

- Learned basics of Tomcat deployment  

---

## Hands-On Practice

Today I performed the following:

- Created a VM using Vagrant  
- Configured RAM, CPU, and IP  

SSH into VM:

```bash
vagrant ssh
```

- Installed Nginx inside VM  
- Started Nginx service  
- Opened browser and accessed website using VM IP  

---

## What Confused Me Today

**Problem:**  
Initially, I couldn’t access the website from my browser  

**Reason:**  
VM IP was not configured correctly / network not reachable  

**Fix:**

- Checked IP in Vagrantfile  
- Restarted VM:

```bash
vagrant reload
```

**Lesson:**  
Always verify network configuration when working with VMs  

---

## Key Commands to Remember

```bash
vagrant init
vagrant up
vagrant ssh
vagrant halt
vagrant reload
vagrant destroy
vagrant global-status --prune

systemctl start nginx
systemctl enable nginx
systemctl status nginx
```

---

## Interview Questions I Can Answer

- What is Vagrant and why is it used?  
- What is provisioning in Vagrant?  
- How do you automate server setup?  
- How does Vagrant differ from Docker?  
- What is systemctl used for?  

---

## What I Learned (Big Picture)

- Vagrant helps create consistent environments  
- Provisioning = automation (core DevOps concept)  
- Manual setup is replaced by scripts  
- Foundation for tools like Terraform and Ansible  

---

## What I Would Improve

- Try multi-VM setup (web + DB)  
- Automate full WordPress deployment  
- Explore Ansible for provisioning instead of shell scripts  

---

## Tomorrow’s Plan

- Continue next section  
- Focus more on automation concepts  
- Practice breaking and fixing VM setups
