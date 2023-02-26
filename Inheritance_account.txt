package account;
import java.util.Scanner;
class account{
String name;
int number;
String type;
account(){};
account(int number,String name,String type){
this.number=number;
this.name=name;
this.type=type;
}
void getdetails(){
Scanner ob=new Scanner(System.in);  
System.out.print("Enter the customer name:");
name=ob.next();
System.out.print("Enter the account number:");
number=ob.nextInt();
System.out.print("Enter the account type:");
type=ob.next();
}
void display(){
    System.out.print("Customer Name:"+ name);
    System.out.print("\nAccount Number:"+number);
    System.out.print("\nAccount Type:"+type);
}
}
class current extends account{
    double deposit;
    double withdraw;
    double balance;
    current(){};
    current(double deposit,double withdraw,double balance,int number,String name,String type){
    super(number,name,type);
    this.deposit=deposit;
    this.withdraw=withdraw;
    this.balance=balance;
    }
    void deposit(){
    Scanner ob=new Scanner(System.in);      
    System.out.print("Enter the deposite amount:");
    deposit=ob.nextDouble();
    }
    void withdraw(){
    Scanner ob=new Scanner(System.in);   
    System.out.print("Enter the withdrawal amount:");
    withdraw=ob.nextDouble();
    }
    void balance(){
    balance=deposit-withdraw;
    System.out.print("Balance amount:"+balance);
    System.out.println();
    }
    void display(){
        System.out.println("DETAILS of Current Account");
        super.display();
        System.out.println("\nDeposit amount:"+deposit);
        System.out.println("Withdrawal amount:"+withdraw);
        System.out.println("Balance amount:"+balance);
    }
    
}
class savings extends account{
    double deposit;
    double withdraw;
    double balance;
    savings(){};
    savings(double deposit,double withdraw,double balance,int number,String name,String type){
    super(number,name,type);
    this.deposit=deposit;
    this.withdraw=withdraw;
    this.balance=balance;
    }
    void deposit(){
    Scanner ob=new Scanner(System.in);      
    System.out.print("Enter the deposite amount:");
    deposit=ob.nextDouble();
    }
    void withdraw(){
    Scanner ob=new Scanner(System.in);   
    System.out.print("Enter the withdrawal amount:");
    withdraw=ob.nextDouble();
    }
    void balance(){
    balance=deposit-withdraw;
    System.out.print("Balance amount:"+balance);
    System.out.println();
    
    }
    void display(){
        System.out.println("DETAILS of Savings Account");
        super.display();
        System.out.println("\nDeposit amount:"+deposit);
        System.out.println("Withdrawal amount:"+withdraw);
        System.out.println("Balance amount:"+balance);
        }
}
public class Accountmain {
    public static void main(String[] args) {
     current ob1=new current(); 
     ob1.getdetails();
     ob1.deposit();
     ob1.withdraw();
     ob1.balance();    
     ob1.display();
     savings ob2=new savings();
     ob2.getdetails();
     ob2.deposit();
     ob2.withdraw();
     ob2.balance();
     ob2.display();
    }
    
}
