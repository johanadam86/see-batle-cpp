
#include <iostream>
#include <stdlib.h>
#include <time.h>
#include <conio.h>
using namespace std;

 int i,j;
 int x,y,a,napravlenie,p,m,k,l,r,abc;
 char xa,ya;

 int mas[25][53] ={      {32,000,21,0000,22,0000,23,0000,24,0000,25,0000,26,0000,27,0000,28,0000,29,0000,30,32,32,000,0,0,0,0,0,0,32,000,21,0000,22,0000,23,0000,24,0000,25,0000,26,0000,27,0000,28,0000,29,0000,30,0000,32},
                         {00,218,196,194,196,194,196,194,196,194,196,194,196,194,196,194,196,194,196,194,196,191,32,0,0,0,0,0,0,0,00,218,196,194,196,194,196,194,196,194,196,194,196,194,196,194,196,194,196,194,196,191,32},
                         {11,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,32,0,0,0,0,0,0,0,11,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,32},
                         {00,195,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,180,32,0,0,0,0,0,0,0,00,195,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,180,32},
                         {12,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,32,0,0,0,0,0,0,0,12,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,32},
                         {00,195,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,180,32,0,0,0,0,0,0,0,00,195,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,180,32},
                         {13,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,32,0,0,0,0,0,0,0,13,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,32},
                         {00,195,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,180,32,0,0,0,0,0,0,0,00,195,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,180,32},
                         {14,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,32,0,0,0,0,0,0,0,14,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,32},
                         {00,195,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,180,32,0,0,0,0,0,0,0,00,195,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,180,32},
                         {15,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,32,0,0,0,0,0,0,0,15,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,32},
                         {00,195,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,180,32,0,0,0,0,0,0,0,00,195,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,180,32},
                         {16,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,32,0,0,0,0,0,0,0,16,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,32},
                         {00,195,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,180,32,0,0,0,0,0,0,0,00,195,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,180,32},
                         {17,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,32,0,0,0,0,0,0,0,17,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,32},
                         {00,195,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,180,32,0,0,0,0,0,0,0,00,195,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,180,32},
                         {18,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,32,0,0,0,0,0,0,0,18,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,32},
                         {00,195,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,180,32,0,0,0,0,0,0,0,00,195,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,180,32},
                         {19,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,32,0,0,0,0,0,0,0,19,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,32},
                         {00,195,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,180,32,0,0,0,0,0,0,0,00,195,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,197,196,180,32},
                         {20,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,32,0,0,0,0,0,0,0,20,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,000,179,32},
                         {00,192,196,193,196,193,196,193,196,193,196,193,196,193,196,193,196,193,196,193,196,217,32,0,0,0,0,0,0,0,00,192,196,193,196,193,196,193,196,193,196,193,196,193,196,193,196,193,196,193,196,217,32},
                         {32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32,32}};

