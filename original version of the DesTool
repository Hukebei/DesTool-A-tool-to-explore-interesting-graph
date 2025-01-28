#include <iomanip>
#include <iostream>
#include <cmath>
using namespace std;

// Struct to hold parabola coefficients
struct ParabolaCoefficients {
    double A;
    double B;
    double C;
};

// Function to calculate parabola coefficients
ParabolaCoefficients calcParabolaVertex(double x1, double y1, double x2, double y2, double x3, double y3) {
    ParabolaCoefficients coeffs;
    coeffs.A = ((y3 - (x3 * (y2 - y1) + x2 * y1 - x1 * y2) / (x2 - x1)) / (x3 * (x3 - x1 - x2) + x1 * x2));
    coeffs.B = (y2 - y1) / (x2 - x1) - coeffs.A * (x1 + x2);
    coeffs.C = y1 - coeffs.A * x1 * x1 - coeffs.B * x1;

    return coeffs;
}

// Function to display the parabola equation
void displayParabolaEquation(double A, double B, double C) {
    cout << fixed << setprecision(2);
    cout << "The parabola equation is: y = " 
         << A << "x^2 + " 
         << B << "x + " 
         << C << endl;
}

// Function to find and display circle equation
void findCircleEquation(double h, double k, double r) {
    if (r <= 0) {
        cout << "Invalid radius. Radius must be greater than 0." << endl;
        return;
    }

    cout << "The equation of the circle is: " << endl;
    cout << "(x - " << h << ")^2 + (y - " << k << ")^2 = " << r * r << endl;
}

