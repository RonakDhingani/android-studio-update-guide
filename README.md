# 📌 Update Android Studio from Old Version to New Version (Linux) 🚀

If you want to upgrade **Android Studio** to the latest version on Linux, follow these step-by-step instructions.

---

## 🛠️ Step 1: Remove the Old Android Studio (Optional but Recommended)
If you installed Android Studio manually (not via **Snap** or **APT**), remove it first to avoid conflicts. Open a terminal and run:

```sh
rm -rf ~/android-studio
rm -rf ~/.local/share/Google/AndroidStudio*
rm -rf ~/.config/Google/AndroidStudio*
rm -rf ~/.cache/Google/AndroidStudio*
```

If you installed via **Snap**, remove it with:

```sh
sudo snap remove android-studio
```

---

## 📦 Step 2: Download & Extract the New Version

1️⃣ Open the terminal and go to your **Downloads** folder:

```sh
cd ~/Downloads
```

2️⃣ Extract the **tar.gz** file:

```sh
tar -xvf android-studio-<new-version>-linux.tar.gz
```
**For Example :
tar -xvf android-studio-2024.2.2.13-linux.tar.gz**


3️⃣ Move the extracted folder to **/opt/** (recommended for global access):

```sh
sudo mv android-studio /opt/
```

---

## 🔧 Step 3: Set Up Android Studio

Run the installer using the following command:

```sh
/opt/android-studio/bin/studio.sh
```

When prompted, select **"Do not import settings"** if asked.

Now, follow the setup wizard and **update SDK & plugins** as required.

---

## 🖥️ Step 4: Create a Desktop Shortcut (Optional)

To add **Android Studio** to your application menu:

1️⃣ Open a terminal and run:

```sh
nano ~/.local/share/applications/android-studio.desktop
```

2️⃣ Add the following content:

```ini
[Desktop Entry]
Version=1.0
Type=Application
Name=Android Studio
Exec=/opt/android-studio/bin/studio.sh
Icon=/opt/android-studio/bin/studio.png
Terminal=false
Categories=Development;IDE;
```

3️⃣ Save the file (**Ctrl + X**, then **Y**, then **Enter**).

4️⃣ Make the shortcut executable:

```sh
chmod +x ~/.local/share/applications/android-studio.desktop
```

---

## ✅ Step 5: Verify Installation

Run Android Studio using:

```sh
/opt/android-studio/bin/studio.sh
```

OR

Search for **"Android Studio"** in your application menu.

---

## 🔧 Troubleshooting

If the app doesn't open, install missing dependencies:

```sh
sudo apt update && sudo apt install libxcb-xinerama0
```

Now your **Android Studio** is successfully updated! 🎉🚀

---

💡 **Enjoy coding with the latest Android Studio!** 🖥️✨

