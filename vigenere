package ex;

public class dkagh {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		String str = "FOIASBTHXVWPGGHXSZTBSNGTIOIMSGGGIHTDKAJEOIXBTPQDGXTVHJKSHMVTRFTLCAOSIASIKIIACGYOALWIRCULIRAPNFOIASBTHXVOAIFDHTLASCFOIASBTHXVOALHGNQINFTLOGXUDHRBHRTEGDYFTTZEASCHATGOBTHWXAPMWRTZGXOHHBXGURTBQXIHXRIHDGHJXWSXGGXZVIHFEKSSBQIBCCLOQHIIGOINFTMVGHIVAHWXIHXCUTPHMFPVHXHBPGRAHUXVAPMVTFOIBQHWSKXZDISSYFDFQDNBIBBVVOAVIATHXHBBXOHNFTFSCMOCWHWXGNLHTFOIBQHMISRCUMVTLVPISHTBSFCIBCCLCUIVNLWRTZDUXTVHHIFPVHXVOAFOIASBTHXVGWTGQXSCTVJFOCTQIBJXMMUKCBTGUTFQTQZTGLKWIMSCKSRHFSLSMBGIMVTKSHXOGVVGXEJBFTWHDLCAOSBTHWXAPMWRTZEKCQESBLQPGHPDSNXOGLCGXJTGQTGHJKWTLCULIHMOXGSSBBFNWGR";
		String str1 = "", str2 = "", str3 = "";
		for(int i=0; i<str.length(); i++){
			if(i % 3 == 0) {
				str1 += str.charAt(i);
			}else if(i % 3 == 1) {
				str2 += str.charAt(i);
			}else if(i % 3 == 2) {
				str3 += str.charAt(i);
			}
		}
				
		System.out.println("String1 : " + str1);
		System.out.println("String2 : " + str2);
		System.out.println("String3 : " + str3);
		System.out.println();
		
		int[] alpha1 = new int[26];
		
		for(int i=0; i<str1.length(); i++) {
			alpha1[str1.charAt(i) - 65]++;
		}
		
		System.out.print("[String1 frequency] ");
		for(int i=0; i<alpha1.length; i++) {
			System.out.print((char)(i+65) + ":" + alpha1[i] + " ");
		}
		System.out.println();
		System.out.println("n = " + str1.length());
		
		double num1 = 0.0;
		
		for(int i=0; i<alpha1.length; i++) {
			num1 += (alpha1[i] * (alpha1[i] - 1));
		}
		System.out.println("sum of fi * (fi-1) = " + num1);
		System.out.printf("[coincidence of string1] %.5f%n", (double) num1 / (str1.length() * (str1.length() - 1)));
		System.out.println();
		
		int[] alpha2 = new int[26];
		
		for(int i=0; i<str2.length(); i++) {
			alpha2[str2.charAt(i) - 65]++;
		}
		
		System.out.print("[String2 frequency] ");
		for(int i=0; i<alpha2.length; i++) {
			System.out.print((char)(i+65) + ":" + alpha2[i] + " ");
		}
		
		System.out.println();
		System.out.println("n = " + str2.length());
		
		double num2 = 0;
		for(int i=0; i<alpha2.length; i++) {
			num2 += (alpha2[i] * (alpha2[i] - 1));
		}
		
		System.out.println("sum of fi * (fi-1) = " + num2);
		System.out.printf("[coincidence of string2] %.5f%n", (double) num2 / (str2.length() * (str2.length() - 1)));
		System.out.println();
		
		int[] alpha3 = new int[26];
		
		for(int i=0; i<str3.length(); i++) {
			alpha3[str3.charAt(i) - 65]++;
		}
		
		System.out.print("[String3 frequency] ");
		for(int i=0; i<alpha3.length; i++) {
			System.out.print((char)(i+65) + ":" + alpha3[i] + " ");
		}
		
		System.out.println();
		double num3 = 0;
		
		for(int i=0; i<alpha3.length; i++) {
			num3 += (alpha3[i] * (alpha3[i] - 1));
		}
		
		System.out.println("n = " + str3.length());
		System.out.println("sum of fi * (fi-1) = " + num3);
		System.out.printf("[coincidence of string3] %.5f%n", (double) num3 / (str3.length() * (str3.length() - 1)));
		System.out.println();
		System.out.println("=> keyword length : 3");
		
