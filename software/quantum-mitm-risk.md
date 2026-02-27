# Quantum Threat Assessment: MITM Risk vs Cryptographic Defenses

## Expanded Summary Table: Quantum MITM Risk vs Cryptographic Defenses

| System / Cryptosystem                  | Key Size     | Logical Qubits Needed (Shor) | Estimated Attack Time (Optimistic) | Quantum MITM Risk   | Notes                                                                                                               |
|----------------------------------------|--------------|------------------------------|------------------------------------|---------------------|---------------------------------------------------------------------------------------------------------------------|
| **RSA-2048 without PFS**               | 2048 bits    | 4,000–6,000                  | Hours–Days                         | High / indefensible | MITM can capture session now and decrypt later once quantum resources are available.                                |
| **RSA-2048 with PFS (ECDHE)**          | 2048 bits    | 4,000–6,000                  | Hours–Days                         | Low / mitigated     | Ephemeral key exchange ensures captured sessions cannot be decrypted retroactively.                                 |
| **ECC-256 with ECDHE (ephemeral key)** | 256 bits     | 1,500–2,000                  | Hours                              | Low                 | Forward secrecy protects past sessions; ECC key compromise affects future sessions only.                            |
| **AES-256 (symmetric)**                | 256 bits     | N/A (Grover)                 | Decades–Centuries                  | Very Low            | Quantum search via Grover reduces effective key strength to ~128 bits.                                              |
| **One-Time Pad (OTP)**                 | Message size | N/A                          | Infinite                           | Unbreakable         | Theoretically secure if key is truly random, single-use, and as long as message; impractical for most applications. |
| **Post-Quantum Cryptography (PQC)**    | Varies       | N/A                          | Years–Decades                      | Low                 | Lattice-, hash-, or code-based algorithms resistant to Shor/Grover attacks; emerging standards.                     |

---

### Acronyms and Abbreviations

| Acronym / Abbreviation | Full Form                               | Brief Description                                                                                |
|------------------------|-----------------------------------------|--------------------------------------------------------------------------------------------------|
| **RSA**                | Rivest–Shamir–Adleman                   | Public-key cryptography based on integer factorization.                                          |
| **ECC**                | Elliptic Curve Cryptography             | Public-key cryptography using elliptic curves for smaller keys with equivalent security.         |
| **ECDHE**              | Elliptic Curve Diffie–Hellman Ephemeral | Ephemeral ECC-based key exchange; provides PFS.                                                  |
| **PFS**                | Perfect Forward Secrecy                 | Prevents compromise of long-term keys from exposing past sessions.                               |
| **AES**                | Advanced Encryption Standard            | Symmetric encryption algorithm; AES-256 uses 256-bit keys.                                       |
| **OTP**                | One-Time Pad                            | Symmetric encryption using a random key as long as the message; theoretically unbreakable.       |
| **MITM**               | Man-in-the-Middle                       | Interception and possible modification of communication.                                         |
| **Shor**               | Shor’s Algorithm                        | Quantum algorithm for factoring integers and breaking RSA/ECC in polynomial time.                |
| **Grover**             | Grover’s Algorithm                      | Quantum algorithm that reduces brute-force search time; halves symmetric key strength.           |
| **TLS**                | Transport Layer Security                | Protocol securing Internet communications; TLS 1.3 supports PFS and strong symmetric encryption. |
