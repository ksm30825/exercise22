package com.kh.Study;
import java.util.Scanner;
import java.util.Random;
public class Study_C_for {
	Scanner sc=new Scanner(System.in);
	public void KSMc1_ksm() {
		
		System.out.print("타이머입력 시간(1~60초) : ");
		int timer = sc.nextInt();
		if(timer>=1&&timer<=60) {
			for(int i=timer;i>0;i--) {
				System.out.println(i+"초 후 동작이 멈춥니다.");
			}
		}else {
			System.out.println("잘못누르셨습니다.");
		}
		System.out.println("종료");
	}
	public void KSMc2_ksm() {
		System.out.print("알람을 끄시겠습니까? (Y/N) : ");
		char ans = sc.next().charAt(0);
		if(ans=='y'||ans=='Y') {
			System.out.println("알람이 꺼집니다");
		}
		else if(ans!='y'&&ans!='Y'&&ans!='n'&&ans!='N') {
			for(int time1=100;time1>0;time1--) {
				System.out.println("잘못 입력하셨습니다.");
				System.out.print("다시 입력하세요. (Y/N)");
				char ans2 = sc.next().charAt(0);
				if(ans2=='y'||ans2=='Y') {
					time1=0;
					System.out.println("알람이 꺼집니다.");
				}
				else if(ans2=='n'||ans2=='N') {
					System.out.println("10분 후 알람이 울립니다.");
					time1=0;
				}
			}
		}
		else if(ans=='n'||ans=='N') {
			for(int time3=10;time3>0;time3--) {
				System.out.println(time3+"분 후 알람이 울립니다.");
				System.out.print("알람끌래?");
				char ans4=sc.next().charAt(0);
				if(ans4=='y'||ans4=='Y') {
					time3=0;
					System.out.println("알람이 꺼집니다.");
				}
				if(time3==1) {
					System.out.println("알람이 울렸습니다. 지각");
				}
			}
		}
	}
	public void KSMc3_ksm() {
		
		int random = new Random().nextInt(10)+1;
		for(int chance=0;chance<5;chance++) {
			System.out.print("정수 입력  : ");
			int input=sc.nextInt();
			if(chance!=5) {
				if(input==random) {
					chance=10;
					System.out.println("정답");
			
				}else {
					System.out.println("다시 입력하세요");
				}
			}
		}
		System.out.println("끄읕~~");
		System.out.println("정답은 "+random+"이었습니다.");
	}
	public void KSMc4_ksm() {
		int sum=0,a=2, input1,input2;
		System.out.print("1수 : ");
		input1=sc.nextInt();
		System.out.print("2수 : ");
		input2=sc.nextInt();
		sum=input1+input2;
		sum=sum+input2;
		System.out.printf("1 : %d+%d=%d\n",input1,input2,sum);
		for(int last=0;last<10;last++) {
			System.out.printf("%d : %d+%d=%d\n",a,sum,input2,sum);
			sum=sum+input2;
			a++;
			
			if(sum==30) {
				last=30;
				System.out.println("30");
			}else if(sum>30){
				last=30;
				System.out.println("넘음");
			}
		}System.out.println("");
	}
	public void CBUc1_ksm() {
		
		System.out.print("수 입력 : ");
		int input=sc.nextInt();
		int sum=0;
		for(int time=0;time<=input;time+=2) {
			sum=sum+time;
			
		}System.out.println(sum);
	}
	public void CBUc2_ksm() {
		
		System.out.print("수 입력 : ");
		int input=sc.nextInt();
		int sum=0;
		int change = 11;
		for(int time=1;time<=input;time++) {
			if(time%change==0) {
				sum+=time;
				System.out.print(time);
				if ((input - time) >= change) {
					System.out.print("+");
				} else {
					System.out.print("="+sum);
				}
			}
		}
		
		if (sum == 0) {
			
			System.out.println(change+"의 배수가 없습니다.");
		}
		
		
	}
	public void CBUc3_ksm() {
		
		System.out.print("줄 수 입력 : ");
		int row=sc.nextInt();
		int max=row;
		for(int r=1;r<=row;r++) {
			for(int c=1;c<=max;c++) {
				System.out.print("*");
			}
			max--;
			System.out.println();
		}
	}
	public void IJYc1_ksm() {
		for(int year=2019;year<=2500;year++) {
			System.out.println("슈퍼문은 "+year+"년에 뜹니다.");
			year+=43;
		}
	}
	public void IJYc2_ksm() {
		System.out.print("적금 액수 : ");
		int money =sc.nextInt();
		System.out.print("적금 부을 개월 수 : ");
		int month =sc.nextInt();
		double interest=0.02;
		int interestMoney=0;
		int monthlyMoney=money+(int)(interest*money);
		int bonus=200000;
		System.out.println(money+"원씩 "+1+"개월을 적금하면 총 금액은 "+monthlyMoney+"원입니다.");
		for(int time=2;time<=month;time++) {
			interestMoney=(int)(money*interest);
			monthlyMoney=monthlyMoney+interestMoney+money;
			if(time%6==0) {
				monthlyMoney=monthlyMoney+bonus;
			}
			System.out.println(money+"원씩 "+time+"개월을 적금하면 총 금액은 "+monthlyMoney+"원입니다.");
			if(time%12==0) {
				interest=interest+0.02;
			}
		}
		
	}
	
