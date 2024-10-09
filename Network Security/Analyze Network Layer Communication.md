# Cybersecurity Incident Report: Analyze Network Layer Communication
> Network layer communication.

> Please visit this [link](https://www.coursera.org/learn/networks-and-network-security?specialization=google-cybersecurity) for further information.

## Scenario

You are a cybersecurity analyst working at a company that specializes in providing IT consultant services. Several customers contacted your company to report that they were not able to access the company website www.yummyrecipesforme.com, and saw the error “destination port unreachable” after waiting for the page to load. 

You are tasked with analyzing the situation and determining which network protocol was affected during this incident. To start, you visit the website and you also receive the error “destination port unreachable.” Next, you load your network analyzer tool, tcpdump, and load the webpage again. This time, you receive a lot of packets in your network analyzer. The analyzer shows that when you send UDP packets and receive an ICMP response returned to your host, the results contain an error message: “udp port 53 unreachable.” 

![Analyze Network](https://github.com/Fulgeo/Google-Cybersecurity-Professional-Certificate/blob/main/Image/analyze%20network.png?raw=true)

In the DNS and ICMP log, you find the following information:

1. In the first two lines of the log file, you see the initial outgoing request from your computer to the DNS server requesting the IP address of yummyrecipesforme.com. This request is sent in a UDP packet.

2. Next you find timestamps that indicate when the event happened. In the log, this is the first sequence of numbers displayed. For example: 13:24:32.192571. This displays the time 1:24 p.m., 32.192571 seconds.

3. The source and destination IP address is next. In the error log, this information is displayed as: 192.51.100.15.52444 > 203.0.113.2.domain. The IP address to the left of the greater than (>) symbol is the source address. In this example, the source is your computer’s IP address. The IP address to the right of the greater than (>) symbol is the destination IP address. In this case, it is the IP address for the DNS server: 203.0.113.2.domain.

4. The second and third lines of the log show the response to your initial ICMP request packet. In this case, the ICMP 203.0.113.2 line is the start of the error message indicating that the ICMP packet was undeliverable to the port of the DNS server.

5. Next are the protocol and port number, which displays which protocol was used to handle communications and which port it was delivered to. In the error log, this appears as: udp port 53 unreachable. This means that the UDP protocol was used to request a domain name resolution using the address of the DNS server over port 53. Port 53, which aligns to the .domain extension in 203.0.113.2.domain, is a well-known port for DNS service. The word “unreachable” in the message indicates the message did not go through to the DNS server. Your browser was not able to obtain the IP address for yummyrecipesforme.com, which it needs to access the website because no service was listening on the receiving DNS port as indicated by the ICMP error message “udp port 53 unreachable.”

The remaining lines in the log indicate that ICMP packets were sent two more times, but the same delivery error was received both times. 

Now that you have captured data packets using a network analyzer tool, it is your job to identify which network protocol and service were impacted by this incident. Then, you will need to write a follow-up report. 

## Provide a Summary of the Problem Found in the DNS and ICMP Traffic Log

- The browser used the **UDP protocol** to contact the DNS server to get the IP address for **yummyrecipesforme.com**.
- The **ICMP protocol** sent an error message indicating there were problems contacting the DNS server.
- **Log event details**:
  - The first two lines show the UDP message from the browser to the DNS server.
  - The third and fourth lines display the ICMP error message: **"udp port 53 unreachable."**
- **Port 53** is used for DNS traffic, meaning the issue is likely with the DNS server.
- There are **flags** in the UDP message, indicated by:
  - A **plus sign** after query ID **35084**, which shows something unusual.
  - The **"A?" symbol**, signaling issues with the DNS protocol operations.
- The **ICMP error** about port 53 strongly suggests that the DNS server is not responding.
- The flags in the outgoing UDP message and the failed domain name retrieval support this conclusion.


## Explain Your Analysis of the Data and Provide at Least One Cause of the Incident

The incident occurred at 1:24 p.m. when several customers reached out to our company reporting an issue with accessing our website, www.yummyrecipesforme.com, encountering the error message "destination port unreachable." In response, the IT team swiftly initiated an investigation by utilizing tcpdump to monitor network traffic and identify the root cause of the problem. The analysis team was actively engaged in detecting the error but was unable to ascertain specific details related to the affected port or the DNS server involved. Unfortunately, the precise cause of the incident remains elusive at this time. The IT department is diligently collaborating with security engineers to resolve the issue and restore normal website functionality.
