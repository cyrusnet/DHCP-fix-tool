# DHCP-fix-tool
Automated PowerShell L1 troubleshooting tool for DHCP lease issues, APIPA addresses , and DNS cache clearance.
# 🛠️ DHCP Network Diagnostics & IP Renewal Tool

A lightweight PowerShell automation tool for Help Desk Specialists to troubleshoot network connection failures, APIPA addresses (169.254.x.x), and stale DHCP leases on client workstations.

---

## 📌 Problem Scenario
In corporate networks, endpoints often encounter connection issues due to:
- Failure to receive a lease from the DHCP server, resulting in an APIPA address (169.254.x.x).
- Stale IP configuration after moving between subnets or VPNs.
- Corrupted DNS cache preventing resolution of internal/external domain names.

## 🚀 Script Workflow & Features
This script automates standard L1 troubleshooting steps into a single execution:
1. Flushes DNS Resolver Cache: Clears outdated or corrupted DNS records (Clear-DnsClientCache).
2. Releases Current IP Lease: Discards the existing IPv4 configuration (ipconfig /release).
3. Renews DHCP Lease: Initiates a new DORA process with the DHCP server to obtain a fresh IP (ipconfig /renew).
4. Verifies Connectivity: Tests ICMP connectivity to an external IP (8.8.8.8) to confirm WAN/Gateway reachability.

## 🛠️ Usage
1. Open PowerShell as Administrator.
2. Run the script: .\DHCP-Fix.ps1

==================================================
==================================================

# 🛠️ ابزار عیب‌یابی شبکه DHCP و نوسازی آی‌پی

یک ابزار سبک خودکارسازی با پاورشل برای کارشناسان هلپ‌دست جهت رفع مشکلات قطعی شبکه، آدرس‌های APIPA (169.254.x.x) و اجاره‌نامه‌های منقضی‌شده DHCP روی سیستم کلاینت‌ها.

---

## 📌 سناریوی مشکل
در شبکه‌های سازمانی، سیستم‌ها اغلب با مشکلات زیر مواجه می‌شوند:
- عدم دریافت آی‌پی از سرور DHCP که منجر به گرفتن آدرس APIPA (169.254.x.x) می‌شود.
- تنظیمات قدیمی آی‌پی پس از جابجایی بین ساب‌نت‌ها یا وی‌پی‌ان.
- خراب شدن کش DNS که مانع از حل نام دامنه‌های داخلی و خارجی می‌شود.

## 🚀 روند کار و ویژگی‌های اسکریپت
این اسکریپت مراحل استاندارد عیب‌یابی لایه ۱ را در یک اجرا خودکار می‌کند:
1. پاکسازی کش DNS: رکوردهای قدیمی یا خراب DNS را پاک می‌کند (Clear-DnsClientCache).
2. آزادسازی آی‌پی فعلی: تنظیمات فعلی IPv4 را دور می‌اندازد (ipconfig /release).
3. دریافت مجدد آی‌پی از DHCP: فرآیند جدید DORA را با سرور DHCP برای دریافت آی‌پی تازه آغاز می‌کند (ipconfig /renew).
4. تایید اتصال: اتصال ICMP به یک آی‌پی خارجی (8.8.8.8) را برای تایید دسترسی به اینترنت/گیت‌وی بررسی می‌کند.

## 🛠️ نحوه استفاده
1. پاورشل (PowerShell) را به صورت Administrator باز کنید.
2. اسکریپت را اجرا کنید: .\DHCP-Fix.ps1

==================================================
==================================================

