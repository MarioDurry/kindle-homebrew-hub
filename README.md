HomebrewHub/Kindle Homebrew Browser is a lightweight KUAL extension designed to bypass the Kindle's download restrictions. It allows you to download homebrew extensions as .zip.txt files via the Kindle's experimental browser, automatically renames them, and installs them into your extensions folder.
🚀 How it Works

The Kindle browser often refuses to download .zip or unknown file types. By hosting them as .zip.txt, we trick the browser into downloading them into the documents folder. This script then handles the "heavy lifting" of renaming and extracting them.
📥 Installation

    Prerequisites: * A Jailbroken Kindle.

        KUAL (Kindle Unified Application Launcher) installed.

    Setup:

        Download the HomebrewBrowserExtractor folder from this repo.

        Connect your Kindle to your PC via USB.

        Copy the HomebrewBrowserExtractor folder into the extensions directory on your Kindle's root.

            Path: Kindle Root/extensions/HomebrewBrowserExtractor/

    Important: Ensure script.sh and clean.sh use Unix (LF) line endings.

🛠 Usage

    Download: Open the experimental browser on your Kindle and navigate to this GitHub repo. Download any of the .zip.txt files (they will save to your documents folder).

    Launch: Open KUAL on your Kindle.

    Install: Tap HomebrewBrowser: Install.

    Check: The script will rename the files, extract them to your extensions folder, and show a "Success" message on your screen.

📂 Folder Structure
Plaintext

extensions/
└── HomebrewBrowserExtractor/
    ├── menu.json
    ├── script.sh
    └── clean.sh
documents/
└── [Your downloaded .zip.txt files go here]

❓ Troubleshooting

    Button not appearing in KUAL? Ensure the folder is not "double-nested" (e.g., extensions/Extractor/Extractor/menu.json). The menu.json must be exactly one folder deep inside extensions.

    Script "Permission Denied"? If you edited the files on Windows, the line endings might be wrong. Use Notepad++ to convert them to Unix (LF).

    Logs: Check documents/install_log.txt for a detailed breakdown of what happened during the last install.
