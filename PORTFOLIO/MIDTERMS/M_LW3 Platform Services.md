<img width="614" alt="image" src="https://github.com/user-attachments/assets/866ea601-87c1-4981-9d3d-39dbb8c23eaa">


# SYSADM1 -- Platform Services

# Requirement: 

-   A virtual machine running Windows Server

    **Objective/s:**

    To analyze IIS logs in the Event Viewer to identify critical web
    service metrics, understand common error codes, and learn how to
    monitor the health of web applications.

**Instructions**

**Part 1: Opening Event Viewer and Loading Logs**

1.  Access the event viewer in the server.

2.  From the event viewer, explore the windows log and list down its
    major categories

<img width="509" alt="image" src="https://github.com/user-attachments/assets/2fb0e7d2-cd2f-4be3-aecb-0e9397326d6a">


**Part 2: Filtering and Analyzing IIS Events**

1.  Apply filter to the windows log categories to display errors for the
    past 12 hours.

<img width="611" alt="image" src="https://github.com/user-attachments/assets/79a33e9f-5fd6-4188-b567-3a6f9d0daebe">


2.  **Identify Critical Events** or recurring events.

-   The critical or recurring events are the Source
    CertificateServicesClient-CertEnroll, Security-SPP and Service
    Control Manager.

3.  **Analyze the Events**:

    -   For each critical or recurring event, **record the following
        details**:

<img width="609" alt="image" src="https://github.com/user-attachments/assets/4657c6cc-9356-47af-8fde-2e12ec4a3e8d">
<img width="610" alt="image" src="https://github.com/user-attachments/assets/3fd36767-a6d9-40e9-93f1-219f989f91b7">


**Part 3: Troubleshooting and Solution Development**

1.  Review the logs and check for recurring errors.

2.  Is there a specific time or pattern to these errors?

<img width="608" alt="image" src="https://github.com/user-attachments/assets/0976b3cb-d1bc-43c2-8372-658eb3162d1a">

-   Yes there is, the errors have occurred at the same time as
    10/17/2024 8:36:24 AM and 10/17/2024 8:27:10 AM.

3.  Draft a Troubleshooting Report:

    -   Based on the events found, create a short report with the
        following sections:

**Report Structure**

**1.** Overview

-   A brief summary of the issue and scope of your analysis.

```{=html}
<!-- -->
```
-   This report summarizes the analysis of errors found in the Server
    Event Viewer, specifically focusing on critical events and errors
    that occurred in the last 12 hours such as Certificate Services
    Client Cert-Enroll, Security-SPP and Service Control Manager. The
    report aimed to identify recurring issues and their potential impact
    on system operations. Some errors also occurred at the same time.

**2.** Key Findings

-   List the critical events you found.

<img width="611" alt="image" src="https://github.com/user-attachments/assets/e72cd35f-c2c7-4cf2-8e2b-2cba4b8373ba">


**3.** Root Causes and Solutions

-   Describe the likely cause of each error and how you would fix it.

1**. CertificateServicesClient-CertEnroll Errors**:

**Likely Causes**: Network issues or misconfigured permissions such as
the specified domain either does not exist or could not be contacted
leading to failure in certificate enrollment.

**Solutions**:

-   Check network connectivity to the Certificate Authority.

-   Verify permissions for the Local System account and ensure Group
    Policy settings are correctly configured.

2\. **Security-SPP Errors**:

**Likely Causes**: Issues with license validation, license acquisition
and activation processes.

**Solutions**:

-   Ensure that the Windows licensing services are running properly.

-   Check the system's internet connection for reaching Microsoft's
    activation servers.

3\. **Service Control Manager Errors**:

**Likely Causes**: Services not starting due to configuration issues
like an attempt was made to logon, but the network logon service was not
started and the system is configured to not allow interactive services
causing it to not function properly.

**Solutions**:

-   For the Windows Time service, ensure the Network Logon service is
    running.

-   Review service configuration settings for the Printer Extensions
    service.

**Part 4: Reflection Questions**

1.  What are the most common causes of a
    **CertificateServicesClient-CertEnroll** and **Security-SPP** error?

-   The most common causes of CertificateServicesClient-CertEnroll and
    Security-SPP errors include network issues, permissions problems,
    and misconfigurations. For CertificateServicesClient-CertEnroll
    errors, if the network is down, doesn't exist and cannot be found
    the system/server can\'t connect to the Certificate Authority to get
    certificates. If the account doesn\'t have the right permissions or
    policies it can't enroll and expired or missing certificates can
    cause problems too. For Security-SPP errors, issues with license
    validation or a bad internet connection can prevent license
    activation and incorrect Group Policy settings can also lead to
    these errors.

2.  How would you **monitor login attempts** to detect potential
    security threats?

-   To monitor login attempts, regularly checking the Security log in
    Event Viewer for Event IDs 4624 which is successful logins and 4625
    the failed logins.

<img width="608" alt="image" src="https://github.com/user-attachments/assets/405748a0-a142-4ce6-8a45-819e60dc668d">

<img width="608" alt="image" src="https://github.com/user-attachments/assets/f8c35a13-f75a-4256-b22f-16ad3f5eb37c">


3.  Why is **monitoring logs** in Event Viewer important for
    administrators?

-   Monitoring logs in Event Viewer is very important because it helps
    in identifying an issue and guide us what or how to troubleshoot
    this system issues, it can also help in detecting login, failed and
    unauthorized access and potential security threats to ensure
    compliance with regulations and improving overall system performance
    and reliability.

<img width="611" alt="image" src="https://github.com/user-attachments/assets/7a073822-9964-4a2d-9705-d8462d0f26e5">
                                                                                         
