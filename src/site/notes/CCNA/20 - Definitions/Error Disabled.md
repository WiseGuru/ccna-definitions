---
{"dg-publish":true,"permalink":"/ccna/20-definitions/error-disabled/","tags":["defs_ccna"],"created":"2023-11-04T12:45:23.000-07:00","updated":"2023-11-08T13:57:21.000-08:00"}
---

#### errdisabled 
- Ports can enter an error-disabled (errdisable) state if it breaks policy and is configured to do so.

| Command                                                      | Description                                                                             |
| ------------------------------------------------------------ | --------------------------------------------------------------------------------------- |
| `SW1:# show errdisable recovery`                             | Show *errdisable* configuration                                                         |
| `SW1:# show port-security <interface ID>`                    | Review port-security status and logs on an interface                                    |
| `SW1:# show errdisable detect`                               | Shows all supported *Errdisable* reasons                                                |
| `SW1:config# errdisable recovery cause <violation>`          | Enables automatic recovery for specific violation causes (psecure-violation, all, etc.) |
| `SW1:config# errdisable recovery interval <time in seconds>` | configures the amount of time *errdisabled* ports will take to recover                  |


# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources

