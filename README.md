# Week 3: Password Security Labs

This repository documents my Week 3 password-security project: learning industry password-auditing tools and understanding the authorized process behind recovering access to a password-protected PDF.

## [**Open the complete project here**](project-modules/README.md)

## Project overview

The project explores how password-auditing tools can test candidate passwords against password-protected PDF data in a controlled lab. It covers the workflow and concepts behind PDF password recovery, compares the assigned tools, and reflects on password strength and responsible handling of recovered information. Testing is limited to files and systems I own or have permission to assess.

## Tools used

| Tool | Project use |
| --- | --- |
| John the Ripper (JTR) | Password-auditing tool covered in Project Module 1. |
| NW Tools | Tool covered in Project Module 2, following the course handout. |

## What I did

- Worked through **Project Module 1**, focused on password cracking with John the Ripper.
- Worked through **Project Module 2**, focused on password cracking with NW Tools.
- Learned how an authorized PDF password-recovery workflow uses a hash representation of the protected file for offline password auditing, then checks a recovered candidate against the PDF.
- Compared the tools' workflows and noted what the exercises showed about password auditing.
- Kept the work within the scope of the assigned lab materials.

## What I learned

- Password-cracking tools can test candidate passwords against password hashes; they do not need the original plaintext password to begin an offline audit.
- PDF password recovery is generally a process of testing candidate passwords against the file's protection, not reversing its encryption. A matching password can then be used to open the PDF.
- Weak, common, or predictable passwords are easier to guess. Long, unique passwords make guessing much harder.
- Different tools can provide different workflows, so it is important to understand the task and the tool before interpreting results.
- Password-auditing results should be handled carefully because recovered credentials and hashes are sensitive.
- These techniques should only be used on systems and data I own or have explicit permission to test.

## Modules

| Module | Topic |
| --- | --- |
| Project Module 1 | Password Cracking with JTR |
| Project Module 2 | Password Cracking with NW Tools |

## Resources

- **Project Module 1 handout:** `W3-PM1 - Week3 - Project Module1 - Password Cracking with JTR v1.pdf`
- **Project Module 2 handout:** `W3-PM2 - Week3 - Project Module2 - Password Cracking with NW Tools v1.pdf`
- **Week 3 projects overview:** `z. Week3 Projects v1.pdf`
- [John the Ripper official website](https://www.openwall.com/john/)

open complete project here https://github.com/sphumelelemtetwa11/week-3-password-security-labs/tree/master/project-modules

The assignment PDFs were provided with the coursework and are not included in this repository. Use the Module 2 handout for the course-specific NW Tools instructions.

## Safety and privacy

This is coursework documentation, not a guide to access other people's accounts. I will only use authorized lab data. I will not publish real passwords, recovered credentials, or unredacted hashes in this public repository.

The original assignment PDFs are not included in this repository.
