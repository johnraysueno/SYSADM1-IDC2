<img width="610" alt="image" src="https://github.com/user-attachments/assets/16975eb2-bae8-4c96-902a-a489ea8118d0">


# SYSADM1 -- Monitoring Print Services in Windows Server 2019

# Requirement: 

-   A virtual machine running Linux and Windows OS

Part 1: Setting Up Print Services

1.  Install and configure **print.srv** domain

<img width="611" alt="image" src="https://github.com/user-attachments/assets/0f8d6b05-be37-4aff-ad59-76d02a93a3a6">


2.  Connect one client to the recently created domain

<img width="610" alt="image" src="https://github.com/user-attachments/assets/02b5a233-edac-4370-8da4-96b3e7ec9b3d">
"}

3.  Install Print Services Role:

<img width="610" alt="image" src="https://github.com/user-attachments/assets/3f5d3c57-be5a-44a0-873d-0fd96096608f">


<img width="608" alt="image" src="https://github.com/user-attachments/assets/3775b1ef-fb54-44a9-b4c5-0f12c7b04f64">


4.  Search the internet for any printer installer and convert it to iso

5.  Install and deploy it as network printer

<img width="612" alt="image" src="https://github.com/user-attachments/assets/27df3901-460d-411b-a762-4c6f54b3fd48">


<img width="612" alt="image" src="https://github.com/user-attachments/assets/4d20c064-887d-494a-816e-0a449cfbc929">


Part 2: Monitoring Print Services

Objective: Familiarize yourself with monitoring tools available in
Windows Server 2019.

1.  Event Viewer:

    -   Open Event Viewer (run eventvwr.msc).

    -   Navigate to Applications and Services Logs \> Microsoft \>
        Windows \> PrintService.

    -   Review logs for print jobs, errors, and warnings.

<img width="611" alt="image" src="https://github.com/user-attachments/assets/4372a197-79b4-43c9-a31b-102a198b1db2">


2.  Performance Monitor:

    -   Open Performance Monitor (run perfmon).

    -   In the left pane, expand Data Collector Sets \> System.

    -   Right-click System Performance and select Start.

    -   Monitor performance metrics related to print services.

<img width="611" alt="image" src="https://github.com/user-attachments/assets/3a2ba8bb-b9a7-45d8-97d1-578a05cbd6c4">


3.  Using Print Management Console:

    -   Open Print Management from Server Manager.

    -   View active print jobs and their status.

    -   Use the Printers node to check the status of all printers.

<img width="607" alt="image" src="https://github.com/user-attachments/assets/98416888-59bb-4d25-b2e6-9fd663ff3b7f">


Part 3: Exploring Third-Party Monitoring Tools

1.  Research at least two third-party print monitoring tools

    -   Consider factors such as features, pricing, and compatibility
        with Windows Server 2019.

#### **1. PaperCut**

-   Features**:**

Print tracking and reporting.

User authentication and access control.

Cost recovery features.

Web-based interface for management.

-   Pricing**:** Pricing is based on the number of users or printers,
    with a free trial available. Contact for specific quotes.

-   Compatibility**:** Compatible with Windows Server 2019 and various
    other operating systems.

#### **2. PrinterLogic**

-   Features**:**

Centralized print management.

Print driver management without the need for print servers.

User self-service portal for managing printers.

Detailed reporting and analytics.

-   Pricing**:** Pricing typically requires a quote based on the number
    of users or devices.

-   Compatibility**:** Works well with Windows Server 2019 and supports
    various environments.

2.  Install and Configure:

    -   Choose one of the tools to install in your environment.

    -   Follow the installation instructions provided by the tool\'s
        documentation.

    -   Configure it to monitor your print services.

3.  Test and Report Findings:

    -   Generate a report or dashboard from the tool.

    -   Analyze the collected data (e.g., print volume, errors, user
        activity).