inline void vivodmas()
{
   system("cls");
   cout <<"       Komputer                        Igrok\n";
   for(int i = 0;i<22;i++)
    {
        for (int j = 0;j<53;j++)
        {
            if(mas[i][j]==21) cout << static_cast<char>(49);
            if(mas[i][j]==22) cout << static_cast<char>(50);
            if(mas[i][j]==23) cout << static_cast<char>(51);
            if(mas[i][j]==24) cout << static_cast<char>(52);
            if(mas[i][j]==25) cout << static_cast<char>(53);
            if(mas[i][j]==26) cout << static_cast<char>(54);
            if(mas[i][j]==27) cout << static_cast<char>(55);
            if(mas[i][j]==28) cout << static_cast<char>(56);
            if(mas[i][j]==29) cout << static_cast<char>(57);
            if(mas[i][j]==30) cout << static_cast<char>(48);
            if(mas[i][j]==11) cout << static_cast<char>(65);
            if(mas[i][j]==12) cout << static_cast<char>(66);
            if(mas[i][j]==13) cout << static_cast<char>(67);
            if(mas[i][j]==14) cout << static_cast<char>(68);
            if(mas[i][j]==15) cout << static_cast<char>(69);
            if(mas[i][j]==16) cout << static_cast<char>(70);
            if(mas[i][j]==17) cout << static_cast<char>(71);
            if(mas[i][j]==18) cout << static_cast<char>(72);
            if(mas[i][j]==19) cout << static_cast<char>(73);
            if(mas[i][j]==20) cout << static_cast<char>(74);
            if(mas[i][j]==218) cout << static_cast<char>(218);
            if(mas[i][j]==193) cout << static_cast<char>(193);
            if(mas[i][j]==192) cout << static_cast<char>(192);
            if(mas[i][j]==195) cout << static_cast<char>(195);
            if(mas[i][j]==197) cout << static_cast<char>(197);
            if(mas[i][j]==179) cout << static_cast<char>(179);
            if(mas[i][j]==196) cout << static_cast<char>(196);
            if(mas[i][j]==194) cout << static_cast<char>(194);
            if(mas[i][j]==180) cout << static_cast<char>(180);
            if(mas[i][j]==191) cout << static_cast<char>(191);
            if(mas[i][j]==217) cout << static_cast<char>(217);
            if(mas[i][j]==176) cout << static_cast<char>(0);// около корабля
            if(mas[i][j]==178&&j>25) cout << static_cast<char>(178); if (mas[i][j]==178&&j<25) cout << static_cast<char>(32);//корабль
            if(mas[i][j]==32) cout << static_cast<char>(32);//пробел
            if(mas[i][j]==42) cout << static_cast<char>(42);//ранил
            if(mas[i][j]==46) cout << static_cast<char>(46);//мимо
            if(mas[i][j]==0) cout << static_cast<char>(0);
        }
        cout << endl;
    }
}

inline void proverka()
{
 for(int y = 0;y<25;y++)
    {
        for (int x = 0;x<53;x++)
        {
            if (mas[y][x]==178)
            {
                mas[y+2][x]==0?mas[y+2][x]=176:0;
                mas[y-2][x]==0?mas[y-2][x]=176:0;
                mas[y][x+2]==0?mas[y][x+2]=176:0;
                mas[y][x-2]==0?mas[y][x-2]=176:0;

                mas[y+2][x+2]==0?mas[y+2][x+2]=176:0;
                mas[y-2][x+2]==0?mas[y-2][x+2]=176:0;
                mas[y+2][x-2]==0?mas[y+2][x-2]=176:0;
                mas[y-2][x-2]==0?mas[y-2][x-2]=176:0;
            }
        }
    }
}

inline void proverka2()
{
 for(int y = 0;y<25;y++)
    {
        for (int x = 0;x<53;x++)
        {
            if (mas[y][x]==42&&mas[y+2][x]!=178&&mas[y-2][x]!=178&&mas[y][x+2]!=178&&mas[y][x-2]!=178)
            {
//##############################################################################

        if (mas[y+2][x]==42)
           {

            if (mas[y+4][x]==178)   goto b1;
            if (mas[y+4][x]==42)
                {
                if (mas[y+6][x]==178)  goto b1;
                if (mas[y+6][x]==42) {mas[y+8][x-2]=46; mas[y+8][x]=46; mas[y+8][x+2]=46;}

                else {mas[y+6][x-2]=46; mas[y+6][x]=46; mas[y+6][x+2]=46;}
                }
            else {mas[y+4][x-2]=46; mas[y+4][x]=46; mas[y+4][x+2]=46;}
           }

        if (mas[y][x+2]==42)
           {

            if (mas[y][x+4]==178) goto b1;
            if (mas[y][x+4]==42)
                {
                if (mas[y][x+6]==178) goto b1;
                if (mas[y][x+6]==42) {mas[y][x-2]=46; mas[y][x+8]=46; mas[y+2][x+8]=46;}

                else {mas[y-2][x+6]=46; mas[y][x+6]=46; mas[y+2][x+6]=46;}
                }
            else {mas[y-2][x+4]=46; mas[y][x+4]=46; mas[y+2][x+4]=46;}
           }

        for (int k = 0;k<3;k++)
                    {
                    for (int l = 0;l<3;l++)
                     {
                      (mas[y-2+2*k][x-2+2*l]==176||mas[y-2+2*k][x-2+2*l]==0)?mas[y-2+2*k][x-2+2*l]=46:0;
                     }
                   }

b1:
    abc=5;







               // (mas[y+2][x]==176||mas[y+2][x]==0)?mas[y+2][x]=46:0;
               // (mas[y-2][x]==176||mas[y-2][x]==0)?mas[y-2][x]=46:0;
               // (mas[y][x+2]==176||mas[y][x+2]==0)?mas[y][x+2]=46:0;
               // (mas[y][x-2]==176||mas[y][x-2]==0)?mas[y][x-2]=46:0;

               // (mas[y+2][x+2]==176||mas[y+2][x+2]==0)?mas[y+2][x+2]=46:0;
               // (mas[y-2][x+2]==176||mas[y-2][x+2]==0)?mas[y-2][x+2]=46:0;
               // (mas[y+2][x-2]==176||mas[y+2][x-2]==0)?mas[y+2][x-2]=46:0;
               // (mas[y-2][x-2]==176||mas[y-2][x-2]==0)?mas[y-2][x-2]=46:0;

//###############################################################################
            }
        }
    }
}

