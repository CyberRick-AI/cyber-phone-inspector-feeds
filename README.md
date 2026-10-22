# Cyber Phone Inspector feeds

Public, data only. The threat lists the Cyber Phone Inspector Android app bundles and refreshes:

| File | What | Source and licence |
|---|---|---|
| `feeds/spyware.json` | spyware and stalkerware package ids, domains, signing certs, IPs | MVT indicator index (Amnesty International Security Lab and the lists it names) |
| `feeds/trackers.json` | advertising, analytics and profiling kits found inside apps | Exodus Privacy, CC BY-SA 4.0 |
| `feeds/malware_hashes.json` | SHA-256 of known Android malware with family and tags | MalwareBazaar, abuse.ch, CC0 |
| `feeds/malicious_hosts.json` | malware distribution and command domains and IPs | URLhaus and ThreatFox, abuse.ch, CC0 |
| `feeds/FEEDS.md` | dates and counts of the current lists | |

A GitHub Action refreshes them weekly with `tools/fetch_feeds.py`. The abuse.ch key is a repository secret (`ABUSECH_AUTH_KEY`) and never appears in this repository's files; without it the two abuse.ch lists are written as skipped. The app downloads these files over HTTPS from this repository's raw address and checks them on the phone. Nothing about any phone is ever sent here.

No code of the app lives here. Issues about the lists are welcome; issues about the app belong with the app.
