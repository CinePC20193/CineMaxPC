# CineMaxPC
Proyecto CineMax

#include <iostream>

using namespace std;

struct Silla
{
    int numeroSilla; //A20, J8, ....
    char * categoria; //Si la silla es general o preferencial
    bool disponibilidad;  //Si la silla ya esta ocupada (TRUE O FALSE)
};

struct Sala
{
    int numeroSala; // Sala 1, Sala 2, Sala 3, ....
    int numeroSillas; // Numero de Silla que tiene la sala
    Silla ** sillas; // Matriz de la sillas 
};

struct Funcion
{
    char * nombrePelicula; //Malefica, La Vida Secreta de Tres Hackers, etc 
    char * duracionCartelera; //Cuanto durará en cartelera
    char * duracionPelicula; //2h30min, 1:30, etc
    Sala *** horarioSemanal; //Horario que contien las salas donde se proyectará la película 
};

struct Catalogo 
{
    Funcion funcion; //El tipo de información que tendría el catalogo sería las funciones que tiene el cine 
    Catalogo * sigFuncion; //Opuntador a la sig. función 
};

struct Cine 
{
    Catalogo * cabeza;
    int tam; 
};
