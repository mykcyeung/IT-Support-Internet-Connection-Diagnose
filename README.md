# IT-Support-Internet-Connection-Diagnose
# 🌐 Internet Connection Check (CMD)

## 📌 Overview
This project is a simple check of internet connectivity using Windows Command Prompt (CMD).  

### 1. Check external connectivity
* bash: ping 8.8.8.8
* Checks if the device can reach the internet using an IP address
* If successful > internet connection is working
* Failed: No internet connection
   *  Restart WiFi/router
   *  Check network cable or WiFi connection
   *  Try reconnecting to network
   *  Contact ISP if issue persists


### 2. Check DNS resolution (domain name test)
* bash: ping google.com
* Tests if domain names can be converted into IP addresses
* If this fails but IP ping works > DNS issue
* Failed: DNS is broken
   *  ipconfig /flushdns : renew cache
   * Change DNS settings (e.g. 8.8.8.8 or 1.1.1.1)
   *  Restart network adapter


### 3. View network configuration
* bash: ipconfig
* Displays IP address, subnet mask, default gateway, and DNS settings
* Failed: DHCP failed (no IP assigned)
  *  ipconfig /release, ipconfig /renew : renew IP address
  *  Restart router
  *  Ensure DHCP is enabled on network

