# Sovereign pkg (`@lgcorzo/pkg`)

[![Go Reference](https://pkg.go.dev/badge/github.com/lgcorzo/pkg/v3.svg)](https://pkg.go.dev/github.com/lgcorzo/pkg/v3)
[![CI](https://github.com/lgcorzo/pkg/actions/workflows/go.yml/badge.svg)](https://github.com/lgcorzo/pkg/actions/workflows/go.yml)
[![License](https://img.shields.io/badge/License-AGPLv3-blue.svg)](https://github.com/lgcorzo/pkg/blob/main/LICENSE)

Collection of common Go utility packages used across the **Sovereign MinIO Ecosystem** and the **Dark Gravity Factory**.

---

## Capabilities & Package Overview

`@lgcorzo/pkg` provides core utility primitives, policy evaluation engines, cryptographic cert management, and environment abstraction routines used across sovereign infrastructure:

| Package | Purpose & Capabilities |
| :--- | :--- |
| `certs` | TLS certificate loading, hot-reloading manager, and X.509 validation primitives. |
| `console` | Terminal formatting, colored logging, and interactive user console utilities. |
| `cors` | Cross-Origin Resource Sharing (CORS) policy parsing and evaluation. |
| `ellipses` | Pattern matching and range expansion for node and drive set declarations. |
| `env` | Secure environment variable retrieval, secret parsing, and web-hosted configuration loaders. |
| `ilm` | Information Lifecycle Management (ILM) rule parsing and expiration/transition evaluation. |
| `ldap` | LDAP authentication validator and identity management integration helpers. |
| `licverifier` | Cryptographic license verification for enterprise sub-modules. |
| `mimedb` | High-performance MIME-type resolution database. |
| `net` | Network helper primitives, custom listener abstractions, host/port parsing, and CIDR checks. |
| `oidc` | OpenID Connect authentication, JWT parsing, and CLI callback authentication server. |
| `policy` | IAM policy evaluation engine, AWS/AIStor action matching, condition checkers, and resource matching. |
| `quick` | Thread-safe, atomic file-backed JSON configuration persistence. |
| `randreader` | Cryptographically secure random number and byte stream reader routines. |
| `rng` | High-performance pseudo-random number generator routines. |
| `safe` | Atomic file writer primitives ensuring crash-safe disk state modification. |
| `sync` | Deduplication (`dedup`) and enhanced error group handling (`errgroup`). |
| `sys` | Low-level OS primitives, file-descriptor limits, sysctl helpers, and cgroup resource monitoring. |
| `wildcard` | Fast pattern and string wildcard matching routines. |
| `xtime` | High-resolution time functions, duration parsing, and ISO8601 formatting. |

---

## Dark Gravity Factory & Sovereign Maintenance Rationale

This repository is maintained as an active, sovereign fork under **[@lgcorzo](https://github.com/lgcorzo)** to support the **Dark Gravity Factory** initiative and the 38 interconnected storage and AI production repositories.

### Why Sovereign Maintenance?

1. **Full Supply-Chain Autonomy:** Zero reliance on upstream breaking license changes, unannounced deprecations, or sudden repository archivals. Every dependency in `@lgcorzo/pkg` is controlled, audited, and built from source.
2. **Dark Gravity Factory Core Integration:** Powers autonomous AI agents, high-throughput distributed object storage, cryptographic key distribution, and enterprise security policies across the Dark Gravity AI pipeline.
3. **Compliance & Security:** Guarantees full alignment with regulatory standards including the EU AI Act, SOC 2 Type II, ISO 25059, and strict zero-CVE SLAs through automated vulnerability scanning (`govulncheck`) and continuous static analysis.
4. **Ecosystem Interoperability:** Native, seamless integration across all 38 repositories in the `@lgcorzo` sovereign ecosystem without module path collisions or upstream dependency rot.

---

## Sovereign MinIO Ecosystem (38 Repositories)

The table below outlines the 38 interconnected repositories comprising the `@lgcorzo` sovereign architecture:

| Category | Repository | Sovereign Role |
| :--- | :--- | :--- |
| **Core Storage & Control** | `lgcorzo/minio` | Distributed High-Performance Object Storage Server |
| | `lgcorzo/mc` | MinIO Client Command-Line Interface |
| | `lgcorzo/kes` | Key Encryption Service for Cloud-Native KMS Integration |
| | `lgcorzo/operator` | Kubernetes Operator for MinIO Clusters |
| | `lgcorzo/directpv` | Direct-Attached Storage CSI Driver for Kubernetes |
| | `lgcorzo/console` | Web-Based Graphical User Interface for MinIO |
| **SDKs & Utility Primitives** | `lgcorzo/pkg` | Common Go Utility Packages & Shared Primitives |
| | `lgcorzo/madmin-go` | MinIO Administrative API Client SDK |
| | `lgcorzo/minio-go` | Official MinIO Go Client SDK |
| | `lgcorzo/kms-go` | Go Client for MinIO KMS Integration |
| **Hardware & SIMD Acceleration** | `lgcorzo/sha256-simd` | SIMD-Accelerated SHA-256 Hashing Engine |
| | `lgcorzo/simdjson-go` | High-Throughput SIMD JSON Parser for Go |
| | `lgcorzo/blake2b-simd` | SIMD-Accelerated BLAKE2b Cryptographic Hash |
| | `lgcorzo/highwayhash` | High-Speed HighwayHash Implementation |
| | `lgcorzo/dchest-siphash` | Fast SipHash Routines |
| **Networking & Middleware** | `lgcorzo/mux` | High-Performance HTTP Request Router |
| | `lgcorzo/certgen` | Zero-Dependency TLS Certificate Generator |
| | `lgcorzo/sio` | Super Encryption IO Primitive for Go Writers/Readers |
| | `lgcorzo/zip` | Streaming ZIP Archive Reader and Writer |
| | `lgcorzo/dsync` | Distributed Mutual Exclusion Synchronization Lock Engine |
| | `lgcorzo/dnscache` | Thread-Safe DNS Resolution Caching Layer |
| | `lgcorzo/event` | Event Notification System Primitives |
| | `lgcorzo/color` | Terminal ANSI Coloring and Formatting Engine |
| | `lgcorzo/parquet-go` | Parquet File Format Processing Utilities |
| **Deployment & Observability** | `lgcorzo/sidekick` | High-Availability Load Balancer & Sidecar Proxy |
| | `lgcorzo/warp` | S3 Performance Benchmarking Suite |
| | `lgcorzo/minio-hs` | MinIO Storage Extensions & Diagnostics Tooling |
| | `lgcorzo/doctor` | Cluster Health Diagnostic & Telemetry Inspector |
| | `lgcorzo/subnet` | Enterprise Support Portal & Diagnostics Integration |
| | `lgcorzo/licverifier` | Cryptographic License Verification Routines |
| **Auxiliary Libraries** | `lgcorzo/aistor-extensions` | Sovereign Extensions for AI Storage Pipelines |
| | `lgcorzo/crypto` | Shared Cryptographic Utility Primitives |
| | `lgcorzo/csv` | Streaming CSV Processing Primitives |
| | `lgcorzo/filepath` | Cross-Platform Path Handling Utilities |
| | `lgcorzo/mountinfo` | OS Mount Point Inspector |
| | `lgcorzo/readpass` | Terminal Password & Secret Masking Helper |
| | `lgcorzo/terminal` | Cross-Platform Terminal Capability Routines |
| | `lgcorzo/wildcard-matching` | Extended String Pattern Evaluation Routines |

---

## Automated CI/CD Maintenance & Compliance Workflow

The diagram below illustrates the automated sovereign CI/CD validation pipeline enforcing security, compliance, and multi-architecture compatibility across `@lgcorzo/pkg`:

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    Dark Gravity CI/CD Automation                        │
└─────────────────────────────────────────────────────────────────────────┘
                                     │
     ┌───────────────────────────────┼───────────────────────────────┐
     ▼                               ▼                               ▼
┌─────────┐                     ┌─────────┐                     ┌─────────┐
│  Build  │                     │ Security│                     │ Compli- │
│ Matrix  │                     │ & Vuln  │                     │  ance   │
└────┬────┘                     └────┬────┘                     └────┬────┘
     │                               │                               │
     ├── Linux (amd64, arm64)        ├── govulncheck                 ├── EU AI Act
     ├── macOS (amd64, arm64)        ├── golangci-lint               ├── SOC 2 Type II
     └── Windows (amd64)             └── race detector               └── ISO 25059
     │                               │                               │
     └───────────────────────────────┼───────────────────────────────┘
                                     │
                                     ▼
                      ┌─────────────────────────────┐
                      │    Sovereign AI Factory     │
                      │   Production Ready Build    │
                      └─────────────────────────────┘
```

---

## Installation & Usage

Import `@lgcorzo/pkg` in your Go project:

```go
import (
	"github.com/lgcorzo/pkg/v3/certs"
	"github.com/lgcorzo/pkg/v3/env"
	"github.com/lgcorzo/pkg/v3/policy"
	"github.com/lgcorzo/pkg/v3/wildcard"
)
```

To run unit tests and linter locally:

```bash
make test
make lint
```

---

## License

Use of `@lgcorzo/pkg` is governed by the GNU AGPLv3 license that can be found in the [LICENSE](LICENSE) file.
