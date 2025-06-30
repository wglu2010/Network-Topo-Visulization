# Network-Topo-Visulization
Visualize your network topology based on retrieved LLDP information(Juniper router only)

Step1: running the python script to collect the LLDP output and render into following text table:
python ./get_lldp_ccl.py
cat lldp_output_ccl.txt
acx7024-1 et-0/0/5 acx2200-2 xe-0/3/0
acx7024-1 et-0/0/1 acx7024-2 et-0/0/0
acx7024-2 et-0/0/0 acx7024-1 et-0/0/1
acx7024-2 et-0/0/1 acx7024-3 et-0/0/1
acx7024-3 et-0/0/1 acx7024-2 et-0/0/1
acx7024-3 et-0/0/0 acx7024-4 et-0/0/1
acx7024-4 et-0/0/4 acx2200-3 xe-0/3/1
acx7024-4 et-0/0/1 acx7024-3 et-0/0/0
acx7100-a et-0/0/1 acx7024-1 et-0/0/0
acx7100-a et-0/0/0 acx7024-4 et-0/0/0
acx2200-2 xe-0/3/1 acx2200-3 xe-0/3/0
acx2200-2 xe-0/3/0 acx7024-1 et-0/0/5
acx2200-3 xe-0/3/0 acx2200-2 xe-0/3/1
acx2200-3 xe-0/3/1 acx7024-4 et-0/0/4

Step2: run a local http server:
 ansible % http-server 
Starting up http-server, serving ./

http-server version: 14.1.1

http-server settings: 
CORS: disabled
Cache: 3600 seconds
Connection Timeout: 120 seconds
Directory Listings: visible
AutoIndex: visible
Serve GZIP Files: false
Serve Brotli Files: false
Default File Extension: none

Available on:
  http://127.0.0.1:8080
  http://192.168.1.25:8080

Step3: open Chrome brower and pointing to http://localhost:8080/lldp-visual-topo/draw_topology_ccl.html

Click the toggle button to display/hide the link label of the network
<img width="854" alt="Screenshot 2025-06-30 at 10 19 32 AM" src="https://github.com/user-attachments/assets/3933e4d8-5c93-4f7e-9538-45a39fde8b0f" />

<img width="868" alt="Screenshot 2025-06-30 at 10 19 19 AM" src="https://github.com/user-attachments/assets/a9e25540-7ca1-4a34-86f6-2f6367aa21da" />