Rubric

  --------------------------------------------------------------------------------------------------------------
  **Criteria**   **1                  **2 (Needs       **3                **4        **5             **Score**
                 (Unsatisfactory)**   Improvement)**   (Satisfactory)**   (Good)**   (Excellent)**   
  -------------- -------------------- ---------------- ------------------ ---------- --------------- -----------

  --------------------------------------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 1: Setting Up Print Services**                                          
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------
  **Domain         No domain Domain     Domain      Domain       Domain           
  Installation**   created   created    created     configured   configured and   
                             with       correctly   well         documented       
                             errors                              thoroughly       
  ---------------- --------- ---------- ----------- ------------ ---------------- --

  ----------------------------------------------------------------------------------

  --------------------------------------------------------------------------------
  **Client       Client not  Connection   Client      Client      Client        
  Connection**   connected   attempt      connected   connected   connected and 
                             failed       but with    correctly   documented    
                                          issues                  well          
  -------------- ----------- ------------ ----------- ----------- ------------- --

  --------------------------------------------------------------------------------

  ------------------------------------------------------------------------------------
  **Print Services Role not    Role        Role        Role         Role installed, 
  Role             installed   installed   installed   installed    configured, and 
  Installation**               with issues correctly   and          documented      
                                                       configured   thoroughly      
  ---------------- ----------- ----------- ----------- ------------ --------------- --

  ------------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Printer      No          Installer    Installer   Installer   Installer      
  Installer      installer   conversion   converted   converted   converted,     
  Conversion**   found       attempted    but not     and used    used, and      
                             but failed   used                    documented     
                                                                  well           
  -------------- ----------- ------------ ----------- ----------- -------------- --

  ---------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Network      Printer    Deployment   Printer      Printer     Printer        
  Printer        not        failed       deployed but deployed    deployed,      
  Deployment**   deployed                not          correctly   tested, and    
                                         functional               documented     
                                                                  well           
  -------------- ---------- ------------ ------------ ----------- -------------- --

  ---------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 2: Monitoring Print Services**                                          
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  ------------------------------------------------------------------------------
  **Event   Event     Opened but  Logs reviewed Logs        Logs reviewed     
  Viewer    Viewer    no logs     but           reviewed    with thorough     
  Usage**   not       reviewed    superficial   with some   analysis and      
            opened                              analysis    documentation     
  --------- --------- ----------- ------------- ----------- ----------------- --

  ------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------
  **Performance   Performance   Opened but  Metrics     Metrics     Metrics       
  Monitor Usage** Monitor not   no metrics  monitored   monitored   monitored,    
                  opened        monitored   but not     with some   analyzed, and 
                                            analyzed    analysis    documented    
                                                                    thoroughly    
  --------------- ------------- ----------- ----------- ----------- ------------- --

  ----------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------
  **Print       Console   Opened but      Active jobs     Active    Active jobs   
  Management    not       functionality   viewed          jobs      viewed and    
  Console       opened    not used        superficially   viewed    documented    
  Usage**                                                 with some thoroughly    
                                                          detail                  
  ------------- --------- --------------- --------------- --------- ------------- --

  ----------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 3: Exploring Third-Party Tools**                                        
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Research   No tools     Research     Research on Research on  Research on    
  on Tools**   researched   incomplete   one tool    two tools    two tools,     
                                         completed   with some    detailed       
                                                     analysis     analysis, and  
                                                                  comparison     
  ------------ ------------ ------------ ----------- ------------ -------------- --

  ---------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------------
  **Installation    Tool not    Installation   Tool         Tool         Tool           
  and               installed   failed         installed    installed    installed,     
  Configuration**                              but not      and          configured,    
                                               configured   configured   and documented 
                                                            with issues  thoroughly     
  ----------------- ----------- -------------- ------------ ------------ -------------- --

  ----------------------------------------------------------------------------------------

  -------------------------------------------------------------------------------
  **Reporting   No report   Report   Report      Report      Comprehensive     
  Findings**    generated   lacks    generated   generated   report with       
                            detail   but lacks   with some   thorough analysis 
                                     analysis    analysis    and documentation 
  ------------- ----------- -------- ----------- ----------- ----------------- --

  -------------------------------------------------------------------------------
