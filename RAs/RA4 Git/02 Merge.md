# Merge (unir)

Sovint, un cop hem estat treballant amb una branca, volem unir (merge) els canvis amb la branca principal.

Els passos per ajuntar dues branques són:

- Crear una **Pull request**, que és una petició per revisar i fusionar els canvis a la branca principal
- Fer un **merge**, que és  l'acció tècnica de combinar els canvis

## Pull request

Per fer una **pull request** amb **GitHub Desktop***:

<center>
<img src="./assets/git0200.png" style="width: 90%; max-width: 600px">
</center>

Apretar aquest botó ens portarà cap a la pàgina web de **GitHub** que correspon a aquesta petició. 

En aquesta pàgina hem de fer una explicació de perquè volem fusionar la nostra branca amb la branca principal.

**Nota:** Normalment, aquest pas es fa per arreglar errors, i al fer la **pull request** s'explica quins canvis s'han fet al codi per arreglar l'error.

<center>
<img src="./assets/git0201.png" style="width: 90%; max-width:600px">
</center>

Després els els usuaris amb permissos per fer **pull request** hauràn de validar i aprovar els canvis al codi principal.

<center>
<img src="./assets/git0203.png" style="width: 90%; max-width:600px">
</center>

Si sou vosaltres mateixos, el l'aprovació l'heu de fer des del mateix usuari.

<center>
<img src="./assets/git0204.png" style="width: 90%; max-width:600px">
</center>

Finalment, es pot esborrar la branca que s'ha fusionat.

<center>
<img src="./assets/git0205.png" style="width: 90%; max-width:600px">
</center>

Finalment, ens hem d'assegurar de tornar a escollir la branca principal i descarregar els canvis remots:

```bash
git checkout main
git pull origin main
```

<style>
.image-container {
    align-items: flex-end;
    display: flex;
    justify-content: space-between;
    margin-top:48px;
    width: 100%;
}

.image-item {
    display: flex;
    flex-grow: 1;
    flex-direction: column;
    padding: 0px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.image-item img {
    max-height: 250px;
    height: auto;
    width: auto;
    max-width: 90%;

}

.image-item-big img:first-child {
    max-height: 500px !important;
}

.image-item div {
    color: #444444;
    text-align: center;
}
</style>
<div class="image-container">
    <div class="image-item">
        <img src="./assets/git0207.png" alt="">
        <div>pull</div>
    </div>
    <div class="image-item">
        <img src="./assets/git0208.png" alt="">
        <div>branques</div>
    </div>
</div>
<br/>
<br/>

## Conflictes

A vegades, les branques no es poden unir perquè els codis són incompatibles i es produeixen conflictes.