		double[] pi = {0.082, 0.015, 0.028, 0.043, 0.127, 0.022, 0.020, 0.061, 0.070, 0.002, 0.008, 0.040, 0.024, 0.067, 0.075, 0.019, 0.001, 0.060, 0.063, 0.091, 0.028, 0.010, 0.023, 0.001, 0.020, 0.001};
		double[] mg1 = new double[26];
		for(int g=0; g<26; g++) {
			double mg = 0;
			for(int i=0; i<26; i++) {
				if(i+g < 25) {
					double mg_1 = ((double)alpha1[i + g] *  (pi[i] / str1.length()));
					mg += mg_1;
				}else {
					double mg_1 = ((double)alpha1[i + g - 25] *  (pi[i] / str1.length()));
					mg += mg_1;
				}
			}
			mg1[g] = mg;
		}
		
		System.out.println();
		System.out.println("[Mg of String1] ");
		for(int i=0; i<mg1.length; i++) {
			System.out.print((char)(i+65) + ":" + mg1[i] + ", ");
			if(i != 0 && i % 5 == 0) {
				System.out.println();
			}
		}
        
        int maxIndex = 0;
        double maxValue = mg1[0];

        // 배열을 순회하면서 최댓값 및 인덱스 찾기
        for (int i = 1; i < mg1.length; i++) {
            if (mg1[i] > maxValue) {
                maxValue = mg1[i];
                maxIndex = i;
            }
        }
        System.out.println();
        System.out.println("=> "+(char)(maxIndex + 65) + " : " + mg1[maxIndex]);
		
		double[] mg2 = new double[26];
		for(int g=0; g<26; g++) {
			double mg = 0;
			for(int i=0; i<26; i++) {
				if(i+g < 25) {
					double mg_2 = ((double)alpha2[i + g] *  (pi[i] / str2.length()));
					mg += mg_2;
				}else {
					double mg_2 = ((double)alpha2[i + g - 25] *  (pi[i] / str2.length()));
					mg += mg_2;
				}
			}
			mg2[g] = mg;
		}
		
		System.out.println();
		System.out.println("[Mg of String2] ");
		for(int i=0; i<mg2.length; i++) {
			System.out.print((char)(i+65) + ":" + mg2[i] + ", ");
			if(i != 0 && i % 5 == 0) {
				System.out.println();
			}
		}
		maxValue = mg2[0];

        // 배열을 순회하면서 최댓값 및 인덱스 찾기
        for (int i = 1; i < mg2.length; i++) {
            if (mg2[i] > maxValue) {
                maxValue = mg2[i];
                maxIndex = i;
            }
        }
        System.out.println();
        System.out.println("=> "+(char)(maxIndex + 65) + " : " + mg2[maxIndex]);
		
		double[] mg3 = new double[26];
		for(int g=0; g<26; g++) {
			double mg = 0;
			for(int i=0; i<26; i++) {
				if(i+g < 25) {
					double mg_3 = ((double)alpha3[i + g] *  (pi[i] / str3.length()));
					mg += mg_3;
				}else {
					double mg_3 = ((double)alpha3[i + g - 25] *  (pi[i] / str3.length()));
					mg += mg_3;
				}
			}
			mg3[g] = mg;
		}
		
		System.out.println();
		System.out.println("[Mg of String3] ");
		for(int i=0; i<mg3.length; i++) {
			System.out.print((char)(i+65) + ":" + mg3[i] + ", ");
			if(i != 0 && i % 5 == 0) {
				System.out.println();
			}
		}
		maxValue = mg3[0];

        // 배열을 순회하면서 최댓값 및 인덱스 찾기
        for (int i = 1; i < mg3.length; i++) {
            if (mg3[i] > maxValue) {
                maxValue = mg3[i];
                maxIndex = i;
            }
        }
        System.out.println();
        System.out.println("=> "+(char)(maxIndex + 65) + " : " + mg3[maxIndex]);
        
        System.out.println("\nKeyword : T O P (19, 14, 15)");
        
        String result = "";
        
        for(int i=0; i<str.length(); i++){
			if(i % 3 == 0) {
				if(str.charAt(i) - 19 < 65) {
					result += (char)(str.charAt(i) - 19 + 26);
				}else {
					result += (char)(str.charAt(i) - 19);
				}
			}else if(i % 3 == 1) {
				if(str.charAt(i) - 14 < 65) {
					result += (char)(str.charAt(i) - 14 + 26);
				}else {
					result += (char)(str.charAt(i) - 14);
				}
			}else if(i % 3 == 2) {
				if(str.charAt(i) - 15 < 65) {
					result += (char)(str.charAt(i) - 15 + 26);
				}else {
					result += (char)(str.charAt(i) - 15);
				}
			}
		}
        
        System.out.print("\nDecrypt : ");
        System.out.println(result);
        
} 
}
