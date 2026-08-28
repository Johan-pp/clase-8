total_dia = 0
facturas_hechas = 0

while True:
    print("-" * 40)
    print("EL LÁPIZ FELIZ")
    print("-" * 40)
    print("1. Registrar una factura")
    print("2. Ver total acumulado del día")
    print("3. Ver cuántas facturas se han registrado")
    print("4. Salir")
    print("-" * 40)

    opcion = input("Elige una opción: ")

    if opcion == "1":
        cantidad = int(input("¿Cuántos productos tiene esta factura? "))
        total_factura = 0

        for i in range(cantidad):
            print(f"Producto {i + 1} de {cantidad}:")
            nombre = input("  Nombre del producto: ")
            precio = float(input("  Precio: "))
            total_factura = total_factura + precio

        print(f"Factura registrada. Total: ${total_factura:,.0f}")
        total_dia = total_dia + total_factura
        facturas_hechas = facturas_hechas + 1
    elif opcion == "2":
        print(f"Total acumulado del día: ${total_dia:,.0f}")  # 👈 NUEVO
    elif opcion == "3":
        print(f"Facturas registradas hoy: {facturas_hechas}")  # 👈 NUEVO
    elif opcion == "4":
        print("¡Gracias por usar el sistema! Hasta pronto.")
        break
    else:
        print("Opción no válida, intenta de nuevo.")
