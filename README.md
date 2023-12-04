#include<iostream> 
using namespace std; 
class Shape {
 
  private:
    int l, b, h; 
    double r, h; 
 
  public:
   
    Shape(int l, int b, int h) {
      this->l = l;
      this->b = b;
      this->h = h;
    }
   
    Shape(double r, double h) {
      this->r = r;
      this->h = h;
    }
    
    friend int volume(Shape s);
    friend double volume(Shape s); 
};


int volume(Shape s) {
  return (s.l * s.b * s.h);
}


double volume(Shape s) {
  return (3.14 * s.r * s.r * s.h);
}

int main() {
 
  Shape box(9, 4, 6); 
  Shape cylinder(10.2, 5.5); 
  cout << "Volume of Box :" << volume(box) << endl; 
  cout << "Volume of Cylinder :" << volume(cylinder) << endl; 
  return 0;
}
# Calculate-volume-of-different-shapes
