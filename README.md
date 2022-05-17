# Ticket-Reservation-

#include<iostream>
#include<fstream>
#include<conio.h>

class Tourbus
{
  int id;
  char destination[200];
  char time[60];
  int maxseats;
  int booked;
  
  public:
  Tourbus()
  {
    id = 0;
    maxseats = 60;
    booked = 0;
    strcpy(destination, " ");
    strcpy(time, "8 : 00 am");
    
  }

  }
