# Lab 06 – Exploring Networking with Cisco Packet Tracer

**Name:** Jason Gillette <br>
**Course/Section:** IS-6113 <br>
**Date:** April 13th, 2025

---

## Introduction

In this lab, we used Cisco Packet Tracer to set up and manage a simulated small office network. Through hands-on activities, we explored device connections, structured cabling, and network simulation for a small office set up.

---

## Module 1: Set Up Your Small Office Network

### 1.0 Introduction

- **1.0.1 Welcome to Exploring Networking with Cisco Packet Tracer:**  
  This section introduced the course and its purpose, highlighting Cisco Packet Tracer as a tool for learning basic networking concepts. Learners are encouraged to explore how devices connect by building and managing a small office network. The section emphasizes accessibility, requiring only a computer and internet connection to begin.

- **1.0.2 First Time in the Course:**  
  This section covered the intended audience and goals for the course, emphasizing that it builds on skills learned in the Getting Started with Cisco Packet Tracer course. Learners will expand their knowledge by configuring and managing a small office network while gaining experience with IoT and cybersecurity concepts. It also highlighted available support resources, including FAQs and Cisco’s virtual assistant, Morgan.

- **1.0.3 Why Should I Take this Course?:**  
  This section explained the purpose and structure of the course, emphasizing hands-on learning in a small office network simulation. It introduced the two modules: the first focuses on setting up devices using wireless technologies, and the second on managing and monitoring the network. The course combines instructional videos with guided Packet Tracer activities to reinforce learning.

### 1.1 Connect Devices using Wireless Technologies

- **1.1.1 Video - Topology Overview:**  
  This section covered the topology views available in Cisco Packet Tracer and how users can navigate between physical and logical locations. It introduced four main areas—home, office, library, and ISP—and explained how equipment is displayed and connected in each. The video also highlighted the use of structured cabling and wiring closets in the office environment, offering a realistic simulation of network infrastructure.

- **1.1.2 Structured Cabling:**  
  This section introduced structured cabling as a method for organizing network infrastructure in a clean and efficient manner. It explained how Packet Tracer's Physical mode supports realistic cable management using wall mounts, color coding, and bend points. These tools help simulate professional network setups and maintain a tidy workspace.

- **1.1.3 Video - Structured Cabling and Devices in a Rack:**  
  This section covered how to use Cisco Packet Tracer’s structured cabling features to simulate realistic network wiring. It demonstrated how to install and connect patch panels and wall mounts using copper cables, manage cable colors, and organize cables with bend points for cleaner topology layouts. The video emphasized best practices in physical cabling and cable management within a simulated office environment.

- **1.1.4 Packet Tracer - Structured Cabling in the Workspace:**  
  This activity focused on creating realistic structured cabling in Cisco Packet Tracer by simulating the installation and connection of network infrastructure. Learners installed patch panels and wall mounts, connected switch ports to patch panel jacks, and routed cables from wall mounts to end-user devices like PCs and printers. The activity emphasized best practices such as cable organization, color coding, and the use of bend points to simulate clean, real-world cable management.

  [capture06](./assets/IS3413_lab06_capture06.PNG)

- **1.1.5 Connect Devices Using Wired and Wireless Technologies:**  
  This section covered the importance of understanding both wired and wireless technologies in modern networking. It emphasized the configuration of Wi-Fi networks and host devices, while also introducing Bluetooth and cellular data as additional wireless communication methods.

- **1.1.6 Packet Tracer - Connect Devices Using Wireless Technologies:**  
 This activity explored how to connect devices using various wireless technologies within Cisco Packet Tracer’s Physical Mode.** Learners connected a laptop to a wireless LAN using a wireless module, paired a tablet with a Bluetooth speaker to play music, and tethered a laptop to a smartphone via Bluetooth to access a website through the cellular network. The exercise emphasized practical use of wireless standards like Wi-Fi and Bluetooth for real-world networking scenarios.

 [capture07](./assets/IS3413_lab06_capture07.PNG)

