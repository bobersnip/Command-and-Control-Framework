This is a Custom Command and Control malware framework titled: LMAOware, 
written by Aidan Nagao (me), Justin Wong, and Edward Chien.

Command and Control Framework Features:
- Implant gathers environment info before running.
  - This specific implant checks for a specific file before running, making it safe to run on an ordinary machine.
    It will detonate itself before any harm is done, if the file is not found.
- Stealer functionality for the Google Chrome default user.
- Implant will send a register request to the server, which will allow commands to be forwarded to the infected host.
- Commands can be sent from the server to any implant via stegonagraphic images (png).
  - Bit strings are hidden within the image pixel values, leaving the images intact, while also concealing (up to) 3 commands.
  - These images are then deleted once used.

This framework was written using C++, Python, HTML, and MySQL.
- The malware implant/agent was written with C++.
- The server was written with Python, using Flask and Gunicorn for hosting.
- The client (used to send commands to the server) was written with HTML and routing with Flask.
- Backend database utilized MySQL.



For some more details regarding this project, please see our slides for it here: 
https://docs.google.com/presentation/d/191optzyMZHfWX9qA45oPp681APqYaaJKk2frK2uthwI/edit#slide=id.g106e742d35d_0_0
