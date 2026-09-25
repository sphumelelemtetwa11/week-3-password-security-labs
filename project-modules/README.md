# Week 3 Project Modules: PDF Password Recovery

This page documents the two coursework exercises for recovering the password to the provided **My Locked PDF1.pdf** lab file. The steps below follow the Module 1 and Module 2 handouts. Add your own screenshots in the evidence spots after completing each step.

> **Authorized lab files only:** Both handouts describe sending the PDF or its password hash to an online service. Only use the non-sensitive practice PDF supplied for this assignment, and first check that your instructor permits the upload. Never upload personal, confidential, or third-party PDFs. Do not publish the PDF, recovered password, or full hash in this public repository.

## Project Module 1: John the Ripper and Johnny

**Goal:** Use John the Ripper (JTR) and its Johnny graphical interface to audit the password protection on the course-provided PDF.

### Steps

1. **Get the lab file.** Download `My Locked PDF1.pdf` from the course materials and keep your working copy in a lab folder. Do not use a personal or confidential PDF.
2. **Install the tools.** Download John the Ripper from the [official Openwall John page](https://www.openwall.com/john/). Get Johnny from the source specified in the assignment handout. Install or extract both as instructed.
3. **Configure Johnny.** Open Johnny, go to its settings, and browse to the `john.exe` executable in the John installation's `run` folder. Save the setting.
4. **Extract the PDF hash.** The handout uses the [OnlineHashCrack PDF hash extractor](https://www.onlinehashcrack.com/tools-pdf-hash-extractor.php). If your instructor authorizes using that service with the supplied practice file, upload the lab PDF and copy the complete PDF hash it returns. Otherwise, use only an instructor-approved local method. Do not use an online extractor with a real or sensitive document.
5. **Save the hash for Johnny.** Paste the complete hash into a plain-text file named `hash1.txt`, following the format shown in the handout. Avoid adding labels, wrapping, or missing characters. Keep this file private; do not commit it.
6. **Load the hash and run the audit.** In Johnny, open `hash1.txt`, select the attack options shown in the handout, and start the session. Let the run complete or record that no password was recovered during your test.
7. **Verify the result.** If the tool recovers a candidate, test it by opening your local lab PDF. Record whether it opened and any timing shown by the tool, but do not put the password or hash in this repository.
8. **Capture evidence.** Add screenshots of the setup, hash-file loading, Johnny session/result, and successful PDF opening (if applicable). Redact the password, full hash, and any unrelated personal information.

### Module 1 evidence

<img width="948" height="1000" alt="hash1 extracted" src="https://github.com/user-attachments/assets/f5da9288-288a-42a1-8e14-0f2b87341cf0" />


<img width="934" height="1064" alt="Johnny password recovered " src="https://github.com/user-attachments/assets/d4346c7d-f5e5-4494-89bc-185c102f223f" />

<img width="947" height="1070" alt="PDF Verification" src="https://github.com/user-attachments/assets/2fb4eb7b-c987-4b93-8ee7-bdc27cc800f0" />




## Project Module 2: Networkwalks Hash Calculator and Password Cracker

**Goal:** Use the two Networkwalks browser-based tools from the assignment to calculate a PDF hash and test password candidates against it.

### Steps

1. **Get the lab file.** Download the course-provided `My Locked PDF1.pdf` from the [Networkwalks project task page](https://networkwalks.com/project-task-lab-password-cracking-with-networkwalks-tools/). Keep it in your lab folder.
2. **Open the Hash Calculator.** In a browser, open the [Networkwalks Hash Calculator](https://networkwalks.com/hash-calculator/).
3. **Calculate the PDF hash.** Upload only the authorized practice PDF. Copy the complete hash produced for the PDF (the handout shows a value beginning with `$pdf$`). Do not truncate or retype it.
4. **Open the Password Cracker.** In a separate browser tab, open the [Networkwalks Password Cracker](https://networkwalks.com/password-cracker/).
5. **Run the password audit.** Paste the complete hash into the tool and start the test as described in the handout. Wait for the tool to finish; results depend on the candidate search and password complexity.
6. **Verify the result.** If a candidate is recovered, enter it into your local copy of the lab PDF and confirm whether it opens. Do not publish the candidate password or complete hash.
7. **Capture evidence.** Add redacted screenshots showing the Hash Calculator, Password Cracker run/result, and PDF verification (if applicable). Hide the full hash and any recovered password before adding screenshots to a public repository.


### Module 2 evidence


<img width="726" height="619" alt="hash-calculator-redacted" src="https://github.com/user-attachments/assets/fea71686-f50d-40f1-b27b-ac0bdab2297a" />

<img width="718" height="819" alt="password-cracker-redacted" src="https://github.com/user-attachments/assets/6ec74662-be64-4fc7-b38a-ff33e5c8b1ea" />

<img width="1278" height="1019" alt="pdf-verification" src="https://github.com/user-attachments/assets/3347043b-e3b0-4506-9747-52607735aea8" />


## What the process taught me

A password-protected PDF uses encryption to protect its contents. A password-auditing tool tests candidates against information derived from the file; it does not simply reverse the encryption to reveal a password. A recovered candidate must still be checked against the PDF. Weak or predictable passwords may be found sooner, while long, unique passwords are generally harder to guess.

The two modules illustrate different workflows: Module 1 uses JTR with Johnny on the computer, while Module 2 uses Networkwalks' browser-based Hash Calculator and Password Cracker. Keep lab files, hashes, and recovered credentials private, even when documenting the learning process.
