
Standalone webapp to list all managed devices in an integrated and organized way. For HPC data center, you can put managed UPS, PDU, Switch, storage servers, JBOD chassis, etc into a single web page. 
It works kind of like a property management system, and most importantly gives admins an integrated interface to manage all critical devices.

Put all the nodes information in a CSV file, by default: nodes.csv. You can also open any CSV files, once they have the format of:
~~~
name,internal-ip,ipmi-ip,mgmt-ip,type,rack,location,status,description,serial
~~~

You can download the index.html, and prepare your notes.csv file. Using any web browser to open it. It should work well offline(some browser might not support well). You need to keep maintaining this nodes.csv file.

You can also start light-weighted web service as a regular user, on a Linux box, like Rocky Linux 9:

~~~
>python3 -m http.server 8​111 --bind 127.0.0.1
~~~

Bind it to an internal network, to keep it away from outsider access, for the sake of security.

Use a web browser to open: 
```
http://127.0.0.1:8111/
```

 <img width="1532" height="663" alt="node-viewer" src="https://github.com/user-attachments/assets/2a99aa28-c5ea-4590-acb6-e795a56c2c50" />

