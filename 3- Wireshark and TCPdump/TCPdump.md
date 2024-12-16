# Tcpdump - Capture your first packet 

## Scenario 
You’re a network analyst who needs to use tcpdump to capture and analyze live network traffic from a Linux virtual machine.

The lab starts with your user account, called analyst, already logged in to a Linux terminal.

Your Linux user's home directory contains a sample packet capture file that you will use at the end of the lab to answer a few questions about the network traffic that it contains.

Here’s how you’ll do this: First, you’ll identify network interfaces to capture network packet data. Second, you’ll use tcpdump to filter live network traffic. Third, you’ll capture network traffic using tcpdump. Finally, you’ll filter the captured packet data.


## Solutions
1. Identify Network Interfaces.
   
* Use `ifconfig` to identify the interfaces that are available:
  
![chrome_71aeK1ZgJE](https://github.com/Fulgeo/Google-Cybersecurity-Professional-Certificate/blob/main/Image/wireshark%20and%20tcp%20dump%20image/1.png)

* Identify the interface options available for packet capture:

![chrome_OslduuRBmA](https://github.com/Fulgeo/Google-Cybersecurity-Professional-Certificate/blob/main/Image/wireshark%20and%20tcp%20dump%20image/2.png)


2. Inspect the network traffic of a network interface with tcpdump.

* Use `sudo tcpdump -i eth0 -v -c5` to filter live network packet data:
  
![chrome_xk2afcYBtV](https://github.com/Fulgeo/Google-Cybersecurity-Professional-Certificate/blob/main/Image/wireshark%20and%20tcp%20dump%20image/3.png)

> `-i eth0`: Capture data specifically drom the `eth0` interface.

> `-v`: Display detailed packet data.

> `-c5`: Capture 5 packets of data.

3. Capture network traffic:

* Capture packet data into a file named called `capture.pcap`:  `sudo tcpdump -i eth0 -nn -c9 port 80 -w capture.pcap &`.

> `-i eth0`: Capture data from the eth0 interface.

> `-nn`: Do not attempt to resolve IP addresses or ports to names.This is best practice from a security perspective, as the lookup data may not be valid. It also prevents malicious actors from being alerted to an investigation.

> `-c9`: Capture 9 packets of data and then exit.

> `port 80`: Filter only port 80 traffic. This is the default HTTP port.

> `-w capture.pcap`: Save the captured data to the named file.

> `&`: This is an instruction to the Bash shell to run the command in the background.

![chrome_czTEkhJt5O](https://github.com/Fulgeo/Google-Cybersecurity-Professional-Certificate/blob/main/Image/wireshark%20and%20tcp%20dump%20image/4.png)

* Use `curl` to generate some HTTP (port 80) traffic: `curl opensource.google.com`.
> Open a website and generate some HTTP (TCP Port 80) traffic that can be captured.   


![chrome_hxKylypKNY](https://github.com/Fulgeo/Google-Cybersecurity-Professional-Certificate/blob/main/Image/wireshark%20and%20tcp%20dump%20image/5.png)

* Verify the packet data has been captured: `ls -l capture.pcap`.

![chrome_HhfPeeYOiq](https://github.com/Fulgeo/Google-Cybersecurity-Professional-Certificate/blob/main/Image/wireshark%20and%20tcp%20dump%20image/6.png)

4. Filter the captured packet data.
* Filter the packet header data from the `capture.pcap` capture file: `sudo tcpdump -nn -r capture.pcap -v`.

![chrome_RUJXqYZJYp](https://github.com/Fulgeo/Google-Cybersecurity-Professional-Certificate/blob/main/Image/wireshark%20and%20tcp%20dump%20image/7.png)


![chrome_bzcD3CgViN](https://github.com/Fulgeo/Google-Cybersecurity-Professional-Certificate/blob/main/Image/wireshark%20and%20tcp%20dump%20image/8.png)

> `-nn`: Disable port and protocol name lookup.

> `-r`: Read capture data from the named file.

> `-v`: Display detailed packet data. 

* Filter the extended packet data from the `capture.pcap` capture file: `sudo tcpdump -nn -r capture.pcap -X`.

![chrome_30Kqm2ODsu](https://github.com/Fulgeo/Google-Cybersecurity-Professional-Certificate/blob/main/Image/wireshark%20and%20tcp%20dump%20image/9.png)

![chrome_fPM4JsnaBf](https://github.com/Fulgeo/Google-Cybersecurity-Professional-Certificate/blob/main/Image/wireshark%20and%20tcp%20dump%20image/10.png)


![chrome_XCBa8KnbDi](https://github.com/Fulgeo/Google-Cybersecurity-Professional-Certificate/blob/main/Image/wireshark%20and%20tcp%20dump%20image/11.png)

> `-nn`: Disable port and protocol name lookup.

> `-r`: Read capure data from the named file.

> `-X`: Display the hexadecimal and ASCII output format packet data. Security analysts can analyze hexadecimal and ASCII output to detect patterns or anomalies during malware analysis or forensic analysis.

> Note: Hexadecimal, also known as hex or base 16, uses 16 symbols to represent values, including the digits 0-9 and letters A, B, C, D, E, and F. American Standard Code for Information Interchange (ASCII) is a character encoding standard that uses a set of characters to represent text in digital form.
