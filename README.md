# Subdomain-Enumeration

🔍 What is a Subdomain?

A subdomain is an extension of a main domain name used to organize and navigate different sections of a website. It appears before the main domain name.

📌 Example:

In blog.example.com:

example.com → is the main domain.

blog → is the subdomain.


#  🔎 Why is Subdomain Enumeration Important?
Subdomain enumeration is a critical step  penetration testing and bug bounty hunting. Here’s why:

✔ Attack Surface Expansion:
Many organizations expose unintended services on subdomains, which may have weak security.

✔ Finding Hidden Web Applications:
Some subdomains may host forgotten or deprecated applications that still contain sensitive information.

✔ Identifying Staging & Development Environments:
Subdomains often reveal test environments, which can be misconfigured or lack security patches.

✔ Detecting Misconfigurations & Data Leaks:
Some subdomains are misconfigured, leaking API keys, database access, or internal documents.

✔ Cloud Asset Discovery:
Many companies use cloud services (AWS, Azure, GCP), and subdomain enumeration helps find cloud-hosted applications.

#  🛠 Common Uses of Subdomains:

✔ Separating services (e.g., shop.example.com for an online store).

✔ Hosting different sites (e.g., support.example.com for customer support).


#  🛠 Methods of Subdomain Enumeration

1️⃣ Passive Enumeration (OSINT-Based)
Passive enumeration gathers subdomains without directly interacting with the target, reducing the risk of detection.

✅ Sources for Passive Enumeration:

● Search Engines (Google, Bing, Yandex) – Using Google Dorks to find indexed subdomains.

● Certificate Transparency Logs (crt.sh) – Checking SSL/TLS certificates for subdomains.

● Wayback Machine (archive.org) – Discovering older subdomains from archived data.

● Public Threat Intelligence (VirusTotal, SecurityTrails, Shodan) – Searching for domain information.

🔹 Example Google Dork for Subdomains:


    site:example.com -www

    

2️⃣ Active Enumeration (Direct Interaction)
Active enumeration involves probing the target domain to uncover subdomains through scanning and brute-force techniques.

✅ Methods for Active Enumeration:

● Brute-Force Attacks – Using wordlists to guess subdomains (e.g., admin.example.com, portal.example.com).

● DNS Probing – Querying DNS records (A, CNAME, MX, TXT) for subdomains.

● Virtual Host Enumeration – Finding subdomains hosted on shared servers.

🔹 Example DNS Recon using dig:


    dig +short subdomain.example.com


# 💻 How to Find Subdomains Using Sublist3r

You can use Sublist3r, a subdomain enumeration tool, to discover subdomains of a target domain.
    
Example Command:

     sublist3r -d example.com

This will list all discovered subdomains of example.com.
