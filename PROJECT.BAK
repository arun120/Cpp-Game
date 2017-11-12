#include<iostream.h>
#include<fstream.h>
#include<conio.h>
#include<string.h>
#include<process.h>
#define mn cout<<"Select members to board\n1.A\n2.B\n3.C\n4.D\n5.E\n6.no"
int time=30,ch[2],a,b;
int l[5]={1,3,6,8,12},ri[5],m=5,n=0;

void playlr();
void playrl();
void clock(int);
void check();
void c();

#define empty cout<<"Empty\n1."<<am<<"\n2."<<bm<<"\nEnter your choice"
#define fill cout<<"fill\n1."<<am<<"\n2."<<bm<<"\nEnter your choice"
#define shift cout<<"shift\n1."<<am<<"L to "<<bm<<"L"<<"\n2."<<bm<<"L to "<<am<<"L"<<"\nEnter your choice"

int x=0,y=0,r;
//Function Declaration
void game(int,int);
void gempty(int,int);
void gfill(int,int);
void gshift(int,int);
void disp(int,int);
void glevel();


void disp(int a,int b,int am,int bm)
{
 clrscr();
 fstream f("sd.txt",ios::in);
 char ch[80];
 int i;
 int c1,c2;
 c1=a-48;
 c2=b-48;
 if(c1==r||c2==r)
  {
   cout<<"\t\tMission Accompanished";
   getch();
   clrscr();
   glevel();
  }
  if(b==58)
  b=232;
  if(bm==58)
  bm=232;
 while(!f.eof())
 {
  f.getline(ch,80);
  for(i=0;ch[i]!='\0';i++)
   {
    if(ch[i]=='x')
     ch[i]=a;
    else if(ch[i]=='W')
     ch[i]=b;
    else if(ch[i]=='A')
     ch[i]=am;
    else if(ch[i]=='B')
     ch[i]=bm;
   }
  cout<<ch<<endl;
  }
 f.close();
 if(b==232)
 b=58;
 if(bm==232)
 bm=58;
 am-=48;bm-=48;
 game(am,bm);
}


void game(int am,int bm)
{
 cout<<"enter your choice:";
 int c;
 cin>>c;
 if(c==1)
  gfill(am,bm);
 if(c==2)
  gshift(am,bm);
 if(c==3)
  gempty(am,bm);
}


void gempty(int am,int bm)
{
 int g;
 s:
 empty;
 cin>>g;
 if(g==1)
  x=0;
 else if(g==2)
  y=0;
 else if(g==3)
  exit(0);
 else
  {
   cout<<"WRONG VALUE PLEASE ENTER AGAIN";
   goto s;
  }
 disp(x+48,y+48,am+48,bm+48);
}


void gfill(int am,int bm)
{
  int g;
  s:
  fill;
  cin>>g;
  if(g==1)
  x=am;
  else if(g==2)
  y=bm;
  else if(g==3)
  exit(0);
  else
  {
   cout<<"WRONG VALUE PLEASE ENTER AGAIN";
   goto s;
  }
 disp(x+48,y+48,am+48,bm+48);
}


void gshift(int am,int bm)
{
 int g;
 int c;
 s:
 shift;
 cin>>g;
 if(g==1)
 {
 c=bm-y;
 if(c<=x)
  {
   x-=c;
   y+=c;
  }
 else if(c>x)
  {
   y+=x;
   x=0;
  }
 }
 else if(g==2)
 {
 c=am-x;
  if(c<=y)
  {
   y-=c;
   x+=c;
  }
  else if(c>x)
  {
   x+=y;
   y=0;
  }
 }
 else if(g==3)
  exit(0);
 else
 {
   cout<<"WRONG VALUE PLEASE ENTER AGAIN";
   goto s;
 }
 disp(x+48,y+48,am+48,bm+48);
}


 void gstart(int am,int bm,int g)
{
 x=y=0;
 r=g;
 disp(x+48,y+48,am+48,bm+48);
}

void glevel()
{
 cout<<"\n\t\tMENU\n\t\t~~~~\n1.LEVEL 1\n2.LEVEL 2\n3.LEVEL 3\nEnter your choice:";
 int ch;
 cin>>ch;
 if(ch==1)
  gstart(9,4,7);
 else if(ch==2)
  gstart(5,7,6);
  else if(ch==3)
   gstart(7,10,9);
}


