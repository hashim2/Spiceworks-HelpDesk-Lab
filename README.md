# Spiceworks Help Desk Lab
# 🎫 Spiceworks Help Desk Lab — Ticket Walkthrough

## Overview

This document walks through the process of creating and resolving a simulated help desk ticket using **Spiceworks Cloud Help Desk**.

---

## Lab Environment

| Field | Value |
|---|---|
| Platform | Spiceworks Cloud Help Desk |
| Organization | Help Desk Lab |
| Technician | Hashim Sufi |
| Date | March 27, 2026 |

---

## Ticket #1 — WiFi Not Connecting to Laptop (LAPTOP01)

### Step 1: Create the Ticket

A new ticket was submitted via the **"Create a Ticket"** form in Spiceworks.

| Field | Value |
|---|---|
| **Contact** | sarahjohnson@techcorp |
| **Summary** | WiFi Not Connecting to Laptop (LAPTOP01) |
| **Description** | My WiFi no longer connects to the office network and it previously connected automatically. I have tried restarting my laptop but the issue persists. I am available all day for troubleshooting and my office is on the 2nd floor. |
| **Assignee** | Hashim Sufi |
| **Priority** | High |
| **Category** | Network |
<img width="941" height="590" alt="IMG_2126" src="https://github.com/user-attachments/assets/c2f2da39-fd1f-4e89-9643-3ff35185eb09" />

> Priority set to **High** — no network connectivity directly impacts the user's ability to work.

---

### Step 2: Diagnose the Issue

- The user's **WiFi certificate had expired**, preventing authentication to the corporate wireless network.
- Confirmed by checking the device record in **Jamf Pro** under asset **LAPTOP01**.

---

### Step 3: Resolve & Communicate
<img width="695" height="596" alt="IMG_2127" src="https://github.com/user-attachments/assets/9353a5f2-992b-487d-90da-4b360beff8ef" />

**Technician response in ticket:**
> "Hello, your WiFi Certificate has expired and I just renewed it on the backend. Can you please check if it's working now?"

**End user confirmation:**
> "Yes it's working now. Thank you!"

---

### Step 4: Internal Note

> Renewed WiFi certificate via Jamf. Steps: navigated to Jamf Pro, located the device under LAPTOP01, pushed updated certificate profile to the device, confirmed deployment was successful.

---

### Step 5: Close the Ticket

Once the user confirmed resolution, the ticket was closed using the **"Close"** button in the ticket view.

> **Best Practice:** Always wait for end-user confirmation before closing a ticket.

---

## Skills Demonstrated

- Ticket intake with proper categorization and priority assignment
- Root cause identification (expired WiFi certificate)
- Remote remediation via MDM (Jamf Pro)
- Clear end-user communication within the ticket thread
- Internal note documentation for team visibility
- Full ticket lifecycle management (Open → Resolved → Closed)

---

## Ticket Summary

| Field | Value |
|---|---|
| **Ticket #** | 9 |
| **Issue** | WiFi not connecting to corporate network |
| **Root Cause** | Expired WiFi certificate on LAPTOP01 |
| **Resolution** | Certificate profile renewed and pushed via Jamf Pro |
| **Priority** | High |
| **Category** | Network |
