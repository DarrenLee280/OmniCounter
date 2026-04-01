# Omni Counter 🔢

A professional-grade, multi-game tracking system designed for TCG and digital strategy enthusiasts. Whether tracking Life in **Magic: The Gathering**, points in **Riftbound**, or Lore in **Lorcana**, this project provides a high-reliability hardware and firmware solution for competitive play.

---

## 📁 Project Structure

This repository is organized into distinct domains to ensure scalability and ease of manufacturing.

*   **`/firmware`**: The PlatformIO project containing all microcontroller source code.
*   **`/hardware`**: Physical design files including PCB layouts and 3D-printable enclosures.
*   **`/docs`**: Datasheets, schematics (PDF), and high-level project information.

---

## 🛠️ Getting Started

### Prerequisites
*   **Operating System**: Fedora (Linux)
*   **IDE**: [Visual Studio Code](https://visualstudio.com)
*   **Extension**: [PlatformIO IDE](https://visualstudio.com)

### Firmware Setup
1.  Open VS Code and select **File > Open Folder...**
2.  Navigate to and select the `firmware/` directory specifically.
3.  PlatformIO will automatically detect the `platformio.ini` and begin indexing.
4.  Connect your Arduino via USB.
5.  Click the **Upload** (→) icon in the bottom status bar.

---

## 🏗️ Hardware Design

The physical components are managed within the `/hardware` folder:
*   **Schematics**: Located in `/hardware/schematics/`.
*   **PCB Layout**: Design files found in `/hardware/pcb/`.
*   **Mechanical**: 3D models (STEP/STL) located in `/hardware/mechanical/`.
*   **BOM**: A full Bill of Materials is available in `/hardware/bom/` for parts ordering.

---

## 🚀 Usage

Once the firmware is flashed and the hardware is assembled:
1.  Power the device via USB or external 5V supply.
2.  [Add specific operation instructions here, e.g., "Press the primary button to increment."]
3.  Data is output via Serial at `115200` baud.

---

## 🛠️ Troubleshooting (Fedora/Linux)

*   **Permission Denied (Serial)**: If you cannot upload to the Arduino on Fedora, add your user to the dialout group:
    ```bash
    sudo usermod -a -G dialout $USER
    ```
    *(Note: You must log out and back in for this to take effect).*
*   **Broken Build**: Ensure you are opening the `firmware/` folder directly in VS Code, not the root `OmniCounter/` folder.

---

## 📝 License
This project is licensed under the [MIT License](LICENSE).
