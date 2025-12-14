# 📻 Sequence SMP Radio Plugin

This is the custom **Spigot/Paper Minecraft Plugin** for Sequence SMP. It acts as the "remote control" for the website audio system.

When an admin runs a command in-game (like `/play`), this plugin sends a signal to the **Backend Server**, which then plays music on the **Website** for all connected players.

[![Live Website](https://img.shields.io/badge/🌐_Visit-Live_Website-2ea44f?style=for-the-badge&logo=google-chrome&logoColor=white)](https://maxllh7809.github.io/Sequence-SMP-Site/)

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spigot](https://img.shields.io/badge/Spigot-E57373?style=for-the-badge&logo=spigotmc&logoColor=white)
[![Frontend](https://img.shields.io/badge/GitHub-Frontend_Website_Repo-blue?style=for-the-badge&logo=github)](https://github.com/Maxllh7809/Sequence-SMP-Site)
[![Audio Backend](https://img.shields.io/badge/GitHub-Audio_Backend_Repo-181717?style=for-the-badge&logo=github)](https://github.com/Maxllh7809/sequence-audio-backend)

## ⚙️ Installation & Setup

1.  Download the `.jar` file from the [Releases](https://github.com/Maxllh7809/sequence-radio-audio/releases) tab (or compile it yourself).
2.  Drag the file into your server's `/plugins` folder.
3.  Restart the server to generate the config file.
4.  Open `plugins/SequenceRadio/config.yml`.
5.  Update the `api-url` to your Render Backend URL:

    ```yaml
    # config.yml
    
    # The URL of your Node.js Backend (Do not include /play at the end, just the base URL)
    # Example: [https://sequence-audio-backend.onrender.com](https://sequence-audio-backend.onrender.com)
    api-url: "[https://YOUR-BACKEND-URL.onrender.com](https://YOUR-BACKEND-URL.onrender.com)"
    ```
6.  Run `/radio reload` or restart the server.

---

## 📜 Commands & Permissions

| Command | Permission | Description |
| :--- | :--- | :--- |
| `/play <url> [name]` | `sequence.radio.admin` | Plays audio from a direct URL for all players on the website. |
| `/stop` | `sequence.radio.admin` | Stops the music for everyone. |
| `/reload` | `sequence.radio.admin` | Reloads the `config.yml` file. |

**Example Usage:**
```minecraft
/play [https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3](https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3) Epic_Battle_Music
````

-----

## 🛠️ How to Compile (For Developers)

If you want to edit the Java code:

1.  Clone this repository.
2.  Open it in **IntelliJ IDEA** or **Eclipse**.
3.  Ensure you have **Maven** installed.
4.  Run `mvn clean package`.
5.  The compiled `.jar` will be in the `target/` folder.

-----

## 👥 Credits

  * **Plugin Development:** Jishnu H Maruthamutu (Hooman)
  * **Website & Integration:** Loh Wei Feng (Max)
  * **Server Owner:** Siqns

© 2025 Sequence SMP
