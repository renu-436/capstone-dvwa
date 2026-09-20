# Reconnaissance

## Objective

The objective of reconnaissance was to identify the local DVWA web service and determine the ports and services exposed by the test application.

## Target

Target:
127.0.0.1

Application:
Damn Vulnerable Web Application (DVWA)

## Commands Used

ip addr

sudo ss -tulpn | grep -E ':80|:443'

nmap -sV -p 80,443 127.0.0.1

## Observation

The reconnaissance process confirmed the availability of the local web service used by DVWA.

Nmap service detection was used to identify the HTTP service.

## Security Relevance

Service enumeration helps identify the attack surface of a system. Unnecessary or outdated services can increase the potential attack surface.

## Evidence

See:

screenshots/task5_nmap_dvwa.png
