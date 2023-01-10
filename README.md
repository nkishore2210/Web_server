# Developing a Simple Webserver.
## Register number:22008365
## Developed by:kishore
# AIM:

Develop a webserver to display about top five web application development frameworks.

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver

# PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<titlt>MY WEBSERVER</title>
</head>
<body>
<h1>WELCOME TO MY SIMPLE WEBSERVER</h1>
</body>
</html>
"""
class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request recieved")
        self.send_response(200)
        self.send_header('Content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())


server_address = ('', 8080)
httpd = HTTPServer(server_address, HelloHandler)
print("my webserver is running.....")
httpd.serve_forever()
```
# OUTPUT:
# server side view:
![Screenshot_20221227_093810](https://user-images.githubusercontent.com/118707090/211476931-75dce359-dd47-44a1-84dc-995188c5ace0.png)
# client side view:
![WhatsApp Image 2023-01-10 at 11 35 22](https://user-images.githubusercontent.com/118707090/211477133-db0fb6ca-6f1b-4a57-bd04-d57918fb5450.jpg)


# RESULT:

The program is executed succesfully

