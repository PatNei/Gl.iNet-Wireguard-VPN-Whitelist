# GL.iNet WireGuard VPN Whitelist

Some websites do not work correctly when accessed through a VPN. This is especially common with government services, banking apps, local streaming providers (like DR/TV2), and technical wikis that block data center IPs.

This repository provides a curated list of domains to create a **Split Tunneling** exception. When configured, your GL.iNet router will route traffic for these specific domains directly through your local ISP, ensuring they remain accessible while keeping the rest of your connection secure behind the VPN.

## 🚀 How to Use (Automatic Update)

You can configure your GL.iNet router to pull the list directly from this repository. This allows you to update the domains here on GitHub and have your router automatically pick up the changes.

### 1. Get the Raw URL
Copy the link to the raw text file in this repository:

[https://raw.githubusercontent.com/PatNei/Gl.iNet-Wireguard-VPN-Whitelist/refs/heads/main/main-whitelist.txt](https://raw.githubusercontent.com/PatNei/Gl.iNet-Wireguard-VPN-Whitelist/refs/heads/main/main-whitelist.txt)

### 2. Configure the Router
1.  Log in to your GL.iNet Admin Panel.
2.  Navigate to **VPN** > **VPN Dashboard**.
3.  Locate **VPN Policy Base on the Target Domain or IP**.
4.  Toggle the policy to **ON**.
5.  Set the mode to **"Do not use VPN (Access Internet Directly)"** for the domains in the list.
    * *This ensures the listed websites bypass the VPN tunnel.*
6.  Look for the option to import or sync from a URL (depending on your firmware version) or simply copy-paste the content of `main-whitelist.txt` into the manual input field.

## 📚 Official Documentation

For a detailed, step-by-step tutorial on how to configure these rules using an online text file source, please refer to the official GL.iNet guide:

* 📖 **[How to configure domain and IP filtering rules for GL.iNet routers via an online text file](https://docs.gl-inet.com/router/en/4/tutorials/how_to_configure_domain_and_ip_filtering_rules_for_glinet_routers_via_an_online_text_file/)**

## 🌍 What is included?

This list is designed to fix common interruptions for users in **Denmark** and technical users. It includes exceptions for:

* **Streaming Services:** `dr.dk`, `tv2.dk`, `viaplay.dk`
* **Technical Resources:** `nixos.wiki`

---
*Feel free to submit a Pull Request to add more domains that are blocked by VPN providers.*
