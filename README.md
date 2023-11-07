Hi Im Demongrae 
- 👋 Hi, I’m @Demongrae
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Demongrae/Demongrae is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

import socket

def scan_ports(target_host, start_port, end_port):
    for port in range(start_port, end_port + 1):
        try:
            # Create a socket object
            s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
            # Set a timeout for the connection attempt (adjust as needed)
            s.settimeout(1)
            # Attempt to connect to the target on the current port
            result = s.connect_ex((target_host, port))
            if result == 0:
                print(f"Port {port} is open")
            s.close()
        except socket.error:
            pass

if __name__ == "__main__":
    target_host = "example.com"  # Replace with the target IP or hostname
    start_port = 1  # Start port number
    end_port = 100  # End port number

    scan_ports(target_host, start_port, end_port)
scan_ports(target_host, start_port, end_port)
f"Port {port} is open"

