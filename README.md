# OTP_GENERATOR

package simple_projects;

import java.util.*;

public class OtpGenerator {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int len = 10;
		System.out.println(passwordGenerator(len));
	}

	static char[] passwordGenerator(int len) {
		System.out.println("Generating password using random(): ");
		System.out.println("Here is your password: ");

		String captital_letters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
		String small_letters = "abcdefghijklmnopqrstuvwxyz";
		String numbers = "123456789";
		String symbols ="!@#$$%^&*";
		String values = captital_letters+small_letters+numbers + symbols;
		Random random = new Random();
		char[] password = new char[len];

		for(int i=0; i<len; i++) {
			password[i]= values.charAt(random.nextInt(values.length()));
		}

		return password;
	}
}
