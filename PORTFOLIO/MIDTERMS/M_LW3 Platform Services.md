+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 069fcc7e6afe48c186edbc180e35981f |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: Sueno, Johnray K.          | DATE PERFORMED:        | /50      |
|                                  | 10/17/2024             |          |
+----------------------------------+------------------------+----------+
| Section: IDC2                    | DATE                   |          |
|                                  | SUBMITTED:10/17/2024   |          |
+----------------------------------+------------------------+----------+

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

![](vertopal_069fcc7e6afe48c186edbc180e35981f/media/image2.png){width="7.027083333333334in"
height="3.3854166666666665in"}

-   The major categories are Application, Security, Setup, System and
    Forwarded Events.

**Part 2: Filtering and Analyzing IIS Events**

1.  Apply filter to the windows log categories to display errors for the
    past 12 hours.

![](vertopal_069fcc7e6afe48c186edbc180e35981f/media/image3.png){width="6.970772090988627in"
height="2.381418416447944in"}

![](vertopal_069fcc7e6afe48c186edbc180e35981f/media/image4.png){width="7.001629483814523in"
height="1.4167946194225722in"}

2.  **Identify Critical Events** or recurring events.

-   The critical or recurring events are the Source
    CertificateServicesClient-CertEnroll, Security-SPP and Service
    Control Manager.

3.  **Analyze the Events**:

    -   For each critical or recurring event, **record the following
        details**:

  -----------------------------------------------------------------------------------------------------------
  **EVENTS**   **SOURCE**                             **TIMESTAMP**   **DESCRIPTION**
  ------------ -------------------------------------- --------------- ---------------------------------------
  67           CertificateServicesClient-CertEnroll   10/17/2024      Certificate enrollment for Local System
                                                      8:36:24 AM      failed to load policy from policy
                                                                      servers. The specified domain either
                                                                      does not exist or could not be
                                                                      contacted.

  68           CertificateServicesClient-CertEnroll   10/17/2024      Certificate enrollment for Local System
                                                      8:36:24 AM      failed in authentication to policy
                                                                      servers.

  70           CertificateServicesClient-CertEnroll   10/17/2024      Certificate enrollment for Local System
                                                      8:36:24 AM      failed because no valid policy can be
                                                                      obtained from policy servers.

  16387        Security-SPP                           10/17/2024      Failed to run
                                                      8:36:24 AM      task\\Microsoft\\Windows\\WS\\License
                                                                      Validation.

  8198         Security-SPP                           10/17/2024      License Activation failed.
                                                      8:27:10 AM      

  1014         Security-SPP                           10/17/2024      Acquisition of End User License failed.
                                                      8:27:10 AM      

  8200         Security-SPP                           10/17/2024      License Acquisition failed.
                                                      8:27:10 AM      

  7023         Service Control Manager                10/17/2024      The Windows Time service terminated
                                                      8:34:49 AM      with the error an attempt was made to
                                                                      logon, but the network logon service
                                                                      was not started.

  7030         Service Control Manager                10/17/2024      The Printer Extensions and
                                                      8:28:29 AM      Notifications service is marked as an
                                                                      interactive service but the system is
                                                                      configured to not allow interactive
                                                                      services causing it to not function
                                                                      properly.
  -----------------------------------------------------------------------------------------------------------

**Part 3: Troubleshooting and Solution Development**

1.  Review the logs and check for recurring errors.

2.  Is there a specific time or pattern to these errors?

![](vertopal_069fcc7e6afe48c186edbc180e35981f/media/image5.png){width="5.636202974628172in"
height="1.2085017497812773in"}

![](vertopal_069fcc7e6afe48c186edbc180e35981f/media/image6.png){width="5.594530839895013in"
height="0.6042508748906387in"}

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

