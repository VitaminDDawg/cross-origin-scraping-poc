This is a proof of concept project. For research purposes only.

Situations arise when there is a website with a public dataset you would like to retrieve but requests/queries are limited to X amount per ip address. 
In general if you're looking to scrape such a site you would need 1000s of proxy servers. But does said site allow "Access-Control-Allow-Origin: *" ?
If so you're in luck. This means a webpage you control can trigger visitors' browsers to make requests to your targets dataset on your behalf. 
Essentially turning your sites visitors into temporary proxy servers. 

How it works.

When a visitor loads your webpage it causes their browser to send a request to your target website. The target website sends the data requested by the 
visitors' browser. The visitors' browser then sends that response data to a webhook site for your collection. All of this happens automatically in the background without 
any user knowledge or concent. 

Visitor -> Your site -> visitor -> target site -> visitor -> webhook

This method can be refined using a dynamic webpage that serves custom requests based on each individual visitor ip address, temporarily blacklisting ip addresses after
max requests and iterating through custom dataset request lists.
