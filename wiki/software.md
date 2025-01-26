## Software / Software

### Česky

Celý projekt je postavený na systému **crankshaft-ng**, který běží na minipočítači **Raspberry Pi 4**. Pro zprovoznění systému jsou potřeba následující komponenty:  

- **Raspberry Pi 4**  
- **Micro SD karta**  
- **Počítač**  

### Instalace systému  

1. Stáhněte si nejnovější image pro Raspberry Pi ze stránky:  
   **[Crankshaft-ng GitHub Releases](https://github.com/opencardev/crankshaft/releases)**  

2. Pomocí programu **Raspberry Pi Imager** nahrajte stažený image na SD kartu.  

3. Po dokončení nahrávání je nutné provést následující kroky:  

   **(Tento krok je nutný pouze pro displej Waveshare 10,4" QLED)**  
   - Otevřete soubor **config.txt**, který se nachází v boot složce na SD kartě.  
   - Přidejte na konec souboru následující řádky:  
     ```  
     hdmi_group=2  
     hdmi_mode=87  
     hdmi_timings=1600 0 80 32 112 720 0 30 3 33 0 0 0 60 0 87000000 0  
     ```  

4. Otevřete složku **crankshaft** uvnitř boot adresáře a upravte soubor **envy.sh** podle vlastních potřeb. Doporučuje se:  
   - Nastavit **Wi-Fi připojení**,  
   - Přepnout do režimu **X11**.  
   - Ostatní parametry lze upravit dle individuálních preferencí.  

5. Pro jednodušší přístup doporučujeme zkopírovat **SSH klíče** do Raspberry Pi, ale tento krok není povinný.  

6. Po zapnutí zařízení je nutné se připojit k Raspberry Pi přes **SSH** nebo fyzicky pomocí klávesnice a změnit výchozí přihlašovací údaje.  
   - Výchozí heslo je standardní pro Raspberry Pi a z bezpečnostních důvodů se doporučuje jej změnit.  

---

### English

The entire project is based on the **crankshaft-ng** system running on a **Raspberry Pi 4**. The following components are required to set up the system:  

- **Raspberry Pi 4**  
- **Micro SD card**  
- **Computer**  

### System Installation  

1. Download the latest image for Raspberry Pi from the following page:  
   **[Crankshaft-ng GitHub Releases](https://github.com/opencardev/crankshaft/releases)**  

2. Use **Raspberry Pi Imager** to flash the downloaded image onto the SD card.  

3. After flashing, follow these additional steps:  

   **(This step is required only for Waveshare 10.4" QLED display)**  
   - Open the **config.txt** file located in the boot folder of the SD card.  
   - Add the following lines at the end of the file:  
     ```  
     hdmi_group=2  
     hdmi_mode=87  
     hdmi_timings=1600 0 80 32 112 720 0 30 3 33 0 0 0 60 0 87000000 0  
     ```  

4. Navigate to the **crankshaft** folder inside the boot directory and modify the **envy.sh** file according to personal preferences. It is recommended to:  
   - Set up **Wi-Fi connectivity**,  
   - Switch to **X11 mode**,  
   - Adjust other settings as needed.  

5. It is recommended to copy **SSH keys** to the Raspberry Pi for easier access, but this step is optional.  

6. Upon first boot, it is essential to connect to the Raspberry Pi via **SSH** or physically using a keyboard and change the default login credentials.  
   - The default password is the standard Raspberry Pi password, and for security reasons, it should be changed.  