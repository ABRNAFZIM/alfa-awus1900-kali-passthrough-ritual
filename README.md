# alfa-awus1900-kali-passthrough-ritual
A step-by-step guide to successfully connecting the Alfa AWUS1900 USB Wi-Fi adapter to Kali Linux running in VirtualBox. After extensive troubleshooting, I discovered a simple but powerful method that finally worked. 
# Alfa AWUS1900 Passthrough Ritual (VirtualBox + Kali Linux)

This guide documents a reliable method for connecting the Alfa AWUS1900 USB Wi-Fi adapter to Kali Linux running in VirtualBox. After extensive troubleshooting, the final solution was surprisingly simple—and deeply symbolic.

## 🛠️ Steps

1. **Connect the Alfa AWUS1900** before launching VirtualBox.
2. Open **VirtualBox** → Select Kali VM → **Settings**.
3. Go to **USB**:
   - Enable USB Controller (preferably USB 3.0).
   - Add the Alfa AWUS1900 to the USB Device Filters.
4. Go to **Network**:
   - Change from **NAT** to **Bridged Adapter**.
   - Under **Name**, select any network interface *except* the Alfa AWUS1900.
5. Save settings.
6. **Unplug** the Alfa AWUS1900.
7. Start Kali VM → Log in.
8. **Reconnect** the Alfa AWUS1900.
9. Confirm detection via `lsusb`, `ip a`, or `iwconfig`.

## 🪄 Symbolic Reflection

> The Alfa awakens not through brute force, but through sequence and intention.  
> This ritual is a reminder: sometimes the key is not in the config file, but in the rhythm of connection.

## 🔍 Diagnostics

You can verify the adapter with:

```bash
lsusb | grep Realtek
ip a
iwconfig
