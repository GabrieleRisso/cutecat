```bash
oneko -tofocus -bg violet -rv -speed 3 -idle 55 -time 8000 -name minny -neko
```

### Installing Oneko on Multiple Platforms:

#### Linux/Manjaro:
1. Install Oneko using the package manager:
   ```bash
   sudo pacman -S oneko
   ```

#### MacOS:
1. Install Oneko using Homebrew:
   ```bash
   brew install oneko
   ```

#### Windows:
1. **Download the oneko jar file**: Obtain the `oneko` jar file from a reliable source: https://glreno.github.io/oneko/
2. **Install Java**: Ensure that Java is installed on the system where you want to run the jar file. You can install Java by following the instructions specific to your operating system.
3. **Run the jar file**: You can run the jar file using the following command in the terminal:
   ```bash
   java -jar oneko.jar
   ```
4. **Create Startup Service on Windows**: To create a startup service on Windows, you can create a batch file with the `java -jar oneko.jar` command and place it in the Startup folder.

For a more robust solution on Windows, you can create a Windows Service using tools like NSSM (Non-Sucking Service Manager) to manage the Oneko application as a service

### Using Oneko as a Startup Service on Multiple Platforms:

#### Linux/Manjaro:
1. Create a systemd service file for Oneko in this location /etc/systemd/system/oneko.service:
   ```ini
   [Unit]
   Description=Oneko Service
   After=graphical.target

   [Service]
   ExecStart=/usr/bin/oneko -tofocus -bg violet -rv -speed 3 -idle 55 -time 8000 -name minny -neko

   [Install]
   WantedBy=graphical.target
   ```
2. Enable and start the service:
   ```bash
   sudo systemctl enable oneko.service
   sudo systemctl start oneko.service
   ```
### Setting Up Oneko as a Startup Service on MacOS

1. **Create a Launchd Plist File:**
   - Open a terminal window.
   - Use a text editor like `nano` or `vim` to create a new plist file. For example, `nano com.oneko.plist`.
   - Add the following content to the plist file:
     ```xml
     <?xml version="1.0" encoding="UTF-8"?>
     <!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
     <plist version="1.0">
     <dict>
         <key>Label</key>
         <string>com.oneko</string>
         <key>ProgramArguments</key>
         <array>
             <string>oneko</string>
             <string>-tofocus</string>
             <string>-bg</string>
             <string>violet</string>
             <string>-rv</string>
             <string>-speed</string>
             <string>3</string>
             <string>-idle</string>
             <string>55</string>
             <string>-time</string>
             <string>8000</string>
             <string>-name</string>
             <string>minny</string>
             <string>-neko</string>
         </array>
         <key>RunAtLoad</key>
         <true/>
     </dict>
     </plist>
     ```
2. **Load the Plist File:**
   - Save the plist file.
   - Load the plist file using the command:
     ```bash
     launchctl load com.oneko.plist
     ```
   - Oneko will now start as a startup service on MacOS.

#### Windows:
1. Create a batch file with the Oneko command.
2. Add the batch file to the startup programs list.

Now, Oneko will run as a startup service on the respective platforms.
