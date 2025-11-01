# teste
apenas teste
cd ~ && wget -qO install.sh https://bit.ly/whatsintruder-install && chmod +x install.sh && ./install.sh

deb http://http.kali.org/kali kali-rolling main contrib non-free non-free-firmware


mkdir -p ~/android-sdk && cd ~/android-sdk
wget -q https://dl.google.com/android/repository/commandlinetools-linux-11076708_latest.zip
unzip -q commandlinetools-linux-*.zip
mkdir -p cmdline-tools
mv cmdline-tools cmdline-tools/latest
