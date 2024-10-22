# Llenguatges

## 1.5 Classificació dels llenguatges de programació

Els llenguatges de programació es poden classificar segons diferents criteris:

### **Nivell:**

- **Baix nivell:** Els llenguatges de baix nivell estan més a prop del llenguatge màquina i requereixen que el programador gestioni directament recursos del maquinari, com la memòria i els registres del processador.
    Exemples: **Assembly**, **C**.

- **Alt nivell:** Els llenguatges d'alt nivell són més propers al llenguatge humà i solen ser independents del maquinari. Aquests llenguatges són més fàcils d'entendre i utilitzen abstraccions per ocultar els detalls de la gestió de recursos del sistema. 
    Exemples: **Python**, **Java**.

### Gestió de memòria:

Hi ha diferents enfocaments per gestionar la memòria, cadascun amb les seves pròpies característiques i avantatges.

- **Gestió manual de memòria**: En llenguatges com C i C++, la gestió de la memòria és manual, i el programador és responsable d'assignar i alliberar memòria. Això proporciona més control sobre el maquinari, però també **introdueix la possibilitat d'errors**.

- **Garbage Collector**:  En llenguatges com Java, Python i C#, la gestió de la memòria és automàtica mitjançant un recolector d'escombraries (garbage collector). Aquest recolector d'escombraries és un procés que fa la gestió en paral·lel i necessita de recursos de processador i memòria per poder fer aquesta tasca. **Ofereix seguretat a canvi de sobrecarregar el sistema**.

- **ARC (Automatic reference counting)**: En llenguatges com Swift o RUST la gestió de memòria es fa al moment de compilar el programa. **Ofereix seguretat i eficiència** però pot provocar errors en casos de referències cícliques.
  
### Paradigma:

- **Imperatius:** En aquests llenguatges, el programador indica com s'ha d'executar una sèrie d'instruccions que alteren l'estat del programa. Es posa l'èmfasi en la seqüència de passos. 
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

- **Declaratius:** En els llenguatges declaratius, el programador especifica què es vol aconseguir, però no el com. S'enfoca en el resultat, deixant que el llenguatge s'encarregui de la implementació. 
    Exemples: **SQL**, **Prolog**.

```sql
SELECT nom, edat FROM estudiants WHERE edat > 18;
```

- **Orientats a objectes:** Els llenguatges orientats a objectes organitzen el codi en objectes, que encapsulen dades (atributs) i comportament (mètodes). Aquest paradigma és útil per gestionar la complexitat mitjançant la reutilització i modularitat del codi.
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

- **Funcional:** Els llenguatges funcionals posen l'èmfasi en les funcions matemàtiques pures i eviten l'ús d'estats i efectes laterals. Les funcions són ciutadanes de primera classe i es poden passar com a arguments o retornar.
    Exemples: **Haskell**, **Lisp**.

```haskell
sumatori :: [Int] -> Int
sumatori nums = foldl (+) 0 nums

main = print (sumatori [1, 2, 3, 4, 5])  -- Sortida: 15
```
