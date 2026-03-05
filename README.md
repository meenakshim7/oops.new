//1.
#include <iostream>
using namespace std;
class Animal 
{
public:
    void eat() 
    {
        cout << "Animal is eating" << endl;
    }
};
class Dog : public Animal 
{
public:
    void bark() 
    {
        cout << "Dog is barking" << endl;
    }
};
int main() 
{
    Dog d;
    d.eat();
    d.bark();
}


//2.
#include <iostream>
using namespace std;
class Animal 
{
public:
    void eat() { cout << "Animal eats" << endl; }
};
class Dog : public Animal 
{
public:
    void bark() { cout << "Dog barks" << endl; }
};
class Puppy : public Dog 
{
public:
    void weep() { cout << "Puppy weeps" << endl; }
};
int main() 
{
    Puppy p;
    p.eat();
    p.bark();
    p.weep();
}


//3.
#include <iostream>
using namespace std;
class A 
{
public:
    void showA() { cout << "Class A" << endl; }
};
class B 
{
public:
    void showB() { cout << "Class B" << endl; }
};
class C : public A, public B {};
int main() 
{
    C obj;
    obj.showA();
    obj.showB();
}


//4.
#include <iostream>
using namespace std;
class Base 
{
public:
    virtual void show() 
    {
        cout << "Base class show" << endl;
    }
};
class Derived : public Base 
{
public:
    void show() 
    {
        cout << "Derived class show" << endl;
    }
};
int main() 
{
    Base* b;
    Derived d;
    b = &d;
    b->show();
}


//5.
#include <iostream>
using namespace std;
class Shape 
{
public:
    virtual void area() 
    {
        cout << "Area of shape" << endl;
    }
};
class Circle : public Shape 
{
public:
    void area() 
    {
        cout << "Area of Circle" << endl;
    }
};
class Square : public Shape 
{
public:
    void area() 
    {
        cout << "Area of Square" << endl;
    }
};
int main() 
{
    Shape* s;
    Circle c;
    Square sq;
    s = &c;
    s->area();
    s = &sq;
    s->area();
}


//6.
#include <iostream>
using namespace std;
class Shape 
{
public:
    virtual void draw() = 0;
};
class Circle : public Shape 
{
public:
    void draw() 
    {
        cout << "Drawing Circle" << endl;
    }
};
int main() 
{
    Circle c;
    c.draw();
}


//7.
#include <iostream>
using namespace std;
class Vehicle 
{
public:
    virtual void start() = 0;
};
class Car : public Vehicle 
{
public:
    void start() 
    {
        cout << "Car starts with key" << endl;
    }
};
int main() 
{
    Car c;
    c.start();
}


//8.
#include <iostream>
using namespace std;
class Base 
{
public:
    virtual ~Base() 
    {
        cout << "Base destructor" << endl;
    }
};
class Derived : public Base 
{
public:
    ~Derived() 
    {
        cout << "Derived destructor" << endl;
    }
};
int main() 
{
    Base* b = new Derived();
    delete b;
}


//9.
#include <iostream>
using namespace std;
class Drawable 
{
public:
    virtual void draw() = 0;
};
class Rectangle : public Drawable 
{
public:
    void draw() 
    {
        cout << "Drawing Rectangle" << endl;
    }
};
int main() 
{
    Rectangle r;
    r.draw();
}


//10.
#include <iostream>
using namespace std;
class Employee 
{
public:
    virtual void salary() 
    {
        cout << "Employee salary" << endl;
    }
};
class Manager : public Employee 
{
public:
    void salary() 
    {
        cout << "Manager salary: 50000" << endl;
    }
};
class Developer : public Employee 
{
public:
    void salary() 
    {
        cout << "Developer salary: 40000" << endl;
    }
};
int main() 
{
    Employee* e;
    Manager m;
    Developer d;
    e = &m;
    e->salary();
    e = &d;
    e->salary();
}
