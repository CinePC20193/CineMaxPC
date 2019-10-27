/*              CineMax

Proyecto final Programación de Computadores
Integrantes:
            Estefania Bermudez Arroyo
            Jessica Tatiana Naizaque Guevara
            Angie Tatiana Peña Peña
Descripción: Código para la administración de un cine con salas multiplex,
que permite la venta de boletas para distintas funciones. */

#include <math.h>
#include <conio.h>
#include <iomanip>
#include <fstream>         
#include <iostream>
#include <string.h>
#include <stdlib.h>
#include <windows.h>
#include "listas.cpp"

using namespace std;
/* Declaración de las estructuras */

struct sSilla
{
    char * numSilla; /*A20, J8, .... */
    char * cat;/*Si la silla es general o preferencial*/
    bool dispo;/*Si la silla ya esta ocupada (TRUE O FALSE)*/
};

struct sProyecciones
{ 
    char * nomPelicula;/*nombre de la película*/
    Lista <sSilla> * sillas; /*Sillas que se tendrán en esa proyección*/
    bool dispoProyeccion; /*Si el campo de la proyección está ocupado*/
};

struct sSala
{
    int numSala;/*Sala 1, Sala 2, Sala 3, ....*/
    int numSillas;/* Numero de Silla que tiene la sala*/
    Lista<sSilla> * sillas;/*Matriz de la sillas predterminadas (siempre están)*/
    sProyecciones ** proyecciones; /*Nombre de las películas que se van a propyectar en sala y las sillas en cada función*/
};

struct sFuncion
{
    char * NomPelicula;/*Malefica, La Vida Secreta de Tres Hackers, etc*/
    char * durCarte;/*Cuanto durará en cartelera*/
    char * durPeli;/*2h30min, 1:30, etc*/
    sSala ** numSalas; /*Vector de apuntadores a salas, son las salas donde se proyectará la película*/
};

//----------------------------------------------configuracionInicial------------------------------------------------------
// Es la configuración inicial de todo el sistema, es decir, la configuración de las salas, de las sillas y de las funciones 
// Esta configuración inical se debe hacer desde un archivo 
//En el archivo de "ConfiguraciónInicial.txt" voy a dividir sel archivo por secciones (1. Función, 2.Sala, 3.Silla)

void configuracionInicial (Lista <sFuncion> * listaCine) 

                                            
//-------------------------------------------------configuracion-----------------------------------------------------
//Recibo la lista de la sección que deseo modificar, es decir, si deseo modificar las salas, las silla o las funciones
//Recibo la lista general donde se guarda toda la información del cine, esto para poder volver llenar el archivo "Configuración.txt"
//Estas configurciones se tienen que guardar en un mismo archivo, es decir, "Configuracion.txt"
//Realizamos el cambio, si "Configuración.txt" en la sección que me mandaron es igual a la lista a la cual le realicé la modificación, retorno TRUE
//Estas configurciones se tienen que guardar en un mismo archovo, es decir, "Configuracion.txt"
//La función retorna TRUE en caso de que la modificación se exitosa, en caso contrario, retorna FALSE

template <typename T>
bool configuracion (Lista <T> * listaModif, Lista <T> * listaGrande)


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

void genTiquete (char* nomPelicula, int proyeccion, Lista <sSala> * listaSala)


//----------------------------------------------------color--------------------------------------------------------
//Recibe un número que está establecido en el compilador para generar un fondo con un color y un texto con otro color (predeterminados en una tabla con 256 combinaciones)

int color (int num)

//----------------------------------------------------consultaCartelera---------------------------------------------
//La función permite leer un archivo HTML que contendrá la configuración de una página web, que permitirá visualizar las funciones que se proyectaran en la semana 

void consultarCartelera()


//-----------------------------------------------------consultaSala--------------------------------------------------
//La función recibe el nombre de una película
//Dado este nombre, el sistema muestra en pantalla las salas y las horas en que se presenta

