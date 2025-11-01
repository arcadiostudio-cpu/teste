nano ~/whatsintruder/whatsintruder.sh  



# --- BUILD APK COM ASSINATURA ---
echo "[*] Compilando APK..."
aapt package -f -m -J src -M AndroidManifest.xml -S res -I $ANDROID_HOME/platforms/android-33/android.jar -F app-unsigned.apk

echo "[*] Gerando DEX..."
dx --dex --output=classes.dex src/

echo "[*] Unindo APK..."
aapt add app-unsigned.apk classes.dex
cp app-unsigned.apk app-unaligned.apk

echo "[*] Alinhando APK..."
zipalign -f -v 4 app-unaligned.apk app.apk

echo "[*] Assinando APK..."
apksigner sign --ks keystore.jks --ks-pass pass:123456 app.apk

echo "[*] APK GERADO: app.apk (ASSINADO)"
