# Installation Troubleshooting

Resolve common installation problems across different platforms.

## Windows Installation Issues

### Installer Won't Run

**Error:** "This app can't run on your PC"

**Solution:**
- Download the correct version (32-bit vs 64-bit)
- Check system requirements
- Run compatibility troubleshooter

### Missing DLL Files

**Error:** "VCRUNTIME140.dll was not found"

**Solution:**
Install Microsoft Visual C++ Redistributable:
1. Download from Microsoft's website
2. Install both x86 and x64 versions
3. Restart computer
4. Retry installation

### Permission Denied Errors

**Solution:**
1. Right-click installer
2. Select "Run as administrator"
3. Click "Yes" on UAC prompt

## macOS Installation Issues

### "App is damaged" Message

**Solution:**
```bash
sudo xattr -r -d com.apple.quarantine /Applications/YourApp.app
```

### Gatekeeper Blocking Installation

**Solution:**
1. System Preferences > Security & Privacy
2. Click lock icon and authenticate
3. Click "Open Anyway" for the app
4. Or temporarily disable Gatekeeper:
   ```bash
   sudo spctl --master-disable
   # Re-enable after install:
   sudo spctl --master-enable
   ```

### Insufficient Privileges

**Solution:**
```bash
sudo chown -R $(whoami) /Applications/YourApp.app
```

## Linux Installation Issues

### Package Dependency Errors

**Ubuntu/Debian:**
```bash
sudo apt --fix-broken install
sudo apt update
sudo apt install -f
```

**Fedora/CentOS:**
```bash
sudo dnf install --allowerasing
```

### Permission Errors During Install

**Solution:**
```bash
sudo chmod +x install.sh
sudo ./install.sh
```

### Library Not Found Errors

**Find missing libraries:**
```bash
ldd /path/to/executable
```

**Install common dependencies:**
```bash
# Ubuntu/Debian
sudo apt install libssl-dev libcurl4-openssl-dev

# Fedora
sudo dnf install openssl-devel libcurl-devel
```

## Network-Related Installation Issues

### Download Fails or Times Out

1. **Check internet connection**
2. **Disable VPN temporarily**
3. **Try different network** (mobile hotspot)
4. **Download via command line:**
   ```bash
   wget -c https://downloads.example.com/installer.exe
   # -c flag resumes interrupted downloads
   ```

### Firewall Blocking Download

1. Temporarily disable firewall
2. Add exception for installer domain
3. Download and re-enable firewall

### Corporate Proxy Issues

Set proxy environment variables:

**Windows:**
```cmd
set HTTP_PROXY=http://proxy.company.com:8080
set HTTPS_PROXY=http://proxy.company.com:8080
```

**Mac/Linux:**
```bash
export HTTP_PROXY=http://proxy.company.com:8080
export HTTPS_PROXY=http://proxy.company.com:8080
```

## Verification Issues

### Installation Completes but App Won't Launch

**Windows:**
1. Check Event Viewer for errors
2. Verify in Programs and Features
3. Reinstall with "Repair" option

**macOS:**
1. Check Console.app for crash logs
2. Verify app in Applications folder
3. Try launching from Terminal:
   ```bash
   /Applications/YourApp.app/Contents/MacOS/YourApp
   ```

**Linux:**
1. Check logs: `journalctl -xe`
2. Verify installation: `which yourapp`
3. Check permissions: `ls -la $(which yourapp)`

### Version Command Doesn't Work

Ensure the application is in your PATH:

**Windows:**
1. Search for "Environment Variables"
2. Edit System PATH
3. Add installation directory
4. Restart terminal

**Mac/Linux:**
Add to `~/.bashrc` or `~/.zshrc`:
```bash
export PATH="/path/to/app:$PATH"
```
Then: `source ~/.bashrc`

## Still Having Issues?

### Collect Diagnostic Information

**Windows:**
```cmd
systeminfo > systeminfo.txt
wmic product where "name like '%YourApp%'" get name,version > installed.txt
```

**macOS:**
```bash
system_profiler SPSoftwareDataType > system.txt
ls -la /Applications/YourApp.app > app_info.txt
```

**Linux:**
```bash
uname -a > system_info.txt
dpkg -l | grep yourapp > package_info.txt  # Debian/Ubuntu
rpm -qa | grep yourapp > package_info.txt  # Fedora/CentOS
```

### Contact Support

Email diagnostics to: install-support@example.com

Include:
- Operating system and version
- Installation method used
- Complete error messages
- Diagnostic files from above
