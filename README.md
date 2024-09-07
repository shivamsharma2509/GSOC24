## Google Summer of Code 2024 Final Report

## General Information

- **Organization:** The Linux Foundation <br/>
- **Project:** User Interfaces for using OAuth2 with Printers and Scanners <br/>
- **Project Page:** [Click here](https://wiki.linuxfoundation.org/gsoc/google-summer-code-2024-openprinting-projects) <br/>
- **Project Repository:** [Click here](https://github.com/shivamsharma2509/CPDB_Backend_OAuthSupport/tree/main) <br/>
- **Proposal:** [Click Here](https://drive.google.com/file/d/1BQcyW8WkD_lmbC8qw1ziu-09sWNfKOtN/view?usp=sharing) <br/>

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
- Setup GOA OAuth based D-bus system.

## Implementation Details

1. OAuth2 flow implementation: It includes initializing GOA client, establishing connection between client and auth server and initiating token exchange.
2. Local server setup for callbacks: The local server setup involved using libmicrohttpd to create an HTTP server on port 8080, handling OAuth2 callback requests, and processing authorization codes to obtain access tokens.
3. Merging OAuth2 code with CPDB: It contains complete OAuth setup which is added to CPDB for client authentication.

## Challenges and Solutions

 - Token handdling: Managing OAuth2 tokens securely was challenging. Implemented secure storage and retrieval mechanisms for tokens.
 - Merging it to CPDB: Initially I was getting lots of error while merging it to CPDB then I made changes to makefile and merged the OAuth code with CPDB.

## Outcomes

The integration successfully streamlined the authentication process, reducing the time required for users to log in to their online accounts from within the print dialog. User feedback indicated a significant improvement in the overall user experience.

- Here is the screenshot of the user interface for authorization:

  <p align="center">
  <img src="https://github.com/shivamsharma2509/GSOC24/blob/main/img/demo.png">
  </p>

- Here is the OAuth workflow

   <p align="center">
   <img src = "https://github.com/shivamsharma2509/GSOC24/blob/main/img/OAuth_Flw.png">
   </p>

## Future Scope

The setup of local server and token exchange is successfully accomplished. However, there are several exciting improvements that could enhance the OAuth2 support:

 1. Implementing support for additional online services: We can implement many more online services in the authentication page by allowing user to use different methods for authentication.
 2. Enhance security for token storage: Security can not be compromised so I will add more security layers for token storage.
 3. Develop a graphival interface for managing OAuth2 tokens.

## Acknowledgement

I am deeply grateful to the OpenPrinting for giving me the incredible opportunity to participate in Google Summer of Code (GSoC) program. My mentors, [Till Kamppeter](https://github.com/tillkamppeter) and Deepak Patankar helped me alot during this journey. These project wouldn't have been possible without both of you.
The weekly project sync with Deepak helped me achieve most of the goals.
