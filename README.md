# HEFAISTOS Platform - DEMO Rulez Repository

> ⚠️ **CRITICAL WARNING - FOR TESTING PURPOSES ONLY** ⚠️
> 
> The data, rules, and configurations contained in this repository are **DEMO outputs** generated from the HEFAISTOS platform. 
>
> **DO NOT deploy these rules into a production environment without thorough validation.** > Data and rules originating from other users **cannot be trusted**. User-generated content may be fake, misleading, poorly optimized, or intentionally malicious. Deploying unverified rules can cause severe harm to your production environment, including catastrophic alert fatigue, SIEM/EDR performance degradation, or ingestion pipeline outages. Always test rules in an isolated lab or non-production environment first.

## Repository Structure

This repository (https://github.com/hefaistos-platform/rulez/tree/main) is organized to reflect the outputs of the HEFAISTOS platform, separated by conceptual OpenTide objects and specific SIEM/EDR query formats.

### `/Objects` (OpenTide Format)

This directory contains the foundational elements of the detection engineering process, structured in the OpenTide format. It is divided into three primary categories:

* **Detection Objectives:** These define the high-level goals and the *why* behind a detection. They outline the specific malicious behavior, intent, or policy violation the system is aiming to identify (e.g., "Detect lateral movement via SMB").
* **Detection Rules:** These are the structured, platform-agnostic representations of the detection logic. **Note: A single file within this directory may contain multiple detection rules.**
* **Threat Vectors:** These define the attack paths, methods, or specific Tactics, Techniques, and Procedures (TTPs) an adversary might utilize to achieve their goal. They provide the necessary threat intelligence context for the rules.

### Format-Specific Output Folders (`/kql`, `/spl`, `/wazuh`, etc.)

Alongside the OpenTide objects, the repository includes format-specific directories. While you may currently only see a few (like `/kql`), the structure supports multiple languages including `/spl`, `/wazuh`, `/xml`, and `/aql`.

* These folders contain **single, standalone rules** exported directly from the HEFAISTOS workbench.
* The rules are formatted specifically for native ingestion into their respective target platforms.

**Supported Platforms (as of 05/2026):**
* **Microsoft Defender / Microsoft Sentinel** (KQL)
* **Splunk** (SPL)
* **IBM QRadar** (AQL / XML)
* **WAZUH**
