# oopimport java.io.*;
	import java.util.*;
	

	public class new class{
		
		public static void main(String[] args) throws Exception {
			
			if (args.length != 1) {
				System.out.println("java filename");
				System.exit(1);
			}	
	

			
			File file = new File(args[0]);
			if (!file.exists()) {
				System.out.printlnargs[0] + " not exist");
				System.exit(2);
			}
	

			int chara = 0;	
			int words = 0;			
			int lines = 0;			
	

			try (
				
				Scanner input = new Scanner(file);
			) {
				while (input.hasNext()) {
					lines++;
					String line = input.nextLine();
					chara += line.length();
				}
			}
	

			try (
				
				Scanner input = new Scanner(file);
			) {
				while (input.hasNext()) {
					String line = input.next();
					words++;
				}
			}
	

			
			System.out.println(file.getName() );
			System.out.println(" chara");
			System.out.println(" words");
			System.out.println(" lines");
		}
	}
