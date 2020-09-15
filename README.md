# First
作业一
package su01;

import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.util.Scanner;

public class Dmo01{
public static void main(String[] args) throws Exception {

		int[] int1= {8,2,7,4,1,6};
		System.out.print("排序前的数组：");
		bianli(int1);
		System.out.print("排序后的数组：");
		paixu(int1);
	}
	private static void bianli(int[] int2) {
		// TODO Auto-generated method stub
		for (int i = 0; i < int2.length; i++) {
			if (i!=int2.length-1) {
				System.out.print(int2[i]+",");
			}
			else {
			System.out.println(int2[i]);
			}
		}
	}

	private static void paixu(int[] int2) {
		// TODO Auto-generated method stub
		for (int i = 0; i < int2.length-1; i++) {
			for (int j = 0; j < int2.length-i-1; j++) {
				if(int2[j]>int2[j+1]) {
					int temp=int2[j];
					int2[j]=int2[j+1];
					int2[j+1]=temp;
				}
			}
		}
		bianli(int2);
	}
  }
