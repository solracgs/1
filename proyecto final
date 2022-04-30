#include<stdio.h>
#include<stdlib.h>

struct jugadores{
	int No_jugador;
	char nombre[50];
	char apellido[50];
	int edad;
	char categoria[50];
	char equipo[50];
	
} jugadores[20];

int main()
{
    int opcion;
    bool repetir = true;
    FILE *ref;
	char LIGA[50];
	int x=0;
    
     do{
	 
	   
		system("cls");
        
        // Texto del menú que se verá cada vez
       printf ("\n\nMenu de Opciones" );
        printf ("\nA. Registrar a jugadores 1");
        printf( "\nB. Imprimir lista de jugadores por categoria 2");
       printf( "\nC. Imprimir lista de jugadores por nombre de equipo 3");
       printf( "\nD. volver al menu 4");
        
        printf("\nIngrese una opcion: ");
        scanf("%d",&opcion);
        
        switch (opcion) {
            case 1:
        			
					if((ref = fopen("c:/unach/liga.txt","w"))==NULL)
					printf("El archivo no fue creado");
					else{
        				  while (x < 6 ){
                				printf( "\nNo_jugador: " );
								scanf( "%d", &jugadores[x].No_jugador );
		    					printf( "\nNombre: " );
		    					fflush(stdin);
								scanf( "%s", &jugadores[x].nombre);
								printf( "\nApellidos: " );
								fflush(stdin);
								scanf( "%s", &jugadores[x].apellido);
								printf( "\nEdad: " );
								fflush(stdin);
								scanf( "%d", &jugadores[x].edad );
								printf( "\nCategoria: " );
								fflush(stdin);
								scanf( "%s", &jugadores[x].categoria);
								printf( "\nEquipo: " );
								fflush(stdin);
								scanf( "%s", &jugadores[x].equipo);
								system("pause>null");
			
								fprintf(ref, "%d  %s  %s  %d  %s  %s \n",jugadores[x].No_jugador,jugadores[x].nombre,jugadores[x].apellido,jugadores[x].edad,jugadores[x].categoria,jugadores[x].equipo);
                			    system("pause>nul");
                			    x++;
               			/* Vacía el buffer de entrada */
            			    } 
						}
            				fclose(ref);
                			break;
                
            case 2:
            	if((ref=fopen("C:/UNACH/LIGA.txt", "r"))==NULL){
		 			printf("EL archivo no fue creado\n");
		
	  				 }
						ref=fopen("C:/UNACH/LIGA.txt","r");
						while(x<6){
						fgets(jugadores[x].categoria,20,ref);
						fscanf(ref,"%d",&jugadores[x].No_jugador);
						fgets(jugadores[x].nombre,20,ref);
						fgets(jugadores[x].apellido,20,ref);
						fscanf(ref,"%d",&jugadores[x].edad);
						fgets(jugadores[x].equipo,20,ref);
						x++;
						}//fin while
	   					x=0;
      
      					while(x <6){
	  
      					printf("\n%s %d %s %s %d %s \n",jugadores[x].categoria,jugadores[x].No_jugador,jugadores[x].nombre,jugadores[x].apellido,jugadores[x].edad,jugadores[x].equipo);
      					x++;
      					}
                	
						system("pause>nul"); 
			     
                          break;
         
            case 3:
                if((ref=fopen("C:/UNACH/LIGA.txt", "r"))==NULL){
		 			printf("EL archivo no fue creado\n");
		
	  				 }
						ref=fopen("C:/UNACH/LIGA.txt","r");
						while(x<6){
						fgets(jugadores[x].equipo,20,ref);
						fscanf(ref,"%d",&jugadores[x].No_jugador);
						fgets(jugadores[x].nombre,20,ref);
						fgets(jugadores[x].apellido,20,ref);
						fscanf(ref,"%d",&jugadores[x].edad);
						fgets(jugadores[x].categoria,20,ref);
						
						x++;
						}//fin while
	   					x=0;
      
      					while(x <6){
	  
      					printf("\n%s %d %s %s %d %s \n",jugadores[x].equipo,jugadores[x].No_jugador,jugadores[x].nombre,jugadores[x].apellido,jugadores[x].edad,jugadores[x].categoria);
      					x++;
      					}
                	
						system("pause>nul"); // Pausa       
						break;     
         	  		}
    } while (repetir);
      
    return 0;
}
