## Introduction 

This capstone project investigates secure network coding techniques for 5G wireless communications. It addresses the growing security challenges brought by 4G, 5G, and upcoming 6G networks including eavesdropping, DoS attacks, MITM, and network slice theft. 
The project proposes integrating forward error correction (FEC) coding with physical-layer security to simultaneously improve transmission reliability, efficiency, and confidentiality in NOMA-based wireless systems. Performance is assessed using Bit Error Rate (BER) and throughput as key metrics across varying SNR conditions.

## Technologies used 

1) Mathlab
2) NOMA (Non-Orthogonal Multiple Access)
3) Reed-Solomon Coding
4) Convolutional Coding
5) QPSK Modulation
6) Rayleigh Fading Channel + AWGN
7) Artifical Noise Injection
8) Dynamic Power Allocation
9) Successive Interference Cancellation

## Features 

- Dual coding scheme comparison — RS-coded NOMA vs. Convolutional-coded NOMA vs. uncoded (baseline) NOMA
- Physical-layer security via artificial noise injection (5% transmit power)
- Channel-aware dynamic power allocation to ensure user fairness and decoding reliability
- Secure NOMA transmission that improves both BER and throughput simultaneously
- Monte Carlo simulation with 300 frames per SNR point for statistical reliability
- SNR range 0–30 dB coverage to model low to high quality channel conditions
- SIC at receiver for accurate signal separation of superimposed user signals

## Project Process

1) Literature Review (Capstone 1) — Studied the evolution of wireless networks (0G–6G), their architectures, security vulnerabilities, coding schemes, and measurement tools
2) System Design — Selected NOMA with RS and Convolutional codes; designed block diagrams for uncoded, Convolutional-coded, and RS-coded NOMA systems
3) MATLAB Simulation (Capstone 2) — Implemented and ran all four system configurations (uncoded NOMA, Conv-coded NOMA, RS-coded NOMA, and their secure variants)
4) Performance Evaluation — Measured BER and throughput across SNR levels; compared proposed schemes against each other and conventional NOMA
5) Benchmarking — Compared proposed designs against existing literature (LDPC, Polar, Turbo codes)
6) Final Selection — Reed-Solomon coded NOMA with security enhancements selected as the best-performing design

## What I've learned from this project

- How NOMA enables multiple users to share the same spectrum, improving spectral efficiency in 5G
- How error correction coding (RS and Convolutional) significantly reduces BER, especially under noisy channel conditions
- The trade-offs between reliability (BER/throughput) and security overhead (artificial noise, added complexity)
- Why RS codes outperform Convolutional codes in burst-error environments — RS uses symbol-level correction, which handles grouped errors better
- How physical-layer security (AN injection) can protect transmissions without traditional encryption, complementing higher-layer security
- Practical workflow for simulating wireless communication systems in MATLAB using tools like Monte Carlo simulation, Rayleigh channel modelling, and SIC decoding

## What can be improved

- Simulation environment — currently assumes ideal channel knowledge (perfect CSI); real-world impairments like synchronization errors, Doppler shifts, and channel estimation inaccuracies are not modelled
- Security model — no active eavesdropper is simulated; a proper adversarial model would give more realistic security evaluation
- Channel variety — only Rayleigh fading is used; Rician or Nakagami-m models would better represent indoor/urban environments
- Coding scheme breadth — LDPC and Polar codes (state-of-the-art for 5G NR) were not tested; including them would provide a more comprehensive comparison
- Multi-user scalability — the system only models two-user downlink NOMA; extending to more users would test real-world applicability
- Hardware validation — MATLAB simulation cannot replace real-time hardware testing; SDR (Software-Defined Radio) implementation would validate practical performance
- Complexity and latency — real-time processing constraints and embedded hardware limitations were not considered

## Results

<img width="1686" height="767" alt="image" src="https://github.com/user-attachments/assets/21ac99fa-7226-42ef-965a-12f298b64f47" />

<img width="1694" height="764" alt="image" src="https://github.com/user-attachments/assets/ecd8dfd2-beb7-412e-adf5-db2971f32701" />

<img width="1732" height="757" alt="image" src="https://github.com/user-attachments/assets/5803b320-dca5-4f9b-bc20-3ff9eaa8f244" />

