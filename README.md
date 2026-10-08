# bai-1.4
public class Employee 
{
    int id;
    String firstname ;
    String lastname ;
    int salary;
    public Employee (int i , String f , String l , int s)
    {
        id=i;
        firstname=f;
        lastname=l;
        salary=s;
    }
    public int getid()
    {
        return id;
    }
    public String getfirstname()
    {
        return firstname;
    }
    public String getlastname()
    {
        return lastname;
    }
    public String getname()
    {
        return firstname + lastname;
    }
    public int getsalary()
    {
        return salary;
    }
    public void setsalary(int s)
    {
        salary=s ;
    }
    public int getannualsalary()
    {
        return salary*12;
    }
    public int raisesalary(int percent)
    {
        salary+=salary*percent/100;
        return salary;
    }
    public String toString()
    {
        return "Employee[id="+id+",name="+firstname+" "+lastname+",salary="+salary+"]";
    }
}
# bai 1.5
public class InvoiceItem {
    String id;
    String desc;
    int qty;
    double unitPrice;
    public InvoiceItem(String i , String d , int q , double uP )
    {
        id=i;
        desc=d;
        qty=q;
        unitPrice=uP;
    }
    public String getId()
    {
        return id;
    }
    public String getDesc()
    {
        return desc;
    }
    public int getQty()
    {
        return qty;
    }
    public void setQty(int q)
    {
        qty=q;
    }
    public double getUnitPrice()
    {
        return unitPrice;
    }
    public void setUnitPrice(double uP)
    {
        unitPrice=uP;
    }
    public double getTotal()
    {
        return unitPrice*qty;
    }
    public  String toString()
    {
        return "InvoiceItem[id=" + id +",desc=" + desc +",qty="+qty+",unitPrice="+ unitPrice +"]";
    }
}
#bai 1.6
public class Account {
    String id ;
    String name ;
    int balance = 0 ;
    public Account(String i , String n)
    {
        id=i;
        name=n;
    }
    public Account(String i , String n , int b)
    {
        id=i;
        name=n;
        balance=b;
    }
    public String getId() 
    {
        return id;
    }
    public String getName()
    {
        return name;
    }
    public int getBalance()
    {
        return balance;
    }
    public  int credit(int amount)
    {
        balance += amount;
        return balance;
    }
    public int debit(int amount)
    {
        if (amount <= balance)
        {
            balance -= amount;
        }
        else
        {
            System.out.println("Amount exceeded balance");
        }
        return balance;
    }
    public int transferTo(Account another, int amount) 
    {
    if (amount <= balance) 
    {
        balance -= amount;
        another.credit(amount);
    } 
    else 
    {
        System.out.println("Amount exceeded balance");
    }
    return balance;
    }
    public String toString() {
    return "Account[id=" + id + ",name=" + name + ",balance=" + balance + "]";
    }
}
