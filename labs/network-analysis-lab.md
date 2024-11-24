# Network Analysis Lab

By Christopher Razo

---

## Overview
This lab documents the process of using Wireshark to capture, analyze, and interpret network traffic for cybersecurity purposes. It focuses on understanding network activity by examining packet data and identifying patterns or anomalies.

---

## Objectives
- Learn how to use Wireshark for network traffic analysis.
- Understand common protocols such as ARP, DNS, TCP, and HTTPS.
- Identify suspicious or unexpected network activity.

---

## Tools Used
- **Wireshark v4.4.2**
- **macOS Monterey**

---

## Steps and Explanations

### Step 1. Downloading Wireshark
**Explanation**: Begin by downloading Wireshark from the official website. This ensures you're using a trusted and verified source for the software.

- **Website**: [Wireshark Download](https://www.wireshark.org/download.html)
- **Action**: Highlight the download button and confirm the version for macOS.

**Screenshot**:  
![Download Wireshark](screenshots/01-download-wireshark.png)

---

### Step 2. Installing Wireshark
**Explanation**: Install Wireshark following the standard macOS installation process. Grant necessary permissions to run the application.

**Screenshot**:  
![Installation Prompt](screenshots/02-installation-prompt.png)

---

### Step 3. Launching Wireshark
**Explanation**: Open Wireshark and allow macOS to run the application. You’ll see the welcome screen listing all available network interfaces.

**Screenshot**:  
![Welcome Screen](screenshots/03-welcome-screen.png)

---

### Step 4. Capturing Network Traffic
**Explanation**: Select the appropriate network interface (e.g., Wi-Fi) to capture live network traffic. Click the green start button to begin capturing packets.

**Screenshot**:  
![Interface Selection](screenshots/04-interface-selection.png)

---

### Step 5. Filtering Packets by Protocols
**Explanation**: Use filters to focus on specific types of network traffic. This lab examines the following protocols:
1. **ARP** (Address Resolution Protocol) – Maps IP addresses to MAC addresses.
2. **DNS** (Domain Name System) – Resolves domain names to IP addresses.
3. **TCP** (Transmission Control Protocol) – Handles reliable data transmission.
4. **HTTPS** (Hypertext Transfer Protocol Secure) – Encrypts web traffic.

**Screenshot**:  
![Packet Capture](screenshots/05-packet-capture.png)

---

### Step 6. Analyzing ARP Traffic
**Explanation**: Analyze ARP traffic to verify the relationship between IP and MAC addresses. Compare captured MAC addresses to known devices in the network. Unexpected MAC/IP combinations may indicate potential anomalies or unauthorized devices.

**Key Observations**:
- Sender IP: `10.0.0.86`
- Sender MAC: `46:c6:f7:33:ed:5d`

**Screenshot**:  
![ARP Analysis](screenshots/06-arp-analysis.png)

---

### Step 7. Analyzing DNS Traffic
**Explanation**: Review DNS traffic to understand domain resolution requests. Check for unusual domain names or excessive DNS queries, which may indicate suspicious behavior.

**Key Observations**:
- No anomalies were observed in DNS queries during this capture.

**Screenshot**:  
![DNS Analysis](screenshots/07-dns-analysis.png)

---

### Step 8. Analyzing TCP Traffic
**Explanation**: Examine TCP traffic for connections between devices. Identify the source and destination IPs, ports, and protocols. Unexpected connections could indicate unauthorized activity.

**Key Observations**:
- Source IP: `10.0.0.86`
- Destination IP: `17.57.144.102` (Apple-related service)
- Protocol: TLSv1.2

**Screenshot**:  
![TCP Analysis](screenshots/08-tcp-analysis.png)

---

### Step 9. Analyzing HTTPS Traffic
**Explanation**: Review HTTPS traffic to ensure it aligns with expected secure web activity. Look for unusual destination IPs or excessive HTTPS connections.

**Key Observations**:
- All HTTPS traffic appeared to be legitimate.
- Common endpoints include known services like Apple and Google.

**Screenshot**:  
![HTTPS Analysis](screenshots/09-https-analysis.png)

---

## Key Learnings
1. Gained hands-on experience with Wireshark’s interface and filtering features.
2. Identified patterns in ARP, DNS, TCP, and HTTPS traffic.
3. Learned to recognize suspicious activity, such as unexpected MAC/IP combinations.

---

## Next Steps
1. Export captured traffic for offline analysis.
2. Apply advanced Wireshark features like custom protocol dissectors.
3. Explore additional tools to complement Wireshark for network security analysis.

---

## References
- [Wireshark Official Documentation](https://www.wireshark.org/docs/)
- [Cybersecurity Portfolio - Christopher Razo](https://c-razo.github.io/portfolio-v2/)

---

## Notes
- Ensure screenshots are properly named and uploaded to the `screenshots/` folder within the `portfolio-v2` repository.
- Confirm all captured data aligns with privacy and ethical guidelines.
