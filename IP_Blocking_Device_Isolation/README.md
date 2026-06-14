- _**IP Blocking and Device Isolation**_

**Objective**

- Demonstrate SOC containment actions by blocking a suspicious IP address and isolating a device using Windows Defender Firewall.

**Tools Used**

- Windows Defender Firewall with Advanced Security
- Command Prompt
- Windows Operating System
  
- _**IP Blocking**_

**Steps Performed**

- Open Windows Defender Firewall with Advanced Security.
- Select Outbound Rules.
- Click New Rule.
- Choose Custom Rule.
- Select All Programs.
- Under Scope, select These IP Addresses under Remote IP Address.
- Add the suspicious IP address.
- Click Next.
- Select Block the Connection.
- Apply the rule to Domain, Private, and Public profiles.
- Name the rule and click Finish.
- Verify the rule is active.
  
**Verification**

- Confirmed the firewall rule was created successfully.
- Verified communication with the blocked IP address was denied.

- _**Device Isolation**_

**Steps Performed**

- Open Windows Defender Firewall with Advanced Security.
- Right-click Windows Defender Firewall with Advanced Security on Local Computer.
- Select Properties.
- Under the Domain Profile tab:
  1) Inbound Connections: Block
  2) Outbound Connections: Block
- Repeat the same configuration for:
1) Private Profile
2) Public Profile
- Click Apply and OK.
- Verify that all network communication is blocked.
  
**Verification**

- Open Command Prompt.
- Run: ping 8.8.8.8
- Confirm that network communication fails.
- Attempt to access a website and verify connectivity is blocked.
  
**SOC Relevance**

- These actions are commonly used during the containment phase of incident response to:
- Block malicious IP communication.
- Prevent malware propagation.
- Stop Command-and-Control (C2) traffic.
- Reduce lateral movement.
- Limit the impact of a security incident.
