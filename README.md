#  Static NAT Configuration – Cisco Packet Tracer Lab

Welcome to my **Cisco Packet Tracer lab project** demonstrating how to configure **Static Network Address Translation (NAT)** using a simple network topology. This simulation is perfect for learners and beginners who want to understand how to make internal devices reachable via public IP addresses.

---

## 🖥️ Project Overview

This lab simulates a small network consisting of:

* A **private internal server**
* A **client PC**
* A **Cisco 1841 router** acting as the NAT device

The router is configured with Static NAT to map a **private IP** (e.g., `10.0.0.100`) to a **public IP** (e.g., `155.4.13.6`) so that external users can reach the server through the public address.

---

## 🔧 What I Did

Here’s a summary of the steps I configured in this project:

1. **Configured NAT Inside and Outside Interfaces**

   * Assigned `ip nat inside` to Fa0/0
   * Assigned `ip nat outside` to Fa0/1

2. **Mapped Private to Public IP**

   * Used the `ip nat inside source static` command to bind the internal server's private IP to its public one.

3. **Saved the Configuration**

   * Wrote everything to memory to persist after reloads.

4. **Verified Everything**

   * Used `show ip interface brief`, `show ip nat translations`, and `show ip nat statistics` to confirm everything worked as expected.

---

## 🧪 What You’ll Learn

* The basics of Static NAT
* How to configure inside and outside NAT interfaces
* How to verify and troubleshoot NAT issues
* The logic behind one-to-one IP mapping

---

## 🧰 Requirements

* Cisco Packet Tracer (v8.2.2 or above recommended)
* Basic understanding of router CLI
* A working knowledge of IP addressing/subnetting

---

## 🧠 Tips

* NAT won’t work if the internal host can’t be reached locally. Always verify local connectivity before troubleshooting NAT.
* Use `no shutdown` on your interfaces; you'd be surprised how often that’s the issue. 😅
* Don’t forget to save your configs using `do write`!

---

## 📈 Next Steps (Suggestions)

* Add dynamic NAT with a pool of IPs
* Experiment with PAT (NAT Overload)
* Simulate external access using another router or ISP cloud device
* Enable real-time debugging with `debug ip nat`

---

## 📝 License

This project is licensed under the **MIT License** – free to use, modify, and share for learning purposes.

---
