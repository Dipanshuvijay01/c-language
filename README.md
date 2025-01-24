#include<stdio.h>
#include<windows.h>
#include<stdlib.h>
void menu();
void breakfast();
void lunch();
void dinner();
void fulllist();
void gotoxy(int x,int y){
COORD c;
c.X=x;
c.Y=y;
SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE),c);
}
int n;
int main(){
	
 fulllist();
int paid,balance;
     int rt,q,a=0,ta=0,r=3,d=2,s=0,t=0,c,n;
 char i[25],hgt[20];
 char ch;
 char dosa,string,pepsi,pasta,lassi,tea,water,coffee;
  int j,k,l;
  	for(k=0;k<36;k++)
	{
		gotoxy(43,k+1);
		printf("!");
	}

  	for(l=0;l<36;l++)
	{
		gotoxy(93,l+1);
		printf("!");
	}
  gotoxy(130,24);
  printf("...breakfast_______1");
  gotoxy(130,26);
  printf("...lunch_______2");
  gotoxy(130,28);
  printf("...dinner________3");
  gotoxy(130,30);
  printf(".....enter the number :-");
  scanf("%d",&n);

switch(n)
{
	case 1:
		breakfast();
    
      break;
      
    case 2:
    	lunch();
     
    	break;
    case 3:
    	dinner();
      
    	break;
    default :
    	exit(0);
}



	for(j=0;j<37;j++)
	{
		gotoxy(113,j+1);
		printf("!");
	}
 
 gotoxy(4,2);
 printf("ITEM");
 gotoxy(24,2);
 printf("RATE");
 gotoxy(44,2);
 printf("QUANTITY");
 gotoxy(64,2);
 printf("AMOUNT");
 do
 {
     r=r+2;
     d++;
     s++;
     gotoxy(75,d);
    printf("enter the number :");
    scanf("%d",&n);
     gotoxy(1,r);
     printf("%d",s);
     gotoxy(4,r);
     if(n==1){
      printf("tea");
      rt=20;
      gotoxy(24,r);
      printf("%d",rt);
      }
     if(n==2){
      printf("lassi");
      rt=40;
      gotoxy(24,r);
      printf("%d",rt);
     }
     
      if(n==3){
        printf("water");
        rt=10;
      gotoxy(24,r);
      printf("%d",rt);
      }
     if(n==4){
      printf("coffee");
      rt=60;
      gotoxy(24,r);
      printf("%d",rt);
     }
      if(n==5){
        printf("coke");
        rt=40;
        gotoxy(24,r);
        printf("%d",rt);
      }
     if(n==6){
      printf("mangosake");
      rt=50;
      gotoxy(24,r);
      printf("%d",rt);
     }
     if(n==7){
      printf("apple");
      rt=20;
      gotoxy(24,r);
      printf("%d",rt);
     }
     if(n==8){
      printf("banana");
      rt=50;
      gotoxy(24,r);
      printf("%d",rt);
     }
     if(n==9){
      printf("sting");
      rt=20;
      gotoxy(24,r);
      printf("%d",rt);
     }
     if(n==10){
      printf("milk");
      rt=60;
      gotoxy(24,r);
      printf("%d",rt);
     }
      if(n==11){
        printf("chole chawal");
        rt=40;
         gotoxy(24,r);
         printf("%d",rt);
         }
     if(n==12){
      printf("dosa");
       rt=20;
         gotoxy(24,r);
         printf("%d",rt);
     }
     if(n==13){
      printf("chicken");
       rt=100;
         gotoxy(24,r);
         printf("%d",rt);
     }
     if(n==14){
      printf("dal roti");
       rt=50;
         gotoxy(24,r);
         printf("%d",rt);
     }
     if(n==15){
      printf("ande");
       rt=50;
         gotoxy(24,r);
         printf("%d",rt);
     }
     if(n==16){
      printf("pulav");
       rt=110;
         gotoxy(24,r);
         printf("%d",rt);
     }
     if(n==17){
      printf("samosa");
       rt=20;
         gotoxy(24,r);
         printf("%d",rt);
     }
     if(n==18){
      printf("nudels");
       rt=90;
         gotoxy(24,r);
         printf("%d",rt);
     }
     if(n==19){
      printf("momos");
       rt=30;
         gotoxy(24,r);
         printf("%d",rt);
     }
     if(n==20){
      printf("aloo parathe");
       rt=60;
         gotoxy(24,r);
         printf("%d",rt);
     }
     if(n==21){
      printf("pasta");
       rt=50;
         gotoxy(24,r);
         printf("%d",rt);
     }
      if(n==22){
        printf("maggy");
         rt=20;
         gotoxy(24,r);
         printf("%d",rt);
      }
      if(n==23){
        printf("paneer tikka");
         rt=100;
         gotoxy(24,r);
         printf("%d",rt);
      }
      if(n==24){
        printf("dal makhani");
         rt=80;
         gotoxy(24,r);
         printf("%d",rt);
      }
     if(n==25){
      printf("chap");
       rt=120;
         gotoxy(24,r);
         printf("%d",rt);
     }
     d++;
     gotoxy(75,d);
     printf("enter the quantity :");
     scanf("%d",&q);
     gotoxy(45,r);
     printf("%d",q);
     d++;
     gotoxy(75,d);
     a=rt*q;
     t=t+a;
     gotoxy(64,r);
     printf("%d",a);
     gotoxy(1,r+1);
     printf("________________________");
     d++;
     gotoxy(75,d);
     printf("do you wand to add another record :");
     scanf("%s",&ch);
    
 } while (ch=='y'||ch=='Y');	
printf(" TOTAL AMOUNT=%d\n",t);
printf("enter the paid amount :");
scanf("%d",&paid);
balance=t-paid;
printf("%d",balance);

return 0;
}

