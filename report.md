# Wireshark Packet Capture Report

## Summary
A one-minute live packet capture was performed on the active network interface while browsing websites and pinging servers. The capture contains multiple network protocols including DNS, TCP, HTTP, HTTPS/TLS, and ICMP.

---

## Identified Protocols

| Protocol     | Purpose | Example Packet Details |
|--------------|---------|------------------------|
| **DNS**      | Resolves domain names to IP addresses | Query: `google.com` → Response: `142.250.183.14` |
| **TCP**      | Reliable transport of data between systems | SYN packet from local IP to `142.250.x.x` (Google) |
| **HTTP**     | Transfers web page content in plaintext | HTTP GET request to `example.com` |
| **HTTPS/TLS**| Secure, encrypted web communication | TLS handshake with `142.250.183.x` |
| **ICMP**     | Network diagnostics (ping) | Echo request and reply to `8.8.8.8` |

---

## Key Observations
1. DNS queries were sent before HTTP/HTTPS requests, confirming hostname resolution before connection.
2. TCP three-way handshakes were clearly visible before data transfer.
3. ICMP traffic confirmed successful connectivity testing to external hosts.
4. HTTPS traffic appeared as encrypted TLS payloads without visible content.
5. HTTP traffic displayed human-readable headers and GET requests.

---

## Conclusion
The captured traffic illustrates a complete network communication flow:
- Domain resolution via DNS
- Connection establishment with TCP
- Data transfer using HTTP/HTTPS
- Diagnostic checks using ICMP
