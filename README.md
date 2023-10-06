
# RETO_Nº_6_CADA_VEZ_MAS_COMPLICAO

### FUNCIONES 1

1. Dado la figura de la imagen, desarrolle:

<a href='https://postimg.cc/qhsS8LrS' target='_blank'><img src='https://i.postimg.cc/qhsS8LrS/png.png' border='0' alt='png'/></a>

* Una función matemática para calcular el volumen y el área superficial.
* Cree dos funciones en python para calcular los valores antes establecidos, al ingresar por teclado r1, r2 y h.
* Revise como utilizar el valor de pi usando import math y math.pi
Dado la figura de la imagen, desarrolle:

```pseudocode
import math
def calcular_volumen(radio_cono:float, altura_cono:float, radio_esfera:float) -> float:
    volumen_cono = (1/3) * math.pi * radio_cono ** 2 * altura_cono
    volumen_esfera = (4/3) * math.pi * radio_esfera ** 3
    return volumen_cono + volumen_esfera
def calcular_area_superficial(radio_cono:float, altura_cono:float, radio_esfera:float) -> float:
    generatriz = math.sqrt(radio_cono ** 2 + altura_cono ** 2)
    area_superficial_cono = math.pi * radio_cono ** 2 + math.pi * radio_cono * generatriz
    area_superficial_esfera = math.pi * 4 * radio_esfera ** 2
    return area_superficial_cono + area_superficial_esfera

if __name__ == "__main__":

 radio_esfera = float(input("Ingresa el radio de la esfera: "))
 radio_cono = float(input("Ingresa el radio de la base del cono: "))
altura_cono = float(input("Ingresa la altura del cono: "))

volumen = calcular_volumen(radio_cono, altura_cono, radio_esfera)
area_superficial = calcular_area_superficial(radio_cono, altura_cono, radio_esfera) 

print("El volumen de la figura es " + str(volumen)+ "y el area superficial de la figura es " + str(area_superficial))
```
[![punto1.png](https://i.postimg.cc/Znkw0kN0/punto1.png)](https://postimg.cc/YG36ysbw)

* para este punto, definí el volumen y el área superficial de cada uno por aparte importe la función math y calcule el perímetro con math.pi.
* para calcular el área superficial del cono, primero halle la generatriz a partir del teorema de Pitágoras y luego y luego lo retorne para hallar el área superficial llamando la generatriz. 
* desde luego inserte la función main, luego el usuario inserta las longitudes del área de la esfera y el cono.
* por ultimo sume el volumen de cono con el volumen de la esfera ya definidos y sume el área superficial del cono y de la esfera ya definidos y imprimí el resultado.
* desde luego. calcule el resultado en calculadora y me da la misma respuesta.  

2. dado la figura de la imagen desarrolle:

<a href='https://postimg.cc/nsz4cnVC' target='_blank'><img src='https://i.postimg.cc/nsz4cnVC/png.png' border='0' alt='png'/></a>

* Una función matemática para calcular el área y el perimetro.
* Cree dos funciones en python para calcular los valores antes establecidos, al ingresar por teclado r, a y b.
* Revise como utilizar el valor de pi usando import math y math.pi

```pseudocode
import math
def calcular_area(a:float, b:float, r:float) -> float:
    area_rectangulo = a * b
    area_circulos = (math.pi * r ** 2) * 2
    return area_rectangulo + area_circulos
def calcular_perimetro(a:float, b:float, r:float) -> float:
    perimetro_rectangulo = 2*b + 2*a
    perimetro_circulos = (math.pi * 2 * r) * 2
    return perimetro_rectangulo + perimetro_circulos

if __name__ == "__main__":
       
 r = float(input("Ingresa el radio de los circulos: "))
 a = float(input("Ingresa la altura del rectangulo: "))
 b = float(input("Ingresa la base del rectangulo: "))

area = calcular_area(a, b, r)
perimetro = calcular_perimetro(a, b, r)

print("El area de la figura es " + str(area)+ "y el perimetro de la figura es " + str(perimetro))
```
[![punto2.png](https://i.postimg.cc/MpYN4GQ5/punto2.png)](https://postimg.cc/zyVxH8pH)

3. Diseñe una función que calcule la cantidad de carne de aves en kilos si se tienen N gallinas, M gallos y K pollitos cada uno pesando 6 kilos, 7 kilos y 1 kilo respectivamente.

```pseudocode
def calcular_cantidad_carne(N, M, K):
    peso_gallina = 6  
    peso_gallo = 7    
    peso_pollito = 1  
    carne_gallinas = N * peso_gallina
    carne_gallos = M * peso_gallo
    carne_pollitos = K * peso_pollito
    return carne_gallinas + carne_gallos + carne_pollitos

# Ejemplo de uso de la función
N = int(input("Ingresa el número de gallinas: "))
M = int(input("Ingresa el número de gallos: "))
K = int(input("Ingresa el número de pollitos: "))

total_carne = calcular_cantidad_carne(N, M, K)
print("La cantidad total de carne de aves en kilos es " + str(total_carne)+ "kilos")
```
[![punto3.png](https://i.postimg.cc/Vkd0ZK5k/punto3.png)](https://postimg.cc/75rLfMgF)

4. Mi mamá me manda a comprar P panes a 300 cada uno, M bolsas de leche a 3300 cada una y H huevos a 350 cada uno. Hacer un programa que me diga las vueltas (o lo que quedo debiendo) cuando me da un billete de B pesos.

```pseudocode
def cantidad_costo_total(p:int, l:int, h:int):
  precio_pan = 300
  precio_leche = 3300
  precio_huevos = 350
  costo = (p * precio_pan) + (l * precio_leche) + (h * precio_huevos)
  return costo

if __name__ == "__main__":
    
 p = int(input("Ingresa la cantidad de panes: "))
 l = int(input("Ingresa la cantidad de bolsas de leche: "))
 h = int(input("Ingresa la cantidad de huevos: "))
 B = int(input("Ingresa el valor del billete en pesos: "))
costo_total = cantidad_costo_total(p, l, h)
if B >= costo_total:
    vueltas = B - costo_total
    print("Las vueltas son " + str(vueltas)+ " pesos")
else:
    debe = costo_total - B
    print("Debes " + str(debe)+ " pesos")
```
[![punto4.png](https://i.postimg.cc/bNTkGGS1/punto4.png)](https://postimg.cc/qzNzSvL7)

5. Haga un programa que utilice una función para calcular el valor de un préstamo C usando interés compuesto del i por n meses.

```pseudocode
def calcular_valor_prestamo(c:float, i:float, n:float) -> float:
  tasa_interes_mensual = i / 12 / 100
  valor_prestamo = c * (1 + tasa_interes_mensual) ** n
  return valor_prestamo

if __name__ == "__main__":

  c = float(input("Ingrese el monto del préstamo: "))
  i = float(input("Ingrese la tasa de interés anual (%): "))
  n = int(input("Ingrese el número de meses: "))

valor_final = calcular_valor_prestamo(c, i, n)
print("El valor del préstamo después de " + str(n)+ " meses es " + str(valor_final))
```

[![punto5.png](https://i.postimg.cc/6QYYXjt4/punto5.png)](https://postimg.cc/yJ3FhTJ7)

6. El número de contagiados de Covid-19 en el país de NuncaLandia se duplica cada día. Hacer un programa que diga el número total de personas que se han contagiado cuando pasen D días a partir de hoy, si el número de contagiados actuales es C.

```pseudocode
def numero_total_contagiados(c:int, d:int):
  n = c * (2 ** d)
  return n

if __name__ == "__main__":

  c = int(input("Ingrese el número actual de contagiados: "))
  d = int(input("Ingrese el número de días a partir de hoy: "))

n_total = numero_total_contagiados(c, d)
print("El numero total de contagiados después de " + str(d)+ " dias sera " + str(n_total))
```
[![punto6.png](https://i.postimg.cc/tgvWD7h8/punto6.png)](https://postimg.cc/t1Ps4qvz)

7. Escriba un programa que pida 5 números reales y calcule las siguientes operaciones usando una función para cada una:

* El promedio
* La mediana
* El promedio multiplicativo (multilplica todos y luego calcula la raíz de la cantidad de operandos)
* Ordenar los números de forma ascendente
* Ordenar los números de forma descendente
* La potencia del mayor número elevado al menor número
* La raíz cúbica del menor número

```pseudocode
def calcular_promedio(n1:float, n2:float, n3:float, n4:float, n5:float) -> float:
    promedio = n1 + n2 + n3 + n4 + n5/ 5
    return promedio
def calcular_mediana(n1:float, n2:float, n3:float, n4:float, n5:float) -> float:
    numeros = [n1, n2, n3, n4, n5]
    numeros_ordenados = sorted(numeros)
    mediana = numeros_ordenados[len(numeros) // 2]
    return mediana
def calcular_promedio_multiplicativo(n1:float, n2:float, n3:float, n4:float, n5:float) -> float:
    producto = n1 * n2 * n3 * n4 * n5
    promedio_multiplicativo = producto ** 1/5 
    return promedio_multiplicativo
def numeros_ascendente(n1:float, n2:float, n3:float, n4:float, n5:float) -> float:
    numeros = [n1, n2, n3, n4, n5]
    ascendente = sorted(numeros)
    return ascendente
def numeros_descendente(n1:float, n2:float, n3:float, n4:float, n5:float) -> float:
    numeros = [n1, n2, n3, n4, n5]
    descendente = sorted(numeros, reverse=True)
    return descendente
def potencia_mayor_numero_elevado_al_menor(n1:float, n2:float, n3:float, n4:float, n5:float) -> float:
    numeros = [n1, n2, n3, n4, n5]
    mayor = max(numeros)
    menor = min(numeros)
    potencia = mayor ** menor
    return potencia
def raiz_cubica_menor_numero(n1:float, n2:float, n3:float, n4:float, n5:float) -> float:
    numeros = [n1, n2, n3, n4, n5]
    mayor = max(numeros)
    menor = min(numeros)
    raiz_cubica = menor ** 1/3
    return raiz_cubica 

if __name__ == "__main__":
    
  n1 = float(input("ingrese el primer numero: "))
  n2 = float(input("ingrese el segundo numero: "))
  n3 = float(input("ingrese el tercer numero: "))
  n4 = float(input("ingrese el cuarto numero: "))
  n5 = float(input("ingrese el quinto numero: "))

promedio = calcular_promedio(n1, n2, n3, n4, n5)
mediana = calcular_mediana(n1, n2, n3, n4, n5)
promedio_multiplicativo = calcular_promedio_multiplicativo(n1, n2, n3, n4, n5)
ascendente = numeros_ascendente(n1, n2, n3, n4, n5)
descendente = numeros_descendente(n1, n2, n3, n4, n5)
potencia =  potencia_mayor_numero_elevado_al_menor(n1, n2, n3, n4, n5)
raiz_cubica = raiz_cubica_menor_numero(n1, n2, n3, n4, n5)


print("El promedio es " + str(promedio))
print("La mediana es " + str(mediana))
print("El Promedio multiplicativo es " + str(promedio_multiplicativo))
print("Los números ordenados de forma ascendente son " + str(ascendente))
print("Los números ordenados de forma descendente son " + str(descendente))
print("Potencia del mayor número elevado al menor número es " + str(potencia))
print("Raíz cúbica del menor número es " + str(raiz_cubica))
```
[![punto7.png](https://i.postimg.cc/PrR1HCLy/punto7.png)](https://postimg.cc/1fD8c5rV)

8. Para el punto anterior incluir las funciones en un archivo independiente e importarlas para su uso.
* hice la primera librería con las funciones 
```pseudocode
def calcular_promedio(n1:float, n2:float, n3:float, n4:float, n5:float) -> float:
    promedio = n1 + n2 + n3 + n4 + n5/ 5
    return promedio
def calcular_mediana(n1:float, n2:float, n3:float, n4:float, n5:float) -> float:
    numeros = [n1, n2, n3, n4, n5]
    numeros_ordenados = sorted(numeros)
    mediana = numeros_ordenados[len(numeros) // 2]
    return mediana
def calcular_promedio_multiplicativo(n1:float, n2:float, n3:float, n4:float, n5:float) -> float:
    producto = n1 * n2 * n3 * n4 * n5
    promedio_multiplicativo = producto ** 1/5 
    return promedio_multiplicativo
def numeros_ascendente(n1:float, n2:float, n3:float, n4:float, n5:float) -> float:
    numeros = [n1, n2, n3, n4, n5]
    ascendente = sorted(numeros)
    return ascendente
def numeros_descendente(n1:float, n2:float, n3:float, n4:float, n5:float) -> float:
    numeros = [n1, n2, n3, n4, n5]
    descendente = sorted(numeros, reverse=True)
    return descendente
def potencia_mayor_numero_elevado_al_menor(n1:float, n2:float, n3:float, n4:float, n5:float) -> float:
    numeros = [n1, n2, n3, n4, n5]
    mayor = max(numeros)
    menor = min(numeros)
    potencia = mayor ** menor
    return potencia
def raiz_cubica_menor_numero(n1:float, n2:float, n3:float, n4:float, n5:float) -> float:
    numeros = [n1, n2, n3, n4, n5]
    mayor = max(numeros)
    menor = min(numeros)
    raiz_cubica = menor ** 1/3
    return raiz_cubica 
```
[![punto8-1.png](https://i.postimg.cc/zGRjyCK3/punto8-1.png)](https://postimg.cc/JsMJgBTW)

* importe las funciones de la librería ya creada
```pseudocode
from punto7 import calcular_promedio
from punto7 import calcular_mediana
from punto7 import calcular_promedio_multiplicativo
from punto7 import numeros_ascendente
from punto7 import numeros_descendente
from punto7 import potencia_mayor_numero_elevado_al_menor
from punto7 import raiz_cubica_menor_numero

if __name__ == "__main__":
    
  n1 = float(input("ingrese el primer numero: "))
  n2 = float(input("ingrese el segundo numero: "))
  n3 = float(input("ingrese el tercer numero: "))
  n4 = float(input("ingrese el cuarto numero: "))
  n5 = float(input("ingrese el quinto numero: "))

promedio = calcular_promedio(n1, n2, n3, n4, n5)
mediana = calcular_mediana(n1, n2, n3, n4, n5)
promedio_multiplicativo = calcular_promedio_multiplicativo(n1, n2, n3, n4, n5)
ascendente = numeros_ascendente(n1, n2, n3, n4, n5)
descendente = numeros_descendente(n1, n2, n3, n4, n5)
potencia =  potencia_mayor_numero_elevado_al_menor(n1, n2, n3, n4, n5)
raiz_cubica = raiz_cubica_menor_numero(n1, n2, n3, n4, n5)


print("El promedio es " + str(promedio))
print("La mediana es " + str(mediana))
print("El Promedio multiplicativo es " + str(promedio_multiplicativo))
print("Los números ordenados de forma ascendente son " + str(ascendente))
print("Los números ordenados de forma descendente son " + str(descendente))
print("Potencia del mayor número elevado al menor número es " + str(potencia))
print("Raíz cúbica del menor número es " + str(raiz_cubica))
```
[![punto8-2.png](https://i.postimg.cc/QM3pVRjn/punto8-2.png)](https://postimg.cc/dh57xNk8)

9. Consultar qué es y cómo funciona pip en python.
* Pip es un administrador de paquetes para Python. Es una herramienta que se utiliza para instalar, desinstalar y actualizar paquetes de software escritos en Python. Pip es un proyecto de código abierto y está disponible para todos los sistemas operativos principales. pip hace que se fácil gestionar las bibliotecas y dependencias de proyectos en python, lo que hace que sea fundamental para desarrollar aplicaciones mas complejas que requieren funcionalidades especificas de terceros.  
* Pip funciona utilizando un repositorio de paquetes llamado Python Package Index (PyPI). PyPI es un sitio web que alberga paquetes de software Python. Para instalar un paquete de PyPI, pip utiliza el comando pip install. El comando pip install toma el nombre del paquete como argumento y lo instala en el sistema. 

10. Hacer un listado de módulos populares para python que se puedan instalar com pip y consultar cómo instalarlos.

* NumPy: Un módulo para computación numérica.
* SciPy: Un módulo para computación científica.
* Matplotlib: Un módulo para visualización de datos.
* Pandas: Un módulo para análisis de datos.
* Scikit-learn: Un módulo para aprendizaje automático.
* Django: Un framework web.
* Flask: Un microframework web.
* PyTorch: Un framework para aprendizaje profundo.
* TensorFlow: Un framework para aprendizaje automático.

para instalar pip se utiliza el siguiente comando:
```pseudocode
pip install [nombre_del_módulo]
```

Referencia 
* Pip en la documentación oficial de Python: https://docs.python.org/3/installing/
