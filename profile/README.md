# MarStack Labs

Infrastructure primitives for people who run their own machines.

Three pieces, built to work together and to work alone: something to run workloads on, something to
hold their secrets, and something to control who reaches the box.

## Projects

| Project | What it is | Status |
|---|---|---|
| `marstack-cloud` | Containers, VMs, and microVMs as one resource type — on a single node or across many baremetal machines, through the same code and the same API | Control plane skeleton |
| `marstack-secrets` | Secret and parameter store. Machine identities, bounded-lifetime access, every read recorded | Early development |
| `marstack-access` | Identity-aware access to Linux hosts. No standing credentials, agentless, sessions you can grep | Pre-release |

Repositories stay private while the interfaces move. Nothing here is ready for anything you care
about.

## How these are built

| | |
|---|---|
| `N=1` is the general case | a one-node deployment takes the same code path as a hundred |
| No standing credentials | a secret long-lived enough to be worth stealing is a design failure |
| Audit outlives its host | owning a component does not erase what it already reported |
| Names, not addresses | every resource is reachable by name from the moment it exists |
| Boundaries are deliberate | what each project refuses to do is written down, with the reasoning |

Go, one binary per project, no runtime to install first.
