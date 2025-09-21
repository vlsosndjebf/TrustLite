Project Name

TrustLite: A Lightweight Trusted Execution Environment for Microwatt

Project Overview

TrustLite aims to enhance the Microwatt open-source POWER core with a lightweight trusted execution environment (TEE). The project integrates a minimal set of hardware security extensions — including secure boot, AES-128 encryption engine, and a simplified memory protection unit (MPU) — to allow execution of sensitive workloads in an isolated and protected context.

Unlike heavyweight security frameworks, TrustLite is designed to remain compact and resource-efficient, making it suitable for IoT, edge computing, and low-power environments where both performance and silicon area are constrained.

Proposal

Secure Boot Support

Add a hardware root of trust mechanism.

On reset, Microwatt verifies a digital signature or hash of the bootloader before execution.

Ensures the CPU always starts in a trusted state.

AES-128 Hardware Engine

Dedicated module to accelerate symmetric encryption and decryption.

Reduces CPU cycles for cryptographic operations and improves energy efficiency.

Verilog/VHDL implementation with test vectors for correctness validation.

Memory Protection Unit (MPU)

Provide region-based access control for program and data memory.

Prevents unauthorized access by restricting execution and read/write permissions.

Lightweight alternative to a full MMU, suitable for embedded use cases.

Integration with Microwatt

Modules connected through Microwatt’s memory interface and control signals.

Expose new control registers for TEE configuration (e.g., enable secure boot, configure MPU regions).

Maintain compatibility with existing toolchains and software workflows.
