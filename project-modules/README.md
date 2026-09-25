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

### My results

- **PDF tested:** `My Locked PDF1.pdf` (course lab copy)
- **Result:** `[Record whether the password was recovered; do not include it]`
- **Tool output/time:** `[Add only if recorded; otherwise write "not recorded"]`
- **What I learned:** `[Describe what you observed about the workflow and password strength]`

### Module 1 evidence

Save your redacted screenshots in this folder and add them here. Example filenames:

- `images/module-1-tool-setup.png`
- `images/module-1-hash-file-redacted.png`
- `images/module-1-johnny-result-redacted.png`
- `images/module-1-pdf-verification.png`

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

### My results

- **PDF tested:** `My Locked PDF1.pdf` (course lab copy)
- **Result:** `[Record whether the password was recovered; do not include it]`
- **Tool output/time:** `[Add only if recorded; otherwise write "not recorded"]`
- **What I learned:** `[Compare this browser-based workflow with Module 1]`

### Module 2 evidence

Save your redacted screenshots in this folder and add them here. Example filenames:

- `images/module-2-hash-calculator-redacted.png`
- `images/module-2-password-cracker-redacted.png`
- `images/module-2-pdf-verification.png`

## What the process taught me

A password-protected PDF uses encryption to protect its contents. A password-auditing tool tests candidates against information derived from the file; it does not simply reverse the encryption to reveal a password. A recovered candidate must still be checked against the PDF. Weak or predictable passwords may be found sooner, while long, unique passwords are generally harder to guess.

The two modules illustrate different workflows: Module 1 uses JTR with Johnny on the computer, while Module 2 uses Networkwalks' browser-based Hash Calculator and Password Cracker. Keep lab files, hashes, and recovered credentials private, even when documenting the learning process.