int zamena()
{
a5:
cin >> xa;
cin>> ya;

if (!(xa>47&&xa<58&&(ya>64&&ya<75)||(ya>96&&ya<107)))
    {
        cout << "\npoprobuite snovo\n";
        goto a5;
    }

xa==49?x=32:0;
xa==50?x=34:0;
xa==51?x=36:0;
xa==52?x=38:0;
xa==53?x=40:0;
xa==54?x=42:0;
xa==55?x=44:0;
xa==56?x=46:0;
xa==57?x=48:0;
xa==48?x=50:0;
ya==65||ya==97?y=2:0;
ya==66||ya==98?y=4:0;
ya==67||ya==99?y=6:0;
ya==68||ya==100?y=8:0;
ya==69||ya==101?y=10:0;
ya==70||ya==102?y=12:0;
ya==71||ya==103?y=14:0;
ya==72||ya==104?y=16:0;
ya==73||ya==105?y=18:0;
ya==74||ya==106?y=20:0;
return 0;
}

int zamena2()
{
a11:
//cout<<"cifra=";
cin >> xa;

//cout<<"bukva=";
cin>> ya;

if (!(xa>47&&xa<58&&((ya>64&&ya<75)||(ya>96&&ya<107))))
    {
        cout << "\npoprobuite snovoppp\n";
        goto a11;
    }

xa==49?x=2:0;
xa==50?x=4:0;
xa==51?x=6:0;
xa==52?x=8:0;
xa==53?x=10:0;
xa==54?x=12:0;
xa==55?x=14:0;
xa==56?x=16:0;
xa==57?x=18:0;
xa==48?x=20:0;
ya==65||ya==97?y=2:0;
ya==66||ya==98?y=4:0;
ya==67||ya==99?y=6:0;
ya==68||ya==100?y=8:0;
ya==69||ya==101?y=10:0;
ya==70||ya==102?y=12:0;
ya==71||ya==103?y=14:0;
ya==72||ya==104?y=16:0;
ya==73||ya==105?y=18:0;
ya==74||ya==106?y=20:0;
return 0;
}

