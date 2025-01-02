# **Building a Comprehensive SOC Automation Workflow with Wazuh, Shuffle, The Hive, and VirusTotal**

## **Project Overview**

This project demonstrates how to build an automated Security Operations Center (SOC) workflow using open-source tools. By integrating **Wazuh**, **Shuffle**, **The Hive**, and **VirusTotal**, this project allows for efficient detection, analysis, and automated response to security incidents. The workflow is designed to improve operational efficiency by automating threat detection, incident response, and case management.

## **Objectives**

- To establish a fully automated SOC environment.
- To integrate Wazuh for monitoring and detecting security threats.
- To automate workflows using Shuffle and VirusTotal for reputation checks.
- To manage incidents and alerts in The Hive, streamlining response and investigation processes.
- To simulate and detect real-world attack scenarios, specifically the **Mimikatz** attack, to generate telemetry for analysis.

## **Skills Learned**

- Configuration of **Wazuh** for log collection and security monitoring.
- Creation of **SOAR workflows** in **Shuffle** for automated incident response.
- Integration of **The Hive** for incident management and alert tracking.
- Utilization of **VirusTotal** for file hash reputation checks.
- Practical knowledge in setting up a **SOC** environment and automated response procedures.
- Simulating real-world attacks, including **Mimikatz**, to generate system telemetry and logs.

## **Tools Used**

- **Wazuh**: Open-source security monitoring and log analysis platform.
- **Shuffle**: SOAR (Security Orchestration, Automation, and Response) tool for automating workflows.
- **The Hive**: Open-source incident response platform for managing alerts and incidents.
- **VirusTotal**: Online service for checking file hash reputations.
- **Sysmon**: System monitor tool for capturing detailed event telemetry.
- **Mimikatz**: Tool for simulating credential theft and gathering system logs to test security defenses.

## **Steps**

### **1. Setting Up the Environment**

- Deployed **Wazuh** on an **Ubuntu server** to handle log ingestion and security monitoring.
- Set up **The Hive** on a separate **Ubuntu server** for incident management.
- Installed **Sysmon** on a **Windows 10** machine to capture detailed system activity and logs.
- Created accounts and configured integrations with **Shuffle** and **VirusTotal** for automation and threat intelligence.

### **2. Simulating and Detecting Malicious Activity**

- **Simulated Mimikatz Attack**: I ran **Mimikatz** on the **Windows 10** machine to simulate credential theft and to generate system telemetry data.
  - Disabled **Windows Defender** to allow Mimikatz to run undetected.
  - Used **PowerShell** to execute **Mimikatz** and simulate credential dumping.
  - Monitored the activity using **Sysmon** and **Wazuh**, which detected the malicious activity based on predefined rules.
  
- Configured **Wazuh** to detect suspicious activities and generate alerts related to Mimikatz activity.

### **3. Automating Incident Response with Shuffle**

- Created automated workflows in **Shuffle** to respond to Wazuh alerts.
- Integrated **VirusTotal** for reputation checks of suspicious files based on extracted hashes from the Mimikatz attack.
- Configured **The Hive** to automatically generate incidents from detected threats, including details about the Mimikatz attack.
- Set up email notifications to alert SOC analysts when incidents were created.

### **4. Analyzing Data and Managing Alerts in The Hive**

- Monitored incident responses in **The Hive**.
- Used **The Hive’s API** to automate the creation of cases with relevant information, including threat severity and details.
- Verified workflow execution by simulating attacks like Mimikatz and confirming automated incident creation.

## **Lessons Learned**

- **Integration is Key**: Seamlessly integrating different security tools (Wazuh, Shuffle, The Hive, VirusTotal) can significantly improve the efficiency of a SOC.
- **Automation Enhances Efficiency**: Automating repetitive tasks such as alert triage and incident creation saves time and ensures a faster response to threats.
- **Simulating Real-World Attacks**: Running **Mimikatz** helped generate valuable telemetry, highlighting the importance of testing security setups with realistic attack scenarios.
- **Real-World Application**: This project gave me practical experience in building a SOC automation workflow, which is highly valuable for real-world security operations.

## **Final Thoughts**

This project showcases the potential of open-source tools for building an effective and automated SOC. The workflow we developed enables real-time detection, analysis, and response to security incidents, demonstrating how automation can enhance SOC operations. By combining monitoring, automation, and case management tools, we can create a streamlined, efficient response to cyber threats.
