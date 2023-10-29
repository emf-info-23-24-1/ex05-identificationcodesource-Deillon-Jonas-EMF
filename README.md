# Ex05-IdentificationCodeSource
## Instructions (15')
Le code source ci-dessous d’une classe vous est donné.
Répondez aux questions du fichier [RESPONSES.md](RESPONSES.md)
```
package parts;

/**
* @author Paul Friedli
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