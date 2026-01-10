# Discord C2 Simulation - Red Team Research Porject

## Project Overview
This project is a controlled red-team simulation designed to study how modern commodity malware abuses legitimate platforms (Discord) as a Command-and-Control (C2) channel.

The research was conducted exclusively on systems owned by the researchers. No third-party systems, users, or networks were involved.

## Objectives

- Simulate real-world malware behavior
- Study C2 over trusted SaaS platforms
- Observe how payload concealment and decoy execution affect user awareness

## Command-and-Control via Legitimate Platforms
Modern adversaries increasingly avoid custom infrastructure and instead abuse legitimate, widely trusted platforms as Command-and-Control (C2) channels. This project simulates that tradecraft by leveraging Discord’s public API as a communication layer.

At a conceptual level:
- The endpoint establishes an outbound HTTPS connection to a well-known SaaS provider
- Communication occurs through standard REST/WebSocket APIs
- All traffic is TLS-encrypted
- No inbound connections are required

From a defender’s perspective, this traffic is indistinguishable from legitimate client activity without behavioral or context-aware analysis.

