# Collection of resources for communication secure Federated Learning
Federated Learning (FL) is a distributed machine learning approach that exchanges machine learning parameters instead of raw data. FL data is stored locally on participating devices, then later transferred to the central FL model for optimization. When machine learning parameters are exchanged online throughout a network, there is a risk of outsiders eavesdropping on transferred information. This collection of resources is centered around popular terminology for deploying communication secure FL.
## Data encryption
* Encrypted data is raw data converted into a cipher or code that is unreadable without a decoding key. The strength of the encryption algorithm is useful for protecting data from unauthorized access. AES or Advanced Encryption Standard is widely known for being a secure method for encrypting data. AES-256 translates to a 256 bit key size for encryption and decryption. <br>
Generally there are two types of data forms that are encrypted:
  <ol>
  <li>Data at-flight refers to data being transported between destinations. When data moves between devices, across a network, or over the internet there is a risk of interception. Security measures such as encryption can better protect data at-flight from sniffing attacks.</li>
  <li>Data at rest refers to data being stored, not undergoing processing or movement throughout the network. Data at rest is less vulnerable than data at-flight or data in use. Strict access controls can further protect data at rest.</li>
  </ol>
* Unencrypted data is raw data that is represented as ‘clear text’, which is easily understandable to humans. Unencrypted data is stored without cryptographic protection, making it vulnerable to various networking attacks such as sniffing attacks or outsider attacks. <br> Unencrypted data can transform into encrypted data using a cryptographic function similar to a checksum.
## Networking
Network security refers to network policies, practices and configurations to protect confidentiality and accessibility of computer networks.
* Internet Protocol (IP) is a protocol that governs the format of data being sent over the internet. IP ensures that data being sent over the internet routes to the correct destination. Every device connected to the internet is assigned an IP address.
* Transmission Control Protocol (TCP) is one of the primary protocols for IP. Data being transmitted over the internet is divided into smaller packets, while TCP verifies the endpoints through a handshake process. TCP mechanisms include monitoring data transmission, verifying the integrity of data through checksums, and controlling the rate of data flow to avoid network congestion. 
* End-to-end encryption (E2EE) refers to a secure communication scheme where data is encrypted on the sender side and can only be decrypted on the receiving side with a secret key. While data is at-flight third-parties cannot reveal contents of the data without the senders secret key. End-to-end encryption is popular within messaging apps such as WhatsApp and even withholds companies providing the service from accessing the data.
* Network security often operates on two sides, the Client side and the Server side:
  <ol>
    <li>Client side - On the client side, a client certificate is issued digitally by a Certificate Authority (CA) for users to prove their identity to a server. The CA provides a digital signature for the client that ensures the certificate is genuine and trustworthy. The server may request a clients certificate for extra layers of network security. Client certificates can be in multiple forms such as: VPNs, bank card identifications, or even RFID cards to enter buildings.</li>
    <li>Server side - A server certificate is similar to a client certificate but is used to validate a servers identity. When a client connects to a secure server, the server presents its digital certificate to the client. When the client verifies the server certificate based on the CA digital signature, a SSL/TLS handshake takes place. Once the server identity is authenticated, a secure connection is established. </li>
    <ul>
      <li>SSL (Secure Sockets Layer) certificates are modern server certifications that provide authentication. When installed on a web server, the http protocol becomes https, allowing a secure connection from the clients browser to the web server. SSL was first developed in the mid-1990s and is still widely used in the industry for historical reasons.</li>
      <li>TLS (Transport Layer Security) is the industry standard for communication protocols. SSL is referred to synonymously with TLS due so similarity, although TLS is considered the successor to the SSL protocol due to being newer and more secure. Both TLS and SSL are similar in purpose and usage of the https protocol. Advantages of TLS include: handshakes requiring fewer steps to establish a secure connection, modern advanced encryption algorithms, and alert messages being encrypted with additional functionality. </li>
    </ul>
  </ol>

## Data compliance
Data compliance refers to standards that comply with lawmaker regulations, corporate policy, and institutional guidelines. Data compliance encourages best practices for managing and protecting data. A list of common regulations applicable to data-driven technologies is below:
* Payment Card Industry’s Data Security Standard (PCI-DSS)
* European Union’s General Data Protection Regulation (GDPR)
* Healthcare Insurance Portability and Accountability Act (HIPAA) 
* California Privacy Rights Act (CPRA)
