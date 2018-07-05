# work-on-java
public class ArmstrongNumber {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner s = new Scanner(System.in);
		int n = s.nextInt();
		System.out.println(armstrong(n));
	}

	public static boolean armstrong(int num) {
		int i = 0;
		int k = num;
		int b = num;
		int sum = 0;
		int rem = 0;
		while (num > 0) {
			num = num / 10;
			i++;
		}
		while (k > 0) {
			rem = k % 10;
			int j = (int) Math.pow(rem, i);
			sum = sum + j;
			k = k / 10;
		}
		if (sum == b) {
			return true;
		} else {
			return false;
		}
	}
