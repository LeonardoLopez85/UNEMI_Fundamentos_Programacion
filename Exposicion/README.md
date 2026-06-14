# --- 1. Definición de la Función ---
# Ahora la función ACEPTA un "parámetro" (precio_base)
# para poder trabajar con él.
def calcular_iva(precio_base):
    print(f"    -> [FUNCIÓN]: ¡Me han llamado! Recibí el valor: {precio_base}")
    print("    -> [FUNCIÓN]: Calculando IVA y Total...")
    
    iva_calculado = precio_base * 0.12
    valor_total = precio_base + iva_calculado
    
    print("    -> [FUNCIÓN]: He terminado. Devolviendo los dos valores...")
    
    # La función DEVUELVE los resultados al programa principal
    return iva_calculado, valor_total

# --- 2. Programa Principal ---
# La ejecución del script SIEMPRE empieza aquí.
print("[PRINCIPAL]: Ha iniciado nuestro código.")

# Pedimos el dato al usuario
# Usamos float() para convertir el texto en un número decimal
valor_ingresado = float(input("[PRINCIPAL]: Ingrese el valor base para calcular el IVA: "))

# --- 3. Invocación (La Llamada) ---
print(f"[PRINCIPAL]: OK. Ahora invocaré la función pasándole el ARGUMENTO: {valor_ingresado}...")

# ¡Este es el momento de la LLAMADA!
# 1. Pasamos 'valor_ingresado' (el argumento) a la función.
# 2. Capturamos los valores que la función 'return' en dos nuevas variables.
iva_obtenido, total_obtenido = calcular_iva(valor_ingresado) 

# --- 4. Retorno ---
print("[PRINCIPAL]: ¡El control ha regresado a mí!")
print(f"[PRINCIPAL]: La función me devolvió el IVA: {iva_obtenido:.2f} y el Total: {total_obtenido:.2f}")

# Ahora el programa principal usa esos valores para el reporte final
print("\n--- RESUMEN FINAL ---")
print(f"Valor Original: {valor_ingresado:.2f}")
print(f"Valor IVA:      {iva_obtenido:.2f}")
print(f"Valor Total:    {total_obtenido:.2f}")
print("---------------------")
print("[PRINCIPAL]: Fin del programa.")
