# Compilació

## 1.3 Diferència entre codi font, objecte i executable

- **Codi font:** És el conjunt d'instruccions escrites en un llenguatge de programació que poden ser llegides per humans. Exemples: un programa en **Python**, **C++** o **Java**.

**Exemple en Python**:
  ```python
  def suma(a, b):
      return a + b

  resultat = suma(3, 5)
  print(resultat)
```

- **Codi objecte:** És el resultat de la compilació parcial del codi font. Conté instruccions en llenguatge màquina, però encara no està preparat per ser executat perquè no inclou totes les referències a llibreries i format del sistema operatiu.

- **Executable:** És el fitxer final generat després de la compilació, que pot ser executat directament per la màquina. En el cas de **Windows**, els fitxers **.exe** són executables.

```bash
./programa      # En Linux
programa.exe    # En Windows
```

- **Llibreries:** Són col·leccions de funcions o recursos que es poden reutilitzar en múltiples programes. Permeten als desenvolupadors evitar la reescriptura de codi repetitiu i facilitar la modularització del codi.

```python
import math   # Importa una llibreria

arrel = math.sqrt(16)
print(arrel)  # Sortida: 4.0
```

<center>
<img src="./assets/compilacioC.png" style="width: 90%; max-width: 500px">
</center>

### Tipus d'arxius binaris

Segons la seva funció i sistema operatiu, hi ha els següents tipus d'arxius binaris:

**Executables**:

- **<ins>Arxius +x</ins> (Executables a Linux i macOS)**:

    En Linux i macOS, els programes executables no tenen una extensió específica com en Windows. Un programa executable es pot identificar pel seu permís d'execució (generalment marcat amb x en els permisos del sistema de fitxers).

    *Exemple*: Els executables a Linux i macOS es poden executar escrivint el seu nom precedit per **./**.

```bash
./programa  # Executa el fitxer 'programa' a Linux o macOS
```

- **<ins>.exe</ins> (Executable Windows)**:

    Un fitxer .exe és un programa executable independent. Conté el codi necessari per ser carregat i executat per la màquina.

    Inclou totes les instruccions necessàries perquè el sistema operatiu sàpiga com executar el programa.

    *Exemples*: aplicacions com Google Chrome o Microsoft Word són distribuïdes com arxius .exe.

- **<ins>.so</ins> (Llibreries a Linux)**:

    A Linux, les llibreries dinàmiques tenen l'extensió .so (Shared Object). Les llibreries **.so** es carreguen dinàmicament durant l'execució d'un programa, permetent compartir funcionalitats entre múltiples aplicacions.

    *Exemples*: llibreries en paquets de sistemes com glibc, la llibreria estàndard de C a Linux.

- **<ins>.dylib</ins> (Llibreries a macOS)**:

    A macOS, les llibreries dinàmiques es denominen .dylib (Dynamic Library). Aquestes llibreries es carreguen quan un programa les requereix, permetent la reutilització de codi entre múltiples aplicacions.

    *Exemples*: Llibreries del sistema operatiu macOS que són utilitzades per diverses aplicacions, com la llibreria de gestió gràfica.

- **<ins>.dll</ins> (Dynamic Link Library a Windows)**:

    Un fitxer .dll és una llibreria dinàmica que conté codi i dades que poden ser utilitzats per diversos programes.

    No es pot executar de manera autònoma com un .exe, sinó que ha de ser carregat per un executable o un altre procés.

    Les .dll permeten compartir funcionalitats comunes entre múltiples programes per evitar la duplicació de codi.

    *Exemples*: una llibreria .dll podria gestionar les crides a la impressora en diversos programes, de manera que tots ells facin ús del mateix codi per a aquesta funció.

### Taula comparativa de carpetes d'arxius binaris

| Sistema | Tipus de Fitxer | Carpeta Habitual |
| ----- | ----- | ----- |
| | | |
| **Linux** | Executable `+x` | `/usr/bin/` |
| | | `/usr/local/bin/` |
| | | `/bin/` |
| | | `/sbin/` |
| | Llibreria `.so` | `/usr/lib/` |
| | | `/usr/local/lib/` |
| | | `/lib/` |
| | | `/lib64/` |
| | | |
| **macOS** | Executable `+x` | `/Applications/` |
| | | `/usr/bin/` |
| | | `/usr/local/bin/` |
| | Llibreria `.dylib` | `/usr/lib/` |
| | | `/usr/local/lib/` |
| | | Dins del paquet de cada aplicació |
| | | |
| **Windows** | Executable `.exe` | `C:\Program Files\` |
| | | `C:\Program Files (x86)\` |
| | |  `C:\Users\<usuari>\AppData\Local\Programs\` |
| | Llibreria `.dll` | `C:\Windows\System32\` |
| | | `C:\Program Files\` | |
