***ZPhishier – Social Media Phishing Simulaton***

-----
**Summary**
ZPhishier is an educational phishing-simulation project built with ZPhisher on Kali Linux, running in a local VM environment. It automates the creation of cloned social-media login pages, demonstrating how easily credentials can be harvested from unsuspecting users. This documentation covers objectives, setup, execution details, results, and recommended best practices for security awareness and prevention.

-----
**Objective**

- To illustrate phishing mechanics ethically for security awareness and training.
- To demonstrate capture of credentials via cloned login pages.

**Scope**

- Simulation only (no real targets).
- Local-only deployment (VM).
- Focused on social-media site templates.
-----
**Legal & Ethical Disclaimer**

**Important:** This tool is strictly for educational and awareness purposes. Unauthorized phishing—against real users or networks—is illegal and unethical. Always obtain explicit permission before any penetration testing or phishing simulations [IRJMETS](https://www.irjmets.com/uploadedfiles/paper/issue_12_december_2024/65449/final/fin_irjmets1734768076.pdf?utm_source=chatgpt.com)[GitHub](https://github.com/htr-tech/zphisher?utm_source=chatgpt.com).

-----
**Attack Overview**

**-Phishing Type**

Cloning of popular social media login pages (e.g., Facebook, Instagram) to harvest credentials.

**-Delivery Method**

Links are generated and tested locally; no external distribution in this demo.

**-Target Audience**

General public (demonstration only on the attacker’s own machine).

-----
**Tools & Environment**

- **ZPhisher**: automated open-source phishing tool with 30+ templates.
- **Operating System**: Kali Linux (inside a virtual machine).
- **Environment**: Local VM (no public hosting).
-----
**Setup & Configuration**

1. **VM Preparation**
   1. Spin up a Kali Linux VM (VirtualBox/VMware).
   1. Ensure Internet access within VM for installing dependencies.
1. **Install ZPhisher**
1. **Launch ZPhisher**

Bash ./zphisher.sh

1. Choose the social-media template.
1. Select “Localhost” or “Serveo/Ngrok” (for local demos, localhost is sufficient). 
-----
**Execution Steps**

1. **Generate Phishing Link**
   1. ZPhisher displays a URL (e.g., http://localhost:8080/facebook).
1. **Simulate User Interaction**
   1. Open the link in a browser tab.
   1. Enter any credentials (email/username + password).
1. **Credential Capture**
   1. ZPhisher logs credentials in the terminal and saves them to logs/ directory.
-----
**Results & Analysis**

- **Captured Data**
  - Plaintext usernames/passwords printed in terminal and stored on disk.
- **Security Triggers**
  - No automated detection in this local setup (real-world defenses like anti-phish filters would block such URLs).
-----
**Mitigation & Recommendations**

**“Do not click on suspicious, catchy messages from unknown sources.”**

1. **User Training**
   1. Regular phishing awareness programs with simulated tests [CISA](https://www.cisa.gov/secure-our-world/teach-employees-avoid-phishing?utm_source=chatgpt.com)[CybeReady](https://cybeready.com/phishing-awareness-training/phishing-prevention-best-practices?utm_source=chatgpt.com).
   1. Teach employees to verify links and check sender domains before interacting [Microsoft Support](https://support.microsoft.com/en-us/windows/protect-yourself-from-phishing-0c7ea947-ba98-3bd9-7184-430e1f860a44?utm_source=chatgpt.com).
1. **Technical Controls**
   1. Enforce email authentication: SPF, DKIM, DMARC to block spoofed senders [CybeReady](https://cybeready.com/phishing-awareness-training/phishing-prevention-best-practices?utm_source=chatgpt.com).
   1. Use web-filtering/proxy to detect and block known phishing domains [NCSC](https://www.ncsc.gov.uk/guidance/phishing?utm_source=chatgpt.com).
   1. Multi-Factor Authentication (MFA) on all critical accounts to mitigate credential theft [NCSC](https://www.ncsc.gov.uk/guidance/phishing?utm_source=chatgpt.com).
1. **Incident Response**
   1. Establish clear reporting channels for suspected phishing (e.g., “Report Phish” button).
   1. Conduct follow-up training for any user who clicks or submits credentials

-----
**Demo Video**

