---
{"dg-publish":true,"permalink":"/ccna/20-definitions/cisco-troubleshooting-methodology/","tags":["defs_ccna"],"created":"2023-11-04T12:45:23.000-07:00","updated":"2023-12-03T13:09:03.907-08:00"}
---

The *Cisco Troubleshooting Methodology* is an 8-step process that loops back and forth around itself. **Always** (always, at any step, for any reason) **DOCUMENT** any and *all changes* that have been made.
1. **Define the problem** in terms of *symptoms* and *potential causes*
2. **Gather facts**
	3. Ask affected users, and collect information from [[CCNA/20 - Definitions/NMS\|NMS]], [[CCNA/20 - Definitions/PCAP\|PCAP]]s, output from [[CCNA/20 - Definitions/25 - Mnemonics and Summaries/Diagnostic Commands\|Diagnostic Commands]], etc.
3. **Analyze information** and **Eliminate potential causes**
4. **Create an action plan** which changes *only one variable* at a time
5. **Implement Action Plan**
	1. *Document all changes made*
6. **Gather results of each change**
7. **Determine if issue is resolved**
	1. If resolved, *document changes* and process is complete.
8. **If unresolved, return to step 4**



*Neil Anderson* with [FlackBox](https://www.flackbox.com/the-cisco-troubleshooting-methodology) proposes a similar but different strategy
1. Define the problem
2. Gather information
3. Analyze information
4. Eliminate potential causes
5. Propose hypothesis
6. Test Hypothesis
7. Solve Problem and Document Solution

![Cisco Troubleshooting Methodology-1.png](/img/user/Attachments/Cisco%20Troubleshooting%20Methodology-1.png)
Source: [FlackBox](https://www.flackbox.com/the-cisco-troubleshooting-methodology)

There are 4 key troubleshooting styles
1. Work around the OSI model
	1. Top down
		1. Application>Physical
	2. Bottom up
		1. Physical>Application
	3. Divide and Conquer
		1. Start in the middle
2. Compare configuration
	1. Between different devices, between backups, etc.
3. Trace the path
	1. Trace the path from source to destination
4. Swap out components
	1. Is something physically broken?

# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources
[Troubleshooting Overview Cisco Systems](https://www.cisco.com/en/US/docs/internetworking/troubleshooting/guide/tr1901.html)
[The Cisco Troubleshooting Methodology - FlackBox](https://www.flackbox.com/the-cisco-troubleshooting-methodology)
