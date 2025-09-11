# EZPasswall
[![Visitor Badge](https://img.shields.io/badge/Chat%20on-Telegram-blue.svg)](https://t.me/peditx) [![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

[**English**](README.md) | [**فارسی**](README_fa.md) | [**简体中文**](README-ch.md) | [**Русский**](README_ru.md)


# هشدار
# این کد قدیمی است و دیگر آپدیت نمی‌شود! برای دریافت نسخه‌های جدید از این لینک استفاده کنید:

# https://github.com/peditx/PeDitXOs
### اسکریپت EZPasswall چیست؟

  این اسکریپت به شما اجازه می‌دهد که با یک دستور ساده، دستگاه OpenWrt را با ظاهری مدرن و ساده به همراه پروتکل‌های OpenVPN، Xray، V2Ray، WireGuard، Cloudflare Warp و ... بهینه کنید. همچنین می‌توانید نرم‌افزار Passwall 1 و Passwall 2 (چه به صورت تکی و چه هردو) را نصب کنید و از داشتن یک اینترنت پایدار با ترافیک تفکیک‌شده و مستمر لذت ببرید. 
  این اسکریپت به مرور تکمیل‌تر خواهد شد.

  دوستدار شما،
[PeDitX](https://github.com/peditx)

## چگونه EZPasswall را نصب کنیم
![نصب تصویر](https://raw.githubusercontent.com/peditx/iranIPS/refs/heads/main/.files/lowspc/main/photo_2024-10-27_21-15-16.jpg)
![نصب تصویر](https://raw.githubusercontent.com/peditx/iranIPS/refs/heads/main/.files/lowspc/main/photo_2024-10-27_20-03-44.jpg)
![نصب تصویر](https://raw.githubusercontent.com/peditx/iranIPS/refs/heads/main/.files/lowspc/main/set1.png)
![نصب تصویر](https://raw.githubusercontent.com/peditx/iranIPS/refs/heads/main/.files/lowspc/main/set2.png)
![نصب تصویر](https://raw.githubusercontent.com/peditx/iranIPS/refs/heads/main/.files/lowspc/main/set3.png)


## اپلیکیشن کنترل‌کننده اندروید  
[![دانلود برای اندروید](https://img.shields.io/badge/Download%20for-Android-green?style=for-the-badge&logo=android)](https://github.com/peditx/EZpasswall/releases/tag/1.0.4)  

⚠ برای استفاده از این اپلیکیشن و کنترل روتر خود با آن، به نصب اسکریپت EZpasswall نیاز دارید.

### حداقل سیستم مورد نیاز برای روتر

- **سی پی یو:** `>= 700 MHz`
- **رم:** `>= 256 MB`

### بهترین روتر های پیشنهادی ما از نطر سازگاری 

- Google WiFi (Gale)
- Linksys EA8100
- Linksys EA8300
- Linksys E8450
- Belkin rt3200
- GL-iNet GL-A1300


### حداقل سیستم مورد نیاز برای کامپیوتر
- **سی پی یو:** `amd یا اینتل`
- **رم :** `۲ گیگابایت`
- **سیستم عامل:** `لینوکس اوبونتو ۲۰.۰۴`



> ⚠  **قبل از نصب:** اطمینان حاصل کنید که `آدرس WAN` و `آدرس LAN` یکسان نیستند.  
> **مثال:** 

> - آدرس LAN: `192.168.1.1`  
> آدرس LAN را به یک IP دیگر تغییر دهید، مانند `10.1.1.1`.



### نصب Passwall

> 🔴 **مهم:** برای روترهایی با `128 MB RAM`، لطفاً به [OpenWrt 22.03.3](https://archive.openwrt.org/releases/22.03.3/targets/) `کاهش دهید`. 🔴

فرمان زیر را در SSH از به روی OpenWrt اجرا کنید:

```bash
rm -f ezp.sh && wget https://raw.githubusercontent.com/peditx/EZpasswall/refs/heads/main/ezp.sh && chmod -X ezp.sh && sh ezp.sh

```

اگر می خواهید ازخدمات تبدیل لینوکس به OpenWrt استفاده کنید کافی است در SSH این دستور زیر را وارد کنید:

```bash
sudo apt-get update
sudo apt-get install curl
rm -f *.sh && wget https://raw.githubusercontent.com/peditx/easywrt/refs/heads/main/start.sh && bash start.sh

```

یا (برای X86/X86-64) فقط این فایل .iso را دانلود کرده و به فلش قابل بوت تبدیل کنید و سپس دستور start.sh را تایپ کنید:
```bash
https://github.com/peditx/easywrt/releases/download/V101/PeDitXOs-101.iso

```
**تمام شد!**


***اگر با دانلود پکیج ها از سورس فورج \ گیت هاب \ سایت اوپن دبلیو آر تی  مشکل دارید و باز شدن کد ها بامشکل مواجه می شود از دستور زیر استفاده کنید و هوست های مختلف را آزمایش کنید و در انتها برای اجرا شدن اسکریپت عدد `۶` رابزنید.***

```bash
rm -f host.sh && wget -O host.sh https://raw.githubusercontent.com/peditx/EZpasswall/refs/heads/main/host.sh && chmod +x host.sh && ./host.sh

```

### پروتکل‌های پشتیبانی شده

- **VLESS:** (XRAY ✅, SING-BOX ✅)
- **VMESS:** (XRAY ✅, SING-BOX ✅)
- **REALITY:** (XRAY ✅, SING-BOX ❌)
- **TROJAN:** (XRAY ✅, SING-BOX ✅)
- **HYSTERIA2:** (XRAY ❌, SING-BOX ✅)
- **TUIC:** (XRAY ❌, SING-BOX ✅)
- **SHADOWSOCKS:** (XRAY ✅, SING-BOX ✅)
- **WIREGUARD:** (XRAY ✅, SING-BOX ✅)
- **SOCKS:** (XRAY ✅, SING-BOX ✅)
- **HTTP:** (XRAY ✅, SING-BOX ✅)



### روترهای پیشنهادی

- Google WiFi (Gale)
- Linksys EA8300
- Linksys E8450
- Belkin rt3200
- GL-iNet GL-A1300
- Xiaomi AX3000T
- ~~Xiaomi 4a Gigabit~~
- TP-Link C6 v3
- Mikrotik Hap ac2
- GL.iNet AR300M (NOR)
- Linksys EA7500 (v1-v2)
- Linksys EA8100 (v1-v2)
- ASUS RT-N66U
- Xiaomi AX3600
- Xiaomi AX3200
- Xiaomi AX6000
- Netgear R7800



### ویژگی‌ها

- نصب خودکار کامل در یک مرحله.
- پشتیبانی از Passwall 1 و 2 بر روی یک روتر.
- نصب اکس روت (انتقال و افزایش فضای داخلی روتر با حافظه فاش) با یک کلیک برای روتر هایی که درگاه یو اس بی دارند.
- X86Tools برای تبدیل Linux x86/x86-64 به OpenWRT، ImmortalWRT، PeDitXRT، MikroTik یا سیستم‌عامل‌های سفارشی برای سیستم‌عامل هایی که نصب مستقیم ندارند.
- تنظیم سریع وایفای فقط با دریافت نام وایفای و پسورد در بخش Extra tools
- پاکسازی حافظه مصرف شده فقط با یک کلیک در بخض Extra tools
- نصب پکیج های تکمیلی openVPN و sing-box و softether و شانت تفکیک آی پی ها با sing-box و ... برای روترها و تین کلاینت هایی که فضای دخیره سازی بالا تر از 512 مگابایت را دارند در بخش Extra Tools
- نصب هوشمند XRAY در فضای موقت در صورت محدود بودن فضای دیسک.
- ترافیک مستقیم IP ها و دامنه های ایران (100%).
- بهبود عملکرد.
- طراحی تم و لوگو جدید.
- اتصال به سرور WARP .
- kill switch پیش‌فرض.
- XRAY Fragment tlshello | 1-3.




### تشکر ویژه

- [تیم OpenWrt](https://github.com/openwrt)
- [تم PeDitX](https://github.com/peditx/luci-theme-peditx)
- [تیم Passwall](https://github.com/xiaorouji)
- [تیم V2Ray](https://github.com/v2ray)
- [PeDitXrt](https://github.com/peditx/PeDitXrt)
- [محمدرضا بروجردی](https://t.me/MR13_B)
- [Sia7ash](https://github.com/Sia7ash)




[PeDitX](https://github.com/peditx) © 2024
