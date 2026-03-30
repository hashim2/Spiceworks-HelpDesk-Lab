# Spiceworks Help Desk Lab

# 🖥️ Spiceworks Help Desk Home Lab

A hands-on IT help desk simulation built using Spiceworks Cloud Help Desk.
This lab demonstrates real-world ticketing workflows including ticket intake,
triage, resolution, escalation, and internal documentation.

---

## 🧰 Lab Environment

| Field | Value |
|---|---|
| **Platform** | Spiceworks Cloud Help Desk |
| **Organization** | Help Desk Lab |
| **Technician** | Hashim Sufi |
| **Certifications** | CompTIA A+ |

---

## 📋 Tickets Completed

| # | Summary | Category | Priority | Outcome |
|---|---|---|---|---|
| 9 | WiFi Not Connecting to Laptop (LAPTOP01) | Network | High | Resolved |
| 12 | Can't Access Financial Database (FinDB) | Software | Medium | Escalated |

---

## Ticket #9 — WiFi Not Connecting to Laptop (LAPTOP01)

### Step 1: Create the Ticket

A new ticket was submitted on behalf of the end user via the Create a Ticket form.

<img width="941" height="590" alt="image" src="https://github.com/user-attachments/assets/eb29ac01-8f2d-47cc-9197-1a67e069dc9d" />


| Field | Value |
|---|---|
| **Organization** | Help Desk Lab |
| **Contact** | sarahjohnson@techcorp.com |
| **Summary** | WiFi Not Connecting to Laptop (LAPTOP01) |
| **Description** | My WiFi no longer connects to the office network and it previously connected automatically. I have tried restarting my laptop but the issue persists. I am available all day for troubleshooting and my office is on the 2nd floor. |
| **Assignee** | Hashim Sufi |
| **Priority** | High |
| **Category** | Network |

> **Priority — High:** The user has no network connectivity, directly
> impacting their ability to work.

---

### Step 2: Diagnose the Issue

After reviewing the ticket, the root cause was identified:

- The user's **WiFi certificate had expired**, preventing the device from
  authenticating to the corporate wireless network
- Confirmed by checking the device record in **Jamf Pro** under asset **LAPTOP01**

---

### Step 3: Resolve & Communicate

The fix was pushed remotely and the technician followed up in the ticket thread.

<img width="695" height="596" alt="image" src="https://github.com/user-attachments/assets/5e2b8ab3-b518-4b17-b37b-b05d1306e7a2" />


**Technician public reply:**
> "Hello, your WiFi Certificate has expired and I just renewed it on the
> backend. Can you please check if it's working now?"

**End user confirmation:**
> "Yes it's working now. Thank you!"

---

### Step 4: Internal Note

> "Renewed WiFi certificate via Jamf. Steps: navigated to Jamf Pro, located
> the device under LAPTOP01, pushed updated certificate profile to the device,
> confirmed deployment was successful."

---

### Step 5: Close the Ticket

Once the end user confirmed the issue was resolved, the ticket was closed
using the Close button in the top-right of the ticket view.

> **Best Practice:** Always wait for end-user confirmation before closing
> a ticket when possible.

---

### Ticket #9 Summary

| Field | Value |
|---|---|
| **Ticket #** | 9 |
| **Issue** | WiFi not connecting to corporate network |
| **Root Cause** | Expired WiFi certificate on LAPTOP01 |
| **Resolution** | Certificate profile renewed and pushed via Jamf Pro |
| **Priority** | High |
| **Category** | Network |
| **Outcome** | ✅ Resolved |

---

## Ticket #12 — Can't Access Financial Database (FinDB)

### Step 1: Create the Ticket

A new ticket was submitted on behalf of the end user via the Create a Ticket form.

![Creating ticket #12 in Spiceworks](screenshots/IMG_5439.jpeg)

| Field | Value |
|---|---|
| **Organization** | Help Desk Lab |
| **Contact** | joshsmith@techcorp.com |
| **Summary** | Can't access Financial Database (FinDB) |
| **Description** | Unable to access the financial database. Credential reset and basic network checks have been performed with no resolution. |
| **Assignee** | Hashim Sufi |
| **Priority** | Medium |
| **Category** | Software |

> **Priority — Medium:** User cannot access a critical system but escalation
> is in progress and a workaround may exist in the interim.

---

### Step 2: Diagnose the Issue

Initial Tier 1 troubleshooting was performed before escalating:

- Reset user credentials for joshsmith@techcorp.com — issue persisted
- Verified network connectivity to the FinDB server — issue persisted

Both steps failed to resolve the issue. The problem is beyond Tier 1 scope
and requires **Database Admin** intervention.

---

### Step 3: Escalate & Communicate

Since the issue could not be resolved at Tier 1, the ticket was escalated
to the Database Admin team with full context.

![Ticket #12 escalation thread in Spiceworks](screenshots/IMG_5438.jpeg)

**Technician public reply:**
> "Hello, I'm escalating this ticket to the Database Admin team. The user's
> account is joshsmith@techcorp.com and they need read-only access to FinDB.
> I have already attempted a credential reset and basic network checks with
> no resolution. Please advise."

---

### Step 4: Internal Note

> "Escalated to Database Admins. Prior troubleshooting: reset credentials,
> verified network connectivity to FinDB — issue persisted. User account:
> joshsmith@techcorp.com, requires read-only access. Awaiting DB team response."

---

### Ticket #12 Summary

| Field | Value |
|---|---|
| **Ticket #** | 12 |
| **Issue** | User unable to access Financial Database (FinDB) |
| **Root Cause** | Permissions issue beyond Tier 1 scope |
| **Resolution** | Escalated to Database Admin team |
| **Priority** | Medium |
| **Category** | Software |
| **Outcome** | 🔺 Escalated |

---

## 🛠️ Skills Demonstrated

- Ticket intake with proper categorization and priority assignment
- Root cause identification and remote remediation via MDM (Jamf Pro)
- Recognizing when a ticket exceeds Tier 1 scope
- Performing and documenting troubleshooting steps before escalating
- Writing clear escalation messages with all relevant user details
- End-user communication within the ticket thread
- Internal note documentation for team visibility
- Full ticket lifecycle management (Open → Resolved / Escalated)

---

## 📁 Repository Structure