void start()
{
fstream f,f1;
char c[80];
f.open("test1.txt",ios::in);
f1.open("test.txt",ios::out);
while(!f.eof())
{
f.getline(c,80);
f1<<c<<endl;
}
f.close();
f1.close();
}
void disp()
{
fstream f("test.txt",ios::in);
char ch[80];
while(!f.eof())
{
f.getline(ch,80);
cout<<ch<<endl;
}
f.close();
}
void lmove1(int m)
{
fstream f("test.txt",ios::in|ios::out);
char ch;
while(!f.eof())
 {
  f>>ch;
   if(ch==',')
   {
    ch='\b';
    f.seekp(f.tellg()-3-m,ios::beg);
    for(int x=1;x<=m;x++)
    f<<ch;
    for(int i=1;i!=500;i++)
     {
      f.seekg(i,ios::cur);
      f>>ch;
      if(ch=='|')
       {
	ch=' ';
	f.seekp(-1,ios::cur);
	f<<ch;
	f<<" |";
	i=500;
       }
     }
   }
 }
f.close();
}
void lmove2(int m)
{
fstream f("test.txt",ios::in|ios::out);
char ch;
while(!f.eof())
 {
  f>>ch;
   if(ch=='<')
   {
    ch='\b';
    f.seekp(f.tellg()-3-m,ios::beg);
    for(int x=1;x<=m;x++)
    f<<ch;
    for(int i=1;i!=500;i++)
     {
      f.seekg(i,ios::cur);
      f>>ch;
      if(ch=='|')
       {
	ch=' ';
	f.seekp(-1,ios::cur);
	f<<ch;
	f<<" |";
	i=500;
       }
     }
   }
 }
f.close();
}
void lmove3(int m)
{
fstream f("test.txt",ios::in|ios::out);
char ch;
while(!f.eof())
 {
  f>>ch;
   if(ch=='(')
   {
   ch='\b';
    f.seekp(f.tellg()-3-m,ios::beg);
    for(int x=1;x<=m;x++)
    f<<ch;
    for(int i=1;i!=500;i++)
     {
      f.seekg(i,ios::cur);
      f>>ch;
      if(ch=='_')
       {
	ch=' ';
	f.seekp(-1,ios::cur);
	f<<ch;
	f<<" _______";
	i=500;
       }
     }
   }
 }
f.close();
}
void rmove1(int m)
{
fstream f("test.txt",ios::in|ios::out);
char ch;
while(!f.eof())
 {
  f>>ch;
   if(ch==8)
   {
   ch=255;
    f.seekp(-1,ios::cur);
    f<<ch;
    for(int i=1;i!=500;i++)
     {
      f.seekg(i,ios::cur);
      f>>ch;
      if(ch=='|')
       {
	ch=8;
	f.seekp(-m-7,ios::cur);
	for(int x=1;x<=m;x++)
	f<<ch;
	i=500;
       }
     }
   }
  }
 f.close();
}
void rmove2(int m)
{
fstream f("test.txt",ios::in|ios::out);
char ch;
f.seekg(241,ios::beg);
while(!f.eof())
 {
  f>>ch;
   if(ch==8)
    {
    ch=255;
    f.seekp(-1,ios::cur);
    f<<ch;
    for(int i=1;i!=500;i++)
     {
      f.seekg(i,ios::cur);
      f>>ch;
      if(ch=='|')
       {
	ch=8;
	f.seekp(-m-7,ios::cur);
    for(int x=1;x<=m;x++)
	f<<ch;
	i=500;
       }
     }
   }
 }
f.close();
}
void rmove3(int m)
{
fstream f("test.txt",ios::in|ios::out);
char ch;
f.seekp(321,ios::beg);
while(!f.eof())
 {
  f>>ch;
  if(ch==8)
    {
   ch=255;
   f.seekp(-1,ios::cur);
    f<<ch;
    for(int i=1;i!=500;i++)
     {
      f.seekg(i,ios::cur);
      f>>ch;
      if(ch=='_')
       {
	ch=8;
	f.seekp(-m-3,ios::cur);
	for(int x=1;x<=m;x++)
	f<<ch;
	i=500;
       }
     }
   }
 }
f.close();
}
void dispm(int n)
{
cout<<"Time:"<<time<<endl;
fstream f;
if(n==0)
f.open("b.txt",ios::in);
if(n==1)
f.open("c.txt",ios::in);
if(n==2)
f.open("d.txt",ios::in);
if(n==3)
f.open("e.txt",ios::in);
if(n==4)
f.open("f.txt",ios::in);
if(n==5)
f.open("g.txt",ios::in);
char ch[80];
while(!f.eof())
{
f.getline(ch,80);

for(int c=0;c<=m;c++)
if(l[c]==12)
l[c]=123;
for(c=0;c<=n;c++)
if(ri[c]==12)
ri[c]=123;

for(int i=0,j=0,k=0;ch[i]!='\0';i++)
{
if(ch[i]=='a')
ch[i]=l[j++]+48;
else if(ch[i]=='b')
ch[i]=l[j++]+48;
if(ch[i]=='c')
ch[i]=l[j++]+48;
else if(ch[i]=='d')
ch[i]=l[j++]+48;
if(ch[i]=='e')
ch[i]=l[j++]+48;
else if(ch[i]=='u')
ch[i]=ri[k++]+48;
else if(ch[i]=='v')
ch[i]=ri[k++]+48;
else if(ch[i]=='w')
ch[i]=ri[k++]+48;
else if(ch[i]=='x')
ch[i]=ri[k++]+48;
else if(ch[i]=='y')
ch[i]=ri[k++]+48;
}
cout<<ch<<endl;
}

for(int d=0;d<=m;d++)
if(l[d]==123)
l[d]=12;
for(d=0;d<=n;d++)
if(ri[d]==123)
ri[d]=12;

f.close();
}

