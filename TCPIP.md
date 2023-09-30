
### What is a networking model?
- A comprehensive set of documents that describe how a computer network should work.
- Similar to a set of blueprints for a house.
### How did TCP/IP get developed?
- In 1970s and 1980s, there was no established networking protocol.
- Leads to vendors having their own networking protocols that only work for their own systems.
- In the late 1970s, the International Organization or Standardization (ISO) began work on a standardized model known as the Open Systems Interconnection (OSI) model. 
- At the same time, universities around the world further developed protocols surrounding work from the US Department of Defense (DOD) to create an open, vendor neutral, public networking model. 
- At the end of 1990s, TCP/IP became a common choice among companies and OSI fell away.
### What is the TCP/IP networking model? 
- Defines a large collection of protocols that allows computers to communicate.
- Uses Request For Comments (RFC) to define a protocol.
- Uses layers that includes protocols and standards to define a category of functions. 
#### TCP/IP Model Layers
- Application | HTTP, POP3, SMTP
- Transport | TCP, UDP
- Network | IP, ICMP
- Link | Ethernet, 802.11 (WiFi)
### What is the application layer?
- Provides services to the application on the computer.
- HTTP defines how web browsers can pull the contents of a webpage from a web browser.
- There are many other protocols that the application layer provides.
#### How does HTTP work? 
1. A message with the HTTP header is sent to the server. This header includes a request to 'get' a file.
2. A response is sent from the server to the client. The http header includes a return code of 200, which means OK. The data includes the requested file
3. This time, data without the http header is sent as part of the response. Usually http transfer data by sending multiple messages. 

### What is the transport layer? 
1. Most commonly used protocols are Transmission Control Protocol (TCP) and User Datagram Protocol (UDP)
2. #todo link to the TCP/UDP chapter once done

### What are same layer and adjacent layer interactions?
| Concepts | Description |
|-|-|
| Same-layer interaction on different computers | Two computers communicate with the same layer on another computer. The protocol defines a header that communicates what the computer wants to do. |
| Adjacent-layer interaction on same computer | The lower level layer provides services to the layer above. The software/hardware that implements the higher level requests that the lower level need to perform the function. |

### What is the network layer?
1. Main protocol is the internet protocol (IP).
2. Main features of IP are addressing and routing. #todo link to WAN IP and routing
