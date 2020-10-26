# TASK
package by.htp.java10.main;

import java.util.*;

public class Mas10 {

	public static void main(String[] args) {
		int i = 0;
		int j = 0;
		int k = 1;
		int x = 1;

		Scanner sc = new Scanner(System.in);

		System.out.println("Введите размерность матрицы: ");
		while (!sc.hasNextInt()) {
			sc.next();
		}
		i = sc.nextInt();
		System.out.println("Новая матрица равна: ");
		if (i % 2 == 0) {

			int[][] mas = new int[i][i];
			k = mas.length;
			int[] mas2 = new int[k];

			init(mas);// инициализация массива

			for (i = 0; i < mas.length; i++) {
				for (j = 0; j < mas[i].length; j++) {

					System.out.printf("%5d ", mas[i][j]);

					if (mas[i][j] > 0 && i == j) {
						mas2[k] = mas[i][j];

						k++;
					}
				}
				System.out.println();

			}
			System.out.println("Положительные элеиенты равны " + k);

		} else {
			System.out.println("Вы ввели нечетное число");
		}

	}

	public static void init(int[][] ar) {
		Random rand = new Random();
		for (int i = 0; i < ar.length; i++) {
			for (int j = 0; j < ar[i].length; j++) {
				ar[i][j] = rand.nextInt(100) - 50;
			}
			System.out.println();
		}

	}

}