- **1.1.7 Video - Explore Device Configuration Using CLI:**  
  This section introduced how to configure networking devices in Cisco Packet Tracer using both the graphical Config tab and the Command Line Interface (CLI). It explained the different operational modes in Cisco IOS, such as user exec, privileged exec, and global configuration mode, and demonstrated how to change basic settings like device names. The video emphasized the importance of saving configurations to ensure persistence after device restarts.

- **1.1.8 Packet Tracer - Explore Device Configuration Using CLI:**  
  This activity guided learners through configuring a network switch using the command-line interface via a console connection in Packet Tracer. Students accessed the switch with terminal emulation, entered privileged and global configuration modes, and applied settings such as hostname and console password. The exercise concluded with saving the configuration to startup memory, reinforcing the process of making persistent changes on Cisco devices.

  [capture08](./assets/IS3413_lab06_capture08.PNG)

---

## Module 2: Manage and Monitor Your Branch Office Network

### 2.0 Structured Wiring / PT Simulation

- **2.0.1 Packet Tracer Simulation Mode:**  
  This section explained Packet Tracer’s Simulation mode, which allows users to observe and analyze network behavior in a controlled, step-by-step manner. Unlike Realtime mode, Simulation mode lets users pause or slow time to view individual packets, making it ideal for troubleshooting and studying protocols. It also provides detailed views of PDU contents, including OSI layer headers, to verify connectivity, services, and security configurations.

- **2.0.2 Video - Network Simulation Mode:**  
  This section introduced Packet Tracer’s Simulation mode, highlighting its ability to slow, pause, and inspect network traffic for deeper analysis. The instructor explained how to use features like the event list, protocol filters, and PDU views to analyze connectivity, security, and protocol behavior. The video also demonstrated how to use simple and complex PDUs to test and monitor network communication step by step.

- **2.0.3 Packet Tracer - Examine Packets in the Small Office:**  
  This activity focused on using Packet Tracer’s Simulation Mode to analyze network behavior by creating and inspecting both simple and complex PDUs. Learners created a basic ping between two devices to observe ICMP packet flow, examined protocol details using OSI model and header views, and configured a complex PDU to send periodic pings with custom parameters. The exercise reinforced how Simulation Mode can be used to test connectivity, troubleshoot issues, and explore how network protocols operate in real-time.

  [capture09](./assets/IS3413_lab06_capture09.PNG)

- **2.0.4 Video - Create, Arrange, Uncluster, Delete, and Connect Clusters:**  
  This section demonstrated how to create, manage, and interact with device clusters in Cisco Packet Tracer. It explained how to group devices into a cluster, rename and navigate within it, and connect clustered devices to external ones using manual cabling. The video also covered how to uncluster or permanently delete clusters, highlighting the flexibility and organization benefits of clustering in network design.

- **2.0.5 Edit and Annotate a Topology:**  
  This section very briefly emphasized the importance of being able to edit and annotate network topologies in Packet Tracer as part of the iterative design process. It highlighted that simulated networks often need updates or improvements and that proper documentation is essential for clarity and maintenance.

- **2.0.6 Video - Edit and Annotate a Topology:**  
  This section demonstrated how to enhance and document network diagrams in Cisco Packet Tracer using editing and annotation tools. The instructor showed how to add and modify notes, highlight sections with shapes and colors, apply background images, and use the network description box to provide context. These tools help make topologies clearer, more organized, and visually representative of real-world layouts.

- **2.0.7 Packet Tracer - Edit Topologies:**  
  This activity guided learners through editing a network topology in Packet Tracer by adding hardware, managing cabling, working with clusters, and documenting changes. Participants installed a new switch and connected it to a patch panel and an existing switch, added a PC to the network to verify connectivity, unclustered and re-clustered devices, and created a new “Second Home” cluster with a PC, home gateway, and cable modem. The activity emphasized structured topology design, logical organization using clusters, and documentation using annotation tools.

  [capture10](./assets/IS3413_lab06_capture10.PNG)

### 2.1 Network Controller

- **2.1.1 The Network Controller:**  
  This section introduced the Network Controller in Packet Tracer as a tool for centralized network management. It explained that the controller provides a graphical user interface (GUI) for monitoring and configuring multiple devices from one location. Access is achieved by connecting to the controller’s IP address through a web browser.

