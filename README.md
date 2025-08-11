# wireshark-network-analysis
# Wireshark Network Traffic Analysis

## Objective
Capture live network packets and identify basic protocols and traffic types.

## Tools Used
- **Wireshark** — Free and open-source network packet analyzer
- Operating System: Windows

## Deliverables
1. **network_capture_task.pcapng** — Full packet capture from live traffic.
2. **report.md** — Summary of identified protocols and packet details.
3. `.pcapng` file for network traffic analysis.

## Steps Performed
1. Installed Wireshark.
2. Started capture on the active network interface.
3. Generated traffic by:
   - Visiting multiple websites in a browser.
   - Running the command:
     ```bash
     ping google.com
     ```
4. Stopped capture after ~1 minute.
5. Applied filters to view:
   - `dns` — Domain Name System queries/responses
   - `tcp` — Transport layer connections
   - `http` — Web requests/responses
6. Identified at least three different protocols.
7. Saved the capture in `.pcapng` format.