void breakfast()
{
  
   system("cls");
	gotoxy(123,2);
	printf("<.........breakfast menu........>");
	gotoxy(123,4);
	printf("||   1  tea ______20/-  ||");
	gotoxy(123,6);
	printf("|| 2   lassi_______40/-  ||");
	gotoxy(123,8);
	printf("||  3 water_______20/-  ||");
	gotoxy(123,10);
	printf("|| 4 coffee______50/-  ||");
	gotoxy(123,12);
	printf("|| 5 coke _____40/-  ||");
	gotoxy(123,14);
	printf("|| 6 mangosake_____50/-  ||");
	gotoxy(123,16);
	printf("|| 7 apple_______20/-  ||");
	gotoxy(123,18);
	printf("|| 8 banana______50/-  ||");
  gotoxy(123,20);
	printf("|| 9 sting ______20/-  ||");
  gotoxy(123,22);
	printf("|| 10 milk______60/-  ||");
	
  
}
void lunch()

{
	system("cls");
	gotoxy(123,2);
	printf("<........lunch menu........>");
	gotoxy(123,4);
	printf("|| 11 chole chawal_____40/-  ||");
	gotoxy(123,6);
	printf("|| 12 dosa_______20/-  ||");
	gotoxy(123,8);
	printf("|| 13 chicken_____100/-  ||");
	gotoxy(123,10);
	printf("|| 14 dal roti_____50/-  ||");
  gotoxy(123,12);
	printf("|| 15 ande ______50/-  ||");
	gotoxy(123,14);
	printf("|| 16 pulav_______110/-  ||");
	gotoxy(123,16);
	printf("|| 17 samosa_______20/-  ||");
	gotoxy(123,18);
	printf("|| 18 nudels_______90/-  ||");
  gotoxy(123,20);
	printf("|| 19 momos______30/-  ||");
  gotoxy(123,22);
	printf("|| 20 aloo parathe_____60/-  ||");
}
void  dinner()
{    
  system("cls");
		gotoxy(123,2);
	printf("<..........dinner menu.............>");
	gotoxy(123,4);
	printf("|| 21 pasta______50/-  ||");
	gotoxy(123,6);
	printf("|| 22 maggy______20/-  ||");
	gotoxy(123,8);
	printf("|| 23 paneer tikka_____100/- ||");
	gotoxy(123,10);
	printf("|| 24 dal makhani_______80/-  ||");
  gotoxy(123,12);
	printf("|| 25 chap____120/-  ||");
	
	
}
void fulllist()
{
  gotoxy(5,4);
	printf("<.........breakfast menu........>");
	gotoxy(5,6);
	printf("|| 1 tea________20/-  ||");
	gotoxy(5,8);
	printf("|| 2 lassi______40/-  ||");
	gotoxy(5,10);
	printf("|| 3 wate_______20/-  ||");
	gotoxy(5,12);
	printf("|| 4 coffee_______50/-  ||");
  gotoxy(5,14);
	printf("|| 5 coke_______40/-  ||");
	gotoxy(5,16);
	printf("|| 6 mangosake______50/-  ||");
	gotoxy(5,18);
	printf("|| 7 apple______20/-  ||");
	gotoxy(5,20);
	printf("|| 8 banana_______50/-  ||");
  gotoxy(5,22);
	printf("|| 9 sting______20/-  ||");
  gotoxy(5,24);
	printf("|| 10 milk_______60/-  ||");
  gotoxy(50,4);
  printf("<........lunch menu........>");
	gotoxy(50,6);
	printf("|| 11 chole chawal____40/-  ||");
	gotoxy(50,8);
	printf("|| 12 dosa_______20/-  ||");
	gotoxy(50,10);
	printf("|| 13 chicken_____100/-  ||");
	gotoxy(50,12);
	printf("|| 14 dal roti_____50/-  ||");
   gotoxy(50,14);
	printf("|| 15 ande_______50/-  ||");
	gotoxy(50,16);
	printf("|| 16 pulav_______110/-  ||");
	gotoxy(50,18);
	printf("||  17 samosa_______20/-  ||");
	gotoxy(50,20);
	printf("|| 18 nudels_______90/-  ||");
  gotoxy(50,22);
	printf("|| 19 momos______30/-  ||");
  gotoxy(50,24);
	printf("|| 20 aloo parathe_____60/-  ||");

gotoxy(100,4);
	printf("<..........dinner menu.............>");
	gotoxy(100,6);
	printf("|| 21 pasta______50/-  ||");
	gotoxy(100,8);
	printf("|| 22 maggy______20/-  ||");
	gotoxy(100,10);
	printf("|| 23 paneer tikka_____100/- ||");
	gotoxy(100,12);
	printf("|| 24 dal makhni_____70/-  ||");
  gotoxy(100,14);
	printf("|| 25 chap_______80/-  ||");

	
}
