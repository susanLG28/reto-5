# reto-5
### punto 1
Dado la figura de la imagen, desarrolle:


![image](https://github.com/user-attachments/assets/0b277c03-20a7-472a-87c7-3eefd986b360)


* Una función matemática para calcular el volumen y el área superficial.
* Cree dos funciones en python para calcular los valores antes establecidos, al ingresar por teclado r1, r2 y h.
* Revise como utilizar el valor de pi usando import math y math.pi

_solucion_


    import math

    def calcular_rectangulo(base, altura):
        area = base * altura
        perimetro = 2*base + 2*altura
        return area, perimetro

    def calcular_circulos(radio):
        area = math.pi * radio**2
        perimetro = (2*radio)*math.pi
        return area, perimetro

    base= float(input("introduce la base del rectangulo "))
    altura = float(input("intoduce la altura del rectangulo "))
    arearectangulo, perimetrorectangulo = calcular_rectangulo(base, altura)
    print(f"rectangulo - area: {arearectangulo:.2f}, perimetro: {perimetrorectangulo:.2f}")

    radio = float(input("introduce radio de los curculos 6"))
    areacirculos, perimetrocirculos = calcular_circulos(radio)
    print(f"circulos - area: {areacirculos:.2f}, perimetro: {perimetrocirculos:.2f}")

    sumaareas = arearectangulo + (areacirculos*2)
    sumaperimetros = perimetrorectangulo +(perimetrocirculos*2)
    print(f"la suma de las areas: {sumaareas:.2f}")
    print(f"la suma de los perimetros: {sumaperimetros:.2f}")

    
### punto 2
Dado la figura de la imagen, desarrolle:


![image](https://github.com/user-attachments/assets/56d4dc00-8817-4392-aaf2-29eb43dd9f6c)


* Una función matemática para calcular el área y el perimetro.
* Cree dos funciones en python para calcular los valores antes establecidos, al ingresar por teclado r, a y b.
* Revise como utilizar el valor de pi usando import math y math.pi

_solucion_


    import math

    def calcular_rectangulo(base, altura):
        area = base * altura
        perimetro = 2*base + 2*altura
        return area, perimetro

    def calcular_circulos(radio):
        area = math.pi * radio**2
        perimetro = (2*radio)*math.pi
        return area, perimetro

    base= float(input("introduce la base del rectangulo "))
    altura = float(input("intoduce la altura del rectangulo "))
    arearectangulo, perimetrorectangulo = calcular_rectangulo(base, altura)
    print(f"rectangulo - area: {arearectangulo:.2f}, perimetro: {perimetrorectangulo:.2f}")

    radio = float(input("introduce radio de los curculos "))
    areacirculos, perimetrocirculos = calcular_circulos(radio)
    print(f"circulos - area: {areacirculos:.2f}, perimetro: {perimetrocirculos:.2f}")

    sumaareas = arearectangulo + (areacirculos*2)
    sumaperimetros = perimetrorectangulo +(perimetrocirculos*2)
    print(f"la suma de las areas: {sumaareas:.2f}")
    print(f"la suma de los perimetros: {sumaperimetros:.2f}")

    
### punto 3
Diseñe una función que calcule la cantidad de carne de aves en kilos si se tienen N gallinas, M gallos y K pollitos cada uno pesando 6 kilos, 7 kilos y 1 kilo respectivamente.

_solucion_

    def CalcularCarneAves(n, m, p):

        peso_gallinas = n * 6
        peso_gallos = m * 7
        peso_pollitos = p * 1
        total_carne = peso_gallinas + peso_gallos + peso_pollitos
        return total_carne

    n = int(input("Ingrese la cantidad de gallinas: "))
    m = int(input("Ingrese la cantidad de gallos: "))
    p = int(input("Ingrese la cantidad de pollitos: "))


    total = CalcularCarneAves(n, m, p)
    print(f"La cantidad total de carne es: {total} kg")


### punto 4 
Haga un programa que utilice una función para calcular el valor de un préstamo C usando interés compuesto del i por n meses.

_solucion_

    def calcular_prestamo(X, i, n):
        pago_final = X * (1 + i) ** n
        return pago_final

    X = float(input("Ingrese el valor del préstamo: "))
    i = float(input("Ingrese la tasa de interés mensual en decimales: "))
    n = int(input("Ingrese el número de meses: "))

    monto = calcular_prestamo(X, i, n)
    print(f"El valor final del préstamo después de {n} meses es: {monto:.2f} pesos")

### punto 5
Escriba un programa que pida 5 números reales y calcule las siguientes operaciones usando una función para cada una:

* El promedio
* El promedio multiplicativo (multilplica todos y luego calcula la raíz de la cantidad de operandos)
* La potencia del mayor número elevado al menor número
* La raíz cúbica del menor número
  
_solucion_


    import math

    def calcular_promedio(numeros):
        return sum(numeros) / len(numeros)

    def calcular_promedio_multiplicativo(numeros):
        producto = 1
        for num in numeros:
            producto *= num
        return producto ** (1 / len(numeros))

    def potencia_mayor_al_menor(numeros):
        mayor = max(numeros)
        menor = min(numeros)
        return mayor ** menor

    def raiz_cubica_menor(numeros):
        menor = min(numeros)
        return menor ** (1/3) if menor >= 0 else -(-menor) ** (1/3)  

    numeros = []
    print("Ingrese 5 números reales:")
    for i in range(5):
        num = float(input(f"Número {i + 1}: "))
        numeros.append(num)

    promedio = calcular_promedio(numeros)
    promedio_mult = calcular_promedio_multiplicativo(numeros)
    potencia = potencia_mayor_al_menor(numeros)
    raiz_cubica = raiz_cubica_menor(numeros)

    print(f"\nPromedio: {promedio:.3f}")
    print(f"Promedio multiplicativo: {promedio_mult:.3f}")
    print(f"Potencia del mayor elevado al menor: {potencia:.3f}")
    print(f"Raíz cúbica del menor número: {raiz_cubica:.3f}")



### punto 6
qué es y cómo funciona pip en python.

#### ¿Qué es pip?
Pip es un acrónimo recursivo que significa "Pip Instalador de Paquetes" o "Pip Instalador de Python" ,es la herramienta estándar para gestionar paquetes en Python desde la versión 2.7.9 y 3.4 en adelante, ya que viene preinstalado en estas versiones, facilita la instalación y gestión de paquetes y sus dependencias, asegurando que todos los componentes necesarios para que un paquete funcione se instalen correctamente.

#### ¿Cómo funciona pip?
Se usa desde la línea de comandos con comandos simples como:

_pip install nombre-paquete_ para instalar un paquete.

_pip uninstall nombre-paquete_ para desinstalar un paquete.

_pip list_ para listar los paquetes instalados.

_pip install --upgrade nombre-paquete_ para actualizar un paquete a su última versión.
 
 Entre algunas otras cosas mas 


### punto 7 
Hacer un listado de módulos populares para python que se puedan instalar com pip y consultar cómo instalarlos.

| Módulo           | Descripción                              | Instalación             |
|------------------|------------------------------------------|-------------------------|
| **numpy**        | Operaciones matemáticas y matrices       | `pip install numpy`      | 
| **pandas**       | Análisis y manejo de datos                | `pip install pandas`     | 
| **matplotlib**   | Crear gráficos y visualizaciones          | `pip install matplotlib` | 
| **seaborn**      | Gráficos estadísticos avanzados           | `pip install seaborn`    | 
| **scipy**        | Cálculo científico y estadísticas         | `pip install scipy`      | 
| **scikit-learn** | Algoritmos de machine learning            | `pip install scikit-learn` | 
| **flask**        | Crear aplicaciones web pequeñas            | `pip install flask`      | 
| **django**       | Framework web completo y robusto            | `pip install django`     | 
| **fastapi**      | Crear APIs modernas y rápidas               | `pip install fastapi`    | 
| **pytest**       | Pruebas automáticas                         | `pip install pytest`     | 
| **selenium**     | Automatizar navegadores                      | `pip install selenium`   | 
