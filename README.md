# Ticket-Reservation-

#include<iostream>
#include<fstream>
#include<conio.h>
#include<string.h>

class Tourbus
{
  int id;
  char destination[200];
  char time[60];
  int maxseats;
  int booked;
  int fare;
  
  public:
  Tourbus()
  {
    id = 0;
    maxseats = 60;
    booked = 0;
    fare = 0;
    strcpy(destination, " ");
    strcpy(time, "8 : 00 am");
  }
  void input();
  void show();
  void display();
  int getID()
  {
    return id;
  }
  char getDestination()
  {
    return destination;
  }
  char getTime()
  {
    return time;
  }
  int getmax()
  {
    return maxseats;
  }
  int getbook()
  {
    return booked;
  }
  int getFare()
  {
    return fare;
  }
  
};
class Ticket
{
  
  
  
  
  
  
  
  
  
void Tourbus::input()
{
  cout<<"Enter Bus ID : ";
  cin>>id;
  cout<<"Enter Destination : ";
  cin>>destination;
  cout<<"Enter Time : ";
  cin>>time;
}
void Tourbus::display()
{
  cout<<time<<"\t"<<id<<"\t"<<destination<<"\t"<<maxseats<<"\t"<<booked<<"\n";
}

void main()
{
  Tourbus b;
  fstream F;
  int pr;
  
  cout<<"Press 1 - Add a new bus. \n";
  cout<<"Press 2 - Display all Buses. \n";
  cout<<"Press 3 - Delete Buses. \n";
  cout<<"Press 4 - Book a ticket. \n";
  cout<<"Press 5 - Show selected Bus. \n";
  cout<<"Press 6 - Exit. \n";
  cout<<"Enter your choice : ";
 
  cin>>pr;

  switch(pr)
  {
    case 1:
    F.open("New.dat", ios::app : ios::binary);
    b.input();
    F.write((char*)&b , sizeof(b));
    F.close();
    cout<<"Bus Added successfull. \n";
    getch();
    clrscr();
    break;
  
    case 2:
    F.open("New.dat", ios::in : ios::binary);
    if(F.fail())
    {
      cout<<"Can\'t open the file.\n";
    }  
    else
    {
       while(F.read((char*)&b,sizeof(b)))
       b.display();
    }
    F.close();
    cout<<"Press a key to continue. \n";
    getch();
    clrscr();
    break;
  
    case 3:
    F.open("New.dat", ios::app : ios::binary);
    
    
  
  
  }
  
  
  
  

  
  
  
  
  
  
  
  
  
  
  
  
  
