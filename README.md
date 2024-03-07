# Clase_10_matrices

#include <iostream>
#include <stdlib.h>

using namespace std;

int leer_radios(float rac[][20]);
void conversiones(float radio, float& area, float& cir);
void asignar(float rac[][20], int num_rac);
void imprimir(float rac[][20], int num_rac);

int main() {

    float RAC[3][20]{};
    int nradios = leer_radios(RAC);

    asignar(RAC,nradios);
    imprimir(RAC, nradios);

    system("Pause");
    return 0;
}

//funcion 1: Leer y asignar radios

int leer_radios(float rac[][20]) {

    int num_rad = 0;

    cout << "Cuantos radios quiere ingresar: ";
    cin >> num_rad;

    system("cls");

    for (int i = 0; i < num_rad; i++)
    {
        cout << "Radios quiere ingresar en la posicion [" << i + 1 << "]: ";
        cin >> rac[0][i];
        cout << endl;
    }

    return num_rad;
}

//funcion 2

void conversiones(float radio, float& area, float& cir) {

    area = 3.1416 * pow(radio, 2);
    cir = 2 * 3.1416 * radio;

}

//funcion 3

void asignar(float rac[][20], int num_rac){


    for (int i = 0; i < num_rac; i++)
    {
        conversiones(rac[0][i], rac[1][i], rac[2][i]);

    }

}

//funcion 4

void imprimir(float rac[][20], int num_rac) {

    for (int i = 0; i < num_rac; i++)
    {
        cout << "Para el radio [" << i + 1 << "]" << endl;
        cout << "Radio: " << rac[0][i] << endl;
        cout << "Area: " << rac[1][i] << endl;
        cout << "Circunferencia: " << rac[2][i] << endl << endl;
    }

}
