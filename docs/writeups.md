# Writeups and Case Studies

Reading how real incidents unfolded — and how practitioners approached authorized testing — is one of the most efficient ways to build intuition for this field. The resources here include public incident analyses, technical blog posts, and educational writeups.

---

## Landmark ICS and OT Incidents

- [Dragos: CRASHOVERRIDE / Industroyer Analysis](https://www.dragos.com/blog/industry-news/crashoverride-reassessing-the-2016-ukraine-electric-power-event/) — Technical analysis of the malware used in the 2016 Ukraine power grid attack. One of the few publicly documented cases of malware designed specifically to disrupt industrial control systems.
- [Mandiant: APT44 / SANDWORM Threat Actor Overview](https://www.mandiant.com/resources/blog/apt44-unearthing-sandworm) — Mandiant's reporting on the threat actor behind multiple destructive ICS attacks, including the Ukraine grid incidents. Useful for understanding how nation-state actors approach ICS targeting.
- [CISA/FBI: Triton/TRISIS Advisory](https://www.cisa.gov/news-events/ics-advisories/icsa-18-240-01) — Government advisory on the Triton malware, which targeted safety instrumented systems (SIS). The first publicly confirmed attack designed to disable industrial safety systems.
- [Kim Zetter: The Untold Story of the World's Most Dangerous Malware (Wired)](https://www.wired.com/story/notpetya-cyberattack-ukraine-russia-code-crashed-the-world/) — Narrative account of NotPetya, which caused over $10 billion in damage and disrupted industrial operations globally. Essential context for understanding real-world attack consequences.

---

## Red Team and Penetration Testing Writeups

- [SpecterOps Blog](https://posts.specterops.io/) — Research blog from the team behind BloodHound, Ghostwriter, and other red team tools. Posts frequently cover Active Directory attack techniques, detection engineering, and adversary simulation methodology.
- [harmj0y (Will Schroeder) Blog](https://harmj0y.medium.com/) — Technical deep-dives on Active Directory, Kerberos abuse, and Windows post-exploitation. Widely referenced in red team training programs.
- [Red Team Journal](https://redteamjournal.com/) — Long-running practitioner publication covering red team program development, methodology, and organizational dynamics. More strategic than technical.
- [Daniel Miessler: USecD](https://danielmiessler.com/blog/) — Practitioner writing covering security fundamentals, OSINT methodology, and security career development. Consistently high quality and beginner-accessible.

---

## Physical Security Writeups

- [Deviant Ollam: Talk Resources and Papers](https://www.deviantollam.com/library/) — Slide decks and supporting materials from Deviant Ollam's conference talks on physical penetration testing, lock bypassing, and access control weaknesses.
- [Recurity Labs: Physical Security Assessment](https://www.recurity-labs.com/) — European security firm with published physical security assessments and research. Covers tailgating, badge cloning, and sensor bypass.
- [DEF CON Physical Security Village Talk Archives](https://www.youtube.com/@physecvillage) — Recorded talks from the Physical Security Village at DEF CON. Covers lockpicking, badge cloning, RFID attacks, and social engineering in physical contexts.

---

## Vulnerability Research and CVE Analyses

- [Claroty Team82 Research](https://claroty.com/team82/research) — Detailed write-ups of ICS and IoT vulnerabilities discovered by Claroty researchers. Well-documented with CVE references and remediation guidance.
- [Project Zero Blog](https://googleprojectzero.blogspot.com/) — Google's zero-day research blog. Technical depth is high; posts on browser, OS, and hypervisor vulnerabilities provide good models for thorough vulnerability documentation.
- [CERT/CC Vulnerability Notes](https://www.kb.cert.org/vuls/) — CERT Coordination Center's public vulnerability database. Includes ICS-relevant entries and coordinated disclosure documentation.

---

## Educational Blog Series

- [PortSwigger Web Security Academy](https://portswigger.net/web-security) — Free, structured curriculum covering web application vulnerabilities with accompanying hands-on labs. One of the best free resources for building web security fundamentals.
- [HackTricks](https://book.hacktricks.xyz/) — Community-maintained reference for penetration testing techniques. Broad coverage including Windows, Linux, web, and network attack patterns in an authorized testing context.
- [The Hacker Recipes](https://www.thehacker.recipes/) — Structured guides for Active Directory, web application, and network attack techniques. Focused on authorized testing methodology.
- [SANS Reading Room](https://www.sans.org/white-papers/) — Archive of practitioner-written white papers covering ICS security, threat hunting, incident response, and security architecture. Free to access.
