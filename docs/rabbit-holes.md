# Rabbit Holes

Security research rarely follows a straight line. These are subtopics encountered while exploring red teaming, OT/ICS, and physical security that turned out to be deeper and more interesting than expected. Each entry includes a brief explanation of why it matters and a few observations.

---

## Protocol Archaeology: Legacy Industrial Protocols

**Why it is interesting:** Many OT environments still run protocols designed in the 1970s and 1980s, long before security was a consideration. Modbus, DNP3, and PROFIBUS were built for reliability and speed, not authentication or encryption. Understanding why they were designed this way reveals a lot about the constraints industrial engineers faced.

**Observations:**

- Modbus, developed by Modicon in 1979, has no authentication. Any device on the network can send commands. This is not a bug — it was a deliberate design choice for simplicity.
- DNP3 added a Secure Authentication extension (SAv5) but adoption has been slow because retrofitting authentication into existing deployments is expensive.
- Many ICS devices cannot be updated or replaced easily; a PLC running in a plant may be expected to operate for 20-30 years.

**Where to start:** The [Modbus specification](https://www.modbus.org/modbus-specifications) is publicly available and short. Reading it alongside a Wireshark capture of Modbus traffic is illuminating.

---

## The Stuxnet Rabbit Hole

**Why it is interesting:** Stuxnet (discovered 2010) remains the most technically sophisticated publicly analyzed piece of malware ever documented. It exploited four zero-day vulnerabilities, forged digital certificates, and physically destroyed centrifuges at a nuclear enrichment facility by subtly manipulating PLC code. Every layer of this story reveals something important.

**Observations:**

- Stuxnet targeted a specific Siemens STEP 7 configuration. Machines without the exact target configuration would receive the malware but not activate the payload.
- The rootkit component hid the malicious ladder logic from engineers reviewing the PLC program — the machines appeared to be running normally on monitors while being actively damaged.
- Ralph Langner's initial public analysis (2010) remains a good technical reference. Kim Zetter's *Countdown to Zero Day* covers the full story in narrative form.

**Where to start:** [Langner's Stuxnet Deep Dive (PDF)](https://otbase.com/wp-content/uploads/2025/08/to-kill-a-centrifuge.pdf)

---

## Bump Keys and the Lock Security Rating Problem

**Why it is interesting:** Most pin tumbler locks sold at hardware stores are vulnerable to bump key attacks. A bump key costs very little to make and can open a standard deadbolt in seconds without leaving obvious signs of entry. The security ratings on consumer locks rarely reflect this.

**Observations:**

- Lock security standards (ANSI/BHMA grades) measure resistance to picking and forced entry, but bump key resistance is not always explicitly tested.
- High-security locks like Medeco and Abloy use design features (rotating pins, sidebar mechanisms) that defeat bumping. They cost significantly more.
- This gap between perceived security and actual security is a recurring theme in physical security research.

**Where to start:** TOOOL's published research on bump key vulnerabilities, and the LockPickingLawyer's comparisons of security-rated versus consumer locks.

---

## Software-Defined Radio and Industrial Wireless

**Why it is interesting:** Industrial environments increasingly use wireless communications for sensors, meters, and telemetry. Much of this wireless traffic is unencrypted and can be received passively with inexpensive SDR hardware. This opens a passive reconnaissance surface that is easy to overlook.

**Observations:**

- Smart meters (AMI) often use 900 MHz ISM band protocols like ANSI C12.22. Traffic can be decoded passively with tools like rtl_433.
- Some older SCADA radio systems still use unencrypted serial-over-radio links that were designed before widespread SDR hardware was available.
- GNU Radio and SDR# are common starting points for SDR experimentation.

**Where to start:** The [Great Scott Gadgets SDR tutorials](https://greatscottgadgets.com/sdr/) and rtl_433 on GitHub for decoding common sensor protocols.

---

## The Insider Threat Dimension in OT

**Why it is interesting:** Most ICS security discussions focus on external attackers. But statistically, a significant portion of ICS incidents involve insiders — disgruntled employees, contractors with standing access, or mistakes by authorized users. The social and organizational layer is just as important as the technical one.

**Observations:**

- The 2000 Maroochy Water Services attack in Australia was carried out by a disgruntled ex-contractor using stolen radio equipment. He released millions of liters of sewage.
- Control system vendors often retain remote access capabilities for support purposes. Credential management for vendor accounts is a common gap.
- CISA's ICS security guidance dedicates sections to access management and supply chain risk for this reason.

**Where to start:** CISA's ICS recommended practices documentation covers insider threat controls. The Maroochy case is well documented in academic ICS security literature.

---

## The MITRE ATT&CK for ICS Matrix

**Why it is interesting:** The standard ATT&CK framework is well known. The ICS-specific extension covers tactics and techniques that map to industrial environments specifically — including things like inhibiting safety systems, manipulating control logic, and spoofing sensor data. It is a different set of adversary behaviors than what you see in enterprise IT attacks.

**Observations:**

- The ICS matrix includes a "Impair Process Control" tactic with no direct equivalent in the enterprise matrix. This reflects attacks that cause physical harm rather than data theft.
- Mapping real ICS incidents like Ukraine 2015/2016 and Triton to the ATT&CK for ICS matrix reveals which techniques are most commonly observed in the wild.
- Detection opportunities in ICS environments are more limited than in IT environments, which shapes how defenders approach the problem.

**Where to start:** [ATT&CK for ICS Matrix](https://attack.mitre.org/matrices/ics/) and the accompanying technique pages, which include mitigations and detection notes.
