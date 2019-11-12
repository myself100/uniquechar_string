# uniquechar_string

import java.util.Scanner;
public class isunique {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		Scanner s=new Scanner(System.in);
		String str=s.nextLine();
		boolean sr=isuni(str);
		System.out.print(sr);                         
	}
	public static boolean isunique(String str) {
		if(str.length()>128) {
			return false;
		}
		boolean []char_set=new boolean[128];
		for(int i=0;i<str.length();i++) {
			int val=str.charAt(i);
			if(char_set[val]) {
				return false;
			}
			char_set[val]=true;
		}
		return true;                                                      ////return true if the char in the string are different 
	}
}
