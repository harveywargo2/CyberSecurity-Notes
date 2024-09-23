# References
- https://softwarekeep.com/help-center/what-is-the-appdata-folder-in-windows-10

** What Is the AppData Folder?**
Every Windows Operating System contains a folder called AppData - short for Application Data.  The AppData folder in Windows 10 is a hidden folder located in C:\Users\<username>\AppData.  It contains custom settings and other information that PC system applications need for their operation.  You won’t need to access or use this folder often, but it contains your important app files such as bookmarks, game data, saved sessions, and so on.  However, sometimes, but rarely, you may need to access the AppData folder and scrutinize its contents.  Several apps use the AppData folder so it's easy to keep data synced between devices. 

**There are several reasons why threat actors target the AppData folder when installing malware:**
- **Persistency:** The AppData folder is hidden by default in Windows, making it less likely for users to stumble upon it and delete malicious files. Additionally, malware placed in AppData can be configured to automatically run each time the user logs in, ensuring its persistence on the system.
- **Accessing User Data:** AppData stores various user-specific data, including browsing history, saved passwords, personal files, and application settings. Threat actors can steal this data for financial gain, identity theft, or targeted attacks.
- **Bypassing Security Measures:** Many security programs focus on scanning traditional program files and system directories. Malware hidden in AppData can potentially avoid detection by these scanners.
- **Legitimate Activities:** AppData also stores legitimate program configurations and data. By mimicking legitimate files and processes, malware can blend in and be less suspicious.
- **Multiple Subfolders:** AppData has various subfolders for different applications and user profiles. This allows threat actors to target specific programs or users for more focused attacks.

**Here are some specific examples of how AppData is exploited by malware:**
- **LNK file manipulation:** Attackers can modify LNK (shortcut) files in AppData to point to malicious content when clicked.
- **Dropping malware in program folders:** Malware can be disguised as legitimate program files and placed in AppData subfolders related to that program.
- **Stealing browser data:** AppData stores browser-specific folders where browsing history, cookies, and saved passwords can be found.
- **Keylogging:** Malware can be injected into legitimate executables or libraries stored in AppData to capture keystrokes for password theft.

**It's important to note that**
- While AppData is a common target, it's not the only one. Threat actors can also target other system directories and user folders.
- Having strong security software with updated definitions and active scanning is crucial to detect and prevent malware in AppData and other locations.
- Users should be cautious about opening suspicious files or clicking on unknown links, even if they appear to be related to legitimate programs.


Common path for malware
```
AppData\Roaming\\Microsoft\Windows\Start Menu\Programs\Startup
```