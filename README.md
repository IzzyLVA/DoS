# DoS Stress Tester v4.0

**WARNING: This tool is for testing and educational purposes only. Misuse of this tool for illegal activities may be subject to severe penalties.**

## Overview

The **DoS Stress Tester** is a Python-based tool designed to simulate network traffic to test the resilience of servers within controlled environments, such as your own local network or test lab. It is strictly intended for **ethical and legal use only**.

With the ability to adjust packet sizes, control threads, and limit packets per second (pps), this tool allows users to simulate a controlled stress test on a specified IP address to understand how it performs under heavy traffic conditions.

**IMPORTANT**: This tool must only be used against IP addresses you own or have explicit permission to test. Unauthorized use against public servers is illegal and can result in criminal prosecution.

## Key Features

- **Customizable Packet Sizes**: Choose from multiple packet sizes for stress testing.
- **Thread Control**: Run multiple threads to simulate real-world traffic.
- **Critical Port Prioritization**: Allows the simulation to focus on essential ports (e.g., HTTP, HTTPS, SSH).
- **Auto-Stop Feature**: Automatically stops the test after a predefined duration (e.g., 5 minutes) for safety.
- **Resource Monitoring**: The tool checks your system's CPU usage and adjusts the number of threads if the load is too high.
- **Logging**: Detailed logs for each action taken, including packet counts and system resource status.

## Ethical and Legal Warning

This tool is designed **exclusively for legal and ethical purposes**, such as testing your own servers or systems in a controlled lab environment. **Do not use this tool against unauthorized IP addresses**, websites, or services.

- Ensure that you have explicit written permission to test any system.
- **Unauthorized use** is a violation of computer crime laws, and can result in severe penalties.
- **DO NOT use this tool for malicious purposes** such as causing Denial of Service (DoS) attacks against third-party services.

By using this tool, you agree to take full responsibility for its use and any legal consequences arising from it.

## Installation

To get started with the **DoS Stress Tester**, you'll need to have Python 3 and some dependencies installed.

### Prerequisites

- Python 3.6 or higher
- `psutil` library (for resource monitoring)

### Steps to Install

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/dos-stress-tester.git
    cd dos-stress-tester
    ```

2. Install required dependencies:
    ```bash
    pip install psutil
    ```

3. Ensure your environment is correctly set up to run Python 3 and that `psutil` is installed:
    ```bash
    python3 -m pip show psutil
    ```

4. Once everything is set up, you can run the script directly:
    ```bash
    python3 dos_stress_tester.py
    ```

## Usage

1. **Run the Script**:
   ```bash
   python3 dos_stress_tester.py
2. **Input the Target IP**:

   The script will prompt you to enter the target IP address. Make sure you only target authorized IP addresses (e.g., your own local server or test machine).
  
3. **Confirmation Prompt**:

    You will be asked to confirm that you want to proceed with the stress test. Type CONFIRM to start the test. Otherwise, the test will be canceled.

4. **Monitoring**:

    The script will log the current progress every 5 seconds, including the number of packets sent and the rate (pps).

5. **Automatic Stop**:

    The test will stop after 5 minutes (by default) to ensure that the system is not overwhelmed.

6. **Test Results**:

    After the test is complete, the script will output a summary with the number of packets sent, the duration, and the average packets per second (pps).

## Configuration

You can customize the behavior of the tool by modifying the following variables in the script:

    VERSION: The version number of the tool.

    THREADS: Number of threads to simulate the attack (based on CPU cores).

    PACKET_SIZES: List of packet sizes to simulate. Default values: [64, 128, 512, 1024].

    SKIP_PORTS: Ports to avoid during the attack (e.g., SSDP).

    CRITICAL_PORTS: Ports that are prioritized (e.g., HTTP, HTTPS, SSH).

    MAX_PPS: Max packets per second per thread.

    DURATION_SEC: Duration in seconds before the test auto-stops.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
