#include<cassert>
#include<cmath>

struct Punto{
    double x,y;
};

struct Circulo{
    Punto centro;
    double radio;
};

const double pi=3.14159;
double GetCircunferencia(const Circulo&);
double GetArea(const Circulo&);
double GetDistancia(const Punto&,const Punto&);
bool IsDentro(const Circulo&, const Punto&);
bool EstanSolapados(const Circulo&, const Circulo&);
bool AreNear(double x, double y, double tolerance = 0.01);

int main(){
    assert(AreNear(GetCircunferencia({{ 0,  0},0.5}), 3.14));
    assert(AreNear(GetCircunferencia({{ 1,  1},2  }), 12.57));
    assert(AreNear(GetCircunferencia({{-2,  1},4  }), 25.13));
    assert(AreNear(GetCircunferencia({{ 8, -5},1  }), 6.28));

    assert(AreNear(GetArea({{ 0,  0},0.5}), 0.79));
    assert(AreNear(GetArea({{ 1,  1},2  }), 12.57));
    assert(AreNear(GetArea({{-2,  1},4  }), 50.27));
    assert(AreNear(GetArea({{ 8, -5},1  }), 3.14));

    assert(IsDentro({{ 0, 0},2},{1,1}) == true );
    assert(IsDentro({{ 4, 4},8},{2,0}) == true );
    assert(IsDentro({{-2,-3},1},{0,0}) == false);

    Circulo c = {{0,0},2};
    assert(IsDentro(c,{0,0}) == true );
    assert(IsDentro(c,{5,3}) == false);

    assert(EstanSolapados(c, {{0, 0}, 2}) == true);
    assert(EstanSolapados(c, {{1, 1}, 2}) == true);
    assert(EstanSolapados(c, {{5, 3}, 1}) == false);
}

//Calcula la circunferencia del círculo utilizando la fórmula de 2*pi*radio del círculo en cuestión.
double GetCircunferencia(const Circulo& c){
    const double circunf = pi * c.radio * 2;
    return circunf;
}

//Calcula el área del círculo utilizando la fórmula de Pi * radio al cuadrado.
double GetArea(const Circulo& c){
    const double area = pi * c.radio * c.radio;
    return area;
}

/*Calcula la distancia entre 2 puntos que luego usaremos para otra función. 
Usando la fórmula del teorema de Pitagoras*/
double GetDistancia(const Punto& p1,const Punto& p2){
    const double dx = p2.x - p1.x;
    const double dy = p2.y - p1.y;
    const double dist = std::sqrt(dx*dx + dy*dy);
    return dist;
}


/*Calcula si el punto se encuentra dentro del círculo.
Utiliza la función anterior y pasa el punto (centro) del círculo, 
esta distancia debe ser menor que el radio del círculo*/
bool IsDentro(const Circulo& c, const Punto& p) {
    double d = GetDistancia(c.centro, p);
    return d < c.radio;
}

/*Calcula si dos círculos se solapan.
Utiliza la función GetDistancia y pasa los puntos centros de los círculos, 
esta distancia debe ser menor que la suma de los radios de los círculos.*/
bool EstanSolapados(const Circulo& c1, const Circulo& c2) {
    double distanciaCentros = GetDistancia(c1.centro, c2.centro);
    return distanciaCentros < c1.radio + c2.radio;
}

/*Se implementa esta función utilizada en clase, para poder realizar los asserts y 
ajustar la precisión que toma el double que resulta de las funciones GetArea y GetCircunferencia*/
bool AreNear(double a, double b, double delta){
	return (a-delta) <= b and b <= (a+delta);
}
