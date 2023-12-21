# 1-trabajo-
import os 
menu = "1. Registrar Alumno\n2. Registrar Notas\n3. Buscar estudiante\n4. Salir)"
subMenuNotas = "1.Parciales\n2.Quices\n3. Trabajos\n4.Regresar al menu principal"
hasError = True 
def menuPrincipal()-> int:
    global hasError
    hasError = True  
    print(menu)
    while (hasError ==True):
        try:
          menu.hasError = False 
          return int(input(":)"))
        except ValueError:
           menu.hasError = True 
           def menuNotas()-> int:
              print(subMenuNotas) 
              os.system("pause")
           *************************
           def regAlumno(diccAlumnos : dict)->dict: 
    codigo = input("ingrese el codigo del estudiante: ")
    nombre = input ("ingrese el nombre del estudiante : ")
    edad = input("ingrese la edad del estudiante: ")
    alumno = {
        "codigo" : codigo, 
        "nombre" : nombre,
        "edad" : edad, 
        "notas" :{
            "parciales" :[],
            "quices" :[], 
            "trabajos" :[], 
        }
    }
    return{codigo:alumno}
def buscarAlumno(codAlumno : str,alumnos : dict):
    data = alumnos.get(codAlumno-1) 
    if(type(data)==dict) :
        for llave,valor in data.items():
            print(f"{llave} : {valor}")
            os.system("pause")
        else: 
            print(f"no se encontro el estudiante con el codigo {codAlumno}") 
            os.system("pause") 
            def buscar(codAlumno : str,alumnos : dict)->dict:
                data = alumnos.get(codAlumno,-1)
                if (type(data) == dict):
                    return data 
                else: 
                    print(f"no se encontro el estudiante con el codigo {codAlumno}")
                    os.system("pause")
            ********************************************
            import os 
def addGrade(alumno : dict,categoria : str):
    dataNota = alumno.get("notas")
    evaluacion = dataNota.get(categoria)
    nota = float(input(f"ingrese la nota de {alumno.get("nombre").upper()} :"))
    evaluacion.append(nota)
    *****************************************************************
    import os 
import notas as nota
menu = "1. Registrar Alumno\n2. Registrar Notas\n3. Buscar estudiante\n4. Salir)"
subMenuNotas = "1.Parciales\n2.Quices\n3. Trabajos\n4.Regresar al menu principal"
hasError = True 
def menuPrincipal()-> int:
    global hasError
    hasError = True  
    print(menu)
    while (hasError ==True):
        try:
          menu.hasError = False 
          return int(input(":)"))
        except ValueError:
           menu.hasError = True 
def menuNotas(alumnos : dict):
    os.system('cls')
        
    isActiveMenu = True 
    while (isActiveMenu):
        os.system("cls")
        try:
            print(subMenuNotas)
            opMenu = int(input(":)")) 
        except ValueError:
            print("Opcion invalida...Recuerda que son enteros")
        else:
            if (opMenu == 1):
                nota.addGrade(alumnos,"parciales")  
            elif (opMenu == 2):
                nota.addGrade(alumnos,"quices")
            elif (opMenu == 3):
                nota.addGrade(alumnos,"trabajos")
            elif (opMenu == 4):
                isActiveMenu = False
            else:
                print("La opcion ingresada es invalida....")
                os.system('pause')
