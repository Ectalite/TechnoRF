# Mise en place des cartes ESP32

# Installation

1. Monter l’antenne fournie sur la carte ESP32.
2. Brancher la carte ESP32 à l’ordinateur via un câble USB.
3. Installer Arduino IDE
    
    [Download Arduino](https://www.arduino.cc/en/donate/)
    
4. Dans **File → Preferences**, ajouter l’URL suivante dans le champ **Additional Board Manager URLs**, puis cliquer OK.
    
    URL : `https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json`
    
5. Dans **Select Board**, sélectionner le port COM où est branchée la carte ESP32.
    1. Dans Boards, sélectionner la carte **ESP32 DEV Board.**
    2. Cliquer OK
    3. L’IDE propose d’installer le nécessaire pour cette board, cliquer oui.
        
        ![Untitled](Mise%20en%20place%20des%20cartes%20ESP32/Untitled.png)
        
    4. Si l’IDE ne trouve plus la carte après installation, sélectionner la board **ESP32 Dev Module**
        
        ![Untitled](Mise%20en%20place%20des%20cartes%20ESP32/Untitled%201.png)
        
    5. Cliquer OK.
6. Installer les librairies :
    1. Aller dans **Sketch → Include Library → Manage Libraries** et taper **ssd1306**. Choisir la librairie d’Adafruit.
        
        ![Untitled](Mise%20en%20place%20des%20cartes%20ESP32/Untitled%202.png)
        
    2. Installer également la librairie GFX en tapant **gfx** dans la barre de recherche et installer la version d’Adafruit.
        
        ![Untitled](Mise%20en%20place%20des%20cartes%20ESP32/Untitled%203.png)
        
    3. Enfin, installer la librairie Lora de Sandeep Mistry
        
        ![Untitled](Mise%20en%20place%20des%20cartes%20ESP32/Untitled%204.png)
        

# Mise en place de la carte Sender

1. Ouvrir le fichier sender.ino en allant dans **File → Open** et sélectionner le fichier fourni.
2. Programmer la carte en pressant sur le bouton **Upload**
    
    La carte doit afficher des informations et envoyer des packets.
    
3. Ouvrir la communication série en allant dans : **Tools → Serial Monitor**
    1. Sélectionner un baudrate de 115200.
    2. Vous devez voir des informations s’afficher.
        
        ![Untitled](Mise%20en%20place%20des%20cartes%20ESP32/Untitled%205.png)
        

# Mise en place de la carte Receiver

1. Ouvrir le fichier **receiver.ino** en allant dans **File → Open** et sélectionner le fichier fourni.
2. Sélectionner la board avec le bon port COM.
3. Upload le code
4. La carte doit afficher les packets reçus et le RSSI.
    
    ![TTGO-LoRa-ESP32-Dev-Board-Receiver.webp](Mise%20en%20place%20des%20cartes%20ESP32/TTGO-LoRa-ESP32-Dev-Board-Receiver.webp)
    

# Source

[TTGO LoRa32 SX1276 OLED with Arduino IDE | Random Nerd Tutorials](https://randomnerdtutorials.com/ttgo-lora32-sx1276-arduino-ide/)