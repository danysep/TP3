# TP3

import java.util.Scanner;

public class Dichotomie {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner scan = new Scanner(System.in);
		System.out.println("nombres de colonnes ?");
		int A = scan.nextInt();
		System.out.println("valeur recherchée ?");
		int elementRecherche  = scan.nextInt();
		long[] tab3 = new long[A];
		for (int k = 0; k < A; k++) {
				System.out.println("valeur de la "+k+" eme colonne");
				long D = scan.nextLong();
				tab3 [k] = D;
			}

		//for (int u = 0; u < A; u++) {
		//System.out.print(tab3 [u] + " ");}
		
	
		int id = 0;
		int ia = A-1;
		boolean elementTrouve = false;
		
		if (tab3[ia] == elementRecherche) {
			elementTrouve = true;
			System.out.print("l'indice de l'element est " +ia);}
		
		if (tab3[id] == elementRecherche) {
			elementTrouve = true;
			System.out.print("l'indice de l'element est " +ia);
			}
			
		
		
		while (elementTrouve == false && ((ia - id) > 1) ) {
			int im = (id + ia)/2;
			if (tab3[im] == elementRecherche) {
				elementTrouve = true;
				System.out.print("l'indice de l'element est " +im);
				return;}
			else {
				if (elementRecherche < tab3[im]) {
					ia = im;}
				else {
					id = im;}}
		}
		if (elementTrouve == false) {
			System.out.print("l'element n'est pas présent");
		}
