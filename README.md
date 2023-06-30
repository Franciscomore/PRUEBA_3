duoc =  {}
def grabar():
    id =int(input("ingrese su rut por favor"))
    nombre = input("ingrese su nombre")
    apellido = input("ingrese su apellido")
    nacimiento = input("ingrese su fecha de nacimiento")
    carrera=input("ingrese su carrera")
    asignatura=input("deme su asignatura")
    promedio=float(input("promedio"))
    duoc[id]={"nombre":nombre, "apellido":apellido, "promedio":promedio, "carrera":carrera}
def buscar(id):
    return duoc.get(id)
    

while True:
    print("1. grabar")
    print("2. buscar")
    print("3. Imprimir certificados de notas")
    print("4. Imprimir certificado de alumno regular")
    print("5. Imprimir certificado de matricula")
    print("0. Salir")

    opcion = input("Ingrese una opción: ")
    print()
    if opcion == "1":
        grabar()
    elif opcion == "2":
        
        id = int(input("Ingrese el rut del alumno: "))
        datos = buscar(id)
        if datos:
            print("ID:", id)
            print("Nombre:", datos["nombre"])
            print("apellido:", datos["apellido"])
    elif opcion == "3":
        id = int(input("Ingrese el rut del alumno para optener su promedio de notas: "))
        datos = buscar(id)
        if datos:
            print("ID:", id)
            print("Nombre:", datos["nombre"])
            print("apellido:", datos["apellido"])
            print("promedio:",datos["promedio"])  
    elif opcion == "4":
        id = int(input("Ingrese el rut del alumno para obtener el certificado de alumno regular: "))
        datos = buscar(id)
        if datos:
            print("ID:", id)
            print("Nombre:", datos["nombre"])
            print("apellido:", datos["apellido"])
            print("carrera:",datos["carrera"])
    elif opcion == "5":
        id = int(input("Ingrese el rut del alumno para obtener certificado de matricula"))
        datos = buscar(id)
        if datos:
            print("ID:", id)
            print("Nombre:", datos["nombre"])
            print("apellido:", datos["apellido"])
            print("carrera:",datos["carrera"]) 
    elif opcion == "0":
        print("a eleguido la opcion salir")
        break        
            
