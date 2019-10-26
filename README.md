/*              CineMax

Proyecto final Programación de Computadores
Integrantes:
            Estefania Bermudez Arroyo
            Jessica Tatiana Naizaque Guevara
            Angie Tatiana Peña Peña
Descripción: Código para la administración de un cine con salas multiplex,
que permite la venta de boletas para distintas funciones. */

#include <math.h>
#include <iomanip>
#include <fstream>
#include <iostream>
#include <string.h>
#include <stdlib.h>
#include "listas.cpp"

using namespace std;
/* Declaración de las estructuras */

struct sSilla
{
    char * numSilla; /*A20, J8, .... */
    char * cat;/*Si la silla es general o preferencial*/
    bool dispo;/*Si la silla ya esta ocupada (TRUE O FALSE)*/
};

struct sSala
{
    int numSala;/*Sala 1, Sala 2, Sala 3, ....*/
    int numSillas;/* Numero de Silla que tiene la sala*/
    Lista<sSilla> * sillas;/*Matriz de la sillas*/
    char ** proyecciones; /*Nombre de las películas que se van a propyectar en es sala*/
};

struct sFuncion
{
    char * NomPelicula;/*Malefica, La Vida Secreta de Tres Hackers, etc*/
    char * durCarte;/*Cuanto durará en cartelera*/
    char * durPeli;/*2h30min, 1:30, etc*/
    int * numSalas; /*Numero de las salas donde se va a proyectar la película*/
};

//----------------------------------------------configuracionInicial------------------------------------------------------
// Es la configuración inicial de todo el sistema, es decir, la configuración de las salas, de las sillas y de las funciones 
// Esta configuración inical se debe hacer desde un archivo 
//En el archivo de "ConfiguraciónInicial.txt" voy a dividir sel archivo por secciones (1. Función, 2.Sala, 3.Silla)

void configuracionInicial (sLista * listaCine) 

                                            
//-------------------------------------------------configuracion-----------------------------------------------------
//Recibo la lista de la sección que deseo modificar, es decir, si deseo modificar las salas, las silla o las funciones
//Recibo la lista general donde se guarda toda la información del cine, esto para poder volver llenar el archivo "Configuración.txt"
//Estas configurciones se tienen que guardar en un mismo archivo, es decir, "Configuracion.txt"
//Realizamos el cambio, si "Configuración.txt" en la sección que me mandaron es igual a la lista a la cual le realicé la modificación, retorno TRUE
//Estas configurciones se tienen que guardar en un mismo archovo, es decir, "Configuracion.txt"
//La función retorna TRUE en caso de que la modificación se exitosa, en caso contrario, retorna FALSE

template <typename T>
bool configuracion (sLista <T> * listaModif, sLista <T> * listaGrande)


//--------------------------------------------------adicionar---------------------------------------------------------
//Recibo la lista donde quiero adicionar información y la información que voy a agregar en la lista 
//Recibo la lista donde quiero adicionar información y la información que voy a agrgar en la lista 

template <typename T>
void adicionar (Lista <T> * lista, T infoNueva)


//------------------------------------------------eliminar-------------------------------------------------------------
//Recibo  la lista donde quiero eliminar información, recibo la información que quiero eliminar
//Recordar que se debe borrar memoria
//La función retorna TRUE cuando la operación fue exitosa, en caso contrario, retorna FALSE 

template <typename T>
bool eliminar (Lista <T> * lista, T infoEliminar)


//---------------------------------------------genTiquete----------------------------------------------------------
//Recibo el nombre de la película que el usuario pidio, recibimos en número de la proyección (1 (9:00-11:00))
//Buscamos la sala que cumple con las dos condiciones, es decir, que tenga esa película en ese número de proyección, en la matriz que se tiene de proyecciones en la lista de salas
//Al final se crearía un archivo "Tiquete.txt" donde se vea el nombre de la película el horario en el que se va a presentar y en la sala donde se va a presentar 

void genTiquete (char* nomPelicula, int proyeccion, sLista <sSala> * listaSala)


//----------------------------------------------------color--------------------------------------------------------
//Recibe un número que está establecido en el compilador para generar un fondo con un color y un texto con otro color (predeterminados en una tabla con 256 combinaciones)

int color (int num)
