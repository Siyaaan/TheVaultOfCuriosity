This is more of a How the internet works when you search a site

This will just be an overview on how the internet works to get the context of web vulnerabilities for bug hunting

*vulnerability* is a weakness in a system where it can be exploited unethically.

	as far as my understanding goes, there will always be a vulnerability on any kind of system in technology.

*packets* 
	It is a complete package of data and information and where it came from and to whom it will be sent. This might be the complete message or mail of each networks 

	packets travel on 1s and 0s right? so does it travel in electricity on onn and off?


Okay so the steps of what happen when you visit a website

	1. you type a domain name on browser
	2. that browser sends a request through dns to locate the ip of the server 
	3. dns then match the domain name to its corresponding ip address of a server (it is important to note that web server doesn't communicate back on the dns)
	4. then the dns sends back the ip address of where that server is 
	5. the connection between the client and the server is built and the dns is removed
	6. the browser delivered the connection to the server and the server answers back and this process is called tcp
	7. it is basically a port from the client connect to a port of the server, depending on the port of that server is what kind of services you will be getting into.
	8. it can be port 80 which is http, port 443 which is https.

	- **You type a domain name into your browser.**
    
- **The browser sends a request to a DNS server to resolve the IP address of that domain.**
    
- **The DNS server matches the domain name to its corresponding IP address** (note: the web server does **not** communicate with the DNS — it's a separate system).
    
- **The DNS server sends the IP address back to the browser.**
    
- **The browser now builds a connection to the server at that IP; DNS is no longer involved.**
    
- **This connection is established using TCP — a reliable communication protocol.**
    
- **The client opens a temporary port and connects to a specific port on the server. The server’s port determines what type of service is being requested.**
    
- **For example, port 80 is used for HTTP (unsecured web), and port 443 is used for HTTPS (secure web).**

Once the connection is successful, the browser then make an http request to the server

![[Pasted image 20250623155750.png]]

And this is how the web server responds

![[Pasted image 20250623155707.png]]









**Reminders**
I still haven't included different types of request

**QUESTIONS:**
why don't just clients connect to a server without the dns.

what happens if a different service is requested like an email server





**Resources**
https://chatgpt.com/share/68590e55-fd68-800d-9364-c39a43658654

[[Yaworski, Peter - Real-World Bug Hunting. A Field Guide to Web Hacking (2019, No Starch Press) - libgen.li.pdf]]

**Reflection**
I feel a sense of uncertainty if I really learned something. I can feel on my self that I actually learned how internet works through browser, dns, and server. It's just there is a feeling that you think this knowledge will slip away from you.

knowledge starts on the middle. Another reason why I feel uncertain is because the concept of how internet works is actually in the middle. What I mean is there is far more details when you deep dive how it works on a low level. And additionally, you know that there is still a higher level of application of knowledge than this.

Getting overwhelmed with a lot of information. This is where you start to realize that you feel kinda overwhelm of how much information to take. Despite how humungous information is, I should keep in mind that I finally have Knowledge to start and step on to Only thing that matters with this realization is your goal. At which direction will you continue moving forward
