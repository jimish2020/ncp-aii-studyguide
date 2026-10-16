# NCP-AII Learner Study Guide · References

TeslaTuring Bookstore · Engineering Knowledge for the AI Era. · buy@teslaturing.com | +971 58 587 6262

Section-specific sources for every chapter of the NCP-AII Learner Study Guide (final edition). A citation such as [S2] in a chapter refers to entry S2 under that chapter below. Each entry gives the address, what the chapter used it for, the version read, the access date and the evidence status. VERIFIED in the book means documentation checked, not executed.

Address of this document: https://github.com/jimish2020/ncp-aii-studyguide/blob/main/NCP-AII_ref

## Contents

- Chapter 01 · How to study and assess readiness
- Chapter 02 · Linux operational foundations
- Chapter 03 · Networking and storage foundations
- Chapter 04 · GPU and AI infrastructure architecture
- Chapter 05 · Deployment sequence and acceptance
- Chapter 06 · Management access and platform trust
- Chapter 07 · Physical installation, power, cooling and cabling
- Chapter 08 · Firmware and hardware validation
- Chapter 09 · Initial storage integration
- Chapter 10 · BlueField and DOCA concepts
- Chapter 11 · MIG
- Chapter 12 · OS and driver lifecycle
- Chapter 13 · BCM, provisioning and HA
- Chapter 14 · Slurm, Enroot and Pyxis
- Chapter 15 · GPU containers and NGC
- Chapter 16 · Diagnostics, stress and test planning
- Chapter 17 · HPL
- Chapter 18 · NCCL and interconnect validation
- Chapter 19 · Fabric, cable and firmware evidence
- Chapter 20 · ClusterKit
- Chapter 21 · NeMo workload validation
- Chapter 22 · Storage testing
- Chapter 23 · Fault isolation and replacement decisions
- Chapter 24 · Server and storage optimisation
- Chapter 25 · Integrated acceptance and incident cases
- Chapter 26 · Exam preparation, practice and remediation

## Chapter 01 · How to study and assess readiness

**S1** · NVIDIA NCP-AII certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Credential description, exam details, prerequisites, validity (§1.1, Table 1.1)  
Version: Page published 2026-08-07 · Accessed: 2026-10-08 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA-Certified Professional: AI Infrastructure Exam Study Guide  
https://dam-cdn.nvd.orangelogic.com/AssetLink/8gauup66xn2gv80pu4m166li0bhyytk4.pdf  
Used for: Job description, domains, weights, objectives, optional training, suggested readings (§1.2–§1.5, Tables 1.2–1.3)  
Version: Revision SEP25 (document 3770919) · Accessed: 2026-10-08 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 02 · Linux operational foundations

**S1** · journalctl(1) manual page · systemd  
https://www.freedesktop.org/software/systemd/man/latest/journalctl.html  
Used for: -b, -k, -p, -u, --since/--until; -k -b -1 example (§2.4, Table 2.1)  
Version: systemd man page, latest; Debian testing copy also consulted · Accessed: 2026-10-08 · Status: PARTIAL CHECK (official page excerpt) · FULL READING PENDING · NOT EXECUTED

**S2** · lspci(8) Linux manual page · pciutils  
https://man7.org/linux/man-pages/man8/lspci.8.html  
Used for: -t, -v, -vv, -vvv, -k (§2.3, §2.5, Table 2.2)  
Version: man7.org copy · Accessed: 2026-10-08 · Status: PARTIAL CHECK (official page excerpt) · FULL READING PENDING · NOT EXECUTED

**S3** · numactl(8) Linux manual page  
https://man7.org/linux/man-pages/man8/numactl.8.html  
Used for: --hardware, --show (policy of the current process), --cpunodebind, --membind (allocation fails if the nodes cannot satisfy it), --preferred; policy inheritance by children (§2.6)  
Version: man7.org copy of the numactl project manual; whole page read 2026-10-13 · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S4** · NVIDIA System Management Interface (nvidia-smi) documentation  
https://docs.nvidia.com/deploy/nvidia-smi/index.html  
Used for: Persistence mode, return codes, Xid/ECC events, PCI and link information, replays, topo -C/-M, GPU identification (§2.2–§2.6)  
Version: Driver version not stated on page · Accessed: 2026-10-08 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S5** · NVIDIA GPUDirect RDMA documentation · Using nvidia-peermem  
https://docs.nvidia.com/cuda/gpudirect-rdma/index.html  
Used for: nvidia-peermem purpose, loading, install order with MLNX_OFED (§2.3)  
Version: CUDA 13.4 docs, updated 2026-09-13 · Accessed: 2026-10-08 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S6** · AMD Instinct GPU cluster networking · Single-node network configuration  
https://instinct.docs.amd.com/projects/gpu-cluster-networking/en/latest/how-to/single-node-config.html  
Used for: LnkCap as maximum supported, LnkSta as current status (§2.5)  
Version: Latest online · Accessed: 2026-10-08 · Status: PARTIAL CHECK (official page excerpt) · FULL READING PENDING · NOT EXECUTED

**S7** · NVIDIA Driver Installation Guide · Optional Components (Using nvidia-peermem; Automatic rebuild of nvidia-peermem)  
https://docs.nvidia.com/datacenter/tesla/driver-installation-guide/latest/optional-components.html  
Used for: Stub build without OFED; rebuild when OFED changes; DKMS BUILD_DEPENDS automatic rebuild (§2.3, Table 2.1a)  
Version: Latest web edition, updated 2026-09-23 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S8** · NVIDIA Driver Persistence · Data Persistence (GPU Initialization Lifecycle; Kernel Driver Lifecycle) and Persistence Daemon  
https://docs.nvidia.com/deploy/driver-persistence/data-persistence.html  
Used for: GPU initialisation lifetime separate from kernel-driver lifetime; persistence daemon recommended, persistence mode legacy (§2.2)  
Version: Web page, last updated 2026-09-09 · relevant sections read · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 03 · Networking and storage foundations

