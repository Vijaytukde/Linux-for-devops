Linux for DevOps: System Administration & Troubleshooting

A hands-on Linux operations reference for cloud and DevOps environments. This repository organizes practical command references, system administration concepts, diagnostic workflows, and scenario-based exercises across core Linux topics.

Scope: The roadmap below describes the intended curriculum. Modules are being developed progressively; only the content currently available in each linked directory should be considered implemented.

What This Repository Covers

* Linux Fundamentals: Shell usage, navigation, files, directories, and system information
* Filesystem Operations: Paths, file management, directory structure, and storage concepts
* Access Control: Permissions, ownership, users, groups, and least-privilege practices
* Process and Service Operations: Process inspection, resource checks, systemd, and service logs
* Networking Diagnostics: DNS, connectivity, listening ports, HTTP requests, and routing fundamentals
* Shell Scripting: Variables, conditions, loops, exit codes, and repeatable operational tasks
* Storage and Capacity: Filesystem utilization, directory usage, mounts, and disk-pressure investigation
* Troubleshooting: Evidence collection, hypothesis testing, root-cause analysis, recovery validation, and operational runbooks

Repository Roadmap

Module	Coverage	Status
01 — Linux Basics	Essential commands, core concepts, hands-on labs, interview questions, and troubleshooting	Available
02 — Filesystem	Filesystem hierarchy, paths, file operations, links, and navigation	Content to be developed
03 — File Permissions	Permission bits, ownership, chmod, chown, umask, and access troubleshooting	Content to be developed
04 — Users & Groups	Accounts, groups, sudo, access checks, and user administration	Planned
05 — Process Management	ps, top, signals, resource utilization, and process troubleshooting	Planned
06 — System Services	systemctl, journalctl, service lifecycle, logs, and startup failures	Planned
07 — Networking	IP configuration, DNS, ping, curl, ss, ports, and connectivity diagnosis	Planned
08 — Shell Scripting	Bash syntax, variables, conditions, loops, functions, and automation	Planned
09 — Storage & Disk Management	df, du, mounts, capacity analysis, and disk-pressure scenarios	Planned
10 — Linux Operations Capstone	Integrated administration tasks, incident scenarios, recovery, and root-cause reports	Planned

Operational Troubleshooting Workflow

The troubleshooting approach emphasizes evidence-based diagnosis rather than random configuration changes.

1. Define the symptom — Identify the affected service, host, user, and time window.
2. Collect evidence — Inspect service status, logs, processes, resource usage, ports, and connectivity as appropriate.
3. Form a hypothesis — Connect observations to likely causes instead of changing settings at random.
4. Test safely — Run focused diagnostic checks and understand their impact before making changes.
5. Apply the smallest suitable fix — Follow least-privilege principles and avoid unnecessary disruption.
6. Verify recovery — Repeat checks and confirm the expected behaviour has returned.
7. Document the outcome — Record evidence, root cause, corrective action, validation, and preventive measures.

Quick Command Reference

The following examples demonstrate common Linux administration and diagnostic commands. Adapt service names and commands to the target distribution and environment.

System and filesystem checks

# Identify the current user and working directory
whoami
pwd
# Check filesystem capacity and directory usage
df -h
du -sh ./* 2>/dev/null

Process and service diagnostics

# Inspect running processes
ps -ef
top
# Check listening TCP and UDP sockets
ss -tuln
# Inspect a service and its recent logs
systemctl status nginx
journalctl -u nginx -n 50 --no-pager

Network and HTTP diagnostics

# Test an HTTP endpoint
curl -I http://localhost
# Check DNS resolution
nslookup example.com

Note: Commands such as systemctl, journalctl, and nslookup may require a compatible Linux distribution or additional utilities.

How Modules Are Structured

As the roadmap is implemented, module documentation will include relevant sections such as:

* Concept explanations and practical examples
* Commands, expected output, and interpretation
* Hands-on labs and scenario-based tasks
* Diagnostic steps and verification criteria
* Common errors, safe remediation, and best practices
* Review questions and practical assignments

Intended Audience

This repository is intended as a practical reference for:

* Linux administrators
* Cloud support engineers
* AWS and cloud infrastructure practitioners
* DevOps engineers
* IT professionals working with system operations and troubleshooting

Engineering Principles

Automation · Security · Reliability · Observability · Documentation

Maintainer

Vijay Tukde

Linux | AWS Cloud | DevOps

GitHub: @Vijaytukde
