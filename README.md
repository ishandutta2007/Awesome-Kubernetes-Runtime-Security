# Awesome-Kubernetes-Runtime-Security

Top Kubernetes Runtime Security Tools Ecosystem

Curated List of SaaS Products & Open-Source GitHub Projects
Focused on Container Runtime Threat Detection, eBPF Observability, Policy Enforcement & Cloud-Native Security
Last updated: September 2026

This repository tracks notable SaaS platforms and open-source projects for Kubernetes Runtime Security. These tools monitor, detect, and respond to threats inside running containers and Kubernetes clusters using eBPF, kernel modules, and system call analysis.

Examples include Falco, Tigera Calico Cloud, Aqua Security, Sysdig Secure, Kubescape, NeuVector, Cilium Tetragon, ARMO Platform, StackRox, and Prisma Cloud (the category leaders).

Open-source emphasis: This section is heavily expanded with every major active project for self-hosting, custom detection rules, and transparent eBPF-based enforcement — ideal for platform teams, security engineers, and organizations that need deep runtime visibility without vendor lock-in.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

Table of Contents

SaaS/Hosted Platforms

Open-Source GitHub Projects

How to Contribute

Disclaimer

SaaS/Hosted Platforms

Tigera Calico Cloud
Commercial Kubernetes security platform built on Calico. Provides L7 network policy enforcement on an eBPF dataplane, runtime threat detection, and compliance reporting.

Aqua Security
Enterprise CNAPP with the Aqua Enforcer runtime sensor (userspace + kernel-module hybrid). Notable for drift prevention and immutable container policies, with SOC 2 Type II certification. MalwareScan engine catches trojanized base images and crypto-miners.

Sysdig Secure
CNAPP built by the creators of Falco. Deep runtime detection with eBPF instrumentation, syscall-level forensics, and managed Falco rule tuning. FedRAMP Moderate authorized. Runtime detection is the core strength.

ARMO Platform
Commercial platform built around Kubescape. Provides runtime detection and response for Kubernetes workloads with posture management integration.

StackRox
Kubernetes-native security platform (now Red Hat Advanced Cluster Security). Admission policy correlation bundled with OpenShift. Provides runtime threat detection and compliance controls.

Prisma Cloud
Palo Alto Networks' comprehensive CNAPP assembled from Twistlock and RedLock acquisitions. Broad coverage across code, cloud, and runtime. Defender agent supports eBPF mode as default. FedRAMP Moderate authorized.

CrowdStrike Falcon Cloud Security
Extends the Falcon EDR agent to containers and Kubernetes with a single eBPF-first agent. FedRAMP High authorized. Strong threat intelligence integration with MITRE ATT&CK correlation.

SentinelOne Singularity Cloud
eBPF-based runtime sensor with EDR lineage. Covers containers, serverless, and VMs. FedRAMP Moderate authorized.

Wiz Runtime Sensor
eBPF agent paired with Wiz's agentless graph. Provides runtime context for risk prioritization. SOC 2 Type II certified.

Open-Source GitHub Projects

Falco
The CNCF graduated runtime security engine. Monitors syscalls and kernel events for anomalous behavior. Powerful rule language, extensive detection library, and broad community adoption. Detection-only — pair with Falcosidekick or SIEM for alerting. Apache-2.0.

Cilium Tetragon
eBPF-based security observability and runtime enforcement from the Cilium team (now Cisco). Deep kernel visibility with process-level enforcement via bpf_send_signal(). Strong synergy with Cilium networking. Apache-2.0.

KubeArmor
Runtime security enforcement system using LSMs (AppArmor, BPF-LSM) for workload hardening and least-permissive policies. Provides inline prevention — blocks actions before execution. Can defend against library backdoors (e.g., xz/liblzma) via runtime file access control. Apache-2.0.

Tracee
Linux runtime security and forensics using eBPF from Aqua Security. Syscall tracing and Perf event analysis for detecting sophisticated attacks and eBPF-based malware. Apache-2.0.

KubeCop
Runtime detection and response for malicious events in Kubernetes workloads from ARMO. Apache-2.0.

NeuVector
Full lifecycle container security platform (now SUSE Security). Runtime detection with process/file/network behavioral learning. Apache-2.0.

Kubescape
Kubernetes posture management and NSA hardening checks. Open-source posture engine that pairs with commercial ARMO runtime. Apache-2.0.

Additional Strong Open-Source Options

eBPF Observability: Pixie (CNCF sandbox, eBPF-based Kubernetes observability with runtime security use cases), Inspektor Gadget (eBPF-based introspection tooling).

Admission Control: Kyverno (Kubernetes-native policy engine for admission gates), OPA Gatekeeper (Open Policy Agent admission controller).

Container Scanning: Trivy (Aqua's scanner, the upstream for many commercial image scanning features).

Reference Stack: The 2026 reference container security stack pairs Falco or Tetragon for runtime, Kyverno for admission, Trivy for scanning, and Sigstore/Cosign for signing.

Frameworks for building custom systems: Combine Falco for detection rules, Tetragon for enforcement, KubeArmor for inline prevention, and Kubescape for posture. Add Prometheus + Grafana for metrics and Falcosidekick for alert routing.

How to Contribute

Fork the repo.

Add/edit entries in README.md (follow existing format).

Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

Submit PR with a short explanation.

Star the repo if you find it useful!

Disclaimer

This is a community-curated list — not exhaustive and not an endorsement.

Kubernetes runtime security tools require kernel compatibility checks (eBPF vs kernel modules) and careful performance testing in production.

Detection-only tools (Falco, Tracee) do not block attacks — pair with enforcement tools (Tetragon, KubeArmor) for prevention.

Made for platform engineers, Kubernetes operators, security architects, and DevSecOps teams.
Let's make Kubernetes runtime security more open, observable, and enforceable.
