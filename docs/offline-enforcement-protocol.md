# Internal Reference: Offline Enforcement Protocol

**Owner:** Manar Engineering  
**Scope:** Module 6, Phase 1 Build Plan  
**Target:** Core Inference Host & Local Enclosure Security  

---

## 5.1 Where this sits in established practice

Physical isolation of sensitive systems is not a technique Manar invented. It is the same principle behind how classified government systems and critical infrastructure are protected, formalised in standards such as NIST SP 800 53's boundary protection control and ISO 27001's guidance on network segregation. Three recognised levels of isolation are relevant to how Manar's deployments are built.

**Physical isolation.** No network interface exists at all. The most stringent form, and the target for the core inference host in every deployment.

**Operational isolation.** Interfaces may exist but are controlled through procedure and human intervention, firewalls, monitored access, restricted physical entry. Applied to the enclosure and access controls around the machine.

**Electronic isolation.** A one directional gateway allows data to move in only one direction, commonly implemented as a data diode. Relevant to how Manar handles model updates and new client documents arriving after initial deployment, addressed in 5.4.

---

## 5.2 Physical layer controls

Unused Ethernet ports are physically covered with port blockers or disabled at the BIOS or UEFI level, not merely left unplugged. Wireless radios are physically removed from the board where the hardware allows it. Where physical removal is not practical, the radio is hard blocked through rfkill and disabled at the BIOS or UEFI level as well, so the control exists at two layers rather than one. Cellular or LTE modules are not installed, and are removed during provisioning if a board ships with one.

Tamper evident seals are placed over the chassis and over any port that was disabled rather than removed, with seal numbers logged in the deployment record at handover. Where the hardware supports a chassis lock, the key stays with the client.

The machine is installed inside whatever locked enclosure was agreed during the Site Read, with access logged by the client using whatever access control the site already runs.

Cameras and sensors connect to a dedicated switch with no physical uplink to the client's main network, verified by tracing the actual cable path during installation rather than reading a diagram. A UPS is fitted so a power interruption does not force a reboot at the exact moment a technician on site is tempted to reconnect a cable temporarily.

---

## 5.3 Software and operating system layer controls

The host firewall drops all outbound traffic by default, with only loopback and the specific local subnets the deployment needs permitted. No default gateway is configured on the inference host unless a client has explicitly requested and agreed to a scoped exception.

Offline mode flags are set at the operating system or container level, not only inside application configuration, so a library call attempting to reach a model hub fails immediately rather than trying the network first. Update checks in the inference runtime are disabled, and model files are pulled once, during provisioning at Manar's own facility, never on the client's live network. Container images are pinned by digest rather than a floating tag, so nothing resolves to a fresh pull at runtime.

No functioning DNS resolver is configured on the deployed host, or the resolver points at loopback, so hardcoded hostnames fail closed. Wifi and Bluetooth are hard blocked through rfkill in addition to the physical control in 5.2, the relevant kernel modules are blacklisted, and no saved wireless profiles exist with auto connect disabled. This redundancy is deliberate. A control that exists at both the physical and software layer survives a mistake at either one alone.

Full disk encryption is applied so a drive removed from the machine cannot be read elsewhere. A checksum of every deployed model artifact is recorded at handover, and either the client or Manar during a scheduled visit can recompute the hash and compare it against the manifest.

Every query, retrieval, and answer is logged to a local encrypted volume that belongs to the client, with nothing shipped externally by default. Remote access, if a client specifically wants a monitoring dashboard or support channel, is a separate connection, scoped in writing, never bundled into a deployment by default.

---

## 5.4 Media handling, an addition worth adopting

Air gapped systems generally still need a way to receive updates, new documents, or a retrained model. That transfer point is usually physical media, and it is also the most documented residual risk in isolated systems, since malware can travel on a USB drive as easily as legitimate data.

**Recommended addition to the protocol.** Any USB drive or physical media used to bring new documents or model updates to a deployed machine is scanned first on a separate, dedicated scanning station that is itself never connected to the deployment network, before the media ever touches the client's machine. This is a small procedural addition, costs one extra device per engineering team, and closes the one gap that physical and software controls above do not, since both of those controls assume the network path is the only path in.

---

## 5.5 Verification protocol, run with the client present at handover

1. **Network scan.** The client's own IT staff run a scan from the host's local network segment and confirm no unexpected listening services and no default gateway.
2. **Live disconnect.** While the system is actively serving a query, the uplink is physically removed in front of the client. The system keeps serving.
3. **Firewall review.** The client's IT staff review the egress firewall rules directly on the host.
4. **Artifact check.** Checksums of installed models are recomputed live and compared against the handover manifest.
5. **Sign off.** A short written verification record is signed by both parties and kept by the client, who can rerun this same procedure at any later date without Manar present, since every step uses tools the client's own staff already has.

---

## 5.6 What this protocol does not cover

It does not cover model correctness, only the offline and data boundary property. It does not cover physical building security beyond the machine itself. It assumes the client is not the adversary, and defends against network dependency and passive vendor overreach rather than an actively malicious insider with physical access. High sensitivity sites, banking, government, defence adjacent work, would need additional controls scoped case by case, potentially including a genuine data diode for the update path described in 5.4 rather than the scan and transfer procedure recommended there as a baseline.