**S1** · NVIDIA DGX H100/H200 User Guide · Introduction  
https://docs.nvidia.com/dgx/dgxh100-user-guide/introduction-to-dgxh100.html  
Used for: Adapter link-layer defaults and speeds; the Table 1 vs Table 5 storage-default conflict (archive PDF p10 / printed p4 and PDF p18 / printed p12); OS and cache storage, cachefilesd, supported cables, port mapping, DensiLink (§3.3–§3.5, §3.10)  
Version: Page last updated 2026-01-26; archive copy dgxh100-user-guide.pdf at commit 844088e (SHA-256 582b174e…492c) · Accessed: 2026-10-08 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA DGX SuperPOD H100 Reference Architecture · Network Fabrics  
https://docs.nvidia.com/dgx-superpod/reference-architecture-scalable-infrastructure-h100/latest/network-fabrics.html  
Used for: In-band and OOB Ethernet, storage fabric, > 40 GBps per-node I/O, 4:3 oversubscription, two-port transceiver (§3.1, §3.5, §3.6, §3.10)  
Version: Page last updated 2025-11-19 · Accessed: 2026-10-08 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S3** · NVIDIA DOCA SDK Documentation v3.5.0 · RDMA over Converged Ethernet  
https://networking-docs.nvidia.com/doca/archive/3-5-0/rdma-over-converged-ethernet  
Used for: Key Considerations (no SM, LID 0, RoCE counters); RoCE Modes (v1 Ethertype 0x8915, v2 UDP 4791); RoCE Lossless Ethernet Configuration (flow control, PFC on all endpoints and switches) (§3.2–§3.4)  
Version: DOCA 3.5.0 · page last updated 2026-09-01 · Accessed: 2026-10-11 · Status: FULL RELEVANT SECTIONS READ · NOT EXECUTED

**S4** · NVIDIA UFM documentation · Diagnostic Tools  
https://docs.nvidia.com/networking/display/ufmsdnappumv41814/diagnostic-tools  
Used for: ibstat/ibstatus fields: LID, SM LID, port state, link width, physical state (§3.3)  
Version: UFM SDN appliance 4.18.14 docs · Accessed: 2026-10-08 · Status: PARTIAL CHECK (official page excerpt) · FULL READING PENDING · NOT EXECUTED

**S5** · NVIDIA GPUDirect RDMA documentation · Using nvidia-peermem  
https://docs.nvidia.com/cuda/gpudirect-rdma/index.html  
Used for: nvidia-peermem with InfiniBand and RoCE, ConnectX-3 or newer (§3.2)  
Version: CUDA 13.4 docs, updated 2026-09-13 · Accessed: 2026-10-08 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S6** · NVIDIA DOCA SDK Documentation v3.5.0 · Congestion Control Infrastructure › DCQCN CC Algorithm  
https://networking-docs.nvidia.com/doca/archive/3-5-0/dcqcn-cc-algorithm  
Used for: ECN marking at the switch, CNP from the receiving NIC, rate reduction at the sender; the release lists DCQCN and ZTR-RTT algorithm pages (§3.4)  
Version: DOCA 3.5.0 · page last updated 2026-10-02 · Accessed: 2026-10-11 · Status: FULL RELEVANT SECTION READ (DCQCN page); ZTR-RTT page title only · NOT EXECUTED

