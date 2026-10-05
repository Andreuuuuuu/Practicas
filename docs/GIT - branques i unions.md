# GIT - branques i unions

**Implantació d'Aplicacions Web**
**2 ASIX**
Andreu Company Delfa

1. Crea una branca que s'anomene primera al teu repositori local, i executa la instrucció necessària per comprovar que s'ha creat.

*Figura 1: Creacio branca*
> Es veu l'execució de `git branch primera` i després `git branch` per comprovar que s'ha creat la branca. La sortida mostra `* main` i `primera`.

2. Crea un nou fitxer en aquesta branca i fusiona'l amb la principal. S'ha produït un conflicte? Raona la resposta.

*Figura 2: Creacio fitxer*
> Es veu `git checkout primera`, la creació del fitxer `primera.txt` amb `touch`, i un `ls` que mostra els fitxers del directori.

*Figura 3: Fusio*
> Es veu `git push origin primera`, després `git checkout main` i finalment `git merge primera`. No hi ha conflicte.

**Raona la resposta** – No hi ha conflicte ja que el fitxer primera.txt es nou i no existia a la branca main. Git pot incorporar fitxers afegits en una branca sense problemes perquè no hi ha cap modificació divergent sobre el mateix contingut. Els conflictes només apareixen quan les mateixes línies d'un fitxer existent s'han modificat de manera diferent a les dues branques.

3. Esborra la branca primera.

4. Crea una branca que s'anomene segona, i modifica un fitxer per produir un conflicte en unir-lo a la branca principal. Lliura el contingut del fitxer on s'ha produït el conflicte.

*Figura 4: Crear nova rama i entrar en ella i crear un nou arxiu*
> Es veu `git checkout -b segona`, la creació del fitxer `prova.txt` amb `echo "Hola que tal" > prova.txt`, `git add prova.txt` i `git commit -m "Afegit prova.txt a segona"`.

*Figura 5: Tornem a main i fem el mateix procediment*
> Es veu `git checkout main`, la creació del mateix fitxer `prova.txt` amb contingut diferent (`echo "Hola com estas" > prova.txt`), `git add` i `git commit`.

*Figura 6: Conflicte en el arxiu, es igual*
> Es veu `git merge segona` i el missatge de conflicte: "CONFLICTO (agregar/agregar): Conflicto de fusión en prova.txt".

*Figura 7: Sortida*
> Es mostra el contingut del fitxer `prova.txt` amb els marcadors de conflicte de Git (`<<<<<<< HEAD`, `=======`, `>>>>>>> segona`).

5. Soluciona el conflicte que has creat al punt anterior i sincronitza la branca segona al remot

*Figura 8: Contingut del arxiu cambiat i pujem el arxiu*
> Es veu com s'ha editat el fitxer per resoldre el conflicte, `git add prova.txt` i `git commit -m "Resolt el conflicte de prova.txt"`.

*Figura 9: Entrem en segona i fem un push*
> Es veu `git checkout segona` i `git push origin segona`.

---
