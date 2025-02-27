Splunk Deployment on Linux Server
=================================

Introduction
------------

Splunk supports all major operating systems and provides a straightforward installation process. This guide focuses on installing **Splunk Enterprise** on a **Linux server** and getting it up and running within minutes.

Typically, Splunk is downloaded from the official website:  
[Splunk Enterprise Download](https://www.splunk.com/en_us/download/splunk-enterprise.html?locale=en_us)

At the time of writing, the latest available version is **9.0.3**.

**Note:** You are not required to create an account or manually download Splunk, as all necessary installation files are already available in the lab environment.

* * *

1\. Verify Installation Files
-----------------------------

Splunk installers are located in `~/Downloads/splunk`. First, navigate to the directory and verify the contents using:

bash

CopyEdit

`cd ~/Downloads/splunk
ls` 

**Expected output:**  
\[Replace with actual screenshot link: screenshots/1\_splunk\_dls\_ls.png\]

The directory should contain the following files:

*   `splunk_installer.tgz` – The main Splunk Enterprise package
*   `splunkforwarder.tgz` – Splunk Universal Forwarder package

* * *

2\. Switch to Root User
-----------------------

Before proceeding with the installation, switch to the **root user**:

nginx

CopyEdit

`sudo su` 

This ensures that all necessary permissions are granted for installation.

* * *

3\. Extract and Install Splunk
------------------------------

Extract the Splunk installer package using the following command:

nginx

CopyEdit

`tar xvzf splunk_installer.tgz` 

This will unpack Splunk into a new directory named `splunk`.

**Expected output:**  
\[Replace with actual screenshot link: screenshots/2\_splunk\_dls\_tar.png\]

* * *

4\. Move Splunk to `/opt/` Directory
------------------------------------

To maintain a clean directory structure, move the extracted `splunk` folder to `/opt/`:

bash

CopyEdit

`mv splunk /opt/` 

Verify the move by listing the contents of `/opt/`:

bash

CopyEdit

`ls /opt/` 

**Expected output:**  
\[Replace with actual screenshot link: screenshots/3\_splunk\_dls\_ls\_dir.png\]

* * *

5\. Start Splunk for the First Time
-----------------------------------

Navigate to Splunk’s `bin` directory and start the service:

bash

CopyEdit

`cd /opt/splunk/bin
./splunk start --accept-license` 

Since this is the first time launching Splunk, you will be prompted to create an **administrator account**.

*   Enter a username: `splunkadmin`
*   Create and confirm a password

**Expected output:**  
\[Replace with actual screenshot link: screenshots/4\_splunk\_dls\_start.png\]

Once Splunk starts, it will be accessible at:  
`http://coffely:8000`

* * *

6\. Access Splunk Web Interface
-------------------------------

Open a web browser inside the virtual machine and navigate to:

arduino

CopyEdit

`http://coffely:8000` 

Alternatively, if using an external connection, replace `coffely` with the **machine's IP address**:

cpp

CopyEdit

`http://MACHINE_IP:8000` 

Login with the **admin credentials** created earlier.

**Expected login screen:**  
\[Replace with actual screenshot link: screenshots/5\_splunk\_dls\_login.png\]

* * *

Conclusion
----------

Congratulations! You have successfully installed and started **Splunk Enterprise** on a Linux machine.

### Next Steps:

*   Explore the **Splunk Web UI**
*   Set up **data ingestion** from different log sources
*   Configure **Splunk Forwarders**

Stay tuned for the next section on configuring log ingestion!

* * *
