#CCNA
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
#todo link to the TCP/UDP chapter once done

### What are same layer and adjacent layer interactions?
| Concepts | Description |
|-|-|
| Same-layer interaction on different computers | Two computers communicate with the same layer on another computer. The protocol defines a header that communicates what the computer wants to do. |
| Adjacent-layer interaction on same computer | The lower level layer provides services to the layer above. The software/hardware that implements the higher level requests that the lower level need to perform the function. |

### What is the network layer?
1. Main protocol is the internet protocol (IP).
2. Main features of IP are addressing and routing. 
#todo link to WAN IP and routing
3. x.x.x.x is called dotted notation. 
4. Routers connect the network to forward IP packets to the correct destination.
### IP Routing basics
1. The client sends the packet to a nearby router.
2. The router checks its known IP table and routes the packet to another router.
3. That router checks its known IP table and sends the packet to its destination (A server)

## What is the link layer? 
1. Actually consist of 2 layers, physical and data-link. 
2. Physical layer defines the cabling and energy flow over the cables.
3. Data-link layer defines the rules and conventions when sending data over the cables. 
### Steps on how ethernet forwards an IP packet
1. Client encapsulates an IP packet between an Ethernet header and Ethernet trailer, creating an Ethernet frame.
2. Client physically transmits the bits of this Ethernet Frame, using electricity flowing over the ethernet cabling.
3. Router receives the electrical signal over a cable and re-creates the same bits by interpreting the meaning of the electrical signals.
4. Router de-encapsulates the IP packet from the Ethernet Frame by removing and discarding the Ethernet header and trailer.

## How does data encapsulation work?
1. Create and encapsulate the application data with any required application layer headers.
2. Encapsulate the data supplied by the application layer inside a transport layer header.
3. Encapsulate the data supplied by the transport layer inside network layer (IP) header
4. Encapsulate the data supplied by the network layer inside a data-link layer header and trailer
5. Transmit the bits.
## What are the names of TCP/IP messages?
| | | TCP | Data | - SEGMENT |
|-|-|-|-| -|
| | IP | Data | Data| - PACKET |
|LH | Data | Data | Data | - FRAME|

# TCP/IP vs OSI Model

OSI 
Application 7
Presentation  6
Session 5
Transport 4
Network 3
Data-Link 2
Physical 1

TCP/IP
Application 5 - 7
Transport 4
Network 3
Data-link 2
Physical 1

## What is a PDU?
- Protocol Data Unit
- OSI model uses them to refer to the bits that include the headers, trailers and data.
- OSI refers to them as Layer x PDU (LXPDU)