# Arxius binaris

## 1.4 Generació de codi intermedi (bytecode) i execució en màquines virtuals

Alguns llenguatges de programació, com **Java** o **C#**, no es compilen directament a codi màquina. En comptes d'això, es genera **codi intermedi**:

- **Codi intermedi (bytecode):** És un format intermig entre el codi font i el codi màquina. Aquest codi no és executat directament pel sistema operatiu, sinó per una màquina virtual.
- **Màquina virtual (JVM/.NET CLR):** Un entorn d'execució que interpreta el codi intermedi i el transforma a instruccions que el sistema pot entendre.


**Exemple pràctic:**
- **Java** compila el seu codi font a **bytecode** que s'executa a la **Java Virtual Machine (JVM)**, la qual permet la portabilitat del codi entre diferents sistemes operatius. **Kotlin** també genera un **bytecode** compatible amb les **JVM** de Java.

### Codi Binari i la Compilació Clàssica

Tradicionalment, quan un programa escrit en un llenguatge com **C** o **C++** es compila, el compilador genera **codi màquina** directament. Aquest codi està específicament adaptat a l'arquitectura del processador de l'ordinador on s'executarà el programa (per exemple, **x86** o **ARM**). Aquest tipus de codi binari és natiu i no requereix cap intermediari per ser executat pel sistema operatiu. Això permet que els programes siguin molt eficients en termes de rendiment, ja que no hi ha cap etapa d'interpretació o traducció addicional.

### Codi Intermedi (Bytecode)

Alguns llenguatges, com **Java**, **Kotlin**, **C#** o **Python**, utilitzen un enfocament diferent. En comptes de compilar el codi directament a codi màquina natiu, generen un **codi intermedi**, conegut com **bytecode**. Aquest bytecode no està destinat a ser executat directament pel processador, sinó que es troba en un format neutre, intermedi, que pot ser interpretat o compilat en temps d'execució per diferents màquines virtuals **(VM)**.

<center>
<img src="./assets/bytecode.webp" style="width: 90%; max-width: 500px">
</center>

**Característiques del Bytecode**:

- És una representació compacta i optimitzada del codi font que resulta més eficient per ser interpretada o compilar-se en temps d'execució.

- No està vinculat a cap arquitectura específica, cosa que permet que el mateix bytecode es pugui executar en qualsevol plataforma que tingui una màquina virtual compatible.

- És una combinació entre la portabilitat del codi font i l'eficiència d'una representació més propera a codi màquina.

### Màquina Virtual (JVM, .NET CLR)

Una **màquina virtual (VM)** és un entorn d'execució que permet interpretar o compilar **just-in-time (JIT)** el bytecode a codi màquina natiu del sistema on s'executa. Les màquines virtuals ofereixen una sèrie d'**avantatges**:

- **Portabilitat**: En lloc de compilar directament el codi a instruccions que només funcionin en un tipus específic de processador, el bytecode generat es pot executar en qualsevol sistema que disposi d'una màquina virtual compatible. Això és el que permet que programes escrits en Java es puguin executar tant en Windows, Linux, macOS o altres plataformes.

- **Seguretat i Control**: Les màquines virtuals permeten executar el bytecode en un entorn controlat, proporcionant mecanismes per evitar que el codi maliciós o defectuós pugui danyar el sistema. Per exemple, la Java Virtual Machine (JVM) aplica mecanismes de seguretat per assegurar-se que el codi que s'executa no realitzi operacions no autoritzades.

- **Optimització en Temps d'Execució**: Gràcies a tècniques com la compilació just-in-time (JIT), la màquina virtual pot convertir parts del bytecode en codi màquina natiu durant l'execució, optimitzant així el rendiment. Aquesta tècnica aprofita les característiques de l'arquitectura de la màquina on s'executa el programa per millorar l'eficiència.

Però les màquines virtuals també tenen algunes **desaventatges**:

- **Rendiment inferior al codi natiu**: Tot i les optimitzacions com la compilació JIT, el rendiment de les aplicacions executades en màquines virtuals sovint és inferior al del codi natiu compilat directament per a l'arquitectura de la màquina. La sobrecàrrega d'interpretació i traducció del bytecode pot afegir latència en l'execució.

- **Ús de recursos addicionals**: Les màquines virtuals requereixen memòria i capacitat de processament addicionals per executar-se, ja que afegeixen una capa d'abstracció sobre el sistema operatiu i el maquinari. Això pot fer que els programes siguin més pesants i consumeixin més recursos.

