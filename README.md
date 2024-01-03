# Network Traffic Analyzer

This Python script is a simple network traffic analyzer designed to run with root privileges on Kali Linux. It captures and decodes Ethernet frames, IPv4 packets, ICMP, TCP segments, and UDP segments, providing details such as source and destination addresses, protocol information, and additional packet-specific information.

## Prerequisites

- Kali Linux
- Python 3.x

## Usage

1. Ensure you have root privileges: `sudo python3 network_analyzer.py`
2. Capture and analyze network traffic.

## Features

- **Ethernet Frame Analysis:** Decodes destination MAC address, source MAC address, and Ethernet protocol.
- **IPv4 Packet Analysis:** Extracts version, header length, Time-to-Live (TTL), protocol, source, and target addresses.
- **ICMP Packet Analysis:** Retrieves ICMP type, code, checksum, and data.
- **TCP Segment Analysis:** Extracts source port, destination port, sequence and acknowledgment numbers, flags (URG, ACK, PSH, RST, SYN, FIN), and data.
- **UDP Segment Analysis:** Provides source port, destination port, length, and data for UDP segments.
- **Other Protocols:** Displays raw data for non-IPv4 packets.

## Code Structure

- **`main()` Function:** The main function sets up a raw socket to capture network packets and processes them based on their protocols.
- **Packet Parsing Functions:** Several functions are defined to parse different types of packets, such as Ethernet frames, IPv4 packets, ICMP, TCP, and UDP segments.
- **Formatting Functions:** Functions are provided to format and print the decoded information in a structured manner.

## Disclaimer

This tool is intended for educational and informational purposes only. Use it responsibly and ensure compliance with applicable laws and regulations. The author is not responsible for any misuse or illegal activities.

## Contributing

Feel free to contribute to the project by opening issues or submitting pull requests.