int sluschainoe_zapolnenie()
{
    a1:
    x = 2+p+(rand()*2)%(20+p);
    y = 2+(rand()*2)%20;

    if(x+6>20+p) goto a1;
    if(y+6>20) goto a1;

    mas[y][x]=178;
    a = rand()%2;

    if (a==1)
        for(i=1;i<4;i++)
        {
           mas[y+2*i][x]=178;
           proverka();
        }
     else
        for(i=1;i<4;i++)
        {
           mas[y][x+2*i]=178;
           proverka();
        }
//+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
//установка 3 палубника комп.++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
      for(j=0;j<2;j++)
   {
    a2:
    x = 2+p+(rand()*2)%(20+p);
    y = 2+(rand()*2)%20;

    if(x+4>20+p) goto a2;
    if(y+4>20) goto a2;

    if(mas[y][x]!=0) goto a2;
    if(mas[y+4][x]!=0) goto a2;
    if(mas[y][x+4]!=0) goto a2;

    mas[y][x]=178;
    a = rand()%2;

    if (a==1)
        for(i=1;i<3;i++)
        {
           mas[y+2*i][x]=178;
           proverka();
        }
    else
        for(i=1;i<3;i++)
        {
           mas[y][x+2*i]=178;
           proverka();
        }
  }
//+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
//установка 2 палубника комп.+++++++++++++++++++++++++++++++++++++++++++++++++++++
for(j=0;j<3;j++)
   {
    a3:
    x = 2+p+(rand()*2)%(20+p);
    y = 2+(rand()*2)%20;

    if(x+2>20+p) goto a3;
    if(y+2>20) goto a3;

    if(mas[y][x]!=0) goto a3;
    if(mas[y+2][x]!=0) goto a3;
    if(mas[y][x+2]!=0) goto a3;

    mas[y][x]=178;
    a = rand()%2;

    if (a==1)
        for(i=1;i<2;i++)
        {
           mas[y+2*i][x]=178;
           proverka();
        }
    else
        for(i=1;i<2;i++)
        {
           mas[y][x+2*i]=178;
           proverka();
        }
   }
//+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
//установка 1 палубника комп.+++++++++++++++++++++++++++++++++++++++++++++++++++++
for(j=0;j<4;j++)
   {
    a4:

    x = 2+p+(rand()*2)%(20+p);
    y = 2+(rand()*2)%20;

    if(x>20+p) goto a4;
    if(mas[y][x]!=0) goto a4;

    mas[y][x]=178;
    proverka();
   }

    return 0;
}
int ruschnoe_zapolnenie()
{


//+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
// 4 палубы игрок++++++++++++++++++++++++
cout << "rasstavte svoi korabli\n4 pal,3 pal,2 pal,1 pal\ncifra=>bukva=>napravlenie\n1->   2\\/    3<-   4/\\\n\n";
cout << "4x-palubnii\n";
a6:

zamena();
cin>>napravlenie;

    switch(napravlenie)
    {
        case 1: if (x+6<=50) {for(i=0;i<4;i++)  mas[y][x+2*i]=178; break;} else {cout << "poprobuite snovo11\n";  goto a6; }
        case 2: if (y+6<=20) {for(i=0;i<4;i++)  mas[y+2*i][x]=178; break;} else {cout << "poprobuite snovo22\n";  goto a6; }
        case 3: if (x-6>=32) {for(i=0;i<4;i++)  mas[y][x-2*i]=178; break;} else {cout << "poprobuite snovo33\n";  goto a6; }
        case 4: if (y-6>=2) {for(i=0;i<4;i++)  mas[y-2*i][x]=178; break;} else {cout << "poprobuite snovo44\n";  goto a6; }
        default : {cout << "poprobuite snovo2\n";  goto a6; }
    }
    proverka();
    vivodmas();
// 3 палубы игрок++++++++++++++++++++++++
for(j=0;j<2;j++)
{
cout << "3x-palubnii\n";
a7:

zamena();
cin>>napravlenie;
switch(napravlenie)
    {
        case 1: if (x+4<=50&&mas[y][x]==0&&mas[y][x+2]==0&&mas[y][x+4]==0) {for(i=0;i<3;i++)  mas[y][x+2*i]=178; break;} else {cout << "poprobuite snovo\n";  goto a7; }
        case 2: if (y+4<=20&&mas[y][x]==0&&mas[y+2][x]==0&&mas[y+4][x]==0) {for(i=0;i<3;i++)  mas[y+2*i][x]=178; break;} else {cout << "poprobuite snovo\n";  goto a7; }
        case 3: if (x-4>=32&&mas[y][x]==0&&mas[y][x-2]==0&&mas[y][x-4]==0) {for(i=0;i<3;i++)  mas[y][x-2*i]=178; break;} else {cout << "poprobuite snovo\n";  goto a7; }
        case 4: if (y-4>=2&&mas[y][x]==0&&mas[y-2][x]==0&&mas[y-4][x]==0) {for(i=0;i<3;i++)  mas[y-2*i][x]=178; break;} else {cout << "poprobuite snovo\n";  goto a7; }
        default : {cout << "poprobuite snovo222\n";  goto a7; }
    }
proverka();
vivodmas();
}
// 2 палубы игрок++++++++++++++++++++++++
for(j=0;j<3;j++)
{
cout << "2x-palubnii\n";
a8:

zamena();
cin>>napravlenie;
switch(napravlenie)
    {
        case 1: if (x+2<=50&&mas[y][x]==0&&mas[y][x+2]==0) {for(i=0;i<2;i++)  mas[y][x+2*i]=178; break;} else {cout << "poprobuite snovo\n";  goto a8; }
        case 2: if (y+2<=20&&mas[y][x]==0&&mas[y+2][x]==0) {for(i=0;i<2;i++)  mas[y+2*i][x]=178; break;} else {cout << "poprobuite snovo\n";  goto a8; }
        case 3: if (x-2>=32&&mas[y][x]==0&&mas[y][x-2]==0) {for(i=0;i<2;i++)  mas[y][x-2*i]=178; break;} else {cout << "poprobuite snovo\n";  goto a8; }
        case 4: if (y-2>=2&&mas[y][x]==0&&mas[y-2][x]==0) {for(i=0;i<2;i++)  mas[y-2*i][x]=178; break;} else {cout << "poprobuite snovo\n";  goto a8; }
        default : {cout << "poprobuite snovo222\n";  goto a8; }
    }
proverka();
vivodmas();
}

// 1 палубы игрок++++++++++++++++++++++++
for(j=0;j<4;j++)
{
cout << "1x-palubnii\n";
a9:
zamena();

if(mas[y][x]==0)  mas[y][x]=178;    else {cout << "poprobuite snovo\n";  goto a9;}

proverka();
vivodmas();
}

    return 0;
}

