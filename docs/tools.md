# Tools

The tools listed here are open-source, publicly available, and widely used in research, lab, and authorized testing contexts. They are organized by category to help you identify what is relevant to your current learning focus.

**Always use tools in authorized environments only.** Running these against systems you do not own or have explicit permission to test is illegal.

---

## OSINT and Reconnaissance

- [Maltego](https://www.maltego.com/) — Graph-based OSINT platform for mapping relationships between entities (people, domains, IPs, organizations). Used for pre-engagement research and threat intelligence workflows. The community edition is free and functional for learning.
- [Shodan](https://www.shodan.io/) — Search engine for internet-connected devices, including exposed ICS/SCADA systems, industrial protocols, and misconfigured services. Essential for understanding the ICS attack surface on the public internet.
- [OSINT Framework](https://osintframework.com/) — Visual directory of OSINT tools organized by category. Good starting point when you need to identify the right tool for a specific research task.
- [theHarvester](https://github.com/laramies/theHarvester) — Command-line tool for gathering emails, subdomains, hosts, and employee names from public sources. Commonly used in the reconnaissance phase of authorized engagements.
- [Recon-ng](https://github.com/lanmaster53/recon-ng) — Modular web reconnaissance framework. Useful for automating OSINT data collection in a structured, repeatable way.

---

## Web Security

- [Burp Suite Community Edition](https://portswigger.net/burp) — Industry-standard web application security testing proxy. The free Community Edition is sufficient for learning. PortSwigger's Web Security Academy provides accompanying labs.
- [OWASP ZAP](https://www.zaproxy.org/) — Open-source web application scanner maintained by OWASP. Good alternative to Burp for automated scanning in lab environments.
- [Nikto](https://github.com/sullo/nikto) — Web server scanner that checks for known vulnerabilities, misconfigurations, and outdated software. Useful for quick baseline assessments in authorized lab testing.
- [SQLMap](https://sqlmap.org/) — Automated SQL injection detection and exploitation tool. Widely used in web application security research and CTF challenges.

---

## Network Analysis

- [Wireshark](https://www.wireshark.org/) — The standard network protocol analyzer. Critical for understanding industrial protocols (Modbus, DNP3, EtherNet/IP) by capturing and dissecting traffic in a lab.
- [Nmap](https://nmap.org/) — Network discovery and security scanner. The foundation of network-level reconnaissance in authorized assessments. Includes NSE scripts for ICS protocol detection.
- [Zeek (formerly Bro)](https://zeek.org/) — Network traffic analysis framework used heavily in ICS/OT environments for protocol inspection and anomaly detection. Understanding Zeek helps with both offense and defense.

---

## RFID and Hardware Research

- [Proxmark3](https://hackerwarehouse.com/product/proxmark3-rdv4-kit/) — Open-source RFID research platform. Used to read, analyze, and clone RFID credentials in authorized physical security assessments. Understanding how it works exposes common access control weaknesses.
- [Flipper Zero](https://flipper.net/) — Multi-protocol portable security research tool covering RFID, NFC, sub-GHz radio, infrared, and more. Popular for hands-on physical security research in lab and authorized contexts.
- [HackRF](https://greatscottgadgets.com/hackrf/) — Software-defined radio (SDR) hardware for transmitting and receiving radio signals. Used for analyzing wireless protocols, including those found in industrial environments.
- [Binwalk](https://github.com/ReFirmLabs/binwalk) — Firmware analysis tool used to extract and analyze embedded file systems. Relevant for ICS device firmware research.

---

## ICS and OT Analysis

- [GrassMarlin](https://github.com/nsacyber/GRASSMARLIN) — NSA-released passive network mapping tool for ICS/SCADA environments. Generates topology maps without sending active traffic, making it safer for sensitive OT networks.
- [Redpoint](https://github.com/digitalbond/Redpoint) — Nmap NSE scripts from Digital Bond specifically designed to enumerate ICS devices and protocols (Modbus, BACnet, EtherNet/IP). Useful for authorized ICS network assessments.
- [PLCScan](https://github.com/yanlinlin82/plcscan) — Utility for scanning and identifying PLC devices on a network. Informative for understanding what ICS assets are exposed in a given environment.
- [Conpot](https://github.com/mushorg/conpot) — Low-interaction ICS/SCADA honeypot. Useful for studying attacker behavior targeting industrial systems in a controlled environment.

---

## AI and Machine Learning Security Testing

- [Garak](https://github.com/leondz/garak) — LLM vulnerability scanner that probes language models for jailbreaks, prompt injection, and unsafe outputs. Useful for anyone researching AI model security.
- [TextAttack](https://github.com/QData/TextAttack) — Python framework for adversarial attacks, data augmentation, and training in NLP. Used in AI security research to test model robustness.
- [ART (Adversarial Robustness Toolbox)](https://github.com/Trusted-AI/adversarial-robustness-toolbox) — IBM open-source library for testing ML model robustness against adversarial examples. Covers image, text, and tabular models.

---

## Frameworks and Platforms

- [Metasploit Framework](https://www.metasploit.com/) — The most widely used open-source penetration testing framework. Most red team training involves Metasploit at some stage. Use only in authorized lab environments.
- [MITRE ATT&CK Navigator](https://mitre-attack.github.io/attack-navigator/) — Web tool for visualizing and annotating ATT&CK matrices. Useful for planning simulated adversary behavior, gap analysis, and detection coverage mapping.
- [ATT&CK for ICS](https://attack.mitre.org/matrices/ics/) — Extension of the ATT&CK framework covering adversary tactics specific to industrial control systems. Essential reference for ICS threat modeling.

---

## Marketplaces

- [Red Team Tools](https://www.redteamtools.com/) — Great website for finding and purchasing tools to assist offensive security assessments.
- [Hacker Warehouse](https://hackerwarehouse.com/) — Another excellent website for finding and purchasing tools to assist offensive security assessments.