void move()
{
clrscr();
start();
int x=0,y=0;
disp();
clrscr();
dispm(m);
disp();
char ch=getch();

do
{
clrscr();
dispm(m);
disp();

if(ch=='a')
{
  lmove1(++x);
  lmove2(x);
  lmove3(x);
//  dispm(m);
 // disp();
  ch=getch();
  if(x==6)
  {
  playrl();
  c();
  if(a>=b)
  clock(a);
  else
  clock(b);
  check();

  }

}
else if(ch=='d')
 {
  rmove1(++y);
  rmove2(y);
  rmove3(y);
//  dispm(m);
//  disp();
  if(x-y==0||y>x)
  {
  start();
  x=y=0;
  playlr();
  c();
  if(a>=b)
  clock(a);
  else
  clock(b);
  check();

  }
  ch=getch();


 }
}while(ch=='a'||ch=='d');
}
void clock(int x)
{
time-=x;
}
void board()
{
mn;

int g=0,h=a;
ch[1]=0;ch[0]=0;
a:
cin>>g;
if(g==1)
ch[0]=1;
else if(g==2)
ch[0]=3;
else if(g==3)
ch[0]=6;
else if(g==4)
ch[0]=8;
else if(g==5)
ch[0]=12;
else if(g==6)
goto a;
cin>>h;
if(h==1)
ch[1]=1;
else if(h==2)
ch[1]=3;
else if(h==3)
ch[1]=6;
else if(h==4)
ch[1]=8;
else if(h==5)
ch[1]=12;
else if(h==6)
ch[1]=0;
}
void playlr()
{
board();
for(int i=0;i<=m;i++)
{
if(ch[0]==l[i])
{
for(int j=i;j<=m;j++)
l[j]=l[j+1];
m--;
}
}
for(i=0;i<=m;i++)
{
if(ch[1]==l[i]&&ch[1]!=0)
{
for(int j=i;j<=m;j++)
l[j]=l[j+1];
m--;
}
}
ri[n++]=ch[0];
if(ch[1]!=0)
{
ri[n++]=ch[1];
}

}


void playrl()
{
board();
for(int i=0;i<=n;i++)
{
if(ch[0]==ri[i])
{
for(int j=i;j<=n;j++)
ri[j]=ri[j+1];
n--;
}
}
for(i=0;i<=n;i++)
{
if(ch[1]==ri[i]&&ch[1]!=0)
{
for(int j=i;j<=n;j++)
ri[j]=ri[j+1];
n--;
}
}
l[m++]=ch[0];
if(ch[1]!=0)
{
l[m++]=ch[1];
}
}
void play()
{
start();
dispm(m);
disp();
playlr();
c();
if(a>=b)
  clock(a);
  else
  clock(b);
  check();

move();
}
void check()
{
if(time<0)
{
clrscr();
cout<<"Mission Failed";
getch();
exit(0);
}

else if(n==5)
{
clrscr();
cout<<"Mission Accmpanished";
getch();
exit(0);
}
}
void c()
{
a=ch[0];
b=ch[1];
}
void main()
{
clrscr();
cout<<"\t\tMENU\n\t\t~~~~\n1.River Crossing\n2.Water Filling";
int ch;
cin>>ch;
clrscr();
if(ch==1)
play();
else if(ch==2)
glevel();
}