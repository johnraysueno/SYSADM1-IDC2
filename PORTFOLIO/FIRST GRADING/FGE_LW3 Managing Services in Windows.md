<img width="608" alt="image" src="https://github.com/user-attachments/assets/89edab74-511d-47e6-a699-494fe761feef">


# SYSADM1 -- Managing Services in Windows

# Requirement: 

-   A virtual machine running Linux and Windows OS

    **Services** are background processes that run independently of user
    interactions in Windows. They provide essential system functions,
    such as network connectivity, printing, and time synchronization.
    This lab will guide you through the process of managing services
    using the Services app.

# Instructions:  {#instructions .list-paragraph}

1.  Open the Start menu and search for \"Services\"

2.  Familiarize yourself with the columns, including Service Name,
    Display Name, Status, and Startup type.

3.  Right-click on a service and select \"Start\", \"Stop\", or
    \"Restart\". Fill out the table below

  <img width="475" alt="image" src="https://github.com/user-attachments/assets/65e40327-1013-4803-9079-1a74f65b2e69">
  <img width="479" alt="image" src="https://github.com/user-attachments/assets/4a43a4be-470b-437d-9930-9593779b5f25">


4.  Select five network services, right-click to view its properties.
    Modify the startup setting to Manual.

> **SS**:

 <img width="475" alt="image" src="https://github.com/user-attachments/assets/e115ce6e-5724-4af9-88f1-f9e10192ce8e">
<img width="475" alt="image" src="https://github.com/user-attachments/assets/60e3afc9-ee72-419a-84c1-3fad83f75339">
<img width="476" alt="image" src="https://github.com/user-attachments/assets/92a27c73-6e69-4e11-bdff-aed6911986c9">
<img width="479" alt="image" src="https://github.com/user-attachments/assets/31eefc9c-c983-4978-a22b-3c3e0cc0613f">
<img width="478" alt="image" src="https://github.com/user-attachments/assets/29fa3b88-d288-4a79-a864-addf7c64196c">


5.  Explore the \"General\", \"Recovery\", and \"Log On\" tabs to
    understand additional service settings.

> General:
<img width="263" alt="image" src="https://github.com/user-attachments/assets/963b3a03-32b8-4d1c-9728-f33f0a29cc80">
<img width="263" alt="image" src="https://github.com/user-attachments/assets/61c0f234-1e5e-4a36-b888-94288bb4e4e3">
<img width="266" alt="image" src="https://github.com/user-attachments/assets/588f4eb3-795f-4643-8f4d-dc1d92529771">


6.  Create a batch file that will be added as a new service later on.
    Refer to the batch file code below.

<img width="352" alt="image" src="https://github.com/user-attachments/assets/c9dd0cc6-6066-4df1-bece-3a14bc50fe4a">


7.  Save the batch file in Z:\\lastname_timer.bat

<img width="506" alt="image" src="https://github.com/user-attachments/assets/11b57164-ebb4-4866-8a1b-cd5cb7522f79">


8.  Use the sc command to add timer.bat service in the command line
    interface.

> *sc create BatchTimerService binPath= \"path_to_your_batch_file.bat\"
> start= auto*
>
> *net start BatchTimerService*
>
> **Replace path_to_your_batch_file.bat with the actual path to your
> batch file.**
>
<img width="458" alt="image" src="https://github.com/user-attachments/assets/238cfadd-9bfd-4fc6-b6b8-d0cc66a8bdd7">


9.  Verify that BatchTimerService has been added to the services.

> **SS:**
>
<img width="388" alt="image" src="https://github.com/user-attachments/assets/01ace57e-f313-4d5e-a7ea-f6d743dfac7f">


10. **Testing the Service:** Now, if you open a new command prompt, you
    should see the timer countdown without requiring your interaction.
    Once the timer finishes, you\'ll see the \"Timer finished!\"
    message.

> **SS:**
>
<img width="326" alt="image" src="https://github.com/user-attachments/assets/ca690636-5206-4656-afdd-90d9f4f679d3">


**Rubric**

  ---------------------------------------------------------------------------------------
  **Criteria**      **Excellent       **Good (7)**    **Needs          **Unsatisfactory
                    (10)**                            Improvement      (1)**
                                                      (3)**            
  ----------------- ----------------- --------------- ---------------- ------------------
  Understanding of  Demonstrates a    Shows a solid   Has a basic      Shows little or no
  Services          deep              understanding   understanding of understanding of
                    understanding of  of services,    services, but    services.
                    the concept of    but may lack    may struggle     
                    services, their   some depth in   with specific    
                    roles, and their  specific areas. concepts.        
                    importance in                                      
                    Windows.                                           

  Service           Successfully      Demonstrates    Can perform      Struggles to
  Management Skills starts, stops,    proficiency in  basic service    perform even basic
                    restarts, and     managing        management       service management
                    configures        services, but   tasks, but may   tasks.
                    services using    may encounter   need assistance  
                    the Services app. minor           or guidance.     
                                      difficulties.                    

  Custom Service    Successfully      Can create a    Has limited      Cannot create a
  Creation          creates and       custom service, experience with  custom service.
                    manages a custom  but may         creating custom  
                    service using the encounter minor services.        
                    appropriate tools difficulties or                  
                    and techniques.   require                          
                                      assistance.                      

  Problem-Solving   Demonstrates      Can effectively May require      Struggles to
                    strong            troubleshoot    assistance to    troubleshoot and
                    problem-solving   and resolve     troubleshoot     resolve issues.
                    skills when       most issues     some issues.     
                    encountering      related to                       
                    challenges or     service                          
                    errors.           management.                      

  Documentation and Provides clear    Documents the   Provides basic   Does not provide
  Reporting         and concise       lab activities  documentation,   any documentation
                    documentation of  adequately, but but may be       or reporting.
                    the lab           may lack some   disorganized or  
                    activities,       detail or       incomplete.      
                    including         clarity.                         
                    relevant                                           
                    screenshots and                                    
                    observations.                                      

  **Score:**        **/50**                                            
  ---------------------------------------------------------------------------------------
