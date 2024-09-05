# RA1: Elements i eines en el desenvolupament d'un programa informàtic

## 1.1 Relació dels programes amb els components del sistema informàtic

Els programes informàtics són conjunts d'instruccions que permeten realitzar diverses tasques sobre un sistema informàtic. Aquests programes interactuen amb diferents components del sistema perquè puguin ser executats correctament. 

<center>
<img src="./assets/motherboard.png" style="max-width: 350px">
</center>

### **Memòria (RAM)**

- La **memòria RAM (Random Access Memory)** és una part essencial del sistema informàtic. És un tipus de memòria volàtil que emmagatzema dades temporalment i s'utilitza per carregar les instruccions dels programes mentre s'executen.
- Els programes s’han de carregar a la RAM perquè la **CPU** pugui accedir ràpidament a les seves instruccions. La velocitat d’accés a la RAM és molt superior a la dels discos durs, fet que permet una execució eficient dels programes.
- Cada procés en execució té assignat un espai a la RAM on guarda les instruccions i les dades necessàries per funcionar. Quan aquest espai es queda curt, el sistema operatiu pot utilitzar la **memòria virtual**, emmagatzemant part d’aquesta informació al disc dur, però amb un rendiment significativament inferior.
  
**Exemple pràctic:**
- Quan obres un navegador web com **Google Chrome**, el sistema carrega el programa a la RAM, de manera que pugui respondre ràpidament a les teves accions, com obrir una nova pestanya o carregar una pàgina web. Si la memòria RAM disponible és insuficient, el sistema pot utilitzar el disc dur per gestionar les tasques, però això alentirà el rendiment.

### **Processador (CPU)**