int main()
{
srand(time(0));

//cout << "       Komputer                        Igrok\n";

vivodmas();

p=0;
sluschainoe_zapolnenie();

cout<< "Esli xotite rasstavit' svoi korabli avtomatichiski nagmite \"0\",\nesli xotite rasstavit' svoi korabli v ruchnuu nagmite druguu cifru";
cin>>m;
cout<<endl;
//cout << "       Komputer                        Igrok\n";
if (m==0)
{
p=30;
sluschainoe_zapolnenie();
}
else
{
    ruschnoe_zapolnenie();
}
//system("cls");
vivodmas();


for(r=1;r<1000;r++)
{
cout << "xod N"<<r<<", vvedite kordinati(snachala cifru,potom bukvu)"<<endl;


  a100:
      for(int i = 0;i<25;i++)
    {
        for (int j = 0;j<25;j++)
        {
           if (mas[i][j]==178) goto b2;
        }

    }

   cout <<       "\n\n\n\n\n\n\n";
   cout <<       "                                                                          \n";
   cout <<       "                          _____                                           \n";
   cout <<       "                ____     |     |     ____                                 \n";
   cout <<       "               |    |    |     |    |    |                                \n";
   cout <<       "               |    |    |     |    |    |                                \n";
   cout <<       "          _    |    |    |     |    |    |                                \n";
   cout <<       "         \\O~   |    |    |     |    |    |                               \n";
   cout <<       "          |\\   |    |    |     |    |    |                               \n";
   cout <<       "       __/_\\___|____|____|_____|____|____|_____                          \n";
   cout <<       "       \\                                      /                          \n";
   cout <<       "        \\   O        O         O        O    /                           \n";
   cout <<       "         \\                                  /                            \n";
   cout <<       "/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\\n";
   cout <<       "    _______     ____     _____    _____     _____                 _       \n";
   cout <<       "   |  ___  |   / __ \\   |  ___|  | ____|   |  _  |       /\\      | |    \n";
   cout <<       "   | |   | |  | /  \\ |  | |___   | |__     | |_| |      /  \\     | |    \n";
   cout <<       "   | |   | |  | |  | |  |  _  \\  |  __|   _|_____|_    / /\\ \\    |_|   \n";
   cout <<       "   | |   | |  | \\__/ |  | |_| |  | |___  |  _____  |  / /__\\ \\    _    \n";
   cout <<       "   |_|   |_|   \\____/   |_____/  |_____| |_|     |_| /_/    \\_\\  |_|   \n";
   getch();
   return 0;






    b2:
     //ход человека
    a12:


    zamena2();
    if(mas[y][x]==178) { mas[y][x]=42; proverka2();/* system("cls");cout <<"       Komputer                        Igrok\n";*/ vivodmas();cout << "ranil,  xodite snova\n"; goto a12;}
    else {mas[y][x]=46;/*system("cls");cout <<"       Komputer                        Igrok\n";*/vivodmas();cout <<"mimo, xod komputera(nagmite enter)\n"; getch(); }



//комп играет за человека для теста
/*
    p=0;
    x = 2+p+(rand()*2)%(20+p);
    y = 2+(rand()*2)%20;

    if(x>20+p) goto a10;
    if(mas[y][x]==178) {cout << "ranil\n"; mas[y][x]=42;proverka2(); vivodmas(); goto a100;}
    if(mas[y][x]==46) goto a100;
    if(mas[y][x]==42) goto a100;
    else { mas[y][x]=46;vivodmas();cout <<"mimo\ntvoi xod\nvvedi kordinati"; }
*/


//ход компа
   a10:

            for(int i = 0;i<25;i++)
    {
        for (int j = 26;j<53;j++)
        {
           if (mas[i][j]==178) goto b3;
        }

    }

   cout <<       "\n\n\n\n\n\n\n";
   cout <<       "                    /\\  /\\                  \n";
   cout <<       "             /\\    /  \\/  \\                \n";
   cout <<       "            /  \\   \\  /    \\               \n";
   cout <<       "            \\   \\   \\/   O  \\             \n";
   cout <<       "             \\   \\  /        \\             \n";
   cout <<       "              \\   \\/   O      \\            \n";
   cout <<       "               \\  /           /              \n";
   cout <<       "                \\/  O        /               \n";
   cout <<       "/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\/\\\n";
   cout <<       "     ____                           _____     \n";
   cout <<       "    / __ \\       /\\      |\\    /|  | ____| \n";
   cout <<       "   | /  \\/      /  \\     | \\  / |  | |__   \n";
   cout <<       "   | | ___     / /\\ \\    |  \\/  |  |  __|  \n";
   cout <<       "   | |__| \\   / /__\\ \\   | |\\/| |  | |___ \n";
   cout <<       "    \\_____/  /_/    \\_\\  |_|  |_|  |_____| \n";
   cout <<       "      ____    __      __   _____    ____      \n";
   cout <<       "     / __ \\   \\ \\    / /  | ____|  |  _ \\ \n";
   cout <<       "    | /  \\ |   \\ \\  / /   | |__    | |_| | \n";
   cout <<       "    | |  | |    \\ \\/ /    |  __|   |  __/   \n";
   cout <<       "    | \\__/ |     \\  /     | |___   |   \\   \n";
   cout <<       "     \\____/       \\/      |_____|  |_|\\_\\ \n";
   getch();
   return 0;
b3:
    p=30;
    x = 2+p+(rand()*2)%(20+p);
    y = 2+(rand()*2)%20;

    if(x>20+p) goto a10;
    if(mas[y][x]==178) {/*system("cls");cout <<"       Komputer                        Igrok\n";*/  mas[y][x]=42;proverka2(); vivodmas();cout <<"ranil\n";getch(); goto a10;}
    if(mas[y][x]==46) goto a10;
    if(mas[y][x]==42) goto a10;
    else { mas[y][x]=46;/*system("cls");cout <<"       Komputer                        Igrok\n";*/vivodmas();cout <<"mimo, "; }

}


}
