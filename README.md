# CSP4CMSIS on STM32 (NUCLEO-F401RE)

This repository contains a complete **STM32CubeIDE project** that demonstrates how to integrate the **CSP4CMSIS** C++ communication library with **FreeRTOS** on an **STM32 Nucleo-F401RE** board. The project shows a simple example of communicating between tasks using channels and is intended as a starting point for embedded real-time systems.

---

## 🧰 Requirements

Before building and running this project, make sure you have the following:

### Hardware
- **STM32 Nucleo-F401RE** development board
- USB cable (connect the board to your PC)

### Software
- **STM32CubeIDE**  
  Download and install from ST’s official site:  
  https://www.st.com/en/development-tools/stm32cubeide.html
- A serial console program (optional), e.g.:
  - `minicom`, `screen`, `picocom` on Linux
  - PuTTY, Tera Term on Windows

---

## 📁 Repository Structure
# CSP4CMSIS on STM32 (NUCLEO-F401RE)

This repository contains a complete **STM32CubeIDE project** that demonstrates how to integrate the **CSP4CMSIS** C++ communication library with **FreeRTOS** on an **STM32 Nucleo-F401RE** board. The project shows a simple example of communicating between tasks using channels and is intended as a starting point for embedded real-time systems.

---

## 🧰 Requirements

Before building and running this project, make sure you have the following:

### Hardware
- **STM32 Nucleo-F401RE** development board
- USB cable (connect the board to your PC)

### Software
- **STM32CubeIDE**  
  Download and install from ST’s official site:  
  https://www.st.com/en/development-tools/stm32cubeide.html
- A serial console program (optional), e.g.:
  - `minicom`, `screen`, `picocom` on Linux
  - PuTTY, Tera Term on Windows

---

## 📁 Repository Structure

├── Core/ # Main application code
├── Drivers/ # STM32 HAL and CMSIS drivers
├── Middlewares/ # FreeRTOS middleware
├── lib/
│ └── CSP4CMSIS/ # CSP4CMSIS library (source + headers)
├── Startup/ # Startup assembly
├── *.ioc # CubeMX configuration file
├── *.ld # Linker scripts
├── README.md # This file
└── LICENSE


- The **CSP4CMSIS library** is included in `lib/CSP4CMSIS/`.  
- Hardware and RTOS configuration is stored in the `.ioc` file.

---

## 🚀 Getting Started

### Import the project in STM32CubeIDE

1. Open **STM32CubeIDE**.
2. Go to **File → Import → Existing Projects into Workspace**.
3. Select the folder where this repository is stored.
4. Click **Finish**.

You should now see the project in **Project Explorer**.

---

## 🔧 Configure and Generate Code

1. In the Project Explorer, open the `.ioc` file by **double-clicking** it.
2. The CubeMX GUI will open inside STM32CubeIDE.
3. You can inspect:
   - Pin settings
   - Clock configuration
   - FreeRTOS settings
4. Once you’ve reviewed settings, click **Project → Generate Code**.

This ensures any changes are correctly reflected in the build.

---

## 🛠️ Build the Project

To compile the project:

1. Select the project in the Project Explorer.
2. Click the **Hammer icon** (Build Project).
3. The build output appears in the **Console** tab.

On success, a `Debug/` folder will be created with object files and the final ELF.

---

## 🔥 Flash and Run

1. Connect the **NUCLEO-F401RE** board via USB.
2. Click the **Debug** or **Run** button in STM32CubeIDE.
3. The firmware will be programmed via the on-board ST-LINK.

---

## 💬 View Output (Optional)

If your application prints messages (e.g., using `printf`), you can view them on a serial terminal.

Example using **minicom** on Linux:

```bash
sudo minicom -D /dev/ttyACM0 -b 115200


