"""
VIDEOTECA DIGITAL
Autor: (Sheila Rodriguez)
Descripción:
Este programa cuenta cuántas películas cumplen dos condiciones:
- Tener una calificación mayor o igual a un valor ingresado por el usuario
- Tener un año de lanzamiento mayor o igual al año límite (2023-2026)
"""

# =========================
# MATRIZ DE PELÍCULAS
# [Título, Año, Calificación, Género]
# =========================

videoteca = [
    ["Oppenheimer", 2023, 8.8, "Drama"],
    ["Barbie", 2023, 7.5, "Comedia"],
    ["Wonka", 2023, 7.2, "Fantasía"],
    ["Intensamente 2", 2024, 7.9, "Animación"],
    ["Deadpool & Wolverine", 2024, 8.2, "Acción"],
    ["Minecraft", 2025, 7.8, "Aventura"],
    ["Duna: Parte Dos", 2024, 8.6, "Ciencia ficción"]
]

# =========================
# FUNCIÓN PRINCIPAL
# =========================

def contar_titulos(matriz, calificacion_minima, año_limite):

    contador = 0

    for pelicula in matriz:
        calificacion = pelicula[2]
        año = pelicula[1]

        # Condición: calificación ≥ umbral Y año ≥ límite
        if calificacion >= calificacion_minima and año >= año_limite:
            contador += 1

    return contador

# =========================
# ENTRADA DE DATOS
# =========================

print("=== VIDEOTECA DIGITAL ===")

calificacion_minima = float(input("Ingrese la calificación mínima (1-10): "))
año_limite = int(input("Ingrese el año límite (2023 - 2026): "))

# =========================
# PROCESO
# =========================

resultado = contar_titulos(videoteca, calificacion_minima, año_limite)

# =========================
# SALIDA
# =========================

print("\n=== RESULTADO ===")
print("Cantidad total de títulos que cumplen ambos criterios:", resultado)
# =========================

resultado = contar_titulos(videoteca, calificacion_minima, año_limite)


# =========================
# SALIDA
# =========================

print("\nCantidad total de títulos que cumplen ambos criterios:", resultado)
