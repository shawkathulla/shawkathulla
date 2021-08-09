import java.util.Scanner;

class _5Assignment
{
    public static void main(String args[])
    {
        System.out.println("This Program will calculate the area of Triangle and Rectangle");
        System.out.println("Enter the Height : ");
        Scanner sc = new Scanner(System.in);
        float h = sc.nextFloat();
        System.out.println("Enter the Base or Width : ");
        float b = sc.nextFloat();
        Area a = new Triangle();
        a.cal(h,b);
        Area c = new Rectangle();
        c.cal(h,b);
        a.display();
        c.display();
    }
}

abstract class Area
{
    abstract void cal(float a1 , float b1);
    
    void display()
    {
        System.out.println("The Calculated Area for the Triangle and Rectangle : ");
    }
}

class Triangle extends Area
{
    double a;
    void cal(float h, float b)
    {
    this.a = ((0.5)*h*b);
    }
    void display()
    {
    super.display();
    System.out.println("The area of triangle is : "+a);
    }
}

class Rectangle extends Area
{
    double a;
    void cal(float h,float b)
    {
    this.a = (h*b);
    }
    void display()
    {
    System.out.println("The area of Rectangle is : "+a);
    }
}
