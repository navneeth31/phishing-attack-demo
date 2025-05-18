# ZPhishier – Social Media Phishing Simulator

---

> ⚠️ **Warning:** I'm not responsible—this is for educational purposes only!!

---

## Summary
ZPhishier is an educational phishing-simulation project built with ZPhisher on Kali Linux, running in a local VM environment. It automates the creation of cloned social-media login pages, demonstrating how easily credentials can be harvested from unsuspecting users. This documentation covers objectives, setup, execution details, results, and recommended best practices for security awareness and prevention.

---

## Objective
- To illustrate phishing mechanics ethically for security awareness and training.  
- To demonstrate capture of credentials via cloned login pages.

## Scope
- Simulation only (no real targets).  
- Local-only deployment (VM).  
- Focused on social-media site templates.

---

## Legal & Ethical Disclaimer
**Important:** This tool is strictly for educational and awareness purposes. Unauthorized phishing—against real users or networks—is illegal and unethical. Always obtain explicit permission before any penetration testing or phishing simulations :contentReference[oaicite:1]{index=1}.

---

## Attack Overview
**Phishing Type**  
Cloning of popular social media login pages (e.g., Facebook, Instagram) to harvest credentials.  
**Delivery Method**  
Links are generated and tested locally; no external distribution in this demo.  
**Target Audience**  
General public (demonstration only on the attacker’s own machine).

---

## Tools & Environment
- **ZPhisher**: automated open-source phishing tool with 30+ templates :contentReference[oaicite:2]{index=2}.  
- **Operating System**: Kali Linux (inside a virtual machine).  
- **Environment**: Local VM (no public hosting).

---

## Setup & Configuration
1. **VM Preparation**  
   - Spin up a Kali Linux VM (VirtualBox/VMware).  
   - Ensure Internet access within VM for installing dependencies.  
2. **Install ZPhisher**
   ```bash
   sudo apt update && sudo apt install git
   git clone https://github.com/htr-tech/zphisher.git
   cd zphisher
   chmod +x zphisher.sh
