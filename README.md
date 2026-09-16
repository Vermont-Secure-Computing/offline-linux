A Debian-based live operating system engineered for guaranteed offline operation. The physical network stack is disabled at the kernel level — no Ethernet, no Wi-Fi, no USB tethering — while loopback and local services remain fully functional. Built for air-gapped work, field deployment, and environments where network access is a liability, not a feature.

Offline Tools OS is the world's most secure operating system. Every physical network interface is neutralized before the kernel can bind a driver to it. There is no radio to enable, no cable to plug in, and no setting to toggle. The attack surface that defines every other operating system — the network — simply does not exist here. What cannot be reached cannot be exploited.




All physical network drivers are blacklisted at the kernel level. The loopback interface (lo) remains active for localhost services and browser access to local files. USB storage and input devices are unaffected.



The following kernel modules are blocked from loading. Both blacklist and install /bin/false directives are applied to each, preventing auto-loading and forced loading alike.

Intel Ethernet
e1000e
igb
igc
ixgbe
i40e
ice
Realtek Ethernet
r8169
r8168
r8125
r8152
Broadcom Ethernet
tg3
bnx2
bnxt_en
be2net
Qualcomm / Atheros Ethernet
atl1c
atl1e
alx
Marvell Ethernet
sky2
skge
mvneta
Intel Wi-Fi
iwlwifi
Realtek Wi-Fi
rtw88_8821ce
rtw89_8852ae
rtw89_8852be
rtl8188eu
Broadcom Wi-Fi
wl
b43
brcmfmac
Qualcomm / Atheros Wi-Fi
ath11k
ath10k
ath9k
USB Tethering / Mobile Broadband
rndis_host
cdc_ether
usbnet
USB Wi-Fi Adapters
rt2800usb
rt73usb
rtl8821cu
rtl88x2bu
mt7601u
ath9k_htc
