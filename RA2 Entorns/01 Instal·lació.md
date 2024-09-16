# Instal·lació

## 2.1 Instal·la entorns de desenvolupament, propietaris i lliures.

Un entorn de desenvolupament software (o IDE, Integrated Development Environment) és un conjunt d'eines que permeten als programadors escriure, provar i depurar codi de manera més eficient. Aquestes eines inclouen, sovint, un editor de codi, eines de compilació i depuració, gestió de versions i altres utilitats.

### Terminal/Eina de comandes
---
<center>
<img src="./assets/logoTerminal.png" style="width: 90%; max-width: 100px">
</center>

L'eina de comandes (també coneguda com a terminal o consola) és una interfície basada en text que permet als desenvolupadors executar ordres del sistema, gestionar fitxers, compilar codi, executar scripts i utilitzar eines de control de versions com Git. Sovint és l'eina central per interactuar amb el sistema operatiu o altres eines de programació sense interfície gràfica.

- **Linux i macOS** tenen Terminals compatibles amb UNIX

- **Windows** té diferents opcions de terminal:

    - Terminal clàssic
    - Terminal PowerShell
    - Terminal WSL Linux (necessita instal·lació apart)

    A Windows es pot instal·lar un entorn de Terminal basat amb Linux, fent ús de WSL. Per fer-ho:

    - Instal·lar Ubuntu des de la botiga d'aplicacions

<center>
<img src="./assets/winwslinstall.png" style="width: 90%; max-width: 300px">
</center>

    - El primer cop que s'obre un terminal d'Ubuntu cal definir un nom d'usuari i una contrasenya.


<center>
<img src="./assets/winwsl.png" style="width: 90%; max-width: 300px">
</center>

### Visual Studio Code
---
<center>
<img src="./assets/logoVisualStudioCode.png" style="width: 90%; max-width: 150px">
</center>

**VS Code** és un editor de codi lleuger i extensible que proporciona una experiència IDE completa. És altament personalitzable a través d'extensions que permeten afegir funcionalitats com depuració, autocompletat de codi, suport per a múltiples llenguatges de programació i integració amb Git. VS Code és molt popular perquè equilibra potència i simplicitat.