**S7** · NVIDIA Cumulus Linux 5.12 User Guide · RDMA over Converged Ethernet (RoCE)  
https://docs.nvidia.com/networking-ethernet-software/cumulus-linux-512/Layer-1-and-Switch-Ports/Quality-of-Service/RDMA-over-Converged-Ethernet-RoCE/  
Used for: Lossless mode (PFC and ECN) and lossy mode (PFC disabled, ECN) for RoCE on Cumulus switches; default RoCE configuration (§3.4, Table 3.2)  
Version: Cumulus Linux 5.12 web page (the fetched page's canonical link names the 5.9 edition; mode descriptions to be re-checked per release) · Accessed: 2026-10-13 · Status: RELEVANT SECTIONS READ · NOT EXECUTED

**S8** · NVIDIA MLNX-OS User Manual 3.12.6300 LTS · IB Router  
https://networking-docs.nvidia.com/mlnxosum/3.12.6300lts/ib-router  
Used for: InfiniBand routing between subnets is a separate router function with its own configuration on supported switches (Table 3.2)  
Version: MLNX-OS 3.12.6300 LTS · Accessed: 2026-10-13 · Status: PARTIAL CHECK (search excerpt) · FULL READING PENDING · NOT EXECUTED


## Chapter 04 · GPU and AI infrastructure architecture

**S1** · NVIDIA DGX H100/H200 User Guide · Introduction to NVIDIA DGX H100/H200 Systems  
https://docs.nvidia.com/dgx/dgxh100-user-guide/introduction-to-dgxh100.html  
Used for: Component table, power and PSU behaviour, BMC interfaces, network port and module mapping (Table 4.1, §4.2, §4.5, §4.11)  
Version: Page last updated 2026-01-26 · Accessed: 2026-10-08 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA System Management Interface (nvidia-smi) documentation  
https://docs.nvidia.com/deploy/nvidia-smi/index.html  
Used for: topo -m legend, nvlink --status and -e, output compatibility and N/A behaviour (Table 4.4, §4.4, Table 4.9)  
Version: Driver version not stated on page · Accessed: 2026-10-08 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S3** · NVIDIA GPUDirect RDMA documentation · Overview and Design Considerations  
https://docs.nvidia.com/cuda/gpudirect-rdma/index.html  
Used for: Direct PCIe path, memory registration, synchronisation, path quality by topology (§4.2, §4.3, §4.4)  
Version: CUDA 13.4 docs, updated 2026-09-13 · Accessed: 2026-10-08 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S4** · NVIDIA DGX SuperPOD H100 Reference Architecture · Network Fabrics  
https://docs.nvidia.com/dgx-superpod/reference-architecture-scalable-infrastructure-h100/latest/network-fabrics.html  
Used for: Four fabrics, rail alignment, SU component counts, storage oversubscription, OOB scope (§4.5–§4.7)  
Version: Page last updated 2025-11-19 · Accessed: 2026-10-08 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S5** · NVIDIA NCP-AII certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Published domain weighting (§4.1)  
Version: Page published 2026-08-07 · Accessed: 2026-10-08 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S6** · Overview of NCCL · NCCL documentation  
https://docs.nvidia.com/deeplearning/nccl/user-guide/docs/overview.html  
Used for: Collective operations, supported transports (§4.1, §4.3, terms)  
Version: NCCL 2.32.3 docs · full page checked by the Review 1 reviewer · Accessed: 2026-10-08 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S7** · Upgrading Multi-GPU Interconnectivity with the Third-Generation NVIDIA NVSwitch (Eassa, Ishii, Wells) · NVIDIA Technical Blog  
https://developer.nvidia.com/blog/upgrading-multi-gpu-interconnectivity-with-the-third-generation-nvidia-nvswitch/  
Used for: 900 GB/s bidirectional per GPU; 3.6 TB/s bisection and 450 GB/s reduction bandwidth for eight H100 GPUs (§4.2)  
Version: Published 2022-08-23, modified 2024-05-15 · vendor technical article, not a product specification · Accessed: 2026-10-09 · Status: FULL ARTICLE READ · NOT EXECUTED

**S8** · NVIDIA DCGM Documentation · Learn › Core Services › Topology and NVLink  
https://docs.nvidia.com/datacenter/dcgm/latest/learn/core-services/topology-and-links.html  
Used for: Read GPU Topology: topology does not predict performance, prove links active or measure bandwidth; Inspect Current Link State: point-in-time; Compare NVLink Error Counters: cumulative, compare before and after (§4.4, §4.9)  
Version: DCGM 4.6 (Latest) · page last updated 2026-09-10 · live page; not taken from the repository archive and not merged with the repository's DCGM 4.7-scope archive copy · Accessed: 2026-10-11 · Status: FULL RELEVANT SECTIONS READ · NOT EXECUTED

**S9** · NCCL 2.32.3 User Guide · Collective Operations (AllReduce)  
https://docs.nvidia.com/deeplearning/nccl/user-guide/docs/usage/collectives.html  
Used for: All-reduce reduces inputs across ranks and places the result in every rank's receive buffer (§4.1, Fig 4.1, Q1)  
Version: NCCL 2.32.3 docs · AllReduce section read · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 05 · Deployment sequence and acceptance

**S1** · NVIDIA DGX SuperPOD: Next Generation Scalable Infrastructure for AI Leadership, Reference Architecture featuring DGX H100 · Network Fabrics  
https://docs.nvidia.com/dgx-superpod/reference-architecture-scalable-infrastructure-h100/latest/network-fabrics.html  
Used for: Four fabrics; build the fabric for the full SU; 32-position SU with 31 DGX nodes; Table 4 counts (§5.2, §5.7, Q8)  
Version: Web edition, last updated 2025-11-19 · FULL (page) · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA DGX SuperPOD Deployment Guide featuring NVIDIA DGX A100 and DGX H100 Systems, DG-11251-001 V15 (BCM 10.24.09)  
https://docs.nvidia.com/dgx-superpod/index.html  
Used for: Physical installation and switch configuration before BCM; site survey; P2P template; chapter order; final validation step (§5.1–§5.5)  
Version: V15, 2024-09-26 · read from the source archive (CR-00-03 local copy, TEMD007-DG11251001-DSPAH100-DeploymentGuide.pdf) · PARTIAL: §1–3 and §8 read, §4–7 headings and selected steps · current web edition not compared · Accessed: 2026-10-09 · Status: PARTIAL · NOT EXECUTED

**S3** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective 1.1 wording: Describe sequence of events for deployment and validation; study guide link unchanged  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S4** · NVIDIA DGX H100/H200 User Guide · Introduction to NVIDIA DGX H100/H200 Systems  
https://docs.nvidia.com/dgx/dgxh100-user-guide/introduction-to-dgxh100.html  
Used for: Compute port to GPU mapping referenced in the scenario (§5.7; Ch 04 Fig 4.6)  
Version: Web edition, last updated 2026-01-26 · FULL (page) · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 06 · Management access and platform trust

**S1** · NVIDIA DGX H100/H200 User Guide · Connecting to DGX H100/H200  
https://docs.nvidia.com/dgx/dgxh100-user-guide/connect-dgx.html  
Used for: Direct console limits; BMC security practices; credentials before and after First Boot Setup; KVM launch; SSH to the OS; Docker 172.17 overlap (§6.1, §6.2, §6.4, §6.8)  
Version: Web edition, last updated 2026-01-26 · FULL (page) · Accessed: 2026-10-12 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA DGX H100/H200 User Guide · Using the Baseboard Management Controller (BMC)  
https://docs.nvidia.com/dgx/dgxh100-user-guide/bmc.html  
Used for: Main controls (Table 8); open ports; static IP via ipmitool and SBIOS; credential rules; remote console; directory services; event filters; SSL certificates; SBIOS CA enrolment (§6.2–§6.5, §6.11)  
Version: Web edition, last updated 2026-01-26 · FULL (page) · Accessed: 2026-10-12 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S3** · NVIDIA DGX H100/H200 User Guide · Security  
https://docs.nvidia.com/dgx/dgxh100-user-guide/security.html  
Used for: Dedicated BMC port; dedicated firewalled management network; VPN for remote access; Secure Flash; firmware encryption (§6.2, §6.6)  
Version: Web edition, last updated 2026-01-26 · FULL (page) · Accessed: 2026-10-12 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S4** · NVIDIA DGX H100/H200 User Guide · Redfish APIs Support  
https://docs.nvidia.com/dgx/dgxh100-user-guide/redfish-api-supp.html  
Used for: Redfish scope, methods, DSP0266 1.7.0; IPMI users on Redfish; 169.254.0.17 host link; account, reset, firmware, BIOS, boot order, PK, telemetry, SEL paging, backup, diagnostics examples (§6.2–§6.6)  
Version: Web edition, last updated 2026-01-26 · FULL (page) · Accessed: 2026-10-12 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S5** · NVIDIA DGX H100/H200 User Guide · SBIOS Settings  
https://docs.nvidia.com/dgx/dgxh100-user-guide/sbios-settings.html  
Used for: Change only documented SBIOS settings; TPM enablement and TPM clearing listed as occasions (procedures not on this page); boot menu; SOL access (§6.6)  
Version: Web edition, last updated 2026-01-26 · FULL (page) · Accessed: 2026-10-12 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S6** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective 1.3 wording: Perform initial configuration of BMC, OOB, and TPM  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 07 · Physical installation, power, cooling and cabling

**S1** · NVIDIA DGX H100/H200 User Guide · Introduction to NVIDIA DGX H100/H200 Systems  
https://docs.nvidia.com/dgx/dgxh100-user-guide/introduction-to-dgxh100.html  
Used for: Components, mechanical, power and environmental specifications; PSU redundancy rules; locking cords; port map and network modules; supported cables (§7.1, §7.4–§7.8)  
Version: User Guide web edition, last updated 2026-01-26 · FULL (page) · Accessed: 2026-10-12 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA DGX H100/H200 User Guide · Safety  
https://docs.nvidia.com/dgx/dgxh100-user-guide/safety.html  
Used for: Qualified persons; site selection; handling; electrical and system-access warnings; rack-mount warnings; ESD; cooling and airflow; controlled-access room (§7.2, §7.3, §7.5)  
Version: User Guide web edition, last updated 2026-01-26 · FULL (page) · Accessed: 2026-10-12 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S3** · NVIDIA DGX H100/H200 User Guide · Managing Power Capping  
https://docs.nvidia.com/dgx/dgxh100-user-guide/power-capping.html  
Used for: Three GPU power-limit sources; N+N needs power capping; default since 24.07.1; raw IPMI defects (§7.4)  
Version: User Guide web edition, last updated 2026-01-26 · FULL (page) · Accessed: 2026-10-12 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S4** · NVIDIA DGX H100/H200 Service Manual · Introduction  
https://docs.nvidia.com/dgx/dgxh100-service-manual/introduction.html  
Used for: Customer-replaceable components; RMA through Enterprise Support; recommended tools; hearing protection; support for installing or moving (§7.2, §7.3, §7.8)  
Version: Service Manual web edition, last updated 2026-09-13 · FULL (page) · Accessed: 2026-10-12 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S5** · NVIDIA DGX H100/H200 Service Manual · Power Supply Replacement  
https://docs.nvidia.com/dgx/dgxh100-service-manual/psu-replacement.html  
Used for: PSU identification; same manufacturer; four working PSUs; full capacity with four; 30-second limit; post-checks (§7.4, §7.5, §7.11)  
Version: Service Manual web edition, last updated 2026-09-13 · FULL (page) · Accessed: 2026-10-12 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S6** · NVIDIA DGX H100/H200 Service Manual · Rack Mount Kit Replacement  
https://docs.nvidia.com/dgx/dgxh100-service-manual/rack-mount-kit.html  
Used for: Shelf-type kit; 29–35 in post spacing; prongs, clips, cage-nut template, screws; C-channel posts (§7.3)  
Version: Service Manual web edition, last updated 2026-09-13 · FULL (page) · Accessed: 2026-10-12 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S7** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective wording 1.5, 1.6, 1.8, 1.9  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 08 · Firmware and hardware validation

**S1** · NVIDIA DGX H100/H200 Firmware Update Guide · About Firmware Updates  
https://docs.nvidia.com/dgx/dgxh100-fw-update-guide/about.html  
Used for: Updatable components by tray; OOB and host methods; activation types (§8.1, §8.3)  
Version: Firmware Update Guide web edition, last updated 2026-09-13 · FULL (page) · Accessed: 2026-10-12 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA DGX H100/H200 Firmware Update Guide · Firmware Update Steps  
https://docs.nvidia.com/dgx/dgxh100-fw-update-guide/sequence.html  
Used for: Preconditions; upgrade path; durations; sequence; CommitImage; AC power cycle; mlxfwmanager and bridge device; TPM and NVMe minimums (§8.1, §8.3, §8.8)  
Version: Firmware Update Guide web edition, last updated 2026-09-13 · FULL (page) · Accessed: 2026-10-12 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S3** · NVIDIA DGX H100/H200 Firmware Update Guide · Viewing the Installed Firmware and Package Versions  
https://docs.nvidia.com/dgx/dgxh100-fw-update-guide/view-fw-components-packages.html  
Used for: show_version usage and example; InfoROM rows not updatable OOB (§8.2)  
Version: Firmware Update Guide web edition, last updated 2026-09-13 · FULL (page) · Accessed: 2026-10-12 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S4** · NVIDIA DCGM Documentation · Diagnostics  
https://docs.nvidia.com/datacenter/dcgm/latest/learn/modules/dcgm-diagnostics.html  
Used for: Diagnostics versus health; suites and uses; plugins; invasive warning; scope limits; exit status; evidence to keep (§8.5, §8.6)  
Version: DCGM 4.6 documentation, last updated 2026-09-10 · FULL (page) · Accessed: 2026-10-12 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S5** · NVIDIA DCGM Documentation · Topology and NVLink  
https://docs.nvidia.com/datacenter/dcgm/latest/learn/core-services/topology-and-links.html  
Used for: Topology versus link status; U/D/X/_ states; cumulative error counters; DCGM observes, does not configure the fabric (§8.4, §8.8)  
Version: Last updated 2026-09-10 · read from archive copy sources/dcgm-topology-nvlink.pdf (text extract) · FULL · Accessed: 2026-10-12 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S6** · NVIDIA DGX H100/H200 User Guide · Redfish APIs Support  
https://docs.nvidia.com/dgx/dgxh100-user-guide/redfish-api-supp.html  
Used for: Firmware inventory endpoint; ForceUpdate (§8.2, §8.3)  
Version: User Guide web edition, last updated 2026-01-26 · FULL (page) · Accessed: 2026-10-12 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S7** · NVIDIA DGX H100/H200 Service Manual · Introduction (Running the Pre-flight Test)  
https://docs.nvidia.com/dgx/dgxh100-service-manual/introduction.html  
Used for: nvsm stress-test recommendation and duration; nvsm show health (§8.6)  
Version: Service Manual web edition, last updated 2026-09-13 · FULL (page) · Accessed: 2026-10-12 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S8** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective wording 1.4, 1.7, 1.10  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 09 · Initial storage integration

**S1** · NVIDIA DGX OS 6 User Guide · System Configurations (Data Storage Configuration)  
https://docs.nvidia.com/dgx/dgx-os-6-user-guide/system_configurations.html  
Used for: Data drives for caching; NFS for long-term data; cachefilesd; fstab example and fsc rule; ping, mount, FSC=yes; RAID 0 loss on drive failure; RAID level change erases data; lsblk TYPE (§9.1, §9.3, §9.5, §9.11)  
Version: Web edition, last updated 2026-09-14 · FULL (page) · Accessed: 2026-10-12 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA DGX OS 6 User Guide · Reimaging the System  
https://docs.nvidia.com/dgx/dgx-os-6-user-guide/reimaging.html  
Used for: Install DGX OS option repartitions all drives including data drives (§9.1)  
Version: Web edition · PARTIAL (search excerpt only; page not opened) · Accessed: 2026-10-12 · Status: PARTIAL · NOT EXECUTED

**S3** · NVIDIA DGX H100/H200 User Guide · Introduction to NVIDIA DGX H100/H200 Systems  
https://docs.nvidia.com/dgx/dgxh100-user-guide/introduction-to-dgxh100.html  
Used for: OS and data-cache drive configuration; storage ConnectX-7 cards (§9.1, §9.2, §9.11)  
Version: User Guide web edition, last updated 2026-01-26 · FULL (page) · Accessed: 2026-10-12 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S4** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective 1.11 wording: Configure initial parameters for third-party storage  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 10 · BlueField and DOCA concepts

**S1** · NVIDIA DOCA 3.5.0 · BlueField Modes of Operation  
https://networking-docs.nvidia.com/doca/archive/3-5-0/bluefield-modes-of-operation  
Used for: Modes and defaults; NIC Mode properties; DPU Mode data path, initialisation, InfiniBand tools; Zero Trust restrictions; reading and changing mode; activation; unsupported transitions; Separated Host Mode (§10.2–§10.4, §10.7)  
Version: DOCA 3.5.0 documentation, page last updated 2026-09-18 · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA DOCA 3.5.0 · DOCA Installation Guide for Linux  
https://networking-docs.nvidia.com/doca/archive/3-5-0/doca-installation-guide-for-linux  
Used for: Host-first order; BF-Bundle installation and upgrade methods (§10.1, §10.5, §10.6)  
Version: DOCA 3.5.0 documentation, page last updated 2026-09-01 · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S3** · NVIDIA DOCA 3.5.0 · DOCA Profiles  
https://networking-docs.nvidia.com/doca/archive/3-5-0/doca-profiles  
Used for: Profile list, contents, recommendations, device-capability limit, OS support (§10.5, Table 10.3)  
Version: DOCA 3.5.0 documentation, page last updated 2026-09-01 · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S4** · NVIDIA DOCA 3.5.0 · BF-Bundle Installation and Upgrade  
https://networking-docs.nvidia.com/doca/archive/3-5-0/bf-bundle-installation-and-upgrade  
Used for: BFB overwrite and firmware update; bfb-install, bf.cfg, RShim log, ready check, bf-info, tmfifo_net0; standard-tools route and validation note; activation rules; ATX power; DOCA Installer; secure boot (§10.4–§10.8, §10.11)  
Version: DOCA 3.5.0 documentation, page last updated 2026-09-01 · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S5** · NVIDIA DOCA · DOCA-Host Installation and Upgrade  
https://docs.nvidia.com/doca/sdk/doca-host-installation-and-upgrade/index.html  
Used for: Local repo then profile; firmware updater; DKMS ≥ 3.2 on RPM; upgrade from 2.5.x vs 2.6.0+ (§10.6)  
Version: Live page; DOCA 3.3.0–3.4.0 excerpts · Accessed: 2026-10-13 · Status: PARTIAL (search excerpt only) · NOT EXECUTED

**S6** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective wording 2.1 and 3.4  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 11 · MIG

**S1** · NVIDIA Multi-Instance GPU User Guide, Release 615 (PDF)  
https://docs.nvidia.com/datacenter/tesla/pdf/MIG_User_Guide.pdf  
Used for: Supported GPUs; concepts; GI/CI; concurrency comparison; deployment and application considerations; device names and CUDA_VISIBLE_DEVICES; enable MIG, Hopper vs Ampere reset and persistence; driver clients; -lgip, -lgipp, -cgi, -C, -cci, -dci, -dgi; persistence and mig-parted; MPS; containers; Kubernetes and Slurm versions; capabilities (§11.1–§11.9)  
Version: Release 615 · project resources copy, sections read · FULL for those sections · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA MIG User Guide · Supported MIG Profiles  
https://docs.nvidia.com/datacenter/tesla/mig-user-guide/latest/supported-mig-profiles.html  
Used for: H100 80GB, 94GB, 96GB and H200 141GB profile names, fractions, copy engines and instance counts (§11.3, Table 11.2)  
Version: Live page, last updated 2026-09-11 · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S3** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective wording 2.2  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 12 · OS and driver lifecycle

**S1** · NVIDIA Driver Installation Guide · Ubuntu  
https://docs.nvidia.com/datacenter/tesla/driver-installation-guide/ubuntu.html  
Used for: Ubuntu releases covered; headers; local and network repositories; pinning packages and 590 renaming; nvidia-open; compute-only; reboot; upgrades (§12.1–§12.6)  
Version: NVIDIA Driver Installation Guide, pages last updated 2026-09-23 · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA Driver Installation Guide · Post-installation Actions  
https://docs.nvidia.com/datacenter/tesla/driver-installation-guide/post-installation-actions.html  
Used for: Manual post-installation actions; nvidia-persistenced; /proc version; local repository removal (§12.3, §12.5)  
Version: NVIDIA Driver Installation Guide, pages last updated 2026-09-23 · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S3** · NVIDIA Driver Installation Guide · Removing the Driver  
https://docs.nvidia.com/datacenter/tesla/driver-installation-guide/removing-the-driver.html  
Used for: Per-distribution removal commands; Fabric Manager and IMEX in the removal list; Azure Linux note (§12.4, §12.7)  
Version: NVIDIA Driver Installation Guide, pages last updated 2026-09-23 · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S4** · NVIDIA DOCA · DOCA-Host Installation and Upgrade  
https://docs.nvidia.com/doca/sdk/doca-host-installation-and-upgrade/index.html  
Used for: Uninstall older stacks; signing and secure boot; headers; repo and profile install; mlnx-fw-updater; openibd and mst restart; doca-kernel-support; upgrade from 2.5.x vs 2.6.0+ (§12.2, §12.8)  
Version: Project-resources PDF copy (20 pages); DOCA version on the page not recorded · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S5** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective wording 3.2 and 3.4  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 13 · BCM, provisioning and HA

**S1** · NVIDIA Base Command Manager 11 · Administrator Manual  
https://docs.nvidia.com/base-command-manager/  
Used for: Concepts §2.1; PXE, iPXE, PXE menu and node-installer §5.1–§5.2; node states §5.5; cm-wlm-setup §7.3; HA concepts, cmha-setup, cmha status, makeactive and Slurm takeover §15 (§13.1–§13.9)  
Version: Revision d9f2901, dated 2026-10-08 · project-resources PDF; link is the BCM documentation landing page, not opened · PARTIAL (sections listed above) · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective wording 3.1, 3.2 and 3.3  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 14 · Slurm, Enroot and Pyxis

**S1** · NVIDIA Pyxis · README (GitHub)  
https://github.com/NVIDIA/pyxis  
Used for: SPANK plugin role; benefits; Enroot requirement; Slurm 21.08 compile coupling; install with make, deb, rpm; plugstack link; options; srun and sbatch examples; # escaping (§14.4–§14.7)  
Version: main branch README · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · Slurm · Generic Resource (GRES) Scheduling  
https://slurm.schedmd.com/gres.html  
Used for: AutoDetect=nvml and nvidia; Gres= still required; NVML requirement; MIG and NVLink detection limit (§14.2–§14.3)  
Version: Live page; search excerpt only · Accessed: 2026-10-13 · Status: PARTIAL (search excerpt) · NOT EXECUTED

**S3** · Slurm · gres.conf manual page  
https://slurm.schedmd.com/gres.conf.html  
Used for: AutoDetect option list (Table 14.1)  
Version: Live page; search excerpt only · Accessed: 2026-10-13 · Status: PARTIAL (search excerpt) · NOT EXECUTED

**S4** · NVIDIA Base Command Manager 11 · Administrator Manual  
https://docs.nvidia.com/base-command-manager/  
Used for: cm-wlm-setup and Pyxis options; Slurm packaged with BCM; HA takeover (§14.1, §14.5)  
Version: Revision d9f2901 · project-resources PDF · PARTIAL (see Ch 13) · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S5** · NVIDIA Multi-Instance GPU User Guide, Release 615  
https://docs.nvidia.com/datacenter/tesla/pdf/MIG_User_Guide.pdf  
Used for: Slurm MIG support from 21.08; Hopper persistence; NCCL limit (§14.3)  
Version: Release 615 · project-resources PDF · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S6** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective wording 3.3  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 15 · GPU containers and NGC

**S1** · NVIDIA Container Toolkit · Installing the NVIDIA Container Toolkit  
https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html  
Used for: Prerequisites; cgroup known issue; repository and pinned packages (1.20.0-1); nvidia-ctk config; Docker, rootless and containerd configuration (§15.1–§15.3, §15.6)  
Version: Project-resources PDF of the live page; URL inferred from the page title, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA Container Toolkit · Running a Sample Workload  
https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/sample-workload.html  
Used for: Docker and Podman sample workloads (§15.4)  
Version: Project-resources PDF of the live page; URL inferred from the page title, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S3** · NVIDIA Container Toolkit · Specialized Configurations with Docker  
https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/docker-specialized.html  
Used for: Environment variables and nvidia-container-cli; --gpus; NVIDIA_VISIBLE_DEVICES values; device quoting (§15.1, §15.4)  
Version: Project-resources PDF of the live page; URL inferred from the page title, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S4** · NGC CLI · Getting Started with the NGC CLI  
https://docs.ngc.nvidia.com/cli/index.html  
Used for: Installer location; ngc config set; API key; organization and team; output formats; tracing variable; ngc -h (§15.5)  
Version: Project-resources PDF of the live page; URL inferred from the page title, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S5** · NGC CLI · registry  
https://docs.ngc.nvidia.com/cli/cmd_registry.html  
Used for: Registry command groups and --org/--team (§15.5)  
Version: Project-resources PDF; URL inferred, not opened · PARTIAL (image subcommands not in the copy) · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S6** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective wording 3.5, 3.6, 3.7  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 16 · Diagnostics, stress and test planning

**S1** · NVIDIA DCGM Documentation · Diagnostics  
https://docs.nvidia.com/datacenter/dcgm/latest/user-guide/dcgm-diagnostics.html  
Used for: Purpose, run levels, plugin table, preparation, environment, exit status, configuration precedence, limits (§16.1–§16.6)  
Version: Project-resources PDF, page dated 2026-09-10; URL inferred from the page title, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA DCGM Documentation · Health Monitoring  
https://docs.nvidia.com/datacenter/dcgm/latest/user-guide/feature-overview.html  
Used for: Passive watches, flags, Healthy meaning, operational windows, offline diagnostics for RMA (§16.1, §16.4, §16.6)  
Version: Project-resources PDF, page dated 2026-09-10; URL inferred, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S3** · NVIDIA DCGM Documentation · Multi-Node Diagnostics  
https://docs.nvidia.com/datacenter/dcgm/latest/user-guide/dcgm-diagnostics.html  
Used for: Boundary of single-node testing; taught in Chapter 18  
Version: Project-resources PDF, page dated 2026-09-10; URL inferred, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S4** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective wording 4.1  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 17 · HPL

**S1** · NVIDIA HPC Benchmarks · NVIDIA HPL Benchmark  
https://docs.nvidia.com/nvidia-hpc-benchmarks/HPL_benchmark.html  
Used for: Package layout, ignored parameters, hpl.sh parameters, DGX H100 affinity, one GPU per rank, srun example, runtime and OOC variables (§17.2–§17.5)  
Version: Live page, no version shown · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA HPC Benchmarks overview and NGC catalog entry  
https://docs.nvidia.com/nvidia-hpc-benchmarks  
Used for: What HPL solves; the four benchmarks; container distribution (§17.1, §17.3)  
Version: Search-result excerpts only · PARTIAL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S3** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective wording 4.2, 4.12  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 18 · NCCL and interconnect validation

**S1** · NVIDIA/nccl-tests · doc/PERFORMANCE.md  
https://github.com/NVIDIA/nccl-tests/blob/master/doc/PERFORMANCE.md  
Used for: Time, algbw, busbw, correction factors, bottleneck (§18.1, §18.3)  
Version: master branch, commit not recorded · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA DCGM Documentation · Multi-Node Diagnostics  
https://docs.nvidia.com/datacenter/dcgm/latest/user-guide/dcgm-diagnostics.html  
Used for: NCCL definition; control, launch and data paths; mndiag workloads; no thresholds (§18.1, §18.4)  
Version: Project-resources PDF, page dated 2026-09-10; URL inferred, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S3** · NVIDIA DCGM Documentation · Health Monitoring  
https://docs.nvidia.com/datacenter/dcgm/latest/user-guide/feature-overview.html  
Used for: NVLink and NVSwitch failure conditions (§18.3)  
Version: Project-resources PDF, page dated 2026-09-10; URL inferred, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S4** · nccl-tests README and provider NCCL test page (search excerpts)  
https://github.com/NVIDIA/nccl-tests  
Used for: all_reduce_perf flags, output columns, mixed-fabric busbw caution (§18.2, §18.3)  
Version: Search-result excerpts only · PARTIAL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S5** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective wording 4.3, 4.10, 4.11  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 19 · Fabric, cable and firmware evidence

**S1** · NVIDIA Firmware Tools (MFT) · mlxcables – Cables Tool  
https://docs.nvidia.com/networking/display/mftv4220/mlxcables+-+cables+tool  
Used for: Capabilities, synopsis, SFF pages, query, DDM, registers, dump (§19.2, §19.3, §19.5)  
Version: MFT 4.22.0, page updated 2021-06-16; URL inferred from page title, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA Firmware Tools (MFT) · Cable Firmware Upgrade with Live-Patch  
https://docs.nvidia.com/networking/display/mftv4220/cable+firmware+upgrade+with+live-patch  
Used for: ISFU prerequisite and update flow (§19.3, §19.5)  
Version: MFT 4.22.0, page updated 2019-09-18; URL inferred, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S3** · NVIDIA Firmware Tools (MFT) · mlxfwmanager – Firmware Update and Query Tool  
https://docs.nvidia.com/networking/display/mftv4220/mlxfwmanager+-+firmware+update+and+query+tool  
Used for: Scope, query forms, output fields, --clear-semaphore caution (§19.4–§19.6)  
Version: MFT 4.22.0, page updated 2026-02-08; URL inferred, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S4** · NVIDIA Firmware Tools (MFT) · Querying the Firmware Image  
https://docs.nvidia.com/networking/display/mftv4220/querying+the+firmware+image  
Used for: flint query forms, security and secure-boot attributes, update method (§19.4)  
Version: MFT 4.22.0, page updated 2021-06-17; URL inferred, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S5** · NVIDIA DCGM Documentation · Health Monitoring  
https://docs.nvidia.com/datacenter/dcgm/latest/user-guide/feature-overview.html  
Used for: ConnectX health conditions (§19.2)  
Version: Project-resources PDF, page dated 2026-09-10; URL inferred, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S6** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective wording 4.4–4.8  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 20 · ClusterKit

**S1** · NVIDIA HPC-X Software Toolkit · ClusterKit  
https://docs.nvidia.com/networking/display/hpcxv2210/clusterkit  
Used for: Test groups and requirements (§20.1, §20.2)  
Version: HPC-X 2.21.0, page updated 2024-10-15 · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA HPC-X Software Toolkit · Running ClusterKit  
https://networking-docs.nvidia.com/hpcxum/2210/running-clusterkit  
Used for: Node selection, options, pairwise logic, tolerances, modes, scopes, oversubscription, stress (§20.2–§20.5)  
Version: HPC-X 2.21.0, page updated 2024-11-04 · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S3** · InfiniBand Cluster Bring-up Procedure · Performance Testing  
https://docs.nvidia.com/networking/display/infinibandclusterbringupprocedure/performance+testing  
Used for: ClusterKit recommended for IB end-to-end validation; preparation steps (§20.1, §20.2)  
Version: Search-result excerpt only · PARTIAL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S4** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective wording 4.9  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 21 · NeMo workload validation

**S1** · NVIDIA/dgxc-benchmarking · DGX Cloud Benchmarking performance recipes (README)  
https://github.com/NVIDIA/dgxc-benchmarking  
Used for: Slurm prerequisites, H100 workload table, DGX H100 RA baselines (§21.2)  
Version: Search-result excerpt only · PARTIAL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · Megatron Bridge · Performance summary  
https://docs.nvidia.com/nemo/megatron-bridge/latest/performance-summary.html  
Used for: Per-GPU metrics and configuration columns (§21.2, §21.3)  
Version: Search-result excerpt only · PARTIAL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S3** · NVIDIA DCGM Documentation · Multi-Node Diagnostics  
https://docs.nvidia.com/datacenter/dcgm/latest/user-guide/dcgm-diagnostics.html  
Used for: Combined compute-communication load; scope of a pass (§21.1)  
Version: Project-resources PDF, page dated 2026-09-10; URL inferred, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S4** · NVIDIA DCGM Documentation · Health Monitoring  
https://docs.nvidia.com/datacenter/dcgm/latest/user-guide/feature-overview.html  
Used for: Health evidence before and after runs (§21.3–§21.5)  
Version: Project-resources PDF, page dated 2026-09-10; URL inferred, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S5** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective wording 4.13  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 22 · Storage testing

**S1** · NVIDIA GPUDirect Storage · Benchmarking and Configuration Guide  
https://docs.nvidia.com/gpudirect-storage/configuration-guide/index.html  
Used for: GDS data path; guide scope; PCIe affinity; gdsio (§22.3, §22.4)  
Version: v1.16 contents; search-result excerpt only · PARTIAL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA GPUDirect Storage · Installation and Troubleshooting Guide  
https://docs.nvidia.com/gpudirect-storage/troubleshooting-guide/index.html  
Used for: gdsio purpose, cuFile, GDS vs CPU comparison, example output (§22.3, §22.4)  
Version: Search-result excerpt only · PARTIAL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S3** · NVIDIA Technical Blog · Choosing the Right Storage for Enterprise AI Workloads  
https://developer.nvidia.com/blog/choosing-the-right-storage-for-enterprise-ai-workloads/  
Used for: Bandwidth, IOPS, latency per app; no one-size-fits-all; storage class differences (§22.1, §22.5)  
Version: Post dated 2022-07-21; project-resources PDF; URL inferred, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S4** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective wording 4.14  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 23 · Fault isolation and replacement decisions

**S1** · NVIDIA DGX H100/H200 Service Manual · Introduction, Power Supply Replacement, Front Fan Module Replacement  
https://docs.nvidia.com/dgx/dgxh100-service-manual/introduction.html  
Used for: CRU list, RMA, tools, pre-flight test; PSU and fan identification and replacement (§23.4–§23.7)  
Version: Live pages, last updated 2026-09-13 · FULL for the three pages · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA System Management (NVSM) User Guide  
https://docs.nvidia.com/dgx/nvsm/index.html  
Used for: Services, commands, health, dump health, GPU roll-up, alert actions, stress test (§23.2, §23.3, §23.6)  
Version: Release 25.03, dated 2026-07-13; project-resources PDF; URL inferred, not opened · sections read · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S3** · NVIDIA DCGM Documentation · Debugging and Troubleshooting  
https://docs.nvidia.com/datacenter/dcgm/latest/user-guide/dcgm-troubleshooting.html  
Used for: Problem-report items, journal, debug logging (§23.3)  
Version: Project-resources PDF, page dated 2026-09-10; URL inferred, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S4** · NVIDIA DCGM Documentation · Health Monitoring  
https://docs.nvidia.com/datacenter/dcgm/latest/user-guide/feature-overview.html  
Used for: Offline diagnostics required for RMA (§23.3)  
Version: Project-resources PDF, page dated 2026-09-10; URL inferred, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S5** · NVIDIA DGX H100/H200 User Guide · Safety  
https://docs.nvidia.com/dgx/dgxh100-user-guide/safety.html  
Used for: PSU and hot-plug safety (§23.4)  
Version: Search-result excerpt only · PARTIAL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S6** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective wording 5.1, 5.2, 5.3  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 24 · Server and storage optimisation

**S1** · NVIDIA-Certified Systems Configuration Guide  
https://docs.nvidia.com/certification-programs/nvidia-certified-configuration-guide/index.html  
Used for: GPU, CPU, memory, PCIe, topology, NIC and storage recommendations (§24.1, §24.5)  
Version: Project-resources PDF, updated 2026-09-30; URL inferred, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · AMD · BIOS & Workload Tuning Guide for AMD EPYC 9004 (Publication 58011)  
https://docs.amd.com/api/khub/documents/goX~9ubv8i5r60A_Qrp3Rw/content  
Used for: NPS values and interleave; NPS=0; LLC as NUMA (§24.2)  
Version: Search-result excerpt only · PARTIAL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S3** · AMD · Linux Network Tuning Guide for AMD EPYC 9004 (Publication 58012 rev 1.5)  
https://docs.amd.com/api/khub/documents/ScFqtjHuoA5CBw6e~hb01Q/content  
Used for: NPS default, LLC as NUMA for NIC tuning, NPS=2 for latency, determinism (§24.2)  
Version: Search-result excerpt only · PARTIAL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S4** · AMD · HPC Linux Network Tuning Guide for AMD EPYC 7003  
https://docs.amd.com/api/khub/documents/C4jRQ~IJbgFXMY7_n0n4ZQ/content  
Used for: P-states and APBDIS for high-bandwidth adapters (§24.2)  
Version: Search-result excerpt only · PARTIAL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S5** · AMD · HPC Tuning Guide for AMD EPYC 9004 (Publication 58002)  
https://docs.amd.com/api/khub/documents/NgOfoW49HKdzztTeLBbekA/content  
Used for: iommu=pt recommendation (§24.2)  
Version: Search-result excerpt only · PARTIAL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S6** · Intel · HPC Cluster Tuning on 3rd Generation Intel Xeon Scalable Processors  
https://www.intel.com/content/www/us/en/developer/articles/guide/hpc-cluster-tuning-on-3rd-generation-xeon.html  
Used for: SNC, IMC interleave, power and C-state recommendations (§24.3)  
Version: Search-result excerpt only · PARTIAL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S7** · Intel · Ethernet Fabric Performance Tuning Guide rev 1.0  
https://cdrdv2-public.intel.com/632488/632488_Intel%20Ethernet%20Fabric%20Performance%20Tuning%20Guide_v1.0.pdf  
Used for: Contrasting BIOS recommendations, SNC disabled (§24.3)  
Version: February 2021; search-result excerpt only · PARTIAL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S8** · NVIDIA Technical Blog · Choosing the Right Storage for Enterprise AI Workloads  
https://developer.nvidia.com/blog/choosing-the-right-storage-for-enterprise-ai-workloads/  
Used for: Bandwidth, IOPS, latency per application (§24.5)  
Version: Post dated 2022-07-21; project-resources PDF; URL inferred, not opened · FULL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S9** · NVIDIA GPUDirect Storage · Benchmarking and Configuration Guide  
https://docs.nvidia.com/gpudirect-storage/configuration-guide/index.html  
Used for: PCIe device affinity for storage (§24.5)  
Version: v1.16 contents; search-result excerpt only · PARTIAL · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S10** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective wording 5.4, 5.5  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 25 · Integrated acceptance and incident cases

**S1** · Sources of Chapters 13, 15 and 16–24  
Used for: Tool behaviour used in Cases 1–4 and Table 25.2  
Version: See each chapter's source list · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Objective wording  
Version: Page dated 2026-08-07 · FULL · Accessed: 2026-10-09 · Status: DOCUMENTATION CHECKED · NOT EXECUTED


## Chapter 26 · Exam preparation, practice and remediation

**S1** · NVIDIA-Certified Professional: AI Infrastructure (NCP-AII) certification page  
https://www.nvidia.com/en-us/learn/certification/ai-infrastructure-professional/  
Used for: Duration, question count, delivery (§26.2)  
Version: Page published 2026-08-07 · Accessed: 2026-10-08 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S2** · NVIDIA-Certified Professional: AI Infrastructure Exam Study Guide  
https://dam-cdn.nvd.orangelogic.com/AssetLink/8gauup66xn2gv80pu4m166li0bhyytk4.pdf  
Used for: Domains, weights and objectives (Tables 26.1, 26.4)  
Version: Revision SEP25 · Accessed: 2026-10-08 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

**S3** · Sources of Chapters 04–24  
Used for: Technical content of form questions, cited per question by chapter  
Version: See each chapter's source list · Accessed: 2026-10-13 · Status: DOCUMENTATION CHECKED · NOT EXECUTED

