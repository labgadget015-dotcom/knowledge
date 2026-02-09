# Security Stack - Seed

## Project
Security / Home-lab / Remote access

## Goal
High-signal, "secure-enough" baseline for home lab, VPN, remote access, and monitoring.

## Stack
- Router model: [TBD]
- ISP: [TBD]
- VLAN support: [TBD]
- VPN: WireGuard (or alternative)
- Monitoring: Uptime Kuma / Prometheus
- Logging: Loki/Grafana

## Constraints
- Self-host where reasonable
- Minimal recurring cost
- Low maintenance

## Current state
- [ ] Baseline network map
- [ ] VPN entrypoint
- [ ] Segmentation (lab vs personal)
- [ ] Basic monitoring

## Open questions
- Threat model focus (casual vs targeted)?
- Which services must be reachable externally?
- Cold storage / disaster recovery plan?

## Next actions
1. Define segments/VLANs
2. Pick VPN topology
3. Decide logging/monitoring stack
