# Docker-Honeypot

A Docker Compose deployment of Cowrie SSH honeypot that captures and logs attacker activity in real-time. 
Monitors login attempts, commands, and file downloads from automated attacks.

**Features**  
SSH honeypot on port 2222  
Real-time attack logging to terminal  
Captures login attempts, commands, and file downloads  
Easy deployment with Docker Compose  

**How to Use**  
Make sure that docker is installed and run the following command:  
`docker-compose up -d`  
Monitor and view commands:  
`docker-compose logs -f cowrie`  
Test Locally:  
`ssh root@localhost -p 2222`  

**Example Output**  
`2024-01-15T10:30:00+0000 [HoneyPotSSHTransport] login attempt [b'root'/b'12345'] succeeded`    
`2024-01-15T10:30:05+0000 [HoneyPotSSHTransport] CMD: whoami`  
`2024-01-15T10:30:08+0000 [HoneyPotSSHTransport] CMD: uname -a`  
`2024-01-15T10:30:12+0000 [HoneyPotSSHTransport] Downloaded http://malicious.com/script.sh`  