void consultaSala (char * nomPelicula)


//-----------------------------------------------------consultaSilla-------------------------------------------------
//La función recibe la hora, el numero de la sala y la lista de las salas
//Teniendo los datos de la hora y de la sala, el sistema muestra en pantalla las lista de sillas disponibles 
//Lo que se muestra en pantalla va a ser una matriz donde se mostrará el color verde en las secciones donde hay sillas disponibles y rojo en el caso contrario

void consultaSilla (int numSala, char * hora, Lista <sSala> * salas)


//-----------------------------------------------------consultaPersonas--------------------------------------------
//La función recibe la fecha de inicio y la fecha final (dd/mm/aa) y la lista general del cine 
//La función va a retornar un entero, que sería el número de personas en ese rango de tiempo dado
//En la función se va a usar un archivo que esta en el computador que contiene la fecha, la cantidad de personas que fueron en esa fecha y la cantidad de ganancias en esa fecha

double consultaPersonas (char * fecInicio, char * fecFinal, Lista <sFuncion> * listaCine)
	

//---------------------------------------------------- consultaGanancia-------------------------------------------
// La función recibe una fecha de inicio y una fecha final y la lista general de cine 
//En la función se va a usar un archivo que esta en el computador que contiene la fecha, la cantidad de personas que fueron en esa fecha y la cantidad de ganancias en esa fecha

double consultaGanancia (char * fecInicial, char * fecFinal, Lista <sFuncion> * listaCine)
	

//----------------------------------------------------imprimirHorario--------------------------------------------
//La función recibe la matriz de proyecciones y el numero de la sala 
//La función muesta el horario de proyecciones que va a tener la sala durante una semana (domingo a domigo)

void imprimirHorario (sProyecciones ** proyecciones, int sala) 

//----------------------------------------------------imprimirSillas----------------------------------------------
//La función recibe la lista de las sillas que se quiere imprimir y la sala de la lista de sillas 
//La función muestra la matriz de sillas, cada silla tendrá un respectivo color, si está color verde significa que la silla está disponible, si está en rojo la silla no está disponible 

void imprimirSillas (Lista <sSillas> * sillas, int sala)
	


//CÓDIGO
int color (int num)
{
    SetConsoleTextAttribute (GetStdHandle(STD_OUTPUT_HANDLE), num);
}

