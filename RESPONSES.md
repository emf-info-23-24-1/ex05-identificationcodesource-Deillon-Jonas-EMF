Pour chacun des mots-clés Java suivants, expliquez ci-dessous ce que c'est `ET`ce que ça fait :

- `package`  
mon explication...

- `private`  
mon explication...

- `this.`  
mon explication...

- `return`  
mon explication...

- `void`  
mon explication...

- `+=`  
mon explication...

Pour chacune des questions ci-dessous, recopier ensuite le bout de code correspondant de la classe `Motocycle` (elle se trouve à nouveau au bas de cette consigne pour faciliter votre travail).

Un getter

```
// Collez votre code Java ici..
```
Un commentaire simple

```
// Collez votre code Java ici..
```
Un commentaire Javadoc

```
// Collez votre code Java ici..
```
Un attribut

```
// Collez votre code Java ici..
```
Une valeur littérale

```
// Collez votre code Java ici..
```
Une méthode privée

```
// Collez votre code Java ici..
```
Un constructeur

```
// Collez votre code Java ici..
```
Une surcharge

```
// Collez votre code Java ici..
```
Un setter

```
// Collez votre code Java ici..
```
Une propriété

```
// Collez votre code Java ici..
```



Répondez ensuite aux questions du fichier [RESPONSES.md](RESPONSES.md) directement dans celui-ci.
```
package parts;

/**
 * @author <a href="mailto:friedlip@edufr.ch">Paul Friedli</a>
 */
public class Motocycle {

    private String marque;
    private int kmParcourus;
    private int anneeMiseEnCirculation;

    public Motocycle() {
        this.marque = "Inconnue";           // Valeur par défaut
        this.kmParcourus = -1;              // Pour indiquer qu'on ne sait pas
        this.anneeMiseEnCirculation = -1;   // Pour indiquer qu'on ne connait pas
    }

    public Motocycle(String marque, int kmParcourus, int anneeMiseEnCirculation) {
        this.marque = marque;
        this.kmParcourus = kmParcourus;
        this.anneeMiseEnCirculation = anneeMiseEnCirculation;
    }

    public String getMarque() {
        return marque;
    }

    public void setMarque(String marque) {
        this.marque = marque;
    }

    public void roule(int km) {
        this.kmParcourus += km;
    }

    public void expertise(String marque) {
        this.marque = marque;
    }

    public void expertise(String marque, int anneeMiseEnCirculation) {
        this.marque = marque;
        this.anneeMiseEnCirculation = anneeMiseEnCirculation;
    }

    private int kmEnMoyenneParAn(int anneeActuelle) {
        if (anneeActuelle != anneeMiseEnCirculation)
            return kmParcourus / (anneeActuelle - anneeMiseEnCirculation);
        else
            return kmParcourus;
    }
}
```