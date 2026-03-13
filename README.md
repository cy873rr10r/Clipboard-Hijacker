# Clipboard-Hijacker Payload
## Objective:
The Clipboard Hijacker Payload is a simple post exploitation method for pentesting purpose. Clipboard-Hijacker Payload aims to monitor, capture, and potentially manipulate clipboard data on a target machine. This data is often used to store sensitive information like passwords, cryptocurrency wallet addresses, credit card details, or other data users copy and paste during normal activities. The payload could also modify clipboard contents to redirect actions like payments or logins to attacker-controlled entities.

This payload automatically send the captured clipboard data to your web server or webhook in every 10 seconds.

## How It Works:

### Capture Clipboard Data: 
The script continuously monitors clipboard contents in every 10 seconds
### Post Data to Server: 
This payload is send an HTTP POST request to your web server or webhook, where the clipboard data is passed as part of the Body.

<b>clipboard_data: </b> Contains the text data from the clipboard.

<b>machine_name and user_name:</b> These environment variables capture additional information about the compromised machine.

### Optional Logging: 
The script also logs clipboard data locally on the machine for redundancy.
### Error Handling: 
The script catches and logs any errors that occur while trying to send data to the web server.
## How to use:
Run Flask webserver your attacker machine using python so you need to install flask.
```
python3 -m pip install flask
```
Now you can run the following command for run the server
```
python3 server.py
```
change your webserver's IP address in clipboardhijacker.ps1 file & run this script using following command or other method like USB rubber ducky, metasploit command execution etc.
```
powershell -NoP -NonI -W h -Exec Bypass .\clipboardhijacker.ps1
```
after that your webserver will getting target machine clipboard data in every 10 sec.

<b>Desclaimer: </b> this program only for pentesting & educational purposes only so don't miss use this program.

### Video Demo
[![Clipboard-Hijacker Demo](https://img.youtube.com/vi/WylviCWbz9M/0.jpg)](https://www.youtube.com/watch?v=https://youtu.be/WylviCWbz9M)

### For More Video subcribe <a href="http://youtube.com/techchipnet">TechChip YouTube Channel</a>
check check check check