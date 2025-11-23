## OSI Model (Open System InterConnection)

- 7 layer

1. UDP / TCP: Transport Layer

- connection establishment

## TCP Handshake and TLS Handshake

TCP handshake is called 3 eay handshake.

1. client -> server : SYNC (hello i want to request google.com)
2. server -> client : SYNC-ACK (i hear you here is my ACK.)
3. client -> server : ACK (got it , new connection open)

- TLS Handshake : TLS works above TCP / UDP - it provides security (encryption)

  - 3 things done by TLS
    - Encryption (creditability) : hide the actual data
    - Authentication : only the valid server can read the data . TLS certificate exchange is done here
    - Integrity : verifies the data is not altered, tempered, forged during transmission

- TLS Handshake

1. Client Hello :
   - client send the list of tls versions
   - list of ciphers suits
   - random strings
2. Server Hello :
   - send final tls version
   - list of cipher suits
   - certificate (pk ) and random string
3. Authentication and session key generate
   - client verifies the certificate with CA(Certificate Authority)
   - when verifies then key are exchange between them and generate session key
4. Finished & secure connection :
   - Both client and server sends finished message with encrypted session key
   - secure connection is established
   - all data is encrypted through first symmetric session key

## How Internet Works ?

1. client want to visit [google.com](https://goggle.com)
2. request goes to **DNS Server** which is resolver
3. resolver send it to **Root Server** : 13 Total Root Server are there in world and root server directs the request to correct TLD (.com)
4. Root Server send it to (Top Level Domain )
   to get ip address of TLD (.com, .org, .in, .np, .io,..) and send back to resolver
5. resolver send request to TLD server(.com) to get ANS (Authoritative Name Server) address
6. resolver send request to that ANS to get actual IP address and send to browser and Caching
7. then browser direct the request to that IP Address to load webpage

## Difference between Session , Cookies and Token

- session based authentication
- token based authentication
