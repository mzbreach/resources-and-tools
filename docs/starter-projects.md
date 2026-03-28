# Starter Projects

These projects are designed for students and early-career practitioners who want to build practical skills in red teaming, OT/ICS security, and physical security research. Each project is self-contained, uses legal methods, and produces a documented artifact that can serve as a portfolio piece.

---

## Project 1: ICS Network Protocol Lab with Conpot

**Objective:** Deploy an ICS honeypot in a local virtual machine, capture and analyze the traffic it generates, and document what an attacker would observe when probing an exposed ICS device.

**Rough scope:**

- Set up a Linux VM (Ubuntu or Debian recommended).
- Install [Conpot](https://github.com/mushorg/conpot), an open-source ICS/SCADA honeypot that simulates Modbus, DNP3, and SNMP services.
- Use Wireshark to capture traffic on the VM's loopback interface while probing the honeypot with tools like Nmap and the Redpoint NSE scripts.
- Document the protocol traffic, what the probing tools report, and what a defender would see in the logs.

**Skills built:** ICS protocol familiarity (Modbus, DNP3), network traffic analysis, honeypot configuration, documentation.

**Why it matters:** Understanding what ICS devices expose to the network is foundational for both attacking and defending them. This project gives you that baseline without touching any real industrial systems.

---

## Project 2: OSINT Profile on a Public Organization

**Objective:** Using only publicly available information, build a structured intelligence profile on a publicly traded company or government agency of your choice. Document your methodology and findings.

**Rough scope:**

- Choose a target organization with significant public presence (public companies or government agencies are good choices because they have broad public disclosure requirements).
- Use tools like Shodan, theHarvester, OSINT Framework, and LinkedIn to gather information about the organization's internet-facing infrastructure, employee structure, and technology footprint.
- Document each step: what you queried, what you found, and what an attacker could infer from it.
- Include a section on what the organization is doing well and what could be improved from an exposure-reduction standpoint.

**Skills built:** OSINT methodology, tool usage (Shodan, theHarvester), structured reporting, defensive awareness.

**Why it matters:** OSINT is the first phase of almost every authorized engagement. This project teaches you to document your process, which is a core professional skill.

---

## Project 3: Home Network Vulnerability Assessment

**Objective:** Conduct an authorized assessment of your own home network, document the attack surface, and produce a remediation report.

**Rough scope:**

- Map your network with Nmap to identify all connected devices.
- Run a web vulnerability scan against your router's admin interface using OWASP ZAP or Nikto.
- Check firmware versions against public CVE databases for your router model.
- Document your findings in a short report following a standard structure: executive summary, findings (severity-rated), and recommendations.

**Skills built:** Network scanning, vulnerability research, CVE analysis, report writing.

**Why it matters:** Writing a professional vulnerability report is a skill that takes practice. Doing it on your own network gives you full authorization and a realistic target. The output is a tangible portfolio artifact.

---

## Project 4: ATT&CK Threat Model for a Fictional Facility

**Objective:** Using the MITRE ATT&CK for ICS matrix, build a threat model for a fictional water treatment facility. Map likely adversary techniques, identify detection gaps, and propose mitigations.

**Rough scope:**

- Review the [ATT&CK for ICS matrix](https://attack.mitre.org/matrices/ics/) and select 8-10 techniques relevant to water treatment operations (e.g., manipulating setpoints, inhibiting alarms).
- Use the ATT&CK Navigator to create a visual heat map of covered techniques.
- For each technique, document: what the attack looks like, what a defender would need to detect it, and one concrete mitigation.
- Write a one-page executive summary suitable for a non-technical audience.

**Skills built:** Threat modeling, ATT&CK framework usage, ICS-specific threat thinking, executive communication.

**Why it matters:** Threat modeling is a core defensive skill that also makes you a better red teamer. Understanding what defenders look for shapes how you think about adversary simulation.

---

## Project 5: Physical Security Observation and Documentation Report

**Objective:** Conduct a non-intrusive physical security observation of a public building or campus (library, university building, coffee shop, etc.) and document the observable access control environment.

**Rough scope:**

- Choose a publicly accessible location you are legally permitted to be in.
- Observe and document: entry points, door hardware types (latch type, presence of deadbolts, electric strikes), badge reader types if visible, camera placement, tailgating susceptibility, and visitor management practices.
- Do not touch, probe, or interact with any security hardware. Observation only.
- Write a short report documenting what you observed, what security controls are present, and what common physical security weaknesses, if any, are observable.

**Skills built:** Physical security awareness, professional observation and documentation, report writing.

**Why it matters:** Physical security assessments begin with reconnaissance. This project builds the observation and documentation habits used in authorized physical engagements while remaining entirely passive and legal.
