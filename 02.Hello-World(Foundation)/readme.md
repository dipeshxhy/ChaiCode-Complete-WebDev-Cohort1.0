# Foundation

```js
// jargons
// hiteshchaoudhary.com
// stateless : state maintain , checkpoints, bookmark , saved , level , etc not in stateless
// session : http is stateless so session need, time given like doctor appointment . it store data
// cookie: store data in cookie format {name  :'hello'}
// come from both side server and client
// http Headers : -client info
/*
                - Browser Info
                - Date & Time
                - Cooke to store
                Note: to give popup about app , ads 
                */
/*
## Reject - Response Model
- Type of Request [Get, Post, Delete, Patch] etc
- Response Code [200, 201, 204, ..., 400, 401, 405, 500,.. ]
  - what action to perform ? Get , Post
  - where to perform : https:api.hitesh.ai/auth
  - was it done ? 200, 201 ok, Not Found , Bad Request

## HTTP/2 (new set of tool )
version 1.1 , image send
75% http2 
enhancements: image , style all files send at once
multiple files : multiplexing
http 1.1 is used as fallback 
  - http means http 2
  - uses compression
  - uses multiplexing (Many files send at same time)
  - uses encryption (https)
    -In Aws , we don't use https for internal communication
    abc ----> kyc (encryption)
    compute cost 
plain text format : clear text format 

    TLS : Transport Layer Security
    TLS Certificate exchange

### Some Jargons
   - User Agent (Browser)
   - TCP (Transmission Control Protocol)
   - FTP (File Transfer Protocol)
          eg: pdf , mp3, mp4, csv type date (excel)
   - IP (Internet Protocol)
        - unique name for each machine / computer (IP Address)
   - URL (Uniform Resource Locator)
          (Link, api, end point)
   - DNS (Domain Name System Server)
         - points URL to IP
          (Red Hat , zOHO keep sever in house it ust machine)
          - contacts / phone book of website / Internet
    - Header (pass additional information)
    - Payload (actual data - email, name, phone, id,..)
    - cache (store the data  )
            - temp storage 
              like showroom type

#### Browser ---------> Client
 - setup TCP connection / UDP
 - exchange  TLS Certificate (https)
 - send verb + URL + Data + more
 - Gets response back [type endPoint  statusCode ]
                      [Get /uses/profile 200]
                      data (img/ csv/ text)
  - TCP Connection is closed (stateless)
  (webrtc , graphql, api., )
  

- total port on computer : 65 , 535



  
*/
```

## HTTP

- Hypertext Transfer Protocol
  - Protocol : set of rules used to transfer HText
  - HText : Hyper Link (to link web docs)

## Human Readable

### Some Terminology

- overhead : excess or indirect consumption of resources(time, memory, bandwidth, processing power)
  cost of doing business
  examples :

1.  Slower Processing Power / Time Overhead
2.  Increased Bandwidth / Communication Overhead
3.  Higher Memory Uses / Space Overhead

Basically its extra consumption of resources beside actual data

- In networking there is protocol overhead
  - that must be transmitted with payload(actual data)
- TCP / UDP

  - TCP (High Overhead): 20 bytes dues to 3way handshake and error check mechanism
    - connection-oriented : connection need to establish before send data (SYNC, SYNC-ACK, ACK)
    - reliable : it guarantee the delivery of data are correct and no data lost
    - Speed: Slower (dues to connection establish and error checking)
    - Header Size (overhead): high (20 Bytes)
    - common uses : web browsing, file transfer, email sending

  -UDP (User Datagram Protocol):

  - connection-less : no need to establish connection before sending data
  - Not Reliable : It does not guarantee the delivery of packets in correct order , packets may be lost
  - Speed : Fast (lower overhead)
  - Header Size : small header (8 bytes)
  - common uses : live streaming , video calling, online games, DNS lookup

- BandWidth : it is maximum volume of data that can be transmit through communication or ntwork channel from one point to another in specified time

  - it is measured of capacity not speed
  - it is generally measured in bps(bits per second), Mbps, Gbps

  **if you have 100Mbps connection, it means your connection can handles maximum 100 Million bits of data every second**

- latency : the delay before a transfer of data
- speed : the overall rate at which data is transmits
  which is combination of higher bandwidth and low latency

- PDU (Protocol Data Unit):

  - it is used as unit in every layer of OSI Model
  - physical : bits
  - Data-link : frames (address : MAC)
  - Network : packet (address: IP)
  - Transport: segment (address : port)
  - 3 layers in one
    -session |
    -presentation | Data
    -application |

- OSI Model :
  - User request then data transfer downward which called encapsulation like
    Application (Data)-> Transport(TCP/UDP) -> Network(IP ) -> Data-link(MAC) -> Physical(cable,wifi)
    in each layer own headers are added and convert into their PDU (UNIT)
  - At Destination Computer : Decapsulate
    Physical(electric, light pulse) -> Data-Link -> as to Application
  - actual data are reconstructed from the headers and Unit send
  - so the user can read it

### Resources

- [TCP / UDP](https://encrypted-tbn1.gstatic.com/licensed-image?q=tbn:ANd9GcQMWEF2Lb26V0PhmncEoPnYfAAsf10CWq5HWpbJgPdPTLEiPZrlXItxp1rE0lUfSE5tL5zFU-XqL1167QIyqYAihx7ZeQv7y2rlEAOgfLa3gK2ZdiM)