	public void NGUc1_ksm() {
		
		System.out.print("수  : ");
		int input = sc.nextInt();
		int count=0;
		System.out.print("{");
		for(int cycle=1;cycle<=input;cycle++) {
			if(input%cycle==0) {
				System.out.print(cycle+" ");
				count++;
				if(input==cycle) {
					System.out.print("");
				}else {
					System.out.print(",");
				}
					
			}
		}System.out.println("}\n갯수 : "+count);
	}
	
	public void CYRc1_ksm() {
		System.out.print("횟수 : ");
		int cycle=sc.nextInt();
		for(int line=1;line<=cycle;line++) {
			System.out.printf("햄찌가 쳇바퀴를 %d번 돌았습니다.\n",line);
		}System.out.println("햄찌 운동끝");
	}
	public void CYRc2_ksm() {
		System.out.println("햄찌에게 먹이를!");
		System.out.println("먹이 1회당 +1포만감");
		System.out.println();
		System.out.print("먹이를 줄 횟수(1~5) : ");
		int feed=sc.nextInt();
		int currentSatisfaction=new Random().nextInt(6)+5;
		System.out.print("햄스터의 현재 포만감 : "+currentSatisfaction+"\n");
		System.out.println();
		String result="";
		for(int time=1;time<=feed;time++) {
			currentSatisfaction++;
			System.out.println("햄스터의 포만감 : "+currentSatisfaction);
			if(currentSatisfaction<10) {
				System.out.println("아직 배고픔");
				result="먹이 찾아 떠남";
			}else if(currentSatisfaction==10) {
				System.out.println("적당");
				result="행복";
			}else if(currentSatisfaction>10) {
				System.out.println("배터짐");
				result="살 찜";
			}System.out.println();
		}System.out.println("\n--먹이주기 종료--\n");
		System.out.printf("햄찌는 %s",result);
		
	}
	public void CYRc3_ksm() {
		System.out.print("행 ; ");
		int row=sc.nextInt();
		System.out.print("열 : ");
		int col=sc.nextInt();
		int output=0;
		if(row==col) {
			for(int r=1;r<=row;r++) {
				for(int c=1;c<=row;c++) {
					int random= new Random().nextInt(2);
					System.out.print(random+" ");
					if(r==c) {
						output+=random;
					}else if(c==col) {
						output+=random;
					}else if(r==col&&c==col) {
						output-=random;
					}
				}System.out.println();
				col--;
			}
			System.out.println("X자 위치의 숫자 합계 : " + output);
		}else {
			System.out.println("같은 수의 행과 열이 아니라서 행렬이 만들어 지지 않습니다.");
		}
	}
	public void NJHc1_ksm() {
		
		System.out.print("총알 갯수 : ");
		int bullet = sc.nextInt();
		for(int i=(bullet-1);i>0;i--) {
			System.out.println("탕!!!!!!");
			System.out.println(i+"발 남았습니다.");
		}
		System.out.println("총알을 다쓰셨습니다.");
	}
	public void NJHc2_ksm() {
		
		int count=0;
		int durability = 300;
		System.out.print("벽을 부수겠습니까? (Y/N) : ");
		char ans= sc.next().charAt(0);
		if(ans=='y'||ans=='Y') {
			for(int i=0;i<=durability;i++) {
				int damage = new Random().nextInt(51);
				System.out.println("damage가 "+damage+"들어왔습니다.");
				durability-=damage;
				System.out.println("벽의 내구도가 "+durability+"만큼 남았습니다.");
				count+=1;
			}System.out.println(count+"회 쳐서 벽이 부숴졌습니다.");
		}
	}
	public void NJHc3_ksm() {
		
		System.out.print("한 무리당 개미 마리수를 입력하세요 : ");
		int per = sc.nextInt();
		System.out.print("몇무리를 만드시겠습니까? : ");
		int swarm = sc.nextInt();
		for(int r=1;r<=swarm;r++) {
			for(int c=1;c<=per;c++) {
				if(c==6) {
					System.out.print("#");
				}else {
					System.out.print("*");
				}
			}System.out.println();
		}
	}
}
