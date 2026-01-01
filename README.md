# Security-of-IoT-and-Edge-Communication-in-the-Quantum-Era:
Security of IoT and Edge Communication in the Quantum Era: Threat Models, Assumptions, and Viable Defenses
Internet of Things (IoT) and edge communication systems form the backbone of modern cyber–physical infrastructure, enabling large-scale sensing, control, and autonomous decision-making under strict resource constraints. The security of these systems currently relies on classical public-key cryptographic primitives whose hardness assumptions are threatened by the emergence of large-scale quantum computation. Unlike traditional security transitions, the quantum threat introduces a temporal asymmetry: data encrypted today may remain vulnerable to retrospective decryption once quantum adversaries mature. This “store-now, decrypt-later” paradigm is particularly critical for IoT and edge systems, where devices are long-lived, computationally constrained, and often deployed in hostile or unattended environments. The central problem addressed in this work is to determine how quantum-capable adversaries fundamentally alter the security assumptions of IoT and edge communication systems, and to identify which classes of cryptographic defenses remain viable under realistic system and adversary constraints.

# Capabilities of adversaries:
We assume an adversary with the following capabilities:
1.Quantum computational power:
Access to fault-tolerant quantum computers capable of executing Shor’s algorithm, enabling polynomial-time factorization and discrete logarithm computation, thereby breaking RSA, Diffie–Hellman, and elliptic-curve cryptography.
2.Data harvesting and long-term storage:
Ability to passively collect encrypted communication today with the intention of decrypting it in the future once sufficient quantum resources become available.
3.Network-level control:
Capability to perform classical attacks such as man-in-the-middle, replay, traffic analysis, and packet injection over public or semi-trusted networks.
4.Device proximity (optional):
In some deployments, physical proximity to IoT devices, enabling side-channel observation or device compromise.

# Adversary Limitations:
1.We explicitly limit the adversary 
2.No assumption of perfect, noise-free quantum hardware
3.Limited access to quantum communication infrastructure
4.No universal physical access to all devices
5.Bounded energy, time, and economic cost

## Security Assumptions
This work operates under the following system and trust assumptions:
1. IoT devices are resource-constrained in terms of computation, memory, and energy, and cannot sustain continuous public-key operations.
2. Edge nodes possess moderate computational resources and can act as cryptographic anchors but are not assumed to be fully trusted.
3. Classical authenticated channels may exist during initial bootstrapping but cannot be assumed to remain secure long-term.
4. Quantum communication links are scarce and cannot be ubiquitously deployed across all IoT devices.
5. Security mechanisms must satisfy latency and reliability constraints imposed by uRLLC and mMTC traffic.

## Attack Surface in Quantum-Adversarial IoT Systems
Under the defined adversary model, IoT and edge communication systems are exposed to the following attack surfaces:
1. Cryptographic compromise of long-term keys due to Shor-enabled attacks.
2. Temporal replay of cryptographically valid but contextually stale messages.
3. Session linkability and metadata leakage through traffic analysis.
4. Device impersonation following delayed key recovery.
5. Control-plane manipulation in edge-assisted coordination loops.

