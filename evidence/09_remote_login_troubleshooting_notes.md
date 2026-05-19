# Remote Login Troubleshooting Notes

## Scope
Validated SSH remote login behavior between IF-MAC-LEG01 and IF-WIN-HP01 using a dedicated Windows test account.

## Key Findings
- Source endpoint identity was verified on IF-MAC-LEG01.
- Destination endpoint identity was verified on IF-WIN-HP01 using the dedicated `sshlab` test account.
- ICMP ping from IF-MAC-LEG01 to IF-WIN-HP01 returned 100% packet loss.
- TCP/22 validation succeeded, confirming SSH-specific connectivity was available.
- SSH authentication succeeded from IF-MAC-LEG01 into IF-WIN-HP01.
- Remote session context was verified using `whoami` and `hostname`.
- A local evidence file, `ssh_success.txt`, was created and validated.

## Conclusion
Although ICMP echo replies were unavailable or filtered, SSH-specific connectivity over TCP/22 was confirmed. The remote login test successfully authenticated from IF-MAC-LEG01 into IF-WIN-HP01 and preserved supporting evidence.
