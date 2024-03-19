# Questions et vos réponses
Pour chacun des mots-clés Java suivants, expliquez ci-dessous ce que c'est `ET`ce que ça fait :

- `package`  
definit le package en tat que parts et lorsque on appelle Motocycle on devra ecrire import package.parts;
- `private`  
definit la sécuritée des attributs sur privé. Ils seront modifiable uniquement dan la classe elle meme ou les sous classes
- `this.`  
séléctionne les attributs de l'entitée
- `return`  
retourne une valeure 
- `void`  
définit que aucune valeur ne doit etre retournée

- `+=`  
ajoute une valeure a la varibale en plus de la précédente

Pour chacune des questions ci-dessous, recopier ensuite le bout de code correspondant de la classe `Motocycle` (elle se trouve à nouveau au bas de cette consigne pour faciliter votre travail).

Un getter

```
    public String getMarque() {
        return marque;
    }
```
Un commentaire simple

```
// Valeur par défaut
```
Un commentaire Javadoc

```
/**
 * @author <a href="mailto:friedlip@edufr.ch">Paul Friedli</a>
 */
```
Un attribut

```
    private int kmParcourus;
```
Une valeur littérale

```
= -1; 
```
Une méthode privée

```
    private int kmEnMoyenneParAn(int anneeActuelle) {
        if (anneeActuelle != anneeMiseEnCirculation)
            return kmParcourus / (anneeActuelle - anneeMiseEnCirculation);
        else
            return kmParcourus;
    }
```
Un constructeur

```
    public Motocycle(String marque, int kmParcourus, int anneeMiseEnCirculation) {
        this.marque = marque;
        this.kmParcourus = kmParcourus;
        this.anneeMiseEnCirculation = anneeMiseEnCirculation;
    }
```
Une surcharge

```
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
```
Un setter

```
    public void setMarque(String marque) {
        this.marque = marque;
    }
```
Une propriété

```
    private String marque;

        public String getMarque() {
        return marque;
    }

    public void setMarque(String marque) {
        this.marque = marque;
    }
```  
  
  
# La classe `Motocycle` 
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