# B.A.T.M.A.N. Advanced (batman-adv) Setup Guide

## 1 Run the Installation Script:
```
chmod +x install_batman_adv.sh
./install_batman_adv.sh
```
## 2 Running and Testing the Setup

### 2.1 Create BATMAN Interfaces:
You need to create BATMAN virtual interfaces for your network devices. Replace eth0 with your actual network interface.
```
sudo batctl if add eth0
```

### 2.2 Bring Up the BATMAN Interface:
"Bring Up the BATMAN Interface" means to configure and activate the BATMAN (Better Approach To Mobile Ad-hoc Networking) interface on your system. This involves setting up the BATMAN-Adv (BATMAN Advanced) protocol, which operates on Layer 2 (data link layer) to create a mesh network.
```
sudo ifconfig bat0 up
```

### 2.3 Assign an IP Address to the BATMAN Interface:
```
sudo ifconfig bat0 " IP adress "
```

## 3 Running The Project:

### 3.1 Run the Installation Script:
If you have a script (batmanInstall.sh) to install BATMAN-Adv, run it as follows:
```
cd network-auto-configuration-master/batman
./batmanInstall.sh
```
### 3.2 Run the Configuration Script:

After installation, run the configuration script (configure_batman.sh):
```
./configure_batman.sh
```

## 4 Verification

### 4.1 Check the BATMAN Interface:
```
ifconfig bat0
```

### 4.2 Verify BATMAN-Adv Nodes: 
This should display the nodes connected in the BATMAN-Adv network.
```
sudo batctl n
```
By following these steps and using the provided scripts, you should be able to install and configure BATMAN-Adv in your project successfully. Make sure to adapt IP addresses and interface names to your specific network configuration.
