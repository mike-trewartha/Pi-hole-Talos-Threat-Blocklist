# Pi-hole Talos Threat Blocklist

## Overview
This blocklist is automatically updated daily with **malicious domains** publicly provided by **Cisco Talos** over the past 12 months. By using this list with **Pi-hole**, you can enhance your home network security by blocking known threats.

## Features
- 🛡 **Daily Updates**: Checks for new Indicators of Compromise (IOCs) daily.
- 🔄 **Rolling 12-Month Window**: Removes domains older than 12 months.
- 🚀 **Lightweight & Effective**: Specifically tailored for Pi-hole.
- 🔗 **Cisco Talos Intelligence**: Comprehensive threat intelligence, leveraging advanced analytics and global visibility to proactively identify, assess, and mitigate cyber threats across networks, endpoints, and cloud environments.

## Installation
### **Step 1: Add the Blocklist to Pi-hole**
1. Open Pi-hole Admin Panel (`http://pi.hole/admin` or `http://<Your-Pi-hole-IP>/admin`).
2. Navigate to **"Group Management" > "Adlists"**.
3. Click **"Add a new adlist"**.
4. Enter the following URL:
   ```
   https://raw.githubusercontent.com/mike-trewartha/Pi-hole-Talos-Threat-Blocklist/main/talos-threats.list
   ```
5. Click **"Add"** and then **"Update Gravity"** to apply changes.

### **Step 2: Manually Update Pi-hole** (Optional)
If needed, you can manually update Pi-hole by running:
```bash
pihole -g
```

## How It Works
- A script fetches **new domain IOCs** as published by Cisco Talos. (https://github.com/Cisco-Talos/IOCs)
- The script **removes domains older than 12 months** as they are likely no longer relevant to the current threat landscape.
- The blocklist file is updated and hosted on GitHub for easy use.

## License
This project is licensed under the Apache License 2.0. Any forks, modifications, or redistributions must acknowledge this original work

## Contributing
- Pull requests are welcome! Please ensure changes are well-documented.
- If you have domain sources you'd like to add, open an issue.

## Disclaimer
This blocklist is based on **publicly available IOCs** from Cisco Talos and is **not officially affiliated with Cisco Talos**. Use at your own risk.

---
📌 **Maintained by [mike-trewartha](https://github.com/mike-trewartha)**