- **Temps d'arrencada més llarg**: L'inici d'una aplicació que depèn d'una màquina virtual pot ser més lent, ja que aquesta ha de carregar-se i interpretar el bytecode abans de començar a executar el codi. Aquest fet és particularment notori en sistemes que no utilitzen la compilació JIT.

- **Compatibilitat limitada amb el maquinari**: Tot i que les màquines virtuals proporcionen portabilitat del codi, tenen limitacions en accedir directament a components de maquinari especialitzat, com per exemple en sistemes amb requisits d'accés a GPU o dispositius d'E/S específics.

- **Dependència d'un entorn d'execució específic**: Els programes que es basen en màquines virtuals no es poden executar si no es disposa de la VM adequada instal·lada al sistema. Això crea una dependència en la instal·lació i la configuració correcta de la màquina virtual.

- **Sobrecàrrega de manteniment**: Les màquines virtuals, com la JVM o la CLR, necessiten ser actualitzades, i les noves versions poden introduir incompatibilitats o problemes de rendiment que requereixin modificacions en el codi del programa per assegurar una execució correcta.

- **Problemes de seguretat**: Tot i que les màquines virtuals poden millorar la seguretat gràcies al seu entorn controlat, també poden ser una font de vulnerabilitats si no s'actualitzen o gestionen correctament. A més, poden existir falles de seguretat en la màquina virtual mateixa que podrien comprometre el sistema.

### Màquines Virtuals Comunes

- **Java Virtual Machine (JVM)**: És la màquina virtual utilitzada per executar aplicacions escrites en Java o altres llenguatges que generen bytecode compatible amb la JVM, com Kotlin o Scala.

    El bytecode de Java és el resultat de la compilació del codi font en fitxers .class, que la JVM pot interpretar i executar.

    Gràcies a la JVM, un programa Java escrit en un entorn es pot executar en qualsevol altre sistema amb una JVM compatible, fent que Java sigui conegut per la seva filosofia "escriu una vegada, executa en qualsevol lloc" (Write Once, Run Anywhere).

- **.NET Common Language Runtime (CLR)**: La CLR és la màquina virtual utilitzada en l'ecosistema .NET per executar llenguatges com C#. 

    Compila codi font en Common Intermediate Language (CIL), que és l'equivalent al bytecode de Java.

    A través de la compilació JIT, la CLR converteix el CIL en codi màquina específic del sistema on s'està executant, permetent que aplicacions .NET siguin multiplataforma.

- **Python Virtual Machine (PVM)**: Python també utilitza un sistema de bytecode, que es genera quan un fitxer Python (.py) és executat. 

    Aquest bytecode es guarda en fitxers .pyc per ser interpretat per la Python Virtual Machine (PVM).

    La PVM interpreta el bytecode en temps real, però no aplica tècniques de compilació JIT com la JVM o la CLR, la qual cosa pot fer que Python sigui més lent en termes de rendiment en comparació amb altres llenguatges.

### Compilació JIT (Just-In-Time)

Una de les tècniques clau utilitzades per màquines virtuals modernes és la **compilació just-in-time (JIT)**. Aquesta tècnica implica compilar parts del bytecode en codi màquina natiu mentre el programa s'executa, en lloc de fer-ho durant la compilació inicial. Això té diversos avantatges:

- **Optimització basada en el context**: La màquina virtual pot optimitzar el codi mentre s'executa, depenent de com es comporta el programa en temps real.

- **Millor rendiment**: Un cop una part del bytecode es compila a codi màquina natiu, aquesta part s'executa a la velocitat del codi natiu.

    *Nota*: Aquest 'millor rendiment' es refereix en comparació a altres aplicacions que funcionen en màquines virtuals. La compilació JIT no pot superar en rendiment a les aplicacions binàries que funcionen directament sobre el processador, sense fer ús de màquines virtuals.

### Conclusions

El concepte de **bytecode** i **màquina virtual** permet portar el programari a un nou nivell de portabilitat i flexibilitat, assegurant que un sol codi intermedi pugui ser executat en múltiples sistemes. 

A més, tècniques com la compilació **JIT** ajuden a mitigar les pèrdues de rendiment, tot i mantenir els avantatges d'una execució segura i optimitzada.