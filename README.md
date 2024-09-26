# EX01 Developing a Simple Webserver
## Date:26/9/24

## AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
```
<!DOCTYPE html>
<head>
    <title>LAPTOP CONFIGURATION</title>
</head>

<body><center>
    <h1>My laptop configuration</h1>MOHAMED FAIZAL<h1></h1></center>
    <table border="2px" align="center" cellpadding="10" style="background-color: antiquewhite;" >
    <tr style="color: black; ">
        <th>DEVICE SPECIFICATION</th>
        <th>DETAILS</th>
    </tr>
    <tr style="color: rgb(0, 0, 0); ">
        <td>BRAND</td>
        <td>LENOVO</td>
    </tr>
    <tr>
        <td>MODEL NAME</td>
        <td>E15 GEN 4</td>
    </tr>
    <tr>
        <td>SCREEN SIZE</td>
        <td>15.6 inches</td>
    </tr>
    <tr>
        <td>COLOR</td>
        <td>BLACK</td>
    </tr>
    <tr>
        <td>RAM</td>
        <td>16GB</td>
    </tr>
    <tr>
        <td>HARD DISK</td>
        <td>CORE i5</td>
    </tr>
    <tr>
        <td>GRAPHICS CARD</td>
        <td>NVIDIA</td>
    </tr>
    <tr>
        <td>SYSTEM TYPE</td>
        <td>64 BIT-OS,X64</td>
    </tr>
</table>

</body>



class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200) 
        self.send_header("content-type", "text/html")       
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver") 
server_address =('',8000)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
```


## OUTPUT:
![Screenshot 2024-09-26 225257](https://github.com/user-attachments/assets/ca69a3a7-5a26-4d5a-b253-8604763b9e7b)


## RESULT:
The program for implementing simple webserver is executed successfully.
