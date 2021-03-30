# java-basic
메가스터디 IT 아카데미 3기 ( 자바기본 )

```java

package day06;
/*
 * JOptionPane을 사용하여 이름과 키, 체중을 입력 받고
   BMI(체질량) 지수를 출력하세요.
   w: 체중
   t: 키 (*단위 : 미터)
   BMI = w/(t^2) 
 */

import javax.swing.JOptionPane;

public class homework01_1 {
	public static void main(String[] args) {
		
		double t ,w ,BMI;
		String name;
		name = JOptionPane.showInputDialog(null, "이름을 입력하시오");
		t = Double.parseDouble(JOptionPane.showInputDialog("키를 입력 하시오(단위 cm)"));
		w = Double.parseDouble(JOptionPane.showInputDialog("몸무게를 입력하시오"));
		
		BMI = w/(t*t);
		
		
		
		JOptionPane.showMessageDialog(null, name+"님의 BMI 수치:" + BMI);
		
		
		

		
		
	} 
  
}
```

```java
package day06;
/*
 * 1) 국, 영, 수 점수를 입력 받아
     평균을 산출하여 A,B,C,D,F 학점을 판별하세요.
  
     A 학점 : 평균 90점 이상
     B 학점 : 평균 80점 이상 ~ 90점 미만
     C 학점 : 평균 70점 이상 ~ 80점 미만
     D 학점 : 평균 60점 이상 ~ 70점 미만
     F 학점 : 60점 미만
     
  (2) 위에서 산출한 평균이 60.5 이상이면 "합격"을, 아니면 "불합격"을 출력하세요.
     60, 61, 61 점일 경우 평균 60.666으로 "합격"이 나와야 합니다.
 *  
 */

import java.util.Scanner;

public class homework02 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int ma;
		int ko;
		int eng;
		double ave;
		
		System.out.println("수학 국어 영어 과목의 점수를 차례대로 입력하시오");
		ma = sc.nextInt();
		ko = sc.nextInt();
		eng = sc.nextInt();
		
		ave = (ma + ko + eng)/3.0;
		
		
		if (ave >= 90) {
			System.out.println("A학점");
		}else if (ave >= 80) {
			System.out.println("B학점");
		}else if (ave >= 70) {
			System.out.println("C학점");
		}else if (ave >= 60) {
			System.out.println("D학점");
		}else { 
			System.out.println("F학점");
		}
		
		System.out.println(ave>=60.5 ? "합격" :"불합격");
		
	}

}
```

```java

package day06;

/*
 * 3. 정수 1개를 입력 받고 2, 3, 5의 배수인 지 각각 판별하세요.
    14 : 2의 배수
    15 : 3의 배수 5의 배수
    30 : 2의 배수 3의 배수 5의 배수
    17 : 해당 사항 없음
 */
import java.util.Scanner;

public class homework03 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int num;
		System.out.println("정수를 입력하시오");
		num = sc.nextInt();
		
		if(num%2==0&&num%3==0&&num%5==0){
			System.out.println(num+"은 2의 배수 3의 배수 5의 배수");
		}else if(num%3==0&&num%5==0){
			System.out.println(num+"은 3의 배수 5의배수");
		}else if(num%2==0) {
			System.out.println(num+"은 2의 배수");
		}else {
			System.out.println("해당사항 없음");
		}
		
		
		
	}

}
```
```java

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		String name;
		double t;
		int age , cnt;
		cnt=0;
			
	
		System.out.println("키를 입력하시오 (단위cm)");
		t = sc.nextDouble();
		System.out.println("나이를 입력하시오");
		age = sc.nextInt();
	
		
		if(t>=80&&t<200) {
			System.out.println("회전목마");
			cnt++;
		}
		
		if(age>=15 && t >=110) {
			System.out.println("유령의 집");
			cnt++;
		}
		
		if( 13<=age && age<60 && t>=140 ) {
			System.out.println("롤러코스터");
			cnt++;
		}
		
		if ( 10<=age && 130<=t && t<200 ) {
			System.out.println("자이로드롭");
			cnt++;
		}
		System.out.println("탈 수 있는 놀이기구 갯수"+cnt);
		
	
		
	}

}
 ```