- El **processador** (o **CPU**, Central Processing Unit) és el component principal del sistema que s'encarrega d'executar les instruccions dels programes. Cada instrucció que s'executa dins d'un programa és processada directament per la CPU.
- La CPU segueix un cicle bàsic d’operacions: **[Fetch-Decode-Execute](https://adacomputerscience.org/concepts/arch_fe_cycle?examBoard=ada&stage=all)**:

<center>
<img src="./assets/fetchdecode.svg" style="max-width: 350px">
</center>


  - **Fetch (Obtenció):** Recull les instruccions del programa que es troben emmagatzemades a la RAM.
  - **Decode (Descodificació):** Interpreta aquestes instruccions per saber què ha de fer.
  - **Execute (Execució):** Realitza l’operació (com sumar números, moure dades de la memòria, o controlar un perifèric).
- La **velocitat del processador**, expressada en **gigahertzs (GHz)**, determina quantes operacions pot realitzar per segon. Una CPU més ràpida pot processar més instruccions i, per tant, fer que els programes s’executin més ràpidament.
- Els processadors moderns tenen diversos **nuclis** (cores), cosa que els permet executar múltiples operacions simultàniament (**multithreading**), millorant encara més el rendiment.

**Exemple pràctic:**
- En un programa que suma dos números, la CPU obtindrà les instruccions per sumar, identificarà les dades involucrades (els dos nombres) i executarà l'operació. Un processador amb diversos nuclis pot fer altres tasques simultàniament, com reproduir música mentre es realitza aquest càlcul.

### **Perifèrics**

- Els **perifèrics** són els dispositius d'entrada i sortida que permeten la interacció entre el sistema informàtic i l'usuari o altres sistemes. Aquests dispositius permeten capturar dades o presentar resultats d'un programa.
- **Perifèrics d'entrada:** Són dispositius que permeten introduir informació al sistema. Exemples: teclat, ratolí, micròfon, escàner.
- **Perifèrics de sortida:** Són dispositius que permeten visualitzar o emmagatzemar la informació processada pel sistema. Exemples: pantalla, impressora, altaveus.
- **Perifèrics d'emmagatzematge:** S'utilitzen per guardar dades de manera permanent o temporal. Exemples: discos durs, unitats SSD, memòries USB.
  
**Exemple pràctic:**

- Quan escrius un document a l'ordinador, el teclat (perifèric d'entrada) envia els caràcters al processador, que els processa i els mostra a la pantalla (perifèric de sortida). Si decideixes guardar el document, les dades es desaran en un disc dur o una unitat SSD (perifèrics d'emmagatzematge).


## 1.2 Fases de desenvolupament d'una aplicació informàtica

El procés de desenvolupament de programes segueix un conjunt de fases, que asseguren que el producte final compleixi els requisits del client i funcioni correctament. Aquestes fases són iteratives en molts enfocaments moderns, especialment en metodologies àgils, on el producte es va refinant i millorant al llarg de diversos cicles.

### 1. **Anàlisi de requeriments**

L'**anàlisi de requeriments** és la primera fase del desenvolupament i una de les més crucials. Es tracta de definir amb claredat què ha de fer el sistema que es vol desenvolupar:

- **Objectius:** S'identifiquen els objectius generals que ha de complir el programari, tant des del punt de vista funcional com no funcional.
- **Funcionalitats:** Es recullen i descriuen les característiques que el sistema haurà de proporcionar. Això inclou tasques específiques que l'usuari podrà realitzar.
- **Limitacions:** Es defineixen els requisits tècnics, legals i de rendiment, així com qualsevol restricció que afecti el desenvolupament, com el temps, pressupost, o limitacions tecnològiques.

**Exemple pràctic:**
- Si es desenvolupa una aplicació de comerç electrònic, durant l'anàlisi de requeriments es defineix que l'usuari ha de poder crear un compte, cercar productes, afegir-los a la cistella i realitzar compres segures amb diversos mètodes de pagament.

### 2. **Disseny**

La fase de **disseny** implica la planificació detallada de com es construirà el sistema, a partir dels requeriments definits:

- **Disseny de l'arquitectura:** Es defineix l'estructura general del sistema. Això inclou com interactuaran els diferents components del sistema (back-end, front-end, bases de dades, etc.).
- **Disseny de les dades:** S'escull l'estructura de dades adequada (bases de dades relacionals o NoSQL, per exemple) i es defineixen els esquemes de les taules o documents.
- **Algorismes:** Es seleccionen els algorismes més eficients per resoldre les tasques que el sistema ha de realitzar, com ara cerques, ordenació, etc.
- **Disseny de la interfície d'usuari (UI):** Si s'aplica, es defineix com serà la interfície amb la qual interactuarà l'usuari, incloent-hi la disposició de botons, menús, formularis, etc.

**Exemple pràctic:**
- Per a una aplicació de comerç electrònic, durant el disseny es defineix l'arquitectura MVC (Model-Vista-Controlador), la base de dades MySQL per emmagatzemar informació sobre els usuaris, productes i comandes, i es crea un disseny atractiu per a la pàgina de compra.

### 3. **Desenvolupament o codificació**

La **codificació** és la fase en la qual es passa del disseny teòric a la implementació pràctica. Els desenvolupadors escriuen el codi font que materialitza les funcionalitats i els algorismes dissenyats prèviament:

- **Selecció del llenguatge de programació:** Es tria el llenguatge o llenguatges de programació adequats segons el projecte. Per exemple, **JavaScript** per al front-end, **Python** o **Java** per al back-end.
- **Escripció del codi:** Els programadors escriuen el codi per implementar cada funcionalitat, seguint les bones pràctiques de programació, com modularitat, reusabilitat i legibilitat.
- **Gestió del codi:** Durant aquesta fase, és fonamental utilitzar eines com **Git** per controlar les versions del codi i facilitar el treball col·laboratiu entre diversos desenvolupadors.

**Exemple pràctic:**
- Un equip de desenvolupadors implementa una API REST en **Node.js** per gestionar les operacions de productes, clients i comandes, mentre un altre equip crea la interfície d'usuari amb **React**.

### 4. **Proves (Testing)**

La fase de **proves** és crucial per assegurar que el programari compleixi els requeriments i funcioni sense errors:

- **Proves unitàries:** Es proven individualment les funcions o mòduls per garantir que cadascuna realitza la seva tasca correctament.
- **Proves d'integració:** Es verifica que els diferents components del sistema interactuen correctament entre si.
- **Proves d'acceptació:** Es comprova que el sistema compleix els requisits del client i que les funcionalitats funcionen segons s'esperava.
- **Proves de rendiment i seguretat:** Es mesura la velocitat, l'eficiència i la resistència del sistema a possibles atacs, assegurant que pot gestionar grans càrregues o situacions extremes.

**Exemple pràctic:**
- Un equip de QA realitza proves automàtiques en les APIs del sistema de comerç electrònic utilitzant **JUnit** i eines com **Postman** per assegurar que els endpoints compleixen les expectatives funcionals i de seguretat.

### 5. **Implementació**

La fase d'**implementació** és quan el programari es posa en producció, de manera que pugui ser utilitzat pels usuaris finals:

- **Desplegament:** S'instal·la el programari en l'entorn on serà utilitzat, que pot ser un servidor local, un servidor remot o el núvol.
- **Configuració:** Es realitzen ajustos específics per assegurar que el programari funciona correctament amb els sistemes existents.
- **Llançament:** Després de les proves finals, el sistema es llança per a l'ús dels usuaris finals. Aquesta fase pot incloure formació als usuaris i suport tècnic inicial.

**Exemple pràctic:**
- Es desplega l'aplicació de comerç electrònic en un servidor **AWS** utilitzant **Docker** per contenir les diferents parts del sistema, i es configura per a l'accés global a través d'Internet.

### 6. **Manteniment**

El **manteniment** és una fase contínua que comença després de la implementació del programari. Inclou:

- **Correcció d'errors:** A mesura que s'utilitza el sistema, poden sorgir errors o problemes no detectats durant les proves. Aquests s'han de corregir amb actualitzacions del programari.
- **Actualitzacions i millores:** Es poden afegir noves funcionalitats o millorar-ne d'existents en funció dels canvis en les necessitats dels usuaris o l'evolució tecnològica.
- **Suport tècnic:** Es proporciona suport als usuaris finals per resoldre dubtes o incidències tècniques.

**Exemple pràctic:**
- Després del llançament de l'aplicació de comerç electrònic, es detecten alguns errors en els mètodes de pagament en determinades regions. Els desenvolupadors els corregeixen i publiquen una actualització del sistema.

<center>
<img src="./assets/lifecycle.png" style="max-width: 350px">
</center>

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

## 1.4 Generació de codi intermedi (bytecode) i execució en màquines virtuals

Alguns llenguatges de programació, com **Java** o **C#**, no es compilen directament a codi màquina. En comptes d'això, es genera **codi intermedi**:

- **Codi intermedi (bytecode):** És un format intermig entre el codi font i el codi màquina. Aquest codi no és executat directament pel sistema operatiu, sinó per una màquina virtual.
- **Màquina virtual (JVM/.NET CLR):** Un entorn d'execució que interpreta el codi intermedi i el transforma a instruccions que el sistema pot entendre.

<center>
<img src="./assets/bytecode.webp" style="max-width: 350px">
</center>

**Exemple pràctic:**
- **Java** compila el seu codi font a **bytecode** que s'executa a la **Java Virtual Machine (JVM)**, la qual permet la portabilitat del codi entre diferents sistemes operatius. **Kotlin** també genera un **bytecode** compatible amb les **JVM** de Java.

## 1.5 Classificació dels llenguatges de programació

Els llenguatges de programació es poden classificar segons diferents criteris:

### **Nivell:**
**Baix nivell:** Els llenguatges de baix nivell estan més a prop del llenguatge màquina i requereixen que el programador gestioni directament recursos del maquinari, com la memòria i els registres del processador.
    Exemples: **Assembly**, **C**.

**Alt nivell:** Els llenguatges d'alt nivell són més propers al llenguatge humà i solen ser independents del maquinari. Aquests llenguatges són més fàcils d'entendre i utilitzen abstraccions per ocultar els detalls de la gestió de recursos del sistema. 
    Exemples: **Python**, **Java**.

### Gestió de memòria:

Hi ha diferents enfocaments per gestionar la memòria, cadascun amb les seves pròpies característiques i avantatges.

**Gestió manual de memòria**: En llenguatges com C i C++, la gestió de la memòria és manual, i el programador és responsable d'assignar i alliberar memòria. Això proporciona més control sobre el maquinari, però també **introdueix la possibilitat d'errors**.

**Garbage Collector**:  En llenguatges com Java, Python i C#, la gestió de la memòria és automàtica mitjançant un recolector d'escombraries (garbage collector). Aquest recolector d'escombraries és un procés que fa la gestió en paral·lel i necessita de recursos de processador i memòria per poder fer aquesta tasca. **Ofereix seguretat a canvi de sobrecarregar el sistema**.

**ARC (Automatic reference counting)**: En llenguatges com Swift o RUST la gestió de memòria es fa al moment de compilar el programa. **Ofereix seguretat i eficiència** però pot provocar errors en casos de referències cícliques.
  
### Paradigma:

**Imperatius:** En aquests llenguatges, el programador indica com s'ha d'executar una sèrie d'instruccions que alteren l'estat del programa. Es posa l'èmfasi en la seqüència de passos. 
    Exemples: **C**, **Java**.

```java
public class Main {
    public static void main(String[] args) {
        int resultat = 0;
        for (int i = 1; i <= 5; i++) {
            resultat += i;
        }
        System.out.println("Sumatori: " + resultat);
    }
}
```

**Declaratius:** En els llenguatges declaratius, el programador especifica què es vol aconseguir, però no el com. S'enfoca en el resultat, deixant que el llenguatge s'encarregui de la implementació. 
    Exemples: **SQL**, **Prolog**.

```sql
SELECT nom, edat FROM estudiants WHERE edat > 18;
```

**Orientats a objectes:** Els llenguatges orientats a objectes organitzen el codi en objectes, que encapsulen dades (atributs) i comportament (mètodes). Aquest paradigma és útil per gestionar la complexitat mitjançant la reutilització i modularitat del codi.
    Exemples: **Java**, **Python**.

```python
class Persona:
    def __init__(self, nom, edat):
        self.nom = nom
        self.edat = edat

    def presentacio(self):
        return f"Soc {self.nom} i tinc {self.edat} anys."

persona = Persona("Anna", 25)
print(persona.presentacio())
```

**Funcional:** Els llenguatges funcionals posen l'èmfasi en les funcions matemàtiques pures i eviten l'ús d'estats i efectes laterals. Les funcions són ciutadanes de primera classe i es poden passar com a arguments o retornar.
    Exemples: **Haskell**, **Lisp**.

```haskell
sumatori :: [Int] -> Int
sumatori nums = foldl (+) 0 nums

main = print (sumatori [1, 2, 3, 4, 5])  -- Sortida: 15
```

## 1.6 Funcionalitat de les eines utilitzades en el desenvolupament de programari

Les eines utilitzades durant el desenvolupament de programari faciliten el treball dels programadors i gestionen el cicle de vida del projecte. Les més comunes inclouen:

### **1. Entorns de Desenvolupament Integrat (IDE)**

Els **Entorns de Desenvolupament Integrat (IDE)** són aplicacions que ofereixen un conjunt d'eines integrades per facilitar l'escriptura, prova i depuració de codi. Inclouen editors de codi, depuradors, intèrprets, compiladors i altres funcionalitats per agilitzar el flux de treball dels desenvolupadors.

**Funcions comunes d'un IDE:**
  - **Editor de codi:** Amb suport per a la sintaxi i completat automàtic.
  - **Depurador:** Permet executar el codi pas a pas, afegir punts de parada (breakpoints) i revisar l'estat de les variables.
  - **Integració amb sistemes de control de versions:** Facilita la gestió de canvis i col·laboració entre equips.
  - **Execució i compilació integrades:** Proporciona eines per executar el programa directament dins de l'IDE.

**Exemples d'IDE:**

  - **Visual Studio:** IDE per a molts llenguatges com **C#**, **C++**, **Python**, entre d'altres.
  - **IntelliJ IDEA:** IDE per a **Java** i altres llenguatges amb fort enfocament en el desenvolupament orientat a objectes.
  - **PyCharm:** IDE especialitzat per a **Python** que ofereix eines per al desenvolupament en **Python** i **Django**.



### **2. Sistemes de Control de Versions**

Els **Sistemes de Control de Versions** són eines que permeten gestionar els canvis al codi font al llarg del temps, mantenint un historial de totes les modificacions realitzades, cosa que facilita la col·laboració en equips de desenvolupadors.

**Funcions clau d'un VCS:**

  - **Gestió de versions:** Permet revisar versions anteriors del projecte i desfer canvis si cal.
  - **Branching i merging:** Facilita la creació de branques paral·leles per desenvolupar funcionalitats o corregir errors, i després ajuntar-les amb el codi principal.
  - **Col·laboració:** Permet que múltiples desenvolupadors treballin en el mateix projecte de manera sincronitzada.
  - **Històric:** Manté un registre de totes les modificacions realitzades, indicant qui va fer cada canvi i quan.

**Exemple de Git:**

Amb **Git**, un desenvolupador pot crear un nou **branch** per implementar una funcionalitat nova sense afectar el codi principal:
```bash
git checkout -b nova-funcionalitat
# Després de fer els canvis, pots ajuntar la branca amb el codi principal
git checkout main
git merge nova-funcionalitat
```

### 3. Eines de compilació i integració contínua

Les eines de **compilació** i **integració contínua (CI)** automatitzen el procés de compilació, prova i desplegament del codi. Aquestes eines s'utilitzen per garantir que els canvis fets al codi s'integrin de manera segura i eficient, reduint errors i assegurant que el codi sigui sempre executable.

**Compilació automàtica:** Compilen el codi font automàticament després de cada canvi, per assegurar-se que no es trenqui cap funcionalitat.

**Execució de proves:** Corren automàticament les suites de proves per verificar que el codi nou no introdueixi errors.

**Desplegament automàtic:** Algunes eines permeten desplegar el codi a entorns de producció de manera automàtica després de completar el procés de compilació i proves.

**Notificacions d'errors:** Notifiquen als desenvolupadors immediatament si algun canvi introdueix errors en el sistema.

**Exemples d'eines de CI:**

  - **Jenkins:** Una de les eines d'integració contínua més utilitzades. Ofereix una gran flexibilitat per automatitzar la compilació, prova i desplegament de projectes.

  - **Travis CI:** Eina d'integració contínua molt popular en projectes **open source** que s'integra fàcilment amb **GitHub**.

### 4. Eines de depuració

Les eines de **depuració** permeten als desenvolupadors analitzar el comportament del codi en temps d'execució, identificant i corregint errors o problemes de rendiment. Aquestes eines són especialment útils per resoldre problemes de codi complexos.

- **Execució pas a pas:** Permet executar el codi línia per línia per veure com canvia l'estat del programa.

- **Breakpoints (punts de parada):** Permeten aturar l'execució del programa en un punt determinat per inspeccionar variables i l'estat actual.

- **Inspecció de variables:** Permet veure el valor de les variables en temps d'execució, ajudant a identificar comportaments inesperats.

### 5. Eines de prova automàtica

Les eines de **prova automàtica** permeten als desenvolupadors escriure tests que verifiquen automàticament el funcionament correcte del codi. Aquestes proves s'executen de manera automàtica, ja sigui durant el desenvolupament o com a part d'un procés d'integració contínua.

- **Proves unitàries:** Verifiquen el correcte funcionament de petites unitats del codi, com funcions o mètodes.

- **Proves d'integració:** Asseguren que diferents components del sistema treballin correctament junts.

- **Proves de rendiment:** Mesuren l'eficiència i rendiment del codi sota diferents condicions.

**Exemple amb JUnit (Prova unitària en Java):**
```java
import org.junit.Test;
import static org.junit.Assert.assertEquals;

public class CalculadoraTest {
    @Test
    public void testSuma() {
        Calculadora calc = new Calculadora();
        int resultat = calc.suma(2, 3);
        assertEquals(5, resultat);
    }
}
```

## 1.7 Característiques i escenaris d'ús de les metodologies àgils de desenvolupament de programari

Les **metodologies àgils** són un conjunt de valors i principis establerts en el **Manifest Àgil** (2001) per a desenvolupar programari de manera flexible, col·laborativa i iterativa. Aquestes metodologies responen a la necessitat d’adaptació ràpida als canvis i a la creixent importància de satisfer les expectatives del client amb un lliurament ràpid i constant de valor. Entre les metodologies més conegudes hi ha **Scrum**, **Kanban** i **Extreme Programming (XP)**, que comparteixen una filosofia comuna però difereixen en els seus enfocaments i pràctiques concretes.

### Principals característiques de les metodologies àgils

**Iteracions curtes i contínues (sprints):**
   - El desenvolupament es divideix en cicles curts i repetitius anomenats *sprints* (generalment d'1 a 4 setmanes).
   - Cada *sprint* culmina amb un lliurament de programari funcional, el qual és una part del producte final, permetent detectar problemes o ajustos de manera primerenca.

**Lliurament de valor contínuament:**
   - Cada iteració busca lliurar valor tangible al client, proporcionant funcions completes o components que es poden avaluar i utilitzar.
   - Això permet mantenir el focus en el valor real per al negoci en lloc de complir simplement requisits tècnics.

**Col·laboració constant amb el client:**
   - El client o el representant del client (Product Owner en Scrum, per exemple) està involucrat activament en el procés de desenvolupament, revisant el progrés i oferint feedback constant.
   - Aquest feedback continu ajuda a ajustar el producte a les necessitats canviants del mercat o del client.

**Autogestió de l'equip:**
   - Els equips àgils són cross-funcionals i autònoms, és a dir, són responsables de planificar, executar i ajustar el treball sense una gestió centralitzada.
   - Això afavoreix la presa de decisions ràpida i fomenta la responsabilitat i la col·laboració interna.

**Flexibilitat i adaptabilitat:**
   - L’èmfasi no està tant en seguir un pla rígid com en adaptar-se als canvis de requisits que puguin sorgir durant el desenvolupament.
   - La prioritat es revisa sovint i les tasques s’adapten a les necessitats actuals del projecte.

**Millora contínua:**
   - Després de cada *sprint*, l’equip participa en una revisió del procés (*retrospectiva*), on s’identifiquen àrees de millora per a futurs cicles.
   - Aquest compromís amb la millora contínua permet optimitzar el procés i augmentar la qualitat del producte a llarg termini.

<center>
<img src="./assets/scrum.jpg" style="max-width: 350px">
</center>

### Kanban Board

El **Kanban Board** és una eina visual utilitzada per gestionar el flux de treball en processos de desenvolupament, sol tenir diverses columnes que representen els diferents estats en què es poden trobar les tasques o elements de treball dins del procés. Les columnes més habituals són:

**Backlog**: Llista de tasques pendents ordenades per prioritat. Que encara no han estat valorades ni posades a la llista 'To Do'.

**To Do**: Tasques acceptades que cal desenvolupar en aquest Sprint.

**In Progress**: Tasques que s’estan desenvolupant actualment.

**Done**: Tasques que ja han estat completades.



<center>
<img src="./assets/kanbanboard.jpg" style="max-width: 350px">
</center>

### Escenaris d'ús de les metodologies àgils

Les metodologies àgils són especialment útils en entorns on els requisits canvien de manera freqüent o on es necessita una resposta ràpida als canvis de mercat o tecnologia. A continuació es detallen alguns escenaris típics d'ús:

**Desenvolupament de productes digitals:** Projectes de desenvolupament de programari on hi ha una alta incertesa sobre els requisits finals o on es busca una iteració constant amb el client, com ara aplicacions web o mòbils.
  
**Projectes amb deadlines ajustats:** En projectes on cal lliurar una solució funcional en poc temps, les iteracions curtes permeten presentar un producte mínim viable (MVP) ràpidament.

**Equips distribuïts:** La metodologia àgil, amb les seves reunions curtes però freqüents, fomenta la comunicació efectiva i la col·laboració, fins i tot en equips distribuïts geogràficament.

**Innovació i R+D:** Quan es treballa en projectes d’investigació o desenvolupament d’idees noves, l'agilitat permet experimentar, fallar ràpid i pivotar de manera eficient.

### Beneficis de les metodologies àgils

**Major satisfacció del client:** El client veu progressos freqüents i pot ajustar les prioritats segons sigui necessari.

**Reducció del risc:** Els problemes es detecten més ràpidament gràcies a les iteracions curtes, reduint així el risc de grans fallides al final del projecte.

**Motivació de l'equip:** La participació activa en la presa de decisions i l'autonomia milloren la motivació i el compromís dels membres de l’equip.

**Alta qualitat del producte:** Les revisions contínues del producte i del procés de desenvolupament asseguren una qualitat elevada i millores contínues.

**Exemples pràctics:**
- **[Scrum](https://www.escueladenegociosydireccion.com/revista/business/scrum-framework-agiliza-trabajo-equipo/):** Metodologia àgil popular amb rols definits com Product Owner, Scrum Master i l’equip de desenvolupament. S’organitza en sprints de 2-4 setmanes.
- **Kanban:** Es basa en visualitzar el flux de treball i limitar el treball en procés per millorar l'eficiència.

