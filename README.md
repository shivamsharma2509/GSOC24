## Google Summer of Code 2024 Final Report

## General Information

- **Organization:** The Linux Foundation <br/>
- **Project:** User Interfaces for using OAuth2 with Printers and Scanners <br/>
- **Project Page:** [Click here](https://wiki.linuxfoundation.org/gsoc/google-summer-code-2024-openprinting-projects) <br/>
- **Project Repository:** [Click here]() <br/>
- **Proposal:** [Click Here]() <br/>

## About Me

Hi, I am Shivam Sharma, currently working at Cognizant Technology Solutions as Engineer Trainee. I was selected as a GSOC 2024 contributor for OpenPrinting @ The Linux Foundation. My project was adding OAuth2 support for using printers and scanners to CUPS. I have managed to add OAuth2 support for client verification to keep client data secure.

## Description

The printing ecosystem in Unix-like systems often requires users to authenticate with online accounts to access cloud-based printing services. Integrating GNOME Online Accounts with CPDB simplifies this process, offering a unified and user-friendly interface for managing print jobs. We also managed to handle token exchange for smooth authentication. GOA provides several libraries for OAuth support, so I used those libraries for token exchange, verifying account and auhtorization URL. Later the part of the authorization URL was done with the help of github OAuth support. I used github for generating cliend id and client secret to help client verify their identity and keep their data safe.

## Objective

The objective of this project is to add OAuth2 support for using printers and scanners. We aim to achieve this by:

- Integrate OAuth2 authentication using GNOME Online Accounts (GOA).
- Develop a local server in C to handle OAuth2 callbacks.
- Ensure seamless integration with CPDB and CUPS.
- Provide a user-friendly interface for managing online accounts within the print dialog.

