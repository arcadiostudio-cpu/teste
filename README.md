mv ~/android-sdk /home/kali/android-sdk
echo 'export ANDROID_HOME="/home/kali/android-sdk"' >> ~/.bashrc
echo 'export PATH="$PATH:$ANDROID_HOME/cmdline-tools/latest/bin:$ANDROID_HOME/platform-tools"' >> ~/.bashrc
source ~/.bashrc


sudo mkdir -p /opt/android-sdk
cd /opt/android-sdk



sudo wget -q https://dl.google.com/android/repository/commandlinetools-linux-11076708_latest.zip
sudo unzip -q commandlinetools-linux-*.zip
sudo mkdir -p cmdline-tools
sudo mv cmdline-tools cmdline-tools/latest
