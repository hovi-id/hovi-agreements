# Hovi Service Level Agreement for SaaS and Cloud Service

**Last update:** May 21, 2025

Hovi cloud services is hosted on [www.hovi.id](https://www.hovi.id) enjoy the following service at all times.

- **Uptime** - 99.9%
  - Customer databases are hosted in the chosen Hovi region: europe
  - Each database is replicated in real-time on redundant storage located in the same data center
  - We work with trusted cloud provider that always deliver at least 99.9% uptime guarantee, so we guarantee 99.9% uptime on a monthly basis (3 nines, excluding planned maintenance)*
  - 99.9% uptime monthly = maximum unplanned downtime of 45 min/month.
  - We usually deliver much better uptime than this (100% most months), as our providers always deliver a much better uptime than their SLA too.
  - *these metrics refer to the availability of the platform itself for all customers. Individual databases may be temporarily unavailable for specific reasons, typically related to the customer's actions or customizations.
- **Planned maintenance operations** happen infrequently, typically once every couple of months, generally last less than 1 hour, and are scheduled outside of business hours in the region where the maintenance is taking place. They are announced by email.

## High Availability

Our data centers are Tier-III certified or equivalent, with N+1 redundancy for power, network and cooling. Each customer database is replicated in real-time on redundant storage located in the same data center, so a failover can happen quickly in case of hardware failure, with no data loss.

## Backups & Disaster Recovery

- 7 full backups for at least 7 days.
- Backups replicated on at least 1 different machine in different data center in Europe. It is not possible to choose or restrict the regions where backups are replicated.
- **For a permanent disaster impacting one server only**:
  - **RPO (Recovery Point Objective)** = 1 hour, i.e. you can lose 1 hour of work max, but in general it will be less than 5 minutes.
  - **RTO (Recovery Time Objective)** = 6 hours, i.e the service should be back online within 6 hours  (Standby promotion time + DNS propagation time included).
- **For data center disasters (one entire data center is completely and permanently down)**:
  - **RPO (Recovery Point Objective)** = 24h, i.e. you can lose maximum 24h of work if the data cannot be recovered and we need to restore the last daily backup.
  - **RTO (Recovery Time Objective)** = 24h, i.e. the service will be restored from the backup within 24 hours in a different data center.

## Security

The safety of your data is very important to us, and we design our systems and procedures to guarantee it. Here are some highlights:

- **SSL** - All web connections to client instances are protected with 256-bit SSL encryption (HTTPS with a 2048-bit modulus SSL certificate), and running behind Grade A SSL stacks. All our certificates chains are using SHA-2 already.
- **Reliable Platform** - Servers with full hardware guarantee, redundant data storage, network and electrical supplies.
- **Passwords** - Customer passwords are protected with industry-standard encryption.
- **Safe Systems** - Our servers are running recent Linux distribution with up-to-date security patches, with firewall and intrusion counter-measures (not disclosed for obvious reasons).
- **Isolation** - Client data stored in dedicated databases - no sharing of data between clients, no access possible from one database to another.
