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

 
 <br> <br><br>
 
 ## Task 4 Overview of Features 
 
 Now that we've set up Burp, let's take a look at everything it has to offer. Web application pentesting can be a messy affair but Burp has something for every step of the way. 
 
 components of Burp Suite
 
 Proxy - What allows us to funnel traffic through Burp Suite for further analysis
 
Target - How we set the scope of our project. We can also use this to effectively create a site map of the application we are testing.
 
Intruder - Incredibly powerful tool for everything from field fuzzing to credential stuffing and more
 
Repeater - Allows us to 'repeat' requests that have previously been made with or without modification. Often used in a precursor step to fuzzing with the aforementioned Intruder
 
Sequencer - Analyzes the 'randomness' present in parts of the web app which are intended to be unpredictable. This is commonly used for testing session cookies
 
Decoder - As the name suggests, Decoder is a tool that allows us to perform various transforms on pieces of data. These transforms vary from decoding/encoding to various bases or URL encoding.
 
Comparer - Comparer as you might have guessed is a tool we can use to compare different responses or other pieces of data such as site maps or proxy histories (awesome for access control issue testing). This is very similar to the Linux tool diff.
 
Extender - Similar to adding mods to a game like Minecraft, Extender allows us to add components such as tool integrations, additional scan definitions, and more!
 
Scanner - Automated web vulnerability scanner that can highlight areas of the application for further manual investigation or possible exploitation with another section of Burp. This feature, while not in the community edition of Burp Suite, is still a key facet of performing a web application test
 <br>
 
 ### Which tool in Burp Suite can we use to perform a 'diff' on responses and other pieces of data?
  <i> ans: Comparer</i>
 <br>
 
 ### What tool could we use to analyze randomness in different pieces of data such as password reset tokens?
 <i> ans: Sequencer</i>
<br>
 
 ### Which tool can we use to set the scope of our project?
  <i> ans: target</i>
 
 <br>
 
 ### While only available in the premium versions of Burp Suite, which tool can we use to automatically identify different vulnerabilities in the application we are examining?
 <i> ans: scanner</i>
 <br>
 
 ###  Encoding or decoding data can be particularly useful when examining URL parameters or protections on a form, which tool allows us to do just that? 
  <i> ans: decoder </i>
 <br>
 
 ### Which tool allows us to redirect our web traffic into Burp for further examination?

   <i> ans: proxy </i>
 <br>

 ### Simple in concept but powerful in execution, which tool allows us to reissue requests?
 <i> ans: Repeater </i>
 <br>
 
 ### With four modes, which tool in Burp can we use for a variety of purposes such as field fuzzing?
  <i> ans: intruder </i>
 <br>

 ### Last but certainly not least, which tool allows us to modify Burp Suite via the addition of extensions?
 <i> ans: extender </i>
 <br>
 
<br><br>
 
 
 
 ## Task 5 Engage Dark Mode 
 
 
