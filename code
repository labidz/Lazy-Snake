#include <iostream>
#include<conio.h>
#include <cstdlib>

using namespace std;

string s="s";
int width=50;
int height=20;
int x=rand()%(height-1);
int y=rand()%(width-1);
int mex=height/2;
int mey=width/2;
bool game=false;
int score =0;
char c;

gamestatus()
{
	game=true;
	if(mey>(width-3)){
	 mey--;
	}
	else if(mex>(height-1)){
		mex--;
	}
	else if(mex<0){
		mex++;
	}
	else if(mey<0){
		mey++;
	}
	s='x';
}

location(){
	x=rand()%(height-1);
	y=rand()%(width-2);
}

body()
{
	//UnFinished;
}

draw()
{
	cout<<"\n"<<"Score: "<<score<<"\nHighScore:211"<<endl;
	if(mey>(width-3)||mex>(height-1)||mex<0||mey<0)
	{
		gamestatus();
	}
  for(int i=0;i<width-1;i++){
  	if(i==0)
  	{cout<<" ";
	  }
  	cout<<"_";
}
	cout<<endl;
	for(int i=0;i<height;i++){
		cout<<"|";
		for(int j=0;j<width-1;j++){
			if(x==mex&&y==mey){
			location();
			score++;
			body();
		}
		if(i==mex&&j==mey){
			cout<<s;
			j+=s.length();
		}
			if(j==y&&i==x){
			cout<<"o";
			j++;
		}
			cout<<" ";
		}
		cout<<"|"<<endl;
	}
	for(int i=1;i<width;i++){
  	if(i==1)
  	{cout<<" ";
	  }
  	cout<<"-";
}
if(game!=true)
	system("cls");
}

key()
{
	if(_kbhit())
	{
		c=_getch();
	}
	if(c=='w')
	mex--;
	else if(c=='a')
	mey--;
	else if(c=='s')
	mex++;
	else if(c=='d')
    mey++;
}

int main()
{
	cout<<"\t\t\t\t\tWelcome to Snake Game\n"<<"\t\t\t\t\tPress Any Key to Start";
	getch();
	while(game!=true)
	{
	 draw();
	 key();
	 	}
	cout<<"\n"<<"Game Over";
}
