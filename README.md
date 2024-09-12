<h1>Setting up a Minecraft Java Edition Server on Windows</h1>



<h2>Description</h2>
 Is a custom Minecraft server offering dynamic game modes like Survival, Creative, and Mini-Games. I was responsible for server setup, plugin development, community management.
<br />


<h2>Languages and Utilities Used</h2>
Languages and Utilities Used:

- Java.
- Server Hosting.


<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>
Setting Up a Minecraft Server

1. Installing Java
- Navigate to https://www.java.com/en/download/.
- Click "Download Java" to get the installer.
- Run the installer and complete the installation.

2. Downloading the Minecraft Server JAR File
- Navigate to https://www.minecraft.net/en-us/download/server.
- Click the `minecraft_server..jar` link to download the file (e.g., `server.jar`).
- Create a folder for your server files, e.g., C:\Users\Admin\Desktop\Minecraft Server.
- Move the downloaded JAR file to this folder.

3. Creating the Initial Batch File
- Open Notepad or a text editor.
- Paste the following code:
  java -Xmx1024M -Xms1024M -jar server.jar nogui
  *To allocate 2GB RAM, use:* 
  java -Xmx2048M -Xms2048M -jar server.jar nogui
- Save the file as startup.bat (Select "All Files" in the Save as type dropdown).

4. Accepting the EULA
- Run startup.bat to generate eula.txt.
- Open eula.txt and change eula=false to eula=true.
- Save and close the file.

5. Configuring Server Properties
- Open server.properties in Notepad.
- Adjust settings:
  - gamemode= (survival, creative, adventure)
  - difficulty= (peaceful, easy, normal, hard)
  - max-players= (set your desired number)
  - server-port= (default is 25565; change if needed)
- Save and close the file.

6. Setting Up Port Forwarding and Firewalls

- For Local Servers:
  - Set a static IP and forward port 25565 on your router. Instructions vary by ISP/router; refer to their manuals or online guides.

- For Remote Servers:
  - Create inbound rules in Windows Firewall and any additional firewalls to allow TCP traffic on port 25565. Refer to provider-specific guides for firewall configurations.

7. Launching Your Server
- Open startup.bat to start the server.
- Pin or create a shortcut for easy access.
- Edit server.properties or startup.bat as needed by stopping the server first.

