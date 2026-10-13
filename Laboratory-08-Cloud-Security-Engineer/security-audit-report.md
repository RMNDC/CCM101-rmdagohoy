# Security Audit Report

## Principle of Least Privilege (PoLP)

Give people only the minimum access they need to do their job, and nothing extra. For cloud user accounts, this limits the damage if a password is stolen: a hacker who steals a worker's password can only access that worker's specific files, instead of taking over the whole company's cloud system.

## Attack Surface

Every door, window, or entry point that a hacker could use to break into a system. For a virtual machine, this includes open network connections, unneeded apps, weak passwords, and outdated software. Having a smaller attack surface means locking down or removing these entry points.

## Default Deny Policy

A default deny policy blocks all network traffic by default and only allows connections that you explicitly trust. Hackers constantly change their locations, IP addresses, and tools, so trying to block bad actors one by one is impossible. Blocking everything first keeps everyone out except approved users.
