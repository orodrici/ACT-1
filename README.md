# ACT-1
#include <iostream>

#include <math.h>

using namespace std;
static unsigned int var;

#define alpha 1.24

extern unsigned int var;

void calcParabolico(void);
void print_results(void);
void lib_func1(void);

int main()
{
   unsigned short int des = -5; 
    
    {
    var = 100;

    var += des;

    //Calculando los parametros en la Tierra con g = 9.8 m/s*s
    calcParabolico();
    print_results();

    //Calculando los parametros en la Luna con g = 1.62 m/s*s
    calcParabolico();
    print_results();

}
    return 0;
}

void calcParabolico(void)
{
    const float g = 9.8;
    char vx0, x, y, vx, vy;
     float v0, ALPHA, t, vy0,y0;
    vx0 = v0 * cos(ALPHA);
    vy0 = v0 * sin(ALPHA);

    vx = vx0;
    vy = vy0-g*t;

    x = vx*t;
    y = y0+vy0*t-(g*pow(t,2)/2);
}

void print_results(void)
{
     char x, y, vx, vy;
    std::cout<<"Los resultados del calculo parabolico son: "<<std::endl;
    std::cout<<"Velocidad en x: "<<vx<<", ";
    std::cout<<"Velocidad en y: "<<vy<<", ";
    std::cout<<"Posicion en x: "<<x<<", ";
    std::cout<<"Posicion en y: "<<y<<std::endl;
}
void lib_func1(void)
{
    std::cout<<"Esta funcion solo cambia el valor de la variable global var"<<std::endl;
    var = 200;
}
void otros_calculos(void)
{
    float Vesf, Z0, w, B, betacero, x;
    int R, wL, G, wC, r, a, b, c;
    const float pi = (3,1416);
    double mu, epsi;
    long f;
    /* Serie simple (1/[(x^2) + (x+1)]) para x entre 1 y 199*/
    for(int x=1; x<200; x++)
      (1/((pow(x,2)) + (x+1)));
    //Agregue aqui la formula
   
    /* Volumen de la esfera */
       Vesf = ((4/3)* pi)*(pow(r,3));
      //Agregue aqui la formula

    /* Raices de la ecuacion (3*x^2) + (5*x) + 8  = 0 */
      //Agregue aqui la formula
    x = ((-5) - (pow(((pow(5,2))-(4*3*8)),(1/2))))/(2*3);
    x = ((-5) + (pow(((pow(5,2))-(4*3*8)),(1/2))))/(2*3);
    /* Impedancia tipica de una linea de transmision
     * Z0 = [(R+wL)/(G+wC)]^(1/2)
     * w = frecuencia angular = 2*pi*f, f = 10kHz */
        //Agregue aqui la formula
       Z0 = pow(((R+wL)/(G+wC)),(1/2));
       w = 2*pi*f; 
    /* Constante de fase de una fibra optica
     * B = {[((a^2)-(b^2))*c+(b^2)]^(1/2)}*betacero
     * betacero = w*(mu*epsi)^(1/2)
     * w = frecuencia angular = 2*pi*f, f = 5GHz
     * mu = 0.00000125664
     * epsi = 0.00000000000088542  */
     epsi = 88542 * (pow(10,(-17)));
     mu = 0,00000125664;
     B = ((pow((((pow(a,2))-(pow(b,2)))*c+(pow(b,2))),(1/2))))*betacero;
     betacero = w* (pow((mu*epsi),(1/2)));
     f = 5 * (pow (10,9));
     w = 2*pi*f;

     


}
