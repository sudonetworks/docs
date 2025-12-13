Week 1
======

12/8 - 12/15

What I am learning.


Topics


Network Security Fundamentals & Concepts
========================================

- Author: Piotr Kaluzny
- Site: INE
- Length: 3h 21m

Security Principles
-------------------

Terms
~~~~~

Principle of Least Privilege
   Very granular access ctrl. The user/device is only allowed to perform
   its specific task or function and nothing more. 😊
Defense in Depth
   There are multiple systems in place to protect data/network. Firewall
   at the perimeter and ISE at that access layer.
Separation of Duties
   More than 1 person is allowed to complete an operation. Example:
   Creating an admin account requires two users to complete.
Asset
   Anything of value to an organization.
Threat
   A person/place/action/environment that can impact or cause harm to an
   asset.
Vulerability
   A weakness on a system.
Risk
   A potential impact/compromise to an asset.
Countermeasure
   A method of reducing risk.
Risk MGMT
   Used to identify, assess, and prioritize and monitor risks.

IDS/IPS Fundamentals
--------------------

How IDS/IPS determine if an attack is done.

Signature
   Set of rules/conditions that describe an attack. Signatures must be
   up-to-date to be effective.
Anomaly Detection
   Initially learns patters of normal network activities. When the
   network activity changes it will alert/drop. Uses a baseline profile
   to compare network activities to.
Policy-Based
   Traffic detected outside the congfigured policy will trigger an
   alarm. Configuration of policy may be cumbersome and require a lot of
   fine tuning.
Reputation Based
   Traffic evaluated based on a 3rd party such as Talos to determine
   malicious IPs, URLs, and domain names.

Sensor Actions
~~~~~~~~~~~~~~

Depends on either if IPS or IDS[^Further_Details].

Alert/Alarm
   Generate an log
Drop
   Kill the malicious packet
Block
   Block the session, all from the attacker or traffic seen between
   client and the attacker
Reset
   Disconnect a TCP Session
Shun
   ask another device to block the malicious traffic for instance with
   an ACL.

Sensor Decision Classification
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

*True*
   event was correct on the classification.
*False*
   event was incorrectly classified and requires signature/policy
   tuning.
*Positive*
   signature/policy alerted on the event.
*Negative*
   Signature/policy did not alert on the event.

Examples:

- True Positive: Event was seen & alerted correctly. **GOOD**

  - This is the ideal outcome. The system is working as intended, and a
    genuine threat is identified and handled.

- True Negative: Normal traffic did not trigger a signature.\ **GOOD**

  - This is the desired baseline state. The system correctly ignores
    benign activity, contributing to a smooth workflow and network
    performance.

- False Positive: Signature alerted on **NORMAL** traffic. **WRONG**

  - This is a nuisance outcome. While not a security breach, frequent
    false alarms lead to “alert fatigue”—where security analysts become
    desensitized and may ignore critical alerts amidst the noise,
    wasting valuable time and resources. This often happens due to
    overly broad or poorly tuned rules.

- False Negative: Attack went undetected. **WRONG**

  - This is the most dangerous outcome. A true intrusion is missed, and
    the security team is unaware of the breach. This can occur with
    zero-day exploits or new attack variants that don’t have a known
    signature.