- **2.1.2 Video - The Network Controller:**  
  This section demonstrated how to connect and interact with the Network Controller in Cisco Packet Tracer to centrally manage network devices. The video showed how to physically connect the controller, verify connectivity via ping, and access its web-based dashboard. Key features explored included device discovery, provisioning, assurance for monitoring network health, policy settings, and an API interface for automation and integration.

- **2.1.3 Packet Tracer - Monitor Your Network Using a Network Controller:**  
  This activity walked learners through implementing and using a Network Controller in Cisco Packet Tracer to monitor a network through its graphical interface. In Part 1, students connect the controller to a switch, verified network connectivity with ping tests, and accessed the controller via a web browser. In Part 2, we explored the controller’s dashboard, documented discovered devices using notes, and observed how the controller dynamically detected newly connected wireless devices through its discovery tools.

  [capture11](./assets/IS3413_lab06_capture11.PNG)

- **2.1.4 Video - Monitor Network Changes Using a Network Controller:**  
  This section demonstrated how to monitor network changes using the Network Controller in Cisco Packet Tracer. The video showed how to configure user credentials, initiate a device discovery process, and view details about discovered devices. It also covered how newly added devices—like switches—can be automatically identified and managed through the controller's centralized dashboard.

- **2.1.5 Packet Tracer - Manage and Configure Your Network Using a Controller:**  
  This activity guided learners through deploying and using a Network Controller in Cisco Packet Tracer to manage and monitor devices on an office network. In Part 1, the controller was physically connected, configured with IP settings, and connectivity was verified. Part 2 focused on setting up user credentials, initiating a discovery process to identify existing devices, and interpreting discovery results. In Part 3, a new switch was added to the network, configured via CLI, and then detected by the controller through a refreshed discovery process.

  [capture12](./assets/IS3413_lab06_capture12.PNG)

### 2.2 Course Summary

- **2.2.1 Packet Tracer Tutored Activity - Troubleshoot a Wireless Connection:**  
  This section introduced a guided Packet Tracer Tutored Activity focused on troubleshooting a wireless connection. I can use hints, allowing them to build and practice diagnostic skills at their own pace. The activity emphasizes identifying and resolving issues in wireless connectivity.

  [capture13](./assets/IS3413_lab06_capture13.PNG)

- **2.2.2 Summary of the Course:**  
  This section summarized the key concepts covered across both modules of the course.Module 1 focused on setting up a small office network using structured cabling and wireless technologies, as well as exploring device configuration through tabs like Physical, Config, CLI, and Desktop. Module 2 emphasized monitoring and managing the network using Simulation mode, editing topologies, analyzing PDUs, and using a Network Controller for centralized management through a browser-based GUI. The course reinforced practical skills in network design, troubleshooting, and device configuration in a simulated environment.

---

## Final Exam

- **Packet Tracer Course Final Exam Screenshot:**  
  
  [capture14](./assets/IS3413_lab06_capture14.PNG)

---

## Conclusion

Completing this lab helped me develop practical skills in configuring, managing, and monitoring a small office network using Cisco Packet Tracer. I became more comfortable using the CLI, Simulation mode, and the Network Controller interface to troubleshoot and visualize network operations. One challenge I faced was correctly setting up wireless connections and structured cabling, which I resolved by carefully reviewing device settings and verifying connections. The experience reinforced the importance of organized network design and centralized management, which I plan to apply in future networking tasks to ensure efficient troubleshooting and scalable configurations.

---

## References

[1] Cisco, “Exploring Networking with Cisco Packet Tracer,” Skills for All, Accessed: *April 13th, 2025*. [Online]. Available: [https://skillsforall.com/course/exploring-networking-cisco-packet-tracer?courseLang=en-US](https://skillsforall.com/course/exploring-networking-cisco-packet-tracer?courseLang=en-US).

[2] ChatGPT [GPT-4 language model], response to “Generate a markdown lab template for Lab-06_Exploring-Networking.pdf,” OpenAI, April 2025. Accessed: *April 13th, 2025*.

---

## Collaboration

No collaboration occurred with this assignment.

---
