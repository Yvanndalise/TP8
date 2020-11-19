# TP8
tp8
---------------------------------------------------------------------
import java.util.Scanner;
import java.util.Arrays;

class recherche {
	public static void main(String[] args) {
		Scanner clavier = new Scanner(System.in);


		System.out.print("Donnez le nombre de case de votre tableau : ");
		int c = clavier.nextInt();
		System.out.println("--------------------------------------------------------");
		System.out.print("Donnez maintenant l'intervalle des nombres du tableau : ");
		int [] tableau = remplirSolution(c,clavier.nextInt(),clavier.nextInt());
		afficherTableauEntier(tableau);
		System.out.println("--------------------------------------------------------");
		System.out.print("Donnez un nombre a rechercher dans le tableau : ");
		int nbRechercher = clavier.nextInt();
		int indiceDuNb = rechercheSequentiel(tableau,nbRechercher);
		System.out.println("L'indice du nombre est : " + indiceDuNb);
	}

	public static int aleatoire (int a,int b){

		int alea = a + (int)(Math.random() * ((b - a) + 1));
		return(alea);
	}

	public static int [] remplirSolution (int pTaille,int a, int b){
		int t [] = new int [pTaille];
		for (int i = 0;i<pTaille;i++ ) {
			t[i] = aleatoire(a,b);
		}
		return(t);
	}

	public static void afficherTableauEntier (int [] pTableau) {
		for (int i = 0;i<pTableau.length;i++ ) {
			System.out.println(" Case ["+i+"] = " +pTableau[i]);
			System.out.println("----------");
		}
	}

	public static int rechercheSequentiel (int [] t,int a) {
		int nb = -1;
		for (int i = 0;i<t.length;i++) {
			if (t[i]==a) {
				nb = i;
			}
		}
	return(nb);
	}
	public static long getTemps() {
		Date d = new Date();
		return d.getTime();
}


}
