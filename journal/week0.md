# Week 0 — Billing and Architecture

---
#### Notes
    - Will be doing this entire bootcamp locally on my personal macbook
    - Redacted a portion of the AWS Account number for security reasons
  
### [Required HomeWork]
- [x] **Watched Week 0 - Live Streamed Video**
- [x] **Watched Chirag's Week 0 - Spend Considerations**
- [x] **Watched Ashish's Week 0 - Security Considerations**
- [x] **Recreate Conceptual Diagram in Lucid Charts or on a Napkin**<br>
  - Link to lucidcharts -> [Cruddur Conceptual Diagram](https://lucid.app/lucidchart/a38d49e1-290a-4010-bd28-4490168f48d8/edit?viewport_loc=-65%2C-11%2C2349%2C1200%2C0_0&invitationId=inv_9d0a9b8c-4862-44b1-8303-74ed28f37080)
  ![Cruddur Conceptual Diagram](assets/W1_RH_Cruddur_Conceptual_Diagram.jpeg "Cruddur Conceptual Diagram")
- [x] **Recreate Logical Architectual Diagram in Lucid Charts**<br>
  - Link to lucidcharts -> [Cruddur Logical Diagram](https://lucid.app/lucidchart/5f5596fb-37fd-4e2e-89ee-65b327d31c67/edit?viewport_loc=-401%2C-174%2C2760%2C1410%2C0_0&invitationId=inv_c37965af-1ad4-4bcc-a512-903f44dab489)
  ![Cruddur Logical Diagram](assets/W1_RH_Cruddur_Logical_Diagram.jpeg "Cruddur Logical Diagram")
- [x] **Create an Admin User**<br>
  ![Create an Admin User](assets/W1_RH_CreateAnAdminUser.png "Create and Admin User")
- [x] **Use CloudShell**<br>
  ![Use CloudShell](assets/W1_RH_UseCloudShell.png "Use CloudShell")
- [x] **Generate AWS Credentials**<br>
  ![Generate AWS Credentials](assets/W1_RH_GenerateAWSCredentials.png "Generate AWS Credentials")
- [x] **Installed AWS CLI**<br>
  ![Installed AWS CLI](assets/W1_RH_InstalledAWSCli.png "Installed AWS CLI")
- [x] **Create a Billing Alarm**<br>
  - Followed the documentation here -> https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/monitor_estimated_charges_with_cloudwatch.html
  - Created 3 billing alarms
  ![BillingAlarm](assets/W1_RH_CreateBillingAlarm.png "BillingAlarm")
- [x] **Create a Budget**<br>
  - Created a monthly budget of $30. An amount that I've comfortably paid for over the past year for experiments.
  ![Budget](assets/W1_RH_CreateABudget.png "Budget")
---
### Homework Challenges
- [x] **Destroy your root account credentials, Set MFA, IAM role**<br>
  - Destroyed Root Access Keys
  - Enabled MFA
  - Created a role for user to AssumeRole with 1hour session limitation and MFA configured.
<br>![root](assets/W1_HC_DestroyRootCredsSetMFA.png "root")
- [ ] **Use EventBridge to hookup Health Dashboard to SNS and send notification when there is a service health issue.**<br>
- [ ] **Review all the questions of each pillars in the Well Architected Tool (No specialized lens)**<br>
- [ ] **Create an architectural diagram (to the best of your ability) the CI/CD logical pipeline in Lucid Charts**<br>
- [ ] **Research the technical and service limits of specific services and how they could impact the technical path for technical flexibility.**<br>
- [x] **Open a support ticket and request a service limit**<br>
  - Followed the documentation here -> https://aws.amazon.com/getting-started/hands-on/request-service-quota-increase/
  - Requested for the AWS Cloudformation resource limit to be increased from 50 to 100.
  ![service-limit](assets/W1_HC_OpenedASupportTicketandRequestAServiceLimit.png "service-limit")
---
### Additional Self-Created Challenges
- [x] **Used aws-vault for programmatic access to better manage aws access keys locally by storing it in local keychain**<br>
  - Used an open-source solution to manage programmatic access locally. It stores the access keys in the local keychain. Security first! -> https://github.com/99designs/aws-vault
  ![aws-vault](assets/W1_HC_use_aws-vault_for_programmatic_access_awscli.png "aws-vault")
- [x] **Created addtional Service Control Policies as account guardrails**<br>
  - Implemented some of examples provided by AWS in the documentation here -> https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps_examples.html
  - Did this so as to prevent any unecessary resources being build in regions that I do not use.
  ![SCPs](assets/W1_HC_Created_additional_SCPs_as_account_guardrails.png "SCPs")
---