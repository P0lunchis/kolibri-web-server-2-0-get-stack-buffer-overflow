# Kolibri WebServer 2.0 - GET Stack Buffer Overflow (Remote Code Execution)

## 📅 Date
July 11, 2014

## ✍️ Exploit Author
- **Christian (Polunchis) Ramirez** — [https://intlabs.ca](https://intlabs.ca)


**Contacts:**  
- polunchis@intlabs.ca  


## 📦 Software Information
- **Affected Software:** Kolibri WebServer 2.0
- **Vendor Website:** *(Not active)*
- **Vulnerability Type:** Stack-Based Buffer Overflow (Remote Code Execution)

## 🖥️ Tested On
- Windows XP SP3 (English)

## 🛡️ Vulnerability Description
A **stack-based buffer overflow vulnerability** exists in **Kolibri WebServer 2.0**.  
By sending an overly long HTTP `GET` request to the server's listening port (**TCP 8080**), an attacker can overwrite the EIP (Instruction Pointer) and gain remote code execution capabilities.

**No authentication** is required to exploit this vulnerability.

## ⚙️ Exploitation Details
- **Port:** 8080/TCP
- **Attack Vector:** Remote
- **Authentication:** Not required
- **Impact:** Full remote code execution with the privileges of the user running the Kolibri service.

## 🛠️ Usage
⚠️ **Warning:**  
This exploit is for educational and authorized penetration testing purposes only. Unauthorized access to systems without permission is illegal.

```bash
# Example usage (if you provide exploit.py or metasploit module here)
python exploit.py --target <IP_ADDRESS> --port 8080
