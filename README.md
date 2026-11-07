### Hi, I'm Mark

Cybersecurity specialist, working on a master's in cybersecurity. Outside work I run a homelab that I treat like a small production network: segmented, monitored, backed up, patched on purpose and documented as code.

**The lab**

- **Virtualization:** Proxmox VE, with LXC containers and VMs behind per-guest firewalls (default deny, rules written from observed traffic, each one soaked with drop logging before it is trusted)
- **Network:** UniFi gateway with segmented VLANs (infrastructure, trusted, IoT, services, guest), DNS through a high-availability Pi-hole pair with a floating VIP, remote access over Tailscale only
- **Home automation:** Home Assistant, kept on its own VLAN with a firewall that only allows what it needs
- **Backups:** Proxmox Backup Server with nightly and weekly jobs, encrypted host-config backups, restore tests, and a monthly offline copy (3-2-1)
- **Monitoring:** Uptime Kuma, Beszel, VictoriaLogs and a daily automated morning check
- **Automation:** Ansible for guest standards and audits, shell and Python for the rest

**How I work**

- **Docs-as-code:** every host, service, decision and change lives in a Markdown wiki in Git, with decision records and a session log
- **Secrets stay out of Git:** a password vault, plus gitleaks in a pre-commit hook and in CI
- **Updates are triaged, not just applied:** for pinned images and held packages I diff what actually changed and check which CVEs it fixes, and whether they apply here, before deciding how urgent it is
- **AI-assisted, human-owned:** I work alongside Claude Code (Anthropic). It drafts, researches and runs read-only checks; I review, decide and make the changes that matter

**Currently**

- Contributing small fixes upstream to the security tools I use
