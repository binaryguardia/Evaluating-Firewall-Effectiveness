# Evaluating-Firewall-Effectiveness
A project documenting the setup and testing of firewall rules using nmap to evaluate their effectiveness on a virtual Kali Linux machine.

## Project Overview

This project focuses on configuring and evaluating firewall rules on a virtual Kali Linux machine. The aim is to understand how different firewall rules impact network security and to test their effectiveness using `nmap` scans.

## Contents

- **Firewall Rules Setup:** A detailed overview of the rules configured.
- **Testing Results:** Analysis of the results from regular and SYN scans using `nmap`.
- **Key Findings:** Insights into the effectiveness of the configured firewall rules.

## Setup and Configuration

### 1. Firewall Rules Configuration

Here is a summary of the firewall rules applied:

```bash
sudo ufw status numbered
