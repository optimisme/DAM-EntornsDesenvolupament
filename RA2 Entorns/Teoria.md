# RA2 Avalua entorns integrats de desenvolupament analitzant-ne les característiques per editar codi font i generar executables.

Un entorn de desenvolupament software (o IDE, Integrated Development Environment) és un conjunt d'eines que permeten als programadors escriure, provar i depurar codi de manera més eficient. Aquestes eines inclouen, sovint, un editor de codi, eines de compilació i depuració, gestió de versions i altres utilitats.

### Terminal/Eina de comandes

L'eina de comandes (també coneguda com a terminal o consola) és una interfície basada en text que permet als desenvolupadors executar ordres del sistema, gestionar fitxers, compilar codi, executar scripts i utilitzar eines de control de versions com Git. Sovint és l'eina central per interactuar amb el sistema operatiu o altres eines de programació sense interfície gràfica.

**Linux i macOS** tenen Terminals compatibles amb UNIX

**Windows** té diferents opcions de terminal:

- Terminal clàssic
- Terminal PowerShell
- Terminal WSL Linux (necessita instal·lació apart)

### VS Code

Visual Studio Code és un editor de codi lleuger i extensible que proporciona una experiència IDE completa. És altament personalitzable a través d'extensions que permeten afegir funcionalitats com depuració, autocompletat de codi, suport per a múltiples llenguatges de programació i integració amb Git. VS Code és molt popular perquè equilibra potència i simplicitat.

### GitHub

GitHub és una plataforma de control de versions basada en Git que permet als desenvolupadors col·laborar en projectes, gestionar versions de codi, revisar canvis i compartir projectes públicament o privadament. 

En conjunt, aquests tres elements formen una base essencial en el procés de desenvolupament modern:

- **Eina de comandes** per la interacció directa amb el sistema.
- **Visual Studio Code** com a entorn per escriure i depurar codi.
- **GitHub** per a la gestió del codi i la col·laboració entre equips.

## 2.1- Instal·la entorns de desenvolupament, propietaris i lliures.

Descarrega i instal·la els següents programes:

**[Visual Studio Code](https://code.visualstudio.com/download)**

**[GitHub Desktop](https://desktop.github.com/download/)**

Per linux, GitHub Desktop s'instal·la des del **Terminal** amb aquestes comandes:

TODO

```bash
wget -qO - https://apt.packages.shiftkey.dev/gpg.key | gpg --dearmor | sudo tee /usr/share/keyrings/shiftkey-packages.gpg > /dev/null
```
```bash
sudo sh -c 'echo "deb [arch=amd64 signed-by=/usr/share/keyrings/shiftkey-packages.gpg] https://apt.packages.shiftkey.dev/ubuntu/ any main" > /etc/apt/sources.list.d/shiftkey-packages.list'
```
```bash
sudo apt update 
```
```bash
sudo apt install github-desktop
```

**Python**

TODO

**Java SDK**

TODO

**Maven**

TODO

**WSL, Windows Subsystem for Linux**

A Windows es pot instal·lar un entorn de Terminal basat amb Linux, fent ús de WSL.

Per fer-ho:

- Instal·lar Ubuntu des de la botiga d'aplicacions
- Obrir un terminal 'Ubuntu'

TODO

## 2.2 - Afegeix i elimina mòduls a l'entorn de desenvolupament.

## 2.3 - Personalitza i automatitza l'entorn de desenvolupament.

## 2.4 - Configura el sistema d'actualització de l'entorn de desenvolupament.

## 2.5 - Genera executables a partir de codi font de diferents llenguatges en un mateix entorn de desenvolupament.

## 2.6 - Genera executables a partir d'un mateix codi font amb diversos entorns de desenvolupament.

## 2.7 - Identifica les característiques comunes i específiques de diversos entorns de desenvolupament.