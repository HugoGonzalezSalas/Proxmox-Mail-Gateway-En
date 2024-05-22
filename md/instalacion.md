# Installing Proxmox Mail Gateway on a Virtual Machine in Proxmox VE

## Prerequisites

Before starting, ensure you meet the following requirements:

- **CPU**: Modern 64-bit compatible processor.
- **RAM**: Minimum 2 GB, 4 GB or more recommended.
- **Storage**: At least 32 GB of disk space.
- **Network**: Compatible network card.
- **Host Operating System**: Proxmox VE installed and configured.

## Step 1: Download the Proxmox Mail Gateway ISO

1. **Download the ISO**:
   - Download the Proxmox Mail Gateway ISO from the following link: [Proxmox Mail Gateway ISO](https://www.proxmox.com/en/downloads/proxmox-mail-gateway/iso/proxmox-mail-gateway-8-1-iso-installer).

## Step 2: Upload the ISO to Proxmox VE

1. **Access the Proxmox VE web interface**:
   - Open a web browser and navigate to your Proxmox VE server's IP address.
   - Log in with your credentials.

2. **Upload the ISO**:
   - In the side panel, select the node where you want to create the VM.
   - Go to the "Content" tab of the storage where you want to upload the ISO.
   - Click "Upload" and select the downloaded ISO.

## Step 3: Create the Virtual Machine

1. **Create a new VM**:
   - In the side panel, select the node where you want to create the VM.
   - Click "Create VM".
   - Configure the VM with the following parameters:
     - **Name**: Proxmox Mail Gateway
     - **OS**: Select "Use CD/DVD disc image file (iso)" and choose the Proxmox Mail Gateway ISO you uploaded.
     - **System**: Use the default settings.
     - **Hard Disk**: Allocate at least 32 GB.
     - **CPU**: Allocate at least 2 CPU cores.
     - **Memory**: Allocate at least 2 GB (4 GB or more recommended).
     - **Network**: Configure the network as needed (bridge or NAT).

2. **Finish creating the VM**:
   - Review and confirm the VM configuration.
   - Click "Finish".

## Step 4: Start the Virtual Machine and Install Proxmox Mail Gateway

1. **Start the VM**:
   - Select the created VM in the side panel.
   - Click "Start" to boot the VM.
   - Click "Console" to access the installation screen.

2. **Install Proxmox Mail Gateway**:
   - Accept the license terms.
   - Select the disk for installing Proxmox Mail Gateway.
   - Configure the language and timezone settings.
   - Set the root password and provide an email address for alerts.
   - Configure the FQDN, server IP, gateway, and DNS.
   - Review and confirm the configuration.
   - Complete the installation and restart the VM.

## Step 5: Access the Proxmox Mail Gateway Web Interface

1. **Access the web interface**:
   - Open a web browser and navigate to `https://<MAIL_GATEWAY_IP>:8006`.
   - Ignore any security certificate warnings.

2. **Log in**:
   - Username: `root`
   - Password: The root password set during installation.

3. **Configure and manage Proxmox Mail Gateway**:
   - Once logged in, you will have access to the Proxmox Mail Gateway administration interface where you can configure and manage your email policies.

## Video Tutorial

You can watch a detailed video tutorial of the installation process at the following link: [Proxmox Mail Gateway Installation Tutorial](https://www.youtube.com/watch?v=94W16qtx8n8).
