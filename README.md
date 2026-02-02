*This project has been created as part of the 42 curriculum by hoskim*

# Description
This project is a practical introduction to the fundamentals of computer **networking**.
The goal is to configure small-scale networks through a dedicated training interface, ensuring proper communication between various devices.

Throughout the 10 levels of exercises, I have learned to:
- **IP Addressing**: Assign and manage TCP/IP addresses effectively.
- **Subnetting**: Understand how subnet masks define network boundaries and host range.
- **Routing & Switching**: Configure routers and switches to direct traffic between different segments.
- **Gateways**: Implement default gateways to allow communication with external networks.

The project focuses on solving non-functioning network diagrams by identifying configuration errors,
such as invalid IP ranges, missing routes, or incorrect masks, and correcting them to achieve specific connectivity goals.

# Instructions
This section explains how to run the training interface, export your configurations, and the requirements for a successful submission.

1. **Running the Training Interface**
The project provides a web-based training interface. To run it locally:
    - **Prerequisites**: Use **Google Chrome** or a **Chromium-based browser**. Firefox is known to have compatibility issues with this tool.
    - **Extraction**: Unzip the provided project file using the following command:
        ```bash
        tar -xvzf net_practice.1.8.tgz
        ```
  - **Execution**: Navigate to the extracted folder and open the `index.html` file in your browser.

2. **How to practice**
    1. **Login**: Enter your 42 intra login in the designated field to use your personal configuration.
    2. **Solving Levels**: Analyze the network diagrams and modify the unshaded fields (IP addresses, Subnet masks, etc.) to meet the goals displayed at the top.
    3. **Verification**: Click the **[Check again[** button to verify if your network functions correctly.
    4. **Log Analysis**: If the configuration fails, check the logs at the bottom of the page to identify issues like invalid IPs or missing gateways.
  
3. **Exporting and Submission**
    - **Exporting**: Once a level is successfully completed, click the **[Get my config]** button. This will download a configuration file for that specific level.
    - **Requirements**:
      - You must complete all **10 levels**.
      - Each level must have its own export file.
      - All 10 files must be placed at the **root of your Git repository**.
    - Final Structure:
        ```Plaintext
        .
        ├── level_1
        ├── level_2
        ...
        ├── level_10
        └── README.md
        ```
    
# Resources
This section outlines the core networking concepts studied during the project, external references, and the role of AI in the development process.

1. **Networking Concepts Studied**
To solve the 10 levels of NetPractice, a deep understanding of the following concepts was required:
    - **TCP/IP Addressing**: The standard suite of protocols for connecting devices on the internet.
    - **Subnet Mask & CIDR**: Used to divide an IP address into network and host portions.
        - *Example*: In `162.168.0.1/25`, the mask defines the range of available hosts.
    - **Network & Broadcast Address*:
        - **Network Address**: The first address in a block (e.g., `162.168.0.0`), representing the network itself.
        - **Broadcast Address**: The last address in a block (e.g., `162.168.0.127`), used to send data to all hosts in the subnet.
    - **Default Gateway**: The ""exit point" for a device to communicate with nodes outside its local subnet, typically a router interface.
    - **Loopback Address**: The address `$127.0.0.1$` (or any `$127.x.x.x$`) used to test the local network interface (TCP/IP stack).
    - **Routers and Switches**:
        - **Switches**: Connect devices within the same network (Layer 2).
        - **Routers**: Connect different networks and route traffic between them (Layer 3).
    - **OSI Model: The Postal Service Analogy**

      To understand the complex process of network communication, it is helpful to visualize it as a 7-step delivery system. While I studied all seven layers, my focus in NetPractice was on the "Addressing and Routing" steps (Layers 2 & 3).

        - **Layer 7 (Application): Writing the Letter** The user creates data (like writing a message).
        - **Layer 6 (Presentation): Translation & Packaging** Ensuring the data is in a format the receiver can read (like translating the letter or encrypting it).
        - **Layer 5 (Session): Starting the Conversation** Establishing a connection between the sender and receiver.
        - **Layer 4 (Transport): Reliability Check** Breaking the letter into smaller pieces if it's too big and making sure every piece arrives safely (TCP/UDP).
        - **Layer 3 (Network): The Address on the Envelope [Focus of NetPractice]** Writing the **IP Address** on the package. **Routers** use this to decide which "city" (network) the package should go to.
        - **Layer 2 (Data Link): The Local Delivery Hub [Focus of NetPractice]** Using **Switches** and MAC addresses to deliver the package from the local post office to the specific house in the neighborhood.
        - **Layer 1 (Physical): The Delivery Truck** The actual wires, fiber optics, and electrical signals that carry the data.
    
2. **Reference Materials**
    - [Wikipedia - IP Subnetwork](https://en.wikipedia.org/wiki/Subnet)
    - [Cisco - IP Addressing and Subnetting for New Users](https://www.cisco.com/c/en/us/support/docs/ip/routing-information-protocol-rip/13788-3.html)
    - [IP Subnet Calculator](https://www.calculator.net/ip-subnet-calculator.html) (Used to verify manual calculations during practice)

3. **Use of AI**
AI was utilized in this project for the following tasks:
    - **Concept Clarification**: Explaining the mathematical relationship between CIDR notation and subnet masks.
    - **Documentation**: Assisting in the translation and structural organization of this `README.md` to ensure it meets the 42 curriculum requirements.
    - **Troubleshooting**: Generating logical edge-case scenarios to better understand why a specific gateway configuration might fail in complex levels (e.g., Level 10).