- A **Windows** i **macOS** descarregar i instal·lar **[Visual Studio Code](https://code.visualstudio.com/download)**

- Per **linux**, cal descarregar un arxiu **.deb** i instal·lar-lo amb:

```bash
sudo apt install ./NOMARXIU.deb 
# Adaptar al nom, per exemple: code_1.92.2-172.deb
```

### GitHub Desktop
---
<center>
<img src="./assets/logoGitHub.png" style="width: 90%; max-width: 150px">
</center>

GitHub és una plataforma de control de versions basada en Git que permet als desenvolupadors col·laborar en projectes, gestionar versions de codi, revisar canvis i compartir projectes públicament o privadament. 

- A **Windows** i **macOS** descarregar i instal·lar **[GitHub Desktop](https://desktop.github.com/download/)**

- Per **linux**, GitHub Desktop s'instal·la des del **Terminal** amb aquestes 3 comandes:
 
```bash
wget -qO - https://apt.packages.shiftkey.dev/gpg.key | gpg --dearmor | sudo tee /usr/share/keyrings/shiftkey-packages.gpg > /dev/null

sudo sh -c 'echo "deb [arch=amd64 signed-by=/usr/share/keyrings/shiftkey-packages.gpg] https://apt.packages.shiftkey.dev/ubuntu/ any main" > /etc/apt/sources.list.d/shiftkey-packages.list'

sudo apt update && sudo apt install github-desktop
```

### Python
---
<center>
<img src="./assets/logoPython.png" style="width: 90%; max-width: 100px">
</center>

Python és un llenguatge de programació d'alt nivell, interpretat i de codi obert, conegut per la seva senzillesa i llegibilitat. 

- A **macOS** ja hi ha Python disponible

- A **Linux** calen els paquets:
```bash
sudo apt install pip
sudo apt install python3-ipykernel
```

- A **Windows** cal instal·lar-lo a través de la botiga d'aplicacions:

<center>
<img src="./assets/winpython.png" style="width: 90%; max-width: 300px">
</center>

### Java
---
<center>
<img src="./assets/logoJava.png" style="width: 90%; max-width: 150px">
</center>

Java és una plataforma informàtica que inclou:

- Un llenguatge de programació,
- Un conjunt de llibreries i la definició d’una màquina virtual.

Hi ha dues versions de Java

<a href="https://www.java.com/en/" target="_blank">Java</a> només inclou la Java Virtual Machine per executar programes Java

<a href="https://www.oracle.com/java/technologies/downloads/" target="_blank">JDK</a>, Java Development Kit a part d’instal·lar la màquina virtual, inclou les eines de desenvolupament (entre elles el compilador)

Cal instal·lar **Java Development Kit (JDK)**, hi ha disponibles les eines de comandes de Java:

- A **Ubuntu Linux**: escolliu el paquet 'x64 Debian'

- A **Windows**: escolliu el paquet 'x64 MSI Installer'

- A **macOS**: escolliu el paquet 'ARM64 DMG Installer'

### Maven
---
<center>
<img src="./assets/logoMaven.png" style="width: 90%; max-width: 150px">
</center>

Maven és una eina que automatitza la compilació de projectes JAVA, i també facilita la gestió de llibreries dels projectes.

Per instal·lar Maven a **Linux** i **macOS**:

```bash
sudo apt install maven # Linux
brew install maven # macOS
```

A windows cal seguir aquests passos (adaptant el número de versió):

- [Descarregar el 'Binary zip archive' de Maven](https://maven.apache.org/download.cgi)
- Descomprimir l'arxiu tipus 'apache-maven-3.9.6-bin.zip' posar-lo a la carpeta "C:\Program Files\Maven\"
- Ha de quedar semblant a: "C:\Program Files\Maven\apache-maven-3.9.6\"
- Obrir el programa "Edit the system environment variables"
- Apretar el botó "Environment Variables"
- A les "System variables" afegir la variable: MAVEN_HOME amb el valor "C:\Program Files\Maven\apache-maven-3.9.6"
- A les "System variables" editar la variable "Path" per afegir-hi "C:\Program Files\Maven\apache-maven-3.9.6\bin"
- Reiniciar Windows
- Reafirmar els teus pensaments que Windows és més fàcil i millor

### MySQL
---
<center>
<img src="./assets/logoMySQL.png" style="width: 90%; max-width: 150px">
</center>
MySQL és un sistema de gestió de bases de dades relacional de codi obert, basat en el llenguatge SQL (Structured Query Language). 

A **Ubuntu Linux**:
```bash
sudo apt update
sudo apt install mysql-server
sudo systemctl start mysql
```

- Per configurar MySQL a **Ubuntu Linux**:
```bash
sudo mysql_secure_installation
```

- Per accedir a MySQL a **Ubuntu Linux**:
```bash
mysql -u root -p
```

- Per aturar/iniciar MySQL a **Ubuntu Linux**:
```bash
sudo systemctl stop mysql
sudo systemctl start mysql
sudo systemctl restart mysql
```

A **macOS**:
```bash
sudo brew install mysql
brew services start mysql
```

- Per configurar MySQL a **macOS**:
```bash
mysql_secure_installation
```

- Per accedir a MySQL a **macOS**:
```bash
mysql -u root -p
```

- Per aturar/iniciar MySQL a **macOS**:
```bash
brew services stop mysql
brew services restart mysql
```

A **Windows**:
```bash
winget install Oracle.MySQL
```

- Per configurar MySQL a **Windows**:
```bash
mysql -u root -p
ALTER USER 'root'@'localhost' IDENTIFIED BY 'nova_contrasenya';
# Altres gestions directament amb codi SQL
```

- Per accedir a MySQL a **Windows**:
```bash
mysql -u root -p
```

- Per aturar/iniciar MySQL a **Windows**:
```bash
net stop MySQL
net start MySQL
```

**MySQL Workbench**
---
<center>
<img src="./assets/logoWorkbench.png" style="width: 90%; max-width: 150px">
</center>

MySQL Workbench és una eina gràfica de codi obert que permet dissenyar, administrar i interactuar amb bases de dades MySQL de manera visual. 

Descarregar i instal·lar de la [pàgina oficial](https://dev.mysql.com/downloads/workbench/)
