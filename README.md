# EX 01 : Developing a Simple Webserver
## DATE : 10/09/2023
## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation
### Step 2:
Design of webserver workflow
### Step 3:
Implementation using Python code
### Step 4:
Serving the HTML pages.
### Step 5:
Testing the webserver

## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """

<!DOCTYPE html>
<html>
<head>
<title>Mithun's Webserver</title>
</head>

<body>
<h1>Top 5 revenue generating companies</h1>
<hr>
<h2>
<ol>
<li>Apple</li>
<li>Amazon</li>
<li>Microsoft</li>
<li>Infosys</li>
<li>Samsung</li>
</ol>
</h2>   

<h1>Done by MithunRaj(212222040100)

</body>
</html>

"""

class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8001)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()


```

Done by MithunRaj (212222040100)
## OUTPUT:
![EX01 output](https://github.com/Mithunlavanyaraj/simplewebserver/assets/120077786/86f43494-fd46-4725-9dcb-40cb4ab75e53)

![output](https://github.com/Mithunlavanyaraj/simplewebserver/assets/120077786/68c0fbb0-0032-4bc9-9b81-de2e137158bc)


## RESULT:
The program for implementing simple webserver is executed successfully.