int main() {
    int a, a1,a2;
    cout << "Welcome to Desmos Helper App v0.1 by Kaibin Huang\n";
    cout << "Choose an option:\n";
    cout << "1000: Calculate equations for Desmos\n";
    cout << "1001: View beautiful pre-existing graph equations\n";
    cin >> a;

    if (a == 1000) {
        cout << "1: Find a parabola equation using three points\n";
        cout << "2: Find a circle equation\n";
        cout << "3: Find a triangle\n";
        cout << "4: Find a quadrilateral\n";
        cin >> a1;

        if (a1 == 1) {
            double x1, y1, x2, y2, x3, y3;

            // Input three points
            cout << "Enter x1, y1: "<<endl;
            cin >> x1 >> y1;
            cout << "Enter x2, y2: "<<endl;
            cin >> x2 >> y2;
            cout << "Enter x3, y3: "<<endl;
            cin >> x3 >> y3;

            // Check for valid input
            if ((x1 == x2) || (x1 == x3) || (x2 == x3)) {
                cout << "Error: x-coordinates must be distinct.\n";
                return 1;
            }

            // Calculate coefficients
            ParabolaCoefficients coeffs = calcParabolaVertex(x1, y1, x2, y2, x3, y3);

            // Display results
            displayParabolaEquation(coeffs.A, coeffs.B, coeffs.C);
        } 
        if (a1 == 2) {
            double h, k, r;

            // Input center and radius
            cout << "Enter the x-coordinate of the center: ";
            cin >> h;
            cout << "Enter the y-coordinate of the center: ";
            cin >> k;
            cout << "Enter the radius of the circle: ";
            cin >> r;

            // Display circle equation
            findCircleEquation(h, k, r);
        }
       if (a1 == 3) {
        double x1, y1, x2, y2, x3, y3;

        // Input three points
        cout << "Enter x1, y1: " << endl;
        cin >> x1 >> y1;
        cout << "Enter x2, y2: " << endl;
        cin >> x2 >> y2;
        cout << "Enter x3, y3: " << endl;
        cin >> x3 >> y3;

        // Check if points form a valid triangle
        double area = 0.5 * abs(x1 * (y2 - y3) + x2 * (y3 - y1) + x3 * (y1 - y2));
        if (area == 0) {
            cout << "Error: Points must not be collinear to form a triangle.\n";
            return 1;
    }

        // Display triangle polygon equation
         cout<<"code:"<<endl;
        cout << "\\operatorname{polygon}\\left(\\left("
            << x1 << "," << y1 << "\\right),\\left("
            << x2 << "," << y2 << "\\right),\\left("
            << x3 << "," << y3 << "\\right)\\right)" << endl;
       }
        if (a1 == 4) {
            double x1, y1, x2, y2, x3, y3, x4, y4;

            // Input four points
            cout << "Enter x1, y1: " << endl;
            cin >> x1 >> y1;
            cout << "Enter x2, y2: " << endl;
            cin >> x2 >> y2;
            cout << "Enter x3, y3: " << endl;
            cin >> x3 >> y3;
            cout << "Enter x4, y4: " << endl;
            cin >> x4 >> y4;

            // Check for validity: Ensure no three points are collinear
            double area1 = 0.5 * abs(x1 * (y2 - y3) + x2 * (y3 - y1) + x3 * (y1 - y2));
            double area2 = 0.5 * abs(x1 * (y3 - y4) + x3 * (y4 - y1) + x4 * (y1 - y3));
            if (area1 == 0 || area2 == 0) {
                cout << "Error: Points must not be collinear or degenerate to form a quadrilateral.\n";
                return 1;
            }

            // Display quadrilateral polygon equation
            cout<<"code:"<<endl;
            cout << "\\operatorname{polygon}\\left(\\left("
                << x1 << "," << y1 << "\\right),\\left("
                << x2 << "," << y2 << "\\right),\\left("
                << x3 << "," << y3 << "\\right),\\left("
                << x4 << "," << y4 << "\\right)\\right)" << endl;
        }

        else {
            cout << "Feature under construction. Please check back later.\n";
        }
    } else if (a == 1001) {
        cout << "1: Heart Shape\n";
        cout << "2: Lemniscate\n";
        cout << "3: Swirling Wave\n";
        cout << "4: Parametric Flower\n";
        cout << "5: Hypotrochoid\n";
        cout << "6: Epicycloid\n";
        cout << "7: Cassini Oval\n";
        cout << "8: Astroid\n";
        cout << "9: Lissajous Curve\n";
        cout << "10: Sine Weave\n";
        cout << "11: Damped Wave\n";
        cout << "12: Harmonograph\n";
        cout << "13: Peanut Shape\n";
        cout << "Other beautiful graph equations coming soon!\n";
        cin >> a2;
        if(a2==1){
            cout<<"(x^2 + y^2 - 1)^3 - x^2y^3 = 0"<<endl;
        }
        if(a2==2)
         {
            cout<<"(x^2 + y^2)^2 = a^2(x^2 - y^2)"<<endl;
            cout<<"Set a = 1 in Desmos"<<endl;
        } 
        if(a2==3)
        {
            cout<<"y = sin(5x)*cos(3x)"<<endl;
        } 
        if(a2==4)
        {
            cout<<"x = sin(2t)*cos(5t)"<<endl;
            cout<<"y = sin(2t)*sin(5t)"<<endl;
        } 
        if(a2==5)
        {
            cout<<"x = (a - b) * cos(t) + h * cos((a - b) / b * t)"<<endl;
            cout<<"y = (a - b) * sin(t) - h * sin((a - b) / b * t)"<<endl;
            cout<<"Set a = 5, b = 3, h = 4"<<endl;
        } 
        if(a2==6)
        {
            cout<<"x = (a + b) * cos(t) - b * cos((a + b) / b * t)"<<endl;
            cout<<"y = (a + b) * sin(t) - b * sin((a + b) / b * t)"<<endl;
            cout<<"Set a = 3, b = 1."<<endl;
        } 
        if(a2==7)
        {
            cout<<"(x^2 + y^2)^2 - 2 * c^2 * (x^2 - y^2) = (a^4 - c^4)"<<endl;
            cout<<"Set a = 2, c = 1.5."<<endl; 
        } 
        if(a2==8)
        {
            cout<<"x^(2/3) + y^(2/3) = a^(2/3)"<<endl;
            cout<<"Set a = 1"<<endl;
        } 
        if(a2==9)
        {
            cout<<"x = A * sin(a * t + δ)"<<endl;
            cout<<"y = B * sin(b * t)"<<endl;
            cout<<"Set A = 1, B = 1, a = 5, b = 4, δ = π/2."<<endl;
        } 
        if(a2==10)
        {
            cout<<"y = sin(x) + sin(2x)"<<endl;
        } 
        if(a2==11)
        {
            cout<<"y = e^(-0.1x) * sin(5x)"<<endl;
        } 
        if(a2==12)
        {
            cout<<"x = A * sin(a * t + φ)"<<endl;
            cout<<"y = B * sin(b * t)"<<endl;
            cout<<"Set A = 1, B = 1, a = 2, b = 3, φ = π/4."<<endl;
        }
        if(a2==13)
        {
            cout<<"(x^2 + y^2)^2 = 4 * a^2 * x^2 + 4 * b^2 * y^2"<<endl;
            cout<<"Set a = 1, b = 0.5."<<endl;
        }
        
    } else {
        cout << "Invalid option selected. Exiting.\n";
    }

    return 0;
}
