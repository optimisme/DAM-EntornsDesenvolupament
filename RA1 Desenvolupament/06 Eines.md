# Eines

## 1.6 Funcionalitat de les eines utilitzades en el desenvolupament de programari

Les eines utilitzades durant el desenvolupament de programari faciliten el treball dels programadors i gestionen el cicle de vida del projecte. Les més comunes inclouen:

### **1. Entorns de Desenvolupament Integrat (IDE)**

Els **Entorns de Desenvolupament Integrat (IDE)** són aplicacions que ofereixen un conjunt d'eines integrades per facilitar l'escriptura, prova i depuració de codi. Inclouen editors de codi, depuradors, intèrprets, compiladors i altres funcionalitats per agilitzar el flux de treball dels desenvolupadors.

-**Funcions comunes d'un IDE:**
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

- **Compilació automàtica:** Compilen el codi font automàticament després de cada canvi, per assegurar-se que no es trenqui cap funcionalitat.

- **Execució de proves:** Corren automàticament les suites de proves per verificar que el codi nou no introdueixi errors.

- **Desplegament automàtic:** Algunes eines permeten desplegar el codi a entorns de producció de manera automàtica després de completar el procés de compilació i proves.

- **Notificacions d'errors:** Notifiquen als desenvolupadors immediatament si algun canvi introdueix errors en el sistema.

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