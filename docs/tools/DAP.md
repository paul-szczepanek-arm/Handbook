## DAPLink

DAPlink is an open source project that implements the embedded firmware required for a Cortex debug probe. The project is hosted on GitHub and is published under an Apache 2.0 license, making it attractive for commercial developments.

The software project is complemented by a series of reference designs for creating the DAPLink debug probe hardware, which is available in the <a href="/docs/v5.6/reference/contributing-tools.html#arm-mbed-hdk" target="_blank">HDK documentation</a>.

### DAPLink features

A DAPLink debug probe connects to your host computer through USB and connects to your target system (the one to be programmed and debugged) through a standard <a href="http://infocenter.arm.com/help/topic/com.arm.doc.faqs/attached/13634/cortex_debug_connectors.pdf" target="_blank">Cortex debug connector</a>. It provides three main features - all over a single USB connection.

#### HID interface

The driver-less HID interface provides a channel over which the CMSIS-DAP debug protocol runs. This enables all the leading industry standard toolchains to program and debug the target system.

Supported tools include:

- Keil MDK.
- IAR Workbench.
- pyOCD.

#### USB drag and drop programming

DAPLink debug probes appear on the host computer as a USB disk. Program files in binary (`.bin`) and hex (`.hex`) formats can be copied onto the USB disk, which then programs them into the memory of the target system.

<span class="notes">**Note:** The DAPLink probe needs to contain the programming algorithms specific to the target system. Therefore, the version of the DAPLink firmware you use must match the target system.</span>

### USB serial port

The DAPLink debug probe also provides a USB serial port, which can be bridged through to a TTL UART on the target system.
The USB serial port will appear on a Windows machine as a COM port, or on a Linux machine as a /dev/tty interface.

For more information on configuring your host computer to use this feature, please the <a href="/docs/v5.6/tutorials/windows-serial-driver.html" target="_blank">Windows serial driver information</a>.

### Further reading

- <a href="https://github.com/ARMmbed/DAPLink/blob/master/README.md" target="_blank">The DAPLink GitHub repo</a>.
- <a href="https://os.mbed.com/platforms/SWDAP-LPC11U35" target="_blank">Debug probes built with DAPLink</a>.
