# Stash

**"git stash"** s'utilitza per emmagatzemar temporalment els canvis no confirmats al teu repositori de Git sense haver de fer un commit. 

Això és útil si vols canviar de branca o actualitzar el codi sense perdre els canvis locals.

Les comandes principals són:

- **git stash**: Emmagatzema els canvis no confirmats (tant els fitxers seguits com els nous).
- **git stash list**: Mostra la llista dels estats desats.
- **git stash apply**: Recupera els canvis emmagatzemats en l'última posició sense eliminar-los de l'stash.
- **git stash pop**: Recupera els canvis emmagatzemats en l'última posició i els elimina de l'stash.
- **git stash drop**: Elimina una entrada específica de l'stash.
- **git stash clear**: Elimina totes les entrades de l'stash.