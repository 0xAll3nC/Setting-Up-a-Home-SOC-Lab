# Splunk: Setting up a Lab  

## Introduction  

### Background  

A few weeks ago, Jasmine, the owner of Coffely, reported a potential data breach that resulted in the theft of her secret recipe. The culprit, James from the IT department, attempted to exfiltrate the sensitive information. However, thanks to the swift response from the forensics team, undeniable evidence was found on his laptop, leading to his apprehension before the recipe could reach competitors.  

To prevent future security incidents, Jasmine has decided to establish an in-house **Security Operations Center (SOC)** to continuously monitor critical logs and network events. She has reached out to our team to deploy an **on-premises SOC solution**, ensuring real-time detection and response to suspicious activities.  

### Objective  

As part of this initiative, we are tasked with setting up a **Security Information and Event Management (SIEM) system** using **Splunk**. The primary goals of this lab include:  

- Installing and configuring **Splunk** on both **Linux** and **Windows** servers.  
- Integrating key log sources from different systems.  
- Setting up ingestion mechanisms via listening ports or forwarders.  

By the end of this setup, we will have a functional **SOC lab** capable of collecting, analyzing, and responding to security events.  

---

## About Splunk and the Lab  

As explained in the **Splunk Basics** training, **Splunk** is a **SIEM** solution that allows us to collect, analyze, and correlate logs in a centralized server in real time.  

This lab will guide you through installing **Splunk** on **Linux** and **Windows**, configuring different log sources, and setting up data ingestion. Each lab covers the following topics:  

### **Linux Lab**  
- Install **Splunk** on **Ubuntu Server**  
- Install and integrate **Universal Forwarder**  
- Collect logs from important system sources like `syslog`, `auth.log`, `auditd`, etc.  

### **Windows Lab**  
- Install **Splunk** on **Windows Machine**  
- Install and integrate **Universal Forwarder**  
- Integrate and monitor **Coffely.THM's weblogs**  
- Collect and analyze **Windows Event Logs**  

---

## Prerequisites  

Before starting this lab, it is recommended to have prior knowledge of **SIEM fundamentals** and **Splunk basics**. The following resources provide essential background:  

- [Intro to SIEM](https://tryhackme.com/room/introtosiem)  
- [Splunk Basics](https://tryhackme.com/room/splunk101)  

---

## Lab Environment  

This SOC lab consists of two virtual machines (**Linux** and **Windows**). The setup process involves:  

1. **Installing Splunk** on both machines.  
2. **Configuring log ingestion** from various sources.  
3. **Establishing data forwarding** mechanisms for centralized log collection.  

This documentation will provide a step-by-step guide to setting up the SOC lab, ensuring a robust security monitoring framework is in place.  
