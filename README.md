# Auto_Tor_IP_changer V 2.1
This is a handy, open-source tool that automatically changes your IP address at regular intervals using the Tor network. It's perfect for anyone who wants to stay anonymous online or avoid tracking. By routing your internet traffic through Tor, you can browse the web with a fresh IP address every few seconds or minutes, depending on your settings.


To install the **Auto_Tor_IP_changer** tool, follow these steps:

---

### 1. **Install Dependencies**
First, ensure that the required dependencies are installed:

```bash
sudo apt-get update
sudo apt-get install tor -y
pip3 install requests[socks]
```

---

### 2. **Clone the Repository**
Clone the GitHub repository to your local system:

```bash
git clone https://github.com/FDX100/Auto_Tor_IP_changer.git
cd Auto_Tor_IP_changer
```

---

### 3. **Run the Install Script**
Run the installation script with **root permissions** since it needs to write to system directories (`/usr/bin` and `/usr/share`):

```bash
sudo python3 install.py
```

This step will:
- Create necessary directories.
- Copy the script to `/usr/share/aut`.
- Create a command shortcut `aut` in `/usr/bin`.

---

### 4. **Verify Installation**
After the installation is complete, you can check if the tool is installed properly by typing:

```bash
aut
```

If the command executes, the tool has been installed successfully.

---

### 5. **Use the Tool**
To use the tool:
1. Open the terminal and type:
   ```bash
   aut
   ```
2. The tool will prompt you for:
   - **Time interval** (e.g., how often the IP should change).
   - **Number of times** to change the IP (e.g., 5 times, or `0` for infinite changes).

3. Configure your browser or system proxy to use `127.0.0.1:9050` as the SOCKS proxy:
   - For most browsers, go to **Network Settings** > **Proxy Configuration**.
   - Set the SOCKS proxy host to `127.0.0.1` and port to `9050`.

4. Once configured, your traffic will automatically route through the TOR network, and the IP will change as per the specified schedule.
