
https://www.google.com/?redirect_to=https://www.attacker.com

Open Redirect vulnerabilities is a method of changing the url's parameter "redirect=" from a usual subdomain of a website to a link where attackers can obtain your sensitive information.

This can also be apply to HTML <meta> tags and javascript. 

**Examples** 

1. SHOPIFY THEME INSTALL OPEN REDIRECT
	1. this is what I call normal open redirect where the url is direct to the malicious configuration of the "redirect" parameter.
2. SHOPIFY LOGIN OPEN REDIRECT
	1. in this example, a "checkout" parameter, which is different from the previous example. Instead of a direct approach where you immediately sent to the attacker page, you first have to go to the legit page of the base website, which is the login page of shopify. It is only after you click the login which the checkout parameter is occured and activated. thus, leading you to the attacker site.
*note that the difference of the end url result differs. first example shows that the exact url of the attacker is fully visible without any extra domain. THIS is the opposite for 2nd example where the shopify has its tailed url which is the attacker, so two domains in 1 url. however, only the rightmost domain is executed and run. And that is how users are "fooled"*


**Insights**
Open redirects occur when a developer mistrusts attacker-controlled input

**Questions**
	1. What are the other parameter's value in a website?
	2. where is that location header? 

It seems like I have to learn javascript fundamentals first. I'm not familiar with DOM.

**Resources**

Source:[[Yaworski, Peter - Real-World Bug Hunting. A Field Guide to Web Hacking (2019, No Starch Press) - libgen.li.pdf]]

https://chatgpt.com/share/685bd820-7afc-800d-bd9f-8613140a7e2d

**Reflection**
	It seems like shopify is always being exploited lol


**TESTING THE VULNERABILITY**

Great! Let’s walk through **how to safely recreate an Open Redirect exploit like the Shopify example** in your **local test environment**, so you can fully understand and experiment with it.

---

## 🧪 Recreating the Shopify-style Open Redirect

### 🧱 **1. Set Up a Simple Web Server**

You can use **Python** to create a basic HTTP server that simulates the redirect behavior.

#### ✅ Create a file called `app.py`:

```python
from flask import Flask, request, redirect

app = Flask(__name__)

@app.route("/login")
def login():
    checkout_url = request.args.get("checkout_url", "/home")
    return redirect("http://mystore.myshopify.com" + checkout_url)

if __name__ == "__main__":
    app.run(debug=True)
```

📝 This simulates how Shopify appended the parameter's value to a base URL.

---

### 🌐 **2. Run Your Server**

In your terminal, run:

```bash
pip install flask
python app.py
```

This will start your server at:

```
http://127.0.0.1:5000
```

---

### 🔥 **3. Test the Vulnerability**

Now try visiting:

```bash
http://127.0.0.1:5000/login?checkout_url=.attacker.com
```

The server will redirect you to:

```
http://mystore.myshopify.com.attacker.com
```

Even though the code only appends the `checkout_url` value, this creates a malicious **subdomain** under `attacker.com`.

You can also try:

```
?checkout_url=//attacker.com
?checkout_url=http://evil.com
```

---

### 🌐 **4. (Optional) Set Up a Fake `attacker.com`**

If you want to simulate this completely:

1. Register a free `.tk` or `.cf` domain.
    
2. Set a wildcard DNS (like `*.yourdomain.tk`) pointing to your local server or a server you control.
    
3. Visit a redirect like:
    
    ```
    http://mystore.myshopify.com.yourdomain.tk
    ```
    

Your domain will catch that request and serve a fake login page, phishing form, or logging script.

---

### ✅ **What You Learned**

- **How subdomain structure can be manipulated** to appear trustworthy.
    
- **How bad redirect logic** can be exploited using clever input (even without full URLs).
    
- How important **sanitizing and validating** user input is, even in "safe-looking" contexts.
    

---

Would you like to build a **defense mechanism** for this next, or expand this into a **bug bounty test checklist**?