+-----------------------------------------------------------------------+
| -   **Event ID 67**: Certificate enrollment for Local System failed   |
|     to load policy from policy servers at 10/17/2024 8:36:24 AM.      |
|                                                                       |
| -   **Event ID 68**: Certificate enrollment for Local System failed   |
|     in authentication to policy servers at 10/17/2024 8:36:24 AM.     |
|                                                                       |
| -   **Event ID 70**: Certificate enrollment for Local System failed   |
|     because no valid policy can be obtained from policy servers at    |
|     10/17/2024 8:36:24 AM.                                            |
|                                                                       |
| -   **Event ID 16387**: Failed to run                                 |
|     task\\Microsoft\\Windows\\WS\\License Validation at 10/17/2024    |
|     8:36:24 AM.                                                       |
|                                                                       |
| -   **Event ID 8198**: License Activation failed at 10/17/2024        |
|     8:27:10 AM.                                                       |
|                                                                       |
| -   **Event ID 1014**: Acquisition of End User License failed at      |
|     10/17/2024 8:27:10 AM.                                            |
|                                                                       |
| -   **Event ID 8200**: License Acquisition failed at 10/17/2024       |
|     8:27:10 AM.                                                       |
|                                                                       |
| -   **Event ID 7023**: The Windows Time service terminated with an    |
|     error at 10/17/2024 8:34:49 AM.                                   |
|                                                                       |
| -   **Event ID 7030**: The Printer Extensions and Notifications       |
|     service is marked as an interactive service but is not            |
|     functioning properly at 10/17/2024 8:28:29 AM.                    |
+=======================================================================+
+-----------------------------------------------------------------------+

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

![](vertopal_069fcc7e6afe48c186edbc180e35981f/media/image7.png){width="6.392687007874016in"
height="2.5508431758530183in"}

![](vertopal_069fcc7e6afe48c186edbc180e35981f/media/image8.png){width="5.7614555993000875in"
height="3.937296587926509in"}

3.  Why is **monitoring logs** in Event Viewer important for
    administrators?

-   Monitoring logs in Event Viewer is very important because it helps
    in identifying an issue and guide us what or how to troubleshoot
    this system issues, it can also help in detecting login, failed and
    unauthorized access and potential security threats to ensure
    compliance with regulations and improving overall system performance
    and reliability.

Grading Rubric

  ---------------------------------------------------------------------------------------------------------------------------------------
  **Criteria**        **Excellent**     **Good**          **Needs                           **Poor**                         **Points**
                                                          Improvement**                                                      
  ------------------- ----------------- ----------------- --------------- ----------------- ------------- ------------------ ------------
  **Log Analysis**    Identifies all    Identifies most   Identifies some                   Fails to                         /10
                      key events (503,  key events with   events, but                       identify key                     
                      404, 500, etc.)   minor errors in   with incomplete                   events or                        
                      with accurate     details.          or incorrect                      provides                         
                      event details.                      details.                          incorrect                        
                                                                                            details.                         

  **Troubleshooting   Proposes logical, Solutions are     Solutions are                     Solutions are                    /10
  Solutions**         effective         mostly correct    somewhat vague                    unclear or                       
                      solutions to all  but miss some key or incomplete.                    incorrect.                       
                      identified        points.                                                                              
                      issues.                                                                                                

  **Report Structure  Well-organized    Report is mostly  Report is                         Report is                        /10
  & Clarity**         report with all   organized with    disorganized or                   unclear or                       
                      sections clearly  minor formatting  missing                           incomplete.                      
                      completed.        issues.           sections.                                                          

  **Recommendations   Provides          Recommendations                   Recommendations                 Fails to provide   /10
  for Monitoring**    thoughtful,       are relevant but                  are vague or                    relevant           
                      proactive         lack depth.                       incomplete.                     recommendations.   
                      recommendations                                                                                        
                      to prevent future                                                                                      
                      issues.                                                                                                

  **Participation &   Actively engaged  Participated but                  Minimal                         Did not            /10
  Effort**            in the activity,  required some                     participation,                  participate        
                      followed          guidance.                         needed                          meaningfully.      
                      instructions                                        significant help.                                  
                      thoroughly.                                                                                            

  **Score**                                                                                                                  **/50**
  ---------------------------------------------------------------------------------------------------------------------------------------
