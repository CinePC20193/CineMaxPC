# CineMaxPC

#include <iostream>

using namespace std;

struct sSilla 
{
    int numSilla; //A20, J8, ....
    char * cat; //Si la silla es general o preferencial
    bool dispo;  //Si la silla ya esta ocupada (TRUE O FALSE)
};

struct sSala
{
    int numSala; // Sala 1, Sala 2, Sala 3, ....
    int numSillas; // Numero de Silla que tiene la sala
    Silla ** sillas; // Matriz de la sillas 
};

struct sFuncion
{
    char * nomPelicula; //Malefica, La Vida Secreta de Tres Hackers, etc 
    char * durCartelera; //Cuanto durará en cartelera
    char * durPelicula; //2h30min, 1:30, etc
    Sala *** horarioSemanal; //Horario que contien las salas donde se proyectará la película 
};

template <typename T>
struct sNodo
{
    T info;
    Nodo <T> * sig; 
};
    
template <typeName T>
struct Lista 
{
    Nodo <T> * cab;
    int tam; 
};

//----------------------------------------------configuracionInicial------------------------------------------------------
// Es la configuración inicial de todo el sistema, es decir, la configuración de las salas, de las sillas y de las funciones 
// Esta configuración inical se debe hacer desde un archivo 

template <typename T>
void configuracionInicial (Lista <T> * lista) 
     
                                            
//-------------------------------------------------configuracion-----------------------------------------------------
//Recibo la lista de la sección que deseo modificar, es decir, si deseo modificar las salas, las silla o las funciones
//Estas configurciones se tienen que guardar en un mismo archovo, es decir, "Configuracion.txt"
//La función retorna TRUE en caso de que la modificación se exitosa, en caso contrario, retorna FALSE

template <typename T>
bool configuracion (Lista <T> * lista)


//--------------------------------------------------adicionar---------------------------------------------------------
//Recibo la lista donde quiero adicionar información y la información que voy a agrgar en la lista 

template <typename T>
void adicionar (Lista <T> * lista, T infoNueva)


//------------------------------------------------eliminar-------------------------------------------------------------
//Recibo  la lista donde quiero eliminar información, recibo la información que quiero eliminar
//La función retorna TRUE cuando la operación fue exitosa, en caso contrario, retorna FALSE 

template <typename T>
bool eliminar (Lista <T> * lista, T infoEliminar)