![image](https://user-images.githubusercontent.com/41240719/152168835-a2d8f3b7-2c2f-41f6-a996-37d59342a141.png)
 
 <br>

 ### With Burp Suite launched, let's first navigate to the 'User options' tab. 
 <br>
 
 ![image](https://user-images.githubusercontent.com/41240719/152169122-3faa10e6-84e2-4d42-a63b-6661568a71cb.png)
 
<br>
 
<i> ans: no answer needed </i>
 
 <br>
 
 

### Next, click on the 'Display' sub-tab. 
 
 
 ![image](https://user-images.githubusercontent.com/41240719/152169495-fd77e1a0-7948-44bd-b36b-bf8e47e36eb6.png)
 
 <i> ans: no answer needed </i>


 <br>
 

### Now, click on the 'Look and feel' drop-down menu. Select 'Darcula'. 
 <br>
 
 ![image](https://user-images.githubusercontent.com/41240719/152170018-a503cff4-4bf6-49c5-a926-3a077f70e93a.png)
 
  <i> ans: no answer needed </i>

<br>
 

### Finally, close and relaunch Burp Suite to have dark theme (or whichever theme you picked) take effect.
 
 <i> ans: no answer needed </i>
 
 <br><br><br>
 
 ### Task 6 Proxy 
 
 Generally speaking, proxy servers by definition allow us to relay our traffic through an alternative route to the internet. This can be done for a variety of reasons ranging from educational filtering (common in schools where restricted content must be blocked) to accessing content that may be otherwise unavailable due to region locking or a ban. Using a proxy, however, for web application testing allows us to view and modify traffic inline at a granular level. Throughout this task, we'll explore the major components of the Burp proxy including interception, request history, and the various configuration options we have access to. 
 
 
 <br>![image](https://user-images.githubusercontent.com/41240719/152172403-e62df214-6298-4ff3-92b2-641adf466075.png)
<br>

Basic diagram of how communications are relayed through a proxy 
 
 we configured our web traffic to route through our instance of Burp Suite. By default, Burp will be set to 'intercept' our traffic. This means a few things:

1. Requests will by default require our authorization to be sent.

2. We can modify our requests in-line similar to what you might see in a man-in-the-middle attack and then send them on.

3. We can also drop requests we don't want to be sent. This can be useful to see the request attempt after clicking a button or performing another action on the website. 

4. And last but not least, we can send these requests to other tools such as Repeater and Intruder for modification and manipulation to induce vulnerabilities.
 
 ### To complete this task you need to connect to the TryHackMe network through OpenVPN. 
 <i> ans: no answer needed </i>
 
 

###  By default, the Burp Suite proxy listens on only one interface. What is it? Use the format of IP:PORT
 <i> ans: 127.0.0.1:8080</i>
 

 ### In Burp Suite, navigate to the Intercept sub-tab of the Proxy section. Enable Intercept
 <i> ans: no answer needed </i>
 
 
 ### Return to your web browser and navigate to the web application hosted on the VM we deployed just a bit ago. Note that the page appears to be continuously loading. Change back to Burp Suite, we now have a request that's waiting in our intercept tab. Take a look at the actions, which shortcut allows us to forward the request to Repeater?
 
  <i> ans: CTRL-R </i>
 
 

 ### How about if we wanted to forward our request to Intruder?
  <i> ans: CTRL-I </i>
 
 
 
 ### 

Burp Suite saves the history of requests sent through the proxy along with their varying details. This can be especially useful when we need to have proof of our actions throughout a penetration test or we want to modify and resend a request we sent a while back. What is the name of the first section wherein general web requests (GET/POST) are saved?
<i> ans: HTTP history </i>
 
 
 
 ### Defined in RFC 6455 as a low-latency communication protocol that doesn't require HTTP encapsulation, what is the name of the second section of our saved history in Burp Suite? These are commonly used in collaborate application which require real-time updates (Google Docs is an excellent example here).
 <i> ans: WebSockets history </i>
 
 
 ###  Before we move onto exploring our target definition, let's take a look at some of the advanced customization we can utilize in the Burp proxy. Move over to the Options section of the Proxy tab and scroll down to Intercept Client Requests. Here we can apply further fine-grained rules to define which requests we would like to intercept. Perhaps the most useful out of the default rules is our only AND rule. What is it's match type?
 
 <i> ans: URL </i>
 
 
 ###  How about it's 'Relationship'? In this situation, enabling this match rule can be incredibly useful following target definition as we can effectively leave intercept on permanently (unless we need to navigate without intercept) as it won't disturb sites which are outside of our scope - something which is particularly nice if we need to Google something in the same browser.
 
  
 <i> ans: Is in target scope </i>
 
 
 <br><br><br>
 
 ## Task 7 Target Definition 
 
 The Target tab in Burp allows us to perform arguably some of the most important parts of a web application penetration test: defining our scope, viewing a site map, and specifying our issue definitions (although this is more useful within report generation and scanning). 

When starting a web application test you'll very likely be provided a few things:

- The application URL (hopefully for dev/test and not prod)
- A list of the different user roles within the application
- Various test accounts and associated credentials for those accounts
- A list of pieces/forms in the application which are out-of-scope for testing and should be avoided
 
 
 From this information, we can now start to build our scope within Burp, something which is incredibly important in the case we are planning on performing any automated testing. Typically this is done in a tiered approach wherein we work our way up from the lowest privileged account (this includes unauthenticated access), browsing the site as a normal user would. Browsing like this to discover the full extent of the site is commonly referenced as the 'happy path'. Following the creation of a site map via browsing the happy path, we can go through and start removing various items from the scope. These items typically fit one of these criteria:

- The item (page, form, etc) has been designated as out of scope in the provided documentation from the client
- Automated exploitation of the item (especially in a credentialed manner) would cause a huge mess (like sending hundreds of password reset emails - If you've done a web app professionally you've probably done this at one point)
- Automated exploitation of the item (especially in a credentialed manner) would lead to damaging and potentially crashing the web app

Once we've removed any restricted or otherwise potentially dangerous items from our scope, we can move onto other areas of testing with the various tools within Burp Suite.


###  Before leaving the Proxy tab, switch Intercept to disabled. We'll still see the pages we navigate to in our history and the target tab, just having Intercept constantly stopping our requests for this next bit will get old fast.
 <i> ans: no answer needed </i>
 
 <br>
 
 ### Navigate to the Target tab in Burp. In our last task, Proxy, we browsed to the website on our target machine (in this case OWASP Juice Shop). Find our target site in this list and right-click on it. Select 'Add to scope'. 
 <i> ans: no answer needed </i>

 <br>
 
 ### Clicking 'Add to scope' will trigger a pop-up. This will stop Burp from sending out-of-scope items to our site map.
 <i> ans: no answer needed </i>
 
 <br>
 
 ### Select 'Yes' to close the popup.
 <i> ans: no answer needed </i>
 
 <br>
 ### Browse around the rest of the application to build out our page structure in the target tab. Once you've visited most of the pages of the site return to Burp Suite and expand the various levels of the application directory. What do we call this representation of the collective web application?
 <i> ans: site map</i>
 
 
 <br>
 
 ### What is the term for browsing the application as a normal user prior to examining it further?
 <i> ans: happy path </i>
 
 
 <br>
 
 ###  One last thing before moving on. Within the target tab, you may have noticed a sub-tab for issue definitions. Click into that now. 
 <i> ans: no answer needed </i>
 
 
 <br>
 
### The issue definitions found here are how Burp Suite defines issues within reporting. While getting started, these issue definitions can be particularly helpful for understanding and categorizing various findings we might have. Which poisoning issue arises when an application behind a cache process input that is not included in the cache key?
 <i> ans: no answer needed </i>
 
 <br><br><br>
 
 
 






 
 
 
 

 
