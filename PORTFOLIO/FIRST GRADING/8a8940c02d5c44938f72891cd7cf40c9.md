+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 8a8940c02d5c44938f72891cd7cf40c9 |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: Sueno_Johnray K.           | DATE PERFORMED:        |          |
|                                  | 08/29/2024             |          |
+----------------------------------+------------------------+----------+
| Section: IDC2                    | DATE SUBMITTED:        |          |
|                                  | 08/292024              |          |
+----------------------------------+------------------------+----------+

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

  ------------------------------------------------------------------------------------------------------------------------
  **Status**   **Name of     **Screenshot**
               Service**     
  ------------ ------------- ---------------------------------------------------------------------------------------------
  Start        Device        ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image2.png){width="4.798611111111111in"
               Management    height="1.1291666666666667in"}
               Enrollment    
               Services      

                             

  Stop         Diagnostic    ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image3.png){width="5.219478346456693in"
               Policy        height="1.5522998687664042in"}
               Service       

  Restart      Geolocation   ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image4.png){width="4.798611111111111in"
               Service       height="1.051388888888889in"}

  Pause        Workstation   ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image5.png){width="4.798611111111111in"
                             height="0.9284722222222223in"}
  ------------------------------------------------------------------------------------------------------------------------

4.  Select five network services, right-click to view its properties.
    Modify the startup setting to Manual.

> **SS**:

  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Before Modfying**                                                                             **After Modifying**
  ----------------------------------------------------------------------------------------------- -----------------------------------------------------------------------------------------------
  ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image6.png){width="3.08209864391951in"      ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image7.png){width="3.120450568678915in"
  height="3.5245778652668416in"}                                                                  height="3.5827395013123358in"}

  ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image8.png){width="3.097645450568679in"     ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image9.png){width="3.2029451006124234in"
  height="3.5920330271216097in"}                                                                  height="3.66163823272091in"}

  ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image10.png){width="3.1795527121609797in"   ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image11.png){width="3.1754363517060367in"
  height="3.6699343832021in"}                                                                     height="3.656084864391951in"}

  ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image12.png){width="3.149667541557305in"    ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image13.png){width="3.182928696412948in"
  height="3.627602799650044in"}                                                                   height="3.6659109798775154in"}

  ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image14.png){width="3.0875in"               ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image15.png){width="3.1326388888888888in"
  height="3.515277777777778in"}                                                                   height="3.5659722222222223in"}
  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

5.  Explore the \"General\", \"Recovery\", and \"Log On\" tabs to
    understand additional service settings.

> General:
>
> ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image16.png){width="3.630197944006999in"
> height="4.1976979440069995in"}
>
> Log On:\
> ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image17.png){width="3.5535083114610675in"
> height="4.075043744531934in"}
>
> Recovery:\
> ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image18.png){width="3.4993678915135606in"
> height="4.001751968503937in"}

6.  Create a batch file that will be added as a new service later on.
    Refer to the batch file code below.

> ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image19.png){width="4.808325678040245in"
> height="2.0055664916885387in"}

7.  Save the batch file in Z:\\lastname_timer.bat

![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image20.png){width="6.863565179352581in"
height="1.6366185476815398in"}

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
> ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image21.png){width="6.277083333333334in"
> height="0.4409722222222222in"}

9.  Verify that BatchTimerService has been added to the services.

> **SS:**
>
> ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image22.png){width="5.1361329833770775in"
> height="1.0001399825021873in"}

10. **Testing the Service:** Now, if you open a new command prompt, you
    should see the timer countdown without requiring your interaction.
    Once the timer finishes, you\'ll see the \"Timer finished!\"
    message.

> **SS:**
>
> ![](vertopal_8a8940c02d5c44938f72891cd7cf40c9/media/image23.png){width="4.354774715660542in"
> height="2.437840113735783in"}

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
