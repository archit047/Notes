# Notes

include<iostream>
using namespace std;


class ATM_Realtime2_after_demonetisation
{

int w1,w2,w3,w4,z=0,z1=0,z2=0,z3=0;

void insufficient()
{
          cout<<"amount is not present.....Insufficient balance"<<endl;
}


void enter_pair()
{
cout<<"the amount is not in the factor of available denominations......please enter the multiple denominations\n";
}


void note(int n)
{

    int counter=0;
    while(n>0)
    {
        if(n>=w1)
        {
            if(a>z)
            {
                z++;
            counter++;
            n-=w1;
            }

        }

         if(n>=w2)
        {
            if(b>z1)
            {
              z1++;
            counter++;
            n-=w2;
            }
        }
         if(n>=w3)
        {
            if(c>z2)
            {
             z2++;
            counter++;
            n-=w3;
            }
        }
          if(n>=w4)
        {
            if(d>z3)
            {
                z3++;
            counter++;
            n-=w4;
            }
        }

   }
    return counter ;
}


};


class ATM_Realtime1_before_demonetisation                             // Derived class
{
int a, b, c, d, z=0, z1=0, z2=0, z3=0;


void insufficients()
{
          cout<<"amount is not present.....Insufficient balance"<<endl;
}


void enter_pairs()
{
cout<<"the amount is not in the factor of available denominations ....please enter the multiple denominations\n";
}


void notes(int n)
{

    int counter=0;
    while(n>0)
    {
        if(n>=2000)
        {
            if(a>z)
            {
                z++;
            counter++;
            n-=2000;
            }

        }

         if(n>=500)
        {
            if(b>z1)
            {
              z1++;
            counter++;
            n-=500;
            }
        }
         if(n>=200)
        {
            if(c>z2)
            {
             z2++;
            counter++;
            n-=200;
            }
        }
          if(n>=100)
        {
            if(d>z3)
            {
                z3++;
            counter++;
            n-=100;
            }
        }

   }
    return counter ;
}

};



class SBI_Account : public ATM_Realtime2_after_demonetisation, public ATM_Realtime1_before_demonetisation                        // multiple inheritence
{

char name;
int acno;
float balance;

void account()
{

        cout << " Account Number: \n";
        cout<<acno<<"\n";
        cout << "Name: \n ";
        cout<<name<<"\n";
        cout << "Balance: \n";
        cout<<balance<<"\n";

}

  
};


int main()
{
SBI_Account obj;
int t,n1,a1,b1,c1,d1,a2,b2,c2,d2;
char demonetisations;

obj.name="ARCHIT NEGI";
obj.acno=99xx xxxx xxxx xx78;
obj.balance=20000;

obj.account();

cout<<" the number of notes of the denominations which are present in the banks \n";
            cout<<"for 2000\n";
            cin>>a1;
            cout<<"for 500\n";
            cin>>b1;
            cout<<"for 200\n";
            cin>>c1;
            cout<<"for 100 \n";
            cin>>d1;



obj.a=a1;
obj.b=b1;
obj.c=c1;
obj.d=d1;   

         

cout<<"demonetisation occurs enters yes or no\n";
cin>>demonetisation;

switch(demonetisation)
{                  
case "YES":
cout<<"enter the new notes currency after the demonetisation\n";
 cin>>a2>>b2>>c2>>d2;

obj.w1=a2;
obj.w2=b2;
obj.w3=c2;
obj.w4=d2;

cout<<"Enter the amount of your choice .......____.......____.......\n";
        cin>>n;

         if(n<100)
        {
            obj.insufficient();
            break;
        }

         else if(n%10 == 0)
        {
            obj.note(n);
        }

           else if(n%10!=0 && n<100)
        {
            obj.enter_pair();
            break;
        }
break;

case"NO":
cout<<"Enter the amount of your choice .......____.......____.......\n";
        cin>>n;

        

        if(n<100)
        {
            obj.insufficients();
            break;
        }

          else if(n%10 == 0)
        {
            obj.notes(n);
        }


        else if(n%10!=0 && n<100)
        {
            obj.enter_pairs();
            break;
        }
break;

default:
break;
}




return 0;
}
