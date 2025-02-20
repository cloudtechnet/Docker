Here’s a step-by-step guide for installing Docker on an Ubuntu 22.04 EC2 instance on AWS:

### **1. Launch an EC2 Instance with Ubuntu 22.04**

1. **Login to AWS Console**:
   - Go to the AWS Management Console and login.

2. **Launch an EC2 Instance**:
   - Select **EC2** from the services.
   - Click on **Launch Instance**.
   - Choose an **Ubuntu 22.04 LTS** AMI (Amazon Machine Image).
   - Select an **Instance Type** (e.g., `t2.micro` for testing).
   - Configure **Instance Details**, **Storage**, and **Security Group** to allow SSH access (port 22).
   - Launch the instance and connect via SSH using your key pair.

### **2. Update the System**

Before installing Docker, it is recommended to update the system's package index and installed packages.

```bash
sudo apt update -y
sudo apt upgrade -y
```

### **3. Install Required Packages**

Install required dependencies:

```bash
sudo apt install -y apt-transport-https ca-certificates curl software-properties-common
```

### **4. Add Docker’s Official GPG Key**

Add Docker’s GPG key to your system to verify the packages:

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

### **5. Set up the Docker Repository**

Add Docker’s official repository to your APT sources list.

```bash
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

### **6. Update the Package Index Again**

After adding the Docker repository, update the package index again:

```bash
sudo apt update -y
```

### **7. Install Docker**

Now install Docker on your EC2 instance:

```bash
sudo apt install -y docker-ce docker-ce-cli containerd.io
```

### **8. Start Docker and Enable it to Run at Boot**

Start the Docker service and enable it to run at boot:

```bash
sudo systemctl start docker
sudo systemctl enable docker
```

### **9. Verify Docker Installation**

Check if Docker is installed correctly:

```bash
sudo docker --version
```

You should see something like:
```
Docker version 20.10.17, build 100c701
```
