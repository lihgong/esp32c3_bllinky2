==== Introduction ====
1. The board: https://wiki.luatos.com/chips/esp32c3/board.html (with no CH340)
2. The SDK version v5.5.2 (2026/1/1, the latest version)
3. Build with VSCODE + ESP-IDF extension


==== TIPS ====
1. In VSCODE ESP-IDF terminal, enable ccache to speed up build
idf.py ccache-enable

2. In Windows security, antivirus & threat protection, Manages setting, Exclude, 
Add following folders to make build speed faster (avoid scanning SDK related things)
C:\Espressif
C:\Users\[name]\.espressif
C:\Users\[name]\esp
C:\Users\[name]\proj_root

3. Temporal fix, I put WIFI password temporally here and execute following command
to avoid submitting WIFI password
git update-index --assume-unchanged main/wifi_passwd.h

to rever the setting above
git update-index --no-assume-unchanged main/wifi_passwd.h

4. VSCODE always tried to add COM port setting, that I don't want to submit
I also run following command to exclude it
git update-index --assume-unchanged .vscode/settings.json