void imprimirHorario (char **horario, int sala)
{
     color(6);
	 cout << "\tProyecciones para la sala " << sala << endl;
	 cout << endl << endl;
	 color(8);
	 cout << "  L  M  W  J  V  S  D\n";
	 cout << "  "
	      << "1"
	      << " ";
	 cout << " "
	      << "2"
	      << " ";
	 cout << " "
	      << "3"
	      << " ";
	 cout << " "
	      << "4"
	      << " ";
	 cout << " "
	      << "5" << endl;
	 for (int z = 0; z < 5; z++) 
	 {
		 for (int r = 0; r < 7; r++) 
		 {
		     if ((*(*(horario+i)+j))== '-')
			 {
			     color (170);
			     cout << (*(*(horario+i)+j);
				 color (7);
			 }
			 else if ((*(*(horario+i)+j))== 'X')
			 {
			     color (204);
			     cout << (*(*(horario+i)+j);
				 color (7);
			 }
		 }
		 cout << endl;
	 }
	color(7); //Color del texto final
}

sFuncion crear_pelicula (int cantSalas, sLista <sSala> *salas) 
{
     sFuncion nueva;
     nueva.nombrePelicula = new char [50];
 	 nueva.duracionCartelera = new char [2]; //Cantidad en días
	 nueva.duracionPelicula = new char [8]; //Formato HH:MM:SS
	 nueva.numSalas = new int [cantSalas];
	 int num, x, proy, dia;
	 char rta;

     cout << "Ingrese el nombre de la pel" << char (161) << "cula nueva\n";
	 cin >> nueva.nombrePelicula;
	 cout << "Ingrese la duraci" << char(162) << "n (en d" << char (161) << "as) de la pel" << char (161) << "cula en cartelera\n";
	 cin >> nueva.duracionCartelera;
 	 cout << "Ingrese la duraci" << char(162) << "n (formato HH:MM:SS) de la pel" << char (161) << "cula\n";
	 cin >> nueva.duracionPelicula;
     cout << "Ingrese la cantidad de salas a utilizar para presentar la pel" << char (161) << "cula "  << nueva.nombrePelicula << endl;
	 cin >> num;
	 if (num < cantSalas)
	 {
	     cout << "A continuaci" << char(162) << "n, ingrese los n" << char (163) << "meros de las salas y horarios donde se proyectar" << char (160) << " la pel" << char (161) << "cula " << nueva.nombrePelicula;
	     for (int i=0; i<num; i++)
	     {
	         cout << "Sala ";
	         cout << char(175) << " ";
		     cin >> x;
		     if ((x < cantSalas) && (x > 0))
		     {
		         cout << "Las proyecciones disponibles para la sala " << x << " aparecen a continuaci" << char(162) << "n resaltadas en color verde: ";
				 sNodo <sSala> *aux = salas->cab;
				 while (aux != NULL)
				 {
				     if (((aux->info).numSala) == x)
					 {
			             imprimirHorario (((aux->info).proyecciones), x);
					 }
					 aux = aux->sig;
				 }
			     cout << "Ingrese 's' si desea que la pel" << char (161) << "cula " << nueva.nombrePelicula <<  " se proyecte en la sala " << x << endl;
			     cin >> rta;
			     if ((rta=='s')||(rta=='S'))
			     {
		             *(nueva.numSalas+i) = x;
				     cout << "¿En qu" << char (130) << " proyecci" << char(162) << "n desea presentar la pel" << char (161) << "cula " << nueva.nombrePelicula << "?\n";
				     cout << "   Elija un n" << char (163) << "mero:\n";
				     cout << "   1. 09:00 a.m. - 11:00 a.m.\n";
				     cout << "   2. 12:00 p.m. - 02:00 p.m.\n";
				     cout << "   3. 03:00 p.m. - 05:00 p.m.\n";
				     cout << "   4. 06:00 p.m. - 08:00 p.m.\n";
				     cout << "   5. 08:00 p.m. - 10:00 p.m.\n";
				     cin >> proy;
				     cout << "¿Qu" << char (130) << " d" << char (161) << "a de la semana desea presentar la pel" << char (161) << "cula " << nueva.nombrePelicula << "?\n";
					 cout << "   Elija un n" << char (163) << "mero:\n";
					 cout << "   1 = Lunes\n";
					 cout << "   2 = Martes\n";
					 cout << "   3 = Mi" << char (130) << "rcoles\n";
					 cout << "   4 = Jueves\n";
					 cout << "   5 = Viernes\n";
					 cout << "   6 = S" << char (160) << "bado\n";
					 cout << "   7 = Domingo\n";
					 cin >> dia;
					 //------------------------------------------------------Guardar en *(*(proyecciones+proy)+dia) una X para quitar disponibilidad
					 //------------------------------------------------------Evaluar posibilidad de proyección inválida
			     }
			     else
			     {
			         cout << "La pel" << char (161) << "cula no se proyectar" << char (160) << " en la sala " << x << endl;
				     i--;
			     }
		     }
		     else
		     {
		         cout << "N" << char (163) << "mero de sala inv" << char (160) << "lido\n";
			     i--;
		     }
	     }
	 }
	 else
   	 {
	     color (12);
	     cout << "N" << char (163) << "mero para la cantidad de salas inv" << char (160) << "lido\n";
	     cout << "Recuerde que debe ser un n" << char (163) << "mero menor o igual a " << cantSalas << endl;
	     color (7);
	 }
	//LIBERAR MEMORIA
}
