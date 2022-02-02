# Burp Suite 

## Task 1 Intro 

Resource [thm](tryhackme.com)

Learning the basics and major components of Burp Suite, the de facto tool to use when performing web app testing.

<body> <p>  

Burp Suite, a framework of web application pentesting tools, is widely regarded as the de facto tool to use when performing web app testing.
By default burp-suite community is installed in kali


### Read the overview and continue on into installation!

 <i> ans: no answer needed </i>
 
 
 ## Task 2 Installation 
 
 
We'll use the Burp Suite Community Edition throughout this lab, however, I'll be covering some paid features briefly as well to help you prepare for eventually using the Professional version.

### If you'll be installing Burp (as it's commonly referred to) from scratch, you'll need to first visit this link: https://portswigger.net/burp/communitydownload
 <i> ans: no answer needed </i>
 
 ### Once you've reached the Port Swigger downloads page, go ahead and download the appropriate version for your operating system
 <i> ans: no answer needed </i>
 
 ### Burp Suite requires Java JRE in order to run. Download and install Java here: https://www.java.com/en/download/
Once you've got everything setup move onto our next task, Gettin' [CA] Certified!

 <i> ans: no answer needed </i>

## Task 3 Gettin' [CA] Certified 
 
 

Before we can start using our new installation (or preinstalled) Burp Suite, we'll have to fix a certificate warning. We need to install a CA certificate as BurpSuite acts as a proxy between your browser and sending it through the internet - It allows the BurpSuite Application to read and send on HTTPS data. 

A certificate warning that will appear unless we install Burp's CA Certificate.

One quick note, in this lab I'll be using Firefox and Foxy Proxy. I use Firefox in this instance as it's a little bit easier to work with when using Burp Suite. 

 First, let's go ahead and launch Burp.
 click on 'Applications' and type in Burp Suite. Click on the Burp Suite icon that appears.
 
 ### launch burp
  <i> ans: no answer needed </i>

 

Once you've launched Burp, you'll be greeted with the following screen:
 ![image](https://user-images.githubusercontent.com/41240719/152121624-3e3c81d2-4a3e-46f4-877a-5dc9c2cd9640.png)

### Once this pops-up, click 'Temporary project' and then 'Next'.

*Now as you likely noticed both 'New project on disk' and 'Open existing project' are both grayed out. As annotated at the top of this window saving projects is a feature associated with Burp Suite Professional as it's pretty common to save and come back to a multi-day web application test. 
  <i> ans: no answer needed </i>
 
 Next, we'll be prompted to ask for what configuration we'd like to use. For now, select 'Use Burp defaults'.
 ![image](https://user-images.githubusercontent.com/41240719/152122102-ba7ca1b7-054b-4309-9f11-5cb5b96f653b.png)
 
### This option is included as it can be incredibly useful to create a custom configuration file for your proxy or other settings, especially depending on how your network configuration and/or if Burp Suite is being launched remotely 
   <i> ans: no answer needed </i>
 
 ### Finally, let's go ahead and Start Burp! Click 'Start Burp' now!
   <i> ans: no answer needed </i>

 You'll now see a screen that looks similar to this:
 ![image](https://user-images.githubusercontent.com/41240719/152122652-1084925c-dd66-4212-b2e7-880c2eb4c4e6.png)

 Since we now have Burp Suite running, the proxy service will have started by default with it. In order to fully leverage this proxy, we'll have to install the CA certificate included with Burp Suite (otherwise we won't be able to load anything with SSL). To do this, let's launch Firefox now!

 ###  *You can do this part with your browser of choice, however, I'll be using Firefox
  <i> ans: no answer needed </i>
 
 

Now that we've started Burp, let's add an extension to our web browser to allow up to easily route or traffic through it! For this room, we'll be using 'FoxyProxy Standard' on Firefox.
 ![image](https://user-images.githubusercontent.com/41240719/152124177-a1af2257-440e-4939-8d09-30955a26dc9d.png)

 Navigate to the following link to install FoxyProxy Standard:
 
 ### Go ahead and install this now!
   <i> ans: no answer needed </i>

 

Next, click on FoxyProxy among your extensions. 
 ![image](https://user-images.githubusercontent.com/41240719/152124638-9999c0a7-34dd-44ce-9e4a-35b4f918ff45.png)
 <br>
 After that, click on 'Options'.
 ![image](https://user-images.githubusercontent.com/41240719/152124712-440e9d4e-957f-42cf-9137-0d01f6a9e951.png)
 <br>
 After that, click 'Add' in the top left. 
 <br>
 ![image](https://user-images.githubusercontent.com/41240719/152124887-61ad8ed1-b5d2-461a-8830-bd76e9bd3c20.png)
 <br>
 Enter in the following settings and then click 'Save'
 ![image](https://user-images.githubusercontent.com/41240719/152128120-cb6cccc8-b785-4f27-9a1f-0a5563d96557.png)
  <br>
 Finally, click on the FoxyProxy extension icon again and select 'Burp'.
 
 ### Next, we'll move onto adding the certificate for Burp!
  <i> ans: no answer needed </i>
 
 ### With Firefox, navigate to the following address: http://localhost:8080
 <i> ans: no answer needed </i>
 

You'll be greeted with the following website:
 ![image](https://user-images.githubusercontent.com/41240719/152125818-d45dd486-511c-4aac-bb2c-bf7603debe02.png)

 ### Click on 'CA Certificate' in the top right to download and save the CA Certificate.
  <i> ans: no answer needed </i>
 
 

Now that we've downloaded the CA Certificate, move over to the settings menu in Firefox. Search for 'Certificates' in the search bar.
 ![image](https://user-images.githubusercontent.com/41240719/152126094-c2df2dee-b83f-415c-9fc4-38426c5d36cf.png)

 ### Click on 'View Certificates'
  <i> ans: no answer needed </i>
 
 ### Next, in the Authorities tab click on 'Import'
   <i> ans: no answer needed </i>
 
 ### Navigate to where you saved the CA Certificate we downloaded previously. Click 'OK' once you've selected this certificate.
    <i> ans: no answer needed </i>

 

Finally, select the following two options seen in this photo:
 ![image](https://user-images.githubusercontent.com/41240719/152126692-09119fa9-44b8-4fcd-af92-da8b6a222c4d.png)

 ### Select 'OK' once you've done this. Congrats, we've now installed the Burp Suite CA Certificate!
  <i> ans: no answer needed </i>

 
 
 ### 

