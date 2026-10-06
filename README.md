**Embedded systems & hardware security engineer** · PhD, University of Huddersfield (2026)

I build and test low-power embedded systems — firmware, PCBs and the measurements that show whether they really work. My PhD developed hardware-rooted device authentication for LoRaWAN IoT nodes, combining SRAM Physical Unclonable Functions with RF fingerprinting on ARM Cortex-M0+ hardware. Alongside it I build embedded security projects end to end, from bootloader to radio link, each with host-side tests and its evidence kept in the repository.

### What I work with
- **Embedded:** C on ARM Cortex-M (STM32L0, SAMD21) · FreeRTOS (tasks, queues, mutexes, watchdog, tickless idle) · Zephyr RTOS *(in progress)* · SPI / I²C / UART · JTAG/SWD + GDB · CMake / arm-none-eabi-gcc
- **Embedded security:** secure boot (SHA-256, ECDSA P-256, anti-rollback, power-fail-safe updates) · flash write protection and read-out protection · AES-128-CTR / AES-CMAC link security · hardware secure element (ATECC608) · key provisioning and backup
- **Testing:** host-side unit tests · known-answer vectors (FIPS-197, RFC 4493, RFC 6979) · simulated power-cut tests
- **Hardware:** KiCad schematic & PCB layout · board bring-up · oscilloscope validation
- **Wireless & RF:** LoRa/LoRaWAN · BLE *(in progress)* · RTL-SDR capture · carrier-frequency-offset analysis
- **Digital design:** VHDL · Verilog/SystemVerilog *(in progress)* · Intel Quartus · ModelSim
- **Analysis:** Python (NumPy, pandas, scikit-learn, matplotlib)

### Research highlights
- 📄 [Complementary failure modes of SRAM-PUF and RF fingerprinting under compound thermal–distance stress](https://doi.org/10.1016/j.adhoc.2026.104413) — *Ad Hoc Networks* (Elsevier), 2026, open access
- 📊 Open dataset: [Zenodo 10.5281/zenodo.19592147](https://doi.org/10.5281/zenodo.19592147) · [IEEE DataPort 10.21227/fecz-fe94](https://doi.org/10.21227/fecz-fe94)
- 🔬 5,488 validated authentication attempts across 27.4–56.1 °C on a 2×2 cross-platform hardware testbed

### Projects
**Finished**
- 🔐 [**STM32L0 FreeRTOS sensor node with a custom secure bootloader**](https://github.com/baliyu/stm32l0-freertos-sensor-node) — FreeRTOS LoRa node with an AES-CTR/CMAC link and replay protection. Own bootloader that checks an ECDSA P-256 signature, refuses downgrades and installs updates safely (power cut simulated at 1,682 points of an install). Bootloader write-protected, read-out protection Level 1, and a boot-time check that halts if the protection is weakened. Limitations written up honestly.
- 🔑 [**MKR WAN 1310 secure-element LoRa node**](https://github.com/baliyu/mkrwan-secure-element-node) — link keys held in an ATECC608 that never reveals them. AES-CTR and CMAC are built from the chip's single-block AES: byte-identical to my software implementation on 2,000 random packets and accepted by the unchanged receiver. Hardware counter as frame counter, and a comparison with SRAM PUFs.

**In progress**
- 📡 [**Zephyr BLE vibration monitor**](https://github.com/baliyu/zephyr-ble-vibration-monitor) on the Arduino Nano 33 BLE — LSM9DS1 sampling, CMSIS-DSP FFT, secure BLE GATT notifications, ztest unit tests and GitHub Actions CI.

**Planned**
- 🔌 **RTL design & verification** — UART, SPI, CDC async FIFO, cocotb
- 🔐 **MCUboot on Zephyr**, compared with my own bootloader

### Contact
📫 baliyu70@gmail.com · [LinkedIn](https://www.linkedin.com/in/bello-aliyu-phd-827462111)
