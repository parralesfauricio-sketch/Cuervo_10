"""
Cuervo_10
Programa de saludo bilingüe (Español / Ruso)

Nivel: Principiante / Junior
Autor: Cuervo_10
"""

import datetime


def saludo(hora=None):
    if hora is None:
        hora = datetime.datetime.now().hour

    if 5 <= hora < 12:
        return "¡Buenos días!", "Доброе утро!"
    elif 12 <= hora < 18:
        return "¡Buenas tardes!", "Добрый день!"
    elif 18 <= hora < 22:
        return "¡Buenas noches!", "Добрый вечер!"
    else:
        return "¡Hola!", "Привет!"


def main():
    nombre = input("¿Cómo te llamas? / Как тебя зовут? ").strip() or "Crack"
    es, ru = saludo()
    ahora = datetime.datetime.now()

    print("\n" + "─" * 45)
    print(f"  {es} {nombre}")
    print(f"  {ru} {nombre}")
    print(f"  {ahora:%d/%m/%Y  %H:%M}")
    print("─" * 45)


if __name__ == "__main__":
    main()
