---
published: false
---
HTTP/1.1

	- Resources:
		 - URL format = 
					> URL_Scheme (eg http) 
					+ Host (eg google.com) 
					+ Port (80 is default, usally hidden) 
					+ URL_Path (route) 
					+ Query_String
					+ Fragment (used just in the browser to navigate the resource)
		
        - URL encoding : 
			- [i-technica.com](http://i-technica.com/whitestuff/urlencodechart.html){:target="_blank"}
			- [urlencoder.org](http://www.urlencoder.org/){:target="_blank"}
		- URL MIME types (content types, [Media type on wikipedia](https://en.wikipedia.org/wiki/Media_type){:target="_blank"})
			- file extension - register the file extension in the MIME app server register 
			- content type negotiations: 
	
	- Messages:
		- Language specification : [w3.org rfc2616](https://www.w3.org/Protocols/rfc2616/rfc2616.html){:target="_blank"}
		- Messages types:
			1) HHTP Request 
				- Methods : 
					- GET (read, safe)
						- parameters get append as query strings to the URL
					- POST (udpate, unsafe) 
						- see POST/redirect/GET pattern : [Post/Redirect/Get](https://en.wikipedia.org/wiki/Post/Redirect/Get){:target="_blank"}
						- parameters get append the HTTP message 
					- PUT (insert, unsafe)
					- DELETE (delete, unsafe)
					- HEAD (read headers form resource)
				- Format: 
					> [method] [URL] [version]
					[headers] (1 or more)
					[body]
					
					eg:
					
					> GET http://server.com/art/1231.aspx HTTP/1.1231
					Host: server.com 
					Accept-Language: fr-FR
					Date: Mon, 30 Ian 2017 20:02:00 GMT
					
				- Common Request Headers:
					- Refer, User-Agent, Accept, Accept-Language, Cookie, If-Modified-Since, Date
					- see also q values : 
						[Browser REST HTTP AcceptHeaders](http://www.newmediacampaigns.com/blog/browser-rest-http-accept-headers){:target="_blank"}
						[w3 rfc2616 sec14](https://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html)
				- Manual, eg with telnet :
						a) set port to 80 : 
							telnet google.com 80
						b) perform request :
							GET /res.jpg HTTP/1.1
							Host:google.com
						see also URL Canonicalization (the process of choosing the best URL when there are several options)
							[Canonical URL](http://catchupdates.com/what-canonical-url-canonicalization/){:target="_blank"}
			
			2) HHTP Response 
				- Format: 
					> [version] [status] [reason]
					[headers] (1 or more)
					[body]
                
				- Status codes: 
					Informational (100-199), 
					Successful (200-299) , eg: 200 - OK
					Redirection (300-399), 
					Client Error (400-499), eg: 404 - Notfound
					Server Error (500 - 599)
				- Check out Fiddler for testing: 
					[fiddler](http://www.telerik.com/fiddler){:target="_blank"}
			
			3) HTTP Connection
				- Connection layers : 
					HTTP (app) ->
						TCP (transport) ->
							IP(network) ->
								Ethernet (data layer) <->
							IP(network) <-
						TCP (transport) <-
					HTTP (app) <-
				- check out [wireshark](https://www.wireshark.org/){:target="_blank"}
				- for parallel connections refer to [w3.org rfc2616 sec8](https://www.w3.org/Protocols/rfc2616/rfc2616-sec8.html){:target="_blank"}
				- persisted connections (HTTP keep-alive, or HTTP connection reuse) are default in 1.1 ([HTTP Persistent Connection](https://en.wikipedia.org/wiki/HTTP_persistent_connection){:target="_blank"})
				- pipeline connections (a technique in which multiple HTTP requests are sent on a single TCP connection without waiting for the corresponding responses, [Connection management in HTTP 1.x](https://developer.mozilla.org/en-US/docs/Web/HTTP/Connection_management_in_HTTP_1.x){:target="_blank"})
			
			4) HTTP Architecture
				- [Architectural Styles and the Design of Network-based Software Architectures](http://www.ics.uci.edu/~fielding/pubs/dissertation/top.htm)
				- Proxy and Caching strategies ([REST HTTP Cache](http://odino.org/rest-better-http-cache/){:target="_blank"})
				
			5) HTTP Security
				- Stateful vs Stateless web approaches : 
					- Embed state in the resource
					- Saved in sessions
					- Cookies  (includes the Set-Cookie attribute in the server response header)
						[HTTP State Management Mechanism](https://tools.ietf.org/html/rfc6265)
				- Authentication 
					- Basic Authentication (basic 64 encoding)
					- Digest Authentication 
					- Windows Authentication 
					- Forms Authentication 
					- OpenID
				- HTTPS
					- approaches: client and server certification 
					- all is encrypted except the host name
					- 443 default port
					- Connection layers : 
						HTTP (app) ->
							SSL/TLS (encryption) -> 
								TCP (transport) ->
									IP(network) ->
										Ethernet (data layer) <->
									IP(network) <-
								TCP (transport) <-
							SSL/TLS (decryption) <-
						HTTP (app) <-
