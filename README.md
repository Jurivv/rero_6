# reto_6


```python
billete: int

def panes_totales(p: int) -> int:
    return p * 300

def huevos_totales(d: int) -> int:
    return d * 350

def bolsas(c: int) -> int:
    return c * 3300

def total(p: int, d: int, c: int) -> int:
    return panes_totales(p) + huevos_totales(d) + bolsas(c)

def vuelto(billete: int, p: int, d: int, c: int) -> int:
    return billete - total(p, d, c)

def debe(billete: int, p: int, d: int, c: int) -> int:
    return total(p, d, c) - billete

if __name__ == "__main__":
    billete = int(input("Valor del billete a pagar: \n"))
    d = int(input("Número de huevos: \n"))
    p = int(input("Número de panes: \n"))
    c = int(input("Número de bolsas de leche: \n"))
    
    if billete in [2000, 5000, 10000, 20000, 50000, 100000]:
        billetes_comerciales = billete
        vuelto_final = vuelto(billete, p, d, c)
        if vuelto_final >= 0:
            print("El vuelto es:", vuelto_final)
        else:
            deber_final = debe(billete, p, d, c)
            print("La persona debe:", deber_final, "pesos adicionales.")
    elif billete != [2000, 5000, 10000, 20000, 50000, 100000]:
         print("No ingreso un billete valido")
    else:
        print("No es un billete real.")
```
```python
c: int
ti: float  # tasa de interes (en porcentaje)
t: int  # tiempo
def interes(c: int, ti: float) -> float:
    return c * (ti / 100)  # Convertimos la tasa de interés a porcentaje

def valor_final(c: int, ti: float, t: int) -> float:
    return c * (1 + interes(c, ti)) ** t

if __name__ == "__main__":
    c = int(input("Ingrese el capital del préstamo: "))
    ti = float(input("Ingrese la tasa de interés  sin el signo %): "))
    t = int(input("Ingrese el tiempo en meses: "))
    print("Este es el interés compuesto:", valor_final(c, ti, t))
```
