# CineMaxPC
Proyecto CineMax

#include <iostream>

using namespace std;

struct Silla
{
    int numeroSilla;
    char * categoria;
};

struct Horario
{
    char * fecha;
    int * numSalas;
    char * hora;
};

struct Sala
{
    int numeroSala;
    int numeroSillas;
    Silla ** sillas;
};

struct Funcion
{
    Sala * salas;
    char * nombrePelicula;
    Horario * horas;
};
hola
