<img width="616" alt="image" src="https://github.com/user-attachments/assets/d0aeba23-f864-4573-94a0-a011c43a23f2">


# SYSADM1 -- Setting Up Webserver

# Requirement: 

-   A virtual machine running Linux and Windows OS

    Task Instructions:

1.  Install IIS by adding it as a role, select necessary features,
    include monitoring tools

    <img width="608" alt="image" src="https://github.com/user-attachments/assets/dc6d62db-55c7-42ba-a54d-872dfed893d0">


2.  Create a website by opening IIS Manager

    -   Right-click on the server's name and select Internet Information
        Services Manager.

    -   Right-click on Sites and select Add Website.

    -   Enter a name, description, physical path (where your website
        files will reside), IP address, port, and host name.

        <img width="610" alt="image" src="https://github.com/user-attachments/assets/eb9b9bff-69cd-4693-abf5-f8469aaf6529">


3.  Configure the Website:

    -   Right-click on your website and select Edit.

    -   Set the Default Document to the name of your main HTML file
        \>default.html

    -   Configure other settings as needed (e.g., SSL certificates,
        authentication)

4.  Create a Web Page:

    -   Create an HTML file in the physical path you specified.

       <img width="610" alt="image" src="https://github.com/user-attachments/assets/961595f3-8883-4440-9ff9-696268d210fd">


    -   Save it as default.html or your preferred name. (name :
        index.html)

       <img width="608" alt="image" src="https://github.com/user-attachments/assets/382b0691-46fc-4ff7-b4d7-20661c1e739d">


5.  Test the Web Server:

    -   Open a web browser and enter the URL of your website (e.g.,
        http://localhost).

    -   You should see your web page displayed.

       <img width="611" alt="image" src="https://github.com/user-attachments/assets/fed653d2-4fdc-4024-bb8c-1142bbd3ecec">


       <img width="610" alt="image" src="https://github.com/user-attachments/assets/e521465e-f7da-4986-a487-e5899dacfcfe">
