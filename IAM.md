## IAM introduction
- IAM has a blobal view
- Pernissions are governed by Policies(JSON)
- MFA(Multi Factor Authentication) can be setup
- IAM has predefined "managed policies"
- We will see IAM policies in details in the future
- Its best to give users the minimal amount of permissions they need to perform their job(least privilege principles)

### IAM Federation
- Big enterprises usually integrate their own repository of users with IAM
- This way one can login into AWS using their company credentials
- Identity Federation uses the SAML standard (Active Directory)

### IAM 101 Brain Dump
- One IAM User PHYSICAL PERSON
- One IAM per Application
- IAM credentials should NEVER BE SHARED
- Never ever ever!!! write IAM credentials in code, EVER
- Never use the ROOT account except for initial setup
- Never use ROOT IAM Credentials