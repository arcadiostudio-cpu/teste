mv ~/android-sdk /home/kali/android-sdk
echo 'export ANDROID_HOME="/home/kali/android-sdk"' >> ~/.bashrc
echo 'export PATH="$PATH:$ANDROID_HOME/cmdline-tools/latest/bin:$ANDROID_HOME/platform-tools"' >> ~/.bashrc
source ~/.bashrc


sudo mkdir -p /opt/android-sdk
cd /opt/android-sdk
