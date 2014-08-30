laboratorio-4
=============
#include <iostream>
#include <conio.h>
#include <stdio.h>
#include <math.h>
using namespace std;

void cargar(int vec[], int n){
int i;
for(i=0;i<n;i++){
cout<<"introducir elemento vec["<<i<<"]";
cin>>vec[i];
}
}
void mostrar(int vec[], int n){
int i;
for(i=0;i<n;i++){
cout<<vec[i]<<" ";
}
}
void inver(int vec[],int n){

	int i,aux;
	for(i=0;i<n/2;i++){
		aux = vec[n-i-1];
		vec[n-i-1] = vec[i];
		vec[i] = aux;
		
	}
}
void ordenardescendentemente(int vec[],int n){
int i,j,aux=0;
for(i=0;i<=n;i++){
for(j=i+1;j<=n-1;j++){
if(vec[i]<vec[j]){
aux=vec[i];
vec[i]=vec[j];
vec[j]=aux;
		}
	}
}

}
void ordenarascendentemente(int vec[],int n){
int i,j,aux=0;
for(i=0;i<=n;i++){
for(j=i+1;j<=n-1;j++){
if(vec[i]>vec[j]){
aux=vec[i];
vec[i]=vec[j];
vec[j]=aux;
		}
	}
}

}

void busquedalineal(int vec[],int n,int k){
int i,j,c=0;
for(i=0;i<n;i++){
	while(c!=k){
	c=vec[i];	
	}
}
cout<<"el elemento esta en la poscicion"<<i;
}
int main(){
	int vector[100],nroElem=0,tam,k=0,t=0;
	char opcion;
	do{
		cout<<endl<<endl<<"******MENU DE VECTORES******";
		cout<<endl<<"a).- Cargar ";
		cout<<endl<<"b).- Mostrar ";
		cout<<endl<<"c).- invertir ";
		cout<<endl<<"d).- ordenar descendentemente ";
		cout<<endl<<"e).- busqueda binaria ";
		cout<<endl<<"f).- busqueda lineal ";
		cout<<endl<<"s).- Salir ";
		cout<<endl<<"Seleccionar opcion : ";
		cin >> opcion;
		switch(opcion){
			case 'a' : cout << "TAMANO DEL VECTOR ? : ";
					 cin >> nroElem;
					 cargar(vector,nroElem);	
					 break;
			case 'b' : mostrar(vector,nroElem);
					 break;
			case 'c' : inver(vector,nroElem);
					 break;
			case 'd' : ordenardescendentemente(vector,nroElem);
					 break;
			
			case 'f' : busquedalineal(vector,nroElem,k);
				cout<<"ingrese elemento que desea encontrar";
				cin>>k;
					 break;
		
		}
	}while(opcion != 's');
	return(1);
}
