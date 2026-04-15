# CyberRange Environment Calibration Tool (v2.4.1)

## Overview
This utility is designed to ensure that the local laboratory environment meets the 
minimum requirements for the assigned challenges. It performs low-level checks 
on CPU floating-point consistency, memory allocation latency, and I/O throughput.

## Package Contents
- `client.c`: Source code for the validation logic (provided for audit purposes).
- `check_env`: Pre-compiled static binary for Linux x64 systems.

## Why use the pre-compiled binary?
To ensure consistent results across different Linux distributions (Ubuntu, Debian, CentOS), 
the `check_env` binary has been statically compiled against glibc. This avoids 
common "library not found" errors and ensures that the calibration metrics are 
standardized for all participants.

## Quick Start
1. Ensure the binary has execution permissions:
   $ chmod +x check_env

2. Run the calibration:
   $ ./check_env

3. Wait for the "SHA-256 (Environment): PASSED" message before starting 
   your coding task.

## Technical Specifications
- Architecture: x86_64 (Linux)
- Compilation: GCC 11.4.0 -static -O2
- Expected Runtime: < 5 seconds

