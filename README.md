def calculadora():
    print("Calculadora básica en Python")
    print("Operaciones disponibles:")
    print("1. Suma (+)")
    print("2. Resta (-)")
    print("3. Multiplicación (*)")
    print("4. División (/)")
    print("5. Potenciación (^)")
    print("6. Módulo (%)")
    print("7. Salir")
    
    while True:
        try:
            # Selección de operación
            opcion = input("\nSeleccione una operación (1-7) o el símbolo de la operación: ")
            
            # Opción para salir
            if opcion == '7' or opcion.lower() == 'salir':
                print("¡Hasta luego!")
                break
            
            # Validación de números
            num1 = float(input("Ingrese el primer número: "))
            num2 = float(input("Ingrese el segundo número: "))
            
            # Realizar operación seleccionada
            if opcion == '1' or opcion == '+':
                print(f"Resultado: {num1} + {num2} = {num1 + num2}")
            elif opcion == '2' or opcion == '-':
                print(f"Resultado: {num1} - {num2} = {num1 - num2}")
            elif opcion == '3' or opcion == '*':
                print(f"Resultado: {num1} * {num2} = {num1 * num2}")
            elif opcion == '4' or opcion == '/':
                if num2 == 0:
                    print("Error: No se puede dividir por cero")
                else:
                    print(f"Resultado: {num1} / {num2} = {num1 / num2}")
            elif opcion == '5' or opcion == '^':
                print(f"Resultado: {num1} ^ {num2} = {num1 ** num2}")
            elif opcion == '6' or opcion == '%':
                print(f"Resultado: {num1} % {num2} = {num1 % num2}")
            else:
                print("Opción no válida. Por favor intente nuevamente.")
                
        except ValueError:
            print("Error: Por favor ingrese números válidos")
        except Exception as e:
            print(f"Ocurrió un error: {e}")

# Ejecutar la calculadora
if _name_ == "_main_":
    calculadora()
