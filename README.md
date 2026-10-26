  #include <iostream>
using namespace std;

int main() {
    int num, m, c, d, u;
    long suma;
    cout << "Ingrese numero de 4 digitos: ";
    cin >> num;

    if (num < 1000 || num > 9999) {
        cout << "No es de 4 digitos";
        return 0;
    }

    m = num / 1000;
    c = (num / 100) % 10;
    d = (num / 10) % 10;
    u = num % 10;

    // m^4 + c^4 + d^4 + u^4
    suma = (m*m*m*m) + (c*c*c*c) + (d*d*d*d) + (u*u*u*u);

    if (suma == num) {
        cout << num << " es Armstrong";
    } else {
        cout << num << " NO es Armstrong";
    }
    return 0;
}
