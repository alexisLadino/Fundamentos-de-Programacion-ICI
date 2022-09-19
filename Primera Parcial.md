![alt](http://www.natacionmexico.com/portal/images/eventlist/venues/small/universidad_de_colima_1321220340.jpg)
#   UNIVERSIDAD DE COLIMA
#### Alexis Vladimir Ladino Munguia
#### INGENIERIA EN COMPUTACION INTELIGENTE
#### 3°B
#### FACULTAD DE INGENERIA MECANICA Y ELECTRICA
#### Walter Alexander Mata López
---
Aqui se podran ver mis programas en clase
---
### 1.1 Print
    print("Hola ici")
---
### 1.2 Encabezado Markdown

    # UNIVERSIDAD DE COLIMA
		## FACULTAD DE INGENERIA MECANICA Y ELECTRICA
		### INGENIERIA EN COMPUTACION INTELIGENTE
---
### 1.3 Interpolación de Cadenas
    name="Alexis"
		edad=23
		print("hola",name,"tienes",edad,"años")
---
### 1.4 fstrings

		mensaje=f"hola {name} ,tienes {edad} años"
		mensaje
		print(mensaje)
    
		print(f"hola {name},tienes {edad} años")
---
### 1.5 Funciones

 		def saludo():
    
		print("Hola mundo")
    
		mi_funcion=saludo()    #asignando la funcion
		saludo()               #Invocando la funcion
		print(mi_funcion)
		
		def saludo2():
        return"Hola mundo"
		saludo2() #Invocacion 
		
		mi_funcion2= saludo2()
		print(mi_funcion2)
		
		a=5
		b=10
		res = f" La suma de {a}+{b} = {a+b}"
		print(res)
	  
		def suma(a,b):
		
         return a+b
		
		res = f"La suma de {a}+{b} = {suma(a,b)}"
		print(res)
---
### 1.6 Listas,Sets,Tuplas y Diccionariossss

		lista_numeros = ["uno","dos","tres"]
		msg_numeros= f"Numeros:{lista_numeros}"
		print(msg_numeros)
		
		tupla_numeros=("uno","dos","tres")
		msg_numeros=f"numeros:{tupla_numeros}"
		print(msg_numeros)
		
		set_numeros={"1","2","3","4","5","6","7","8","9","10"}
		print(set_numeros)
		
		dict_numeros={"1":"uno","2":"dos","3":"tres"}
		msg_dict_numeros=f"numeros:{dict_numeros}"
		print(msg_dict_numeros)
		
		dos= f"Numeros:{dict_numeros['2']}"
		print(dos)
---
### 1.7 Ejercicio en clase
  
- Escriba una funcion que mediante fstrings retorne el mensaje "Hola -nombre- tienes -edad- años".
  Los argumentos de la funcion: año actua, año de nacimiento y nombre
	 
	  nombre="Alexis"
		edad=23
		
		def act(nombre,edad):
    	 return(nombre,edad)
	 
	  mensaje=f"hola {nombre} tienes {edad}"
		print(mensaje)
---
### 1.8 Fstrings aplicadas
- EJEMPLO 1
		
			num_materia=["No. ",1,2,3,4]
			name_materia=["Materia","Estructura de datos","Ecuaciones diferenciales","Programacion funcional","Metodos numericos"]
			name_profesor=["Profesor","Edgar","Xochilt","Eli","Soto"]              
			print (f"{num_materia[0]:^5}{name_materia[0]:^30}{name_profesor[0]:<6}")
			for i in range (1,5):
    			print(f"{num_materia[i]:^5}{name_materia[i]:<30}{name_profesor[i]:<6}")
					
- EJEMPLO 2

			alumnos=["Pepe","Wicho","Javier","Rodolfo","Dylan"]
			name_materia=[6,8,6,8,7]
			name_materia2=[8,9,10,8,9]
			name_materia3=[8,8,7,6,9]
			name_materia4=[9,9,9,9,10]

			encabezado=["Nombre","Programacion funcional","Metodos numericos","Estructura de datos","Ingles"]

			def reporte (fmt):
					print(f"{encabezado[0]:^{fmt}}{encabezado[1]:^{fmt}}{encabezado[2]:^{fmt}}{encabezado[3]:^{fmt}}{encabezado[4]:^{fmt}}")
					for i in range (5):
								print(f"{alumnes[i]:*^{fmt}}{name_materia[i]:*^{fmt}}{name_materia2[i]:*^{fmt}}{name_materia3[i]:*^{fmt}}{name_materia4[i]:*^{fmt}}")
			reporte(20)
---
### 1.9 Programas en clase de funciones y manejo de fstrings


			# %%
			def saludo_edad_(nombre:str,a_nacimiento:int):
					edad= 2022-a_nacimiento
					print("Hola",nombre,"tienes",edad,"años")

			def calcular_edad(a_actual:int,a_nacimiento:int)->int:
					return a_actual-a_nacimiento

			def saludo(nombre:str,edad:int):
					print ("Hola",nombre,"tienes",edad,"años")

			def cuadrados(numu:int,numd:int):
					return (numu*numu) + (numd*numd)
			if __name__=="__main__":
					print(cuadrados(2,2))
			# %%
			def tabla(x):
					for i in range (11):
							print(x,"*",i,"=",x*i)


			if __name__=="__main__":
					print(tabla(3))
			# %%
			#Clase del 12 de septiembre 
			def tabla(t,n):
					for i in range (1,n+1):
							print(t,"*",i,"=",t*i)
			if __name__=="__main__":
					print(tabla(3,2))
			# %%
			def tabla(t:int,n:int,spc:int):
					for i in range (1,t+1):
							for j in range (1,n+1):
									print(f""i,"*",j,"=",i*j)
			t=int(input("¿Hasta que tablas quieres calcular?"))
			n=int(input("¿Hasta que numero quieres calcular?"))
			tabla(t,n)
			# %%
			def tabla(t:int,n:int,spc:int):
					for i in range (1,t+1):
							for j in range (1,n+1):
									print(f"{i:^{spc}} * {j:^{spc}} = {i*j:^{spc}}")
			t=int(input("¿Hasta que tablas quieres calcular?"))
			n=int(input("¿Hasta que numero quieres calcular?"))
			spc=int(input("¿Que espaciado quieres?"))
			tabla(t,n,spc)
---
### 1.10 Programas operacionales
- Suma

			def suma(num:int,num2:int)->int: return num+num2

			if __name__ == "__main__":
					print(suma(3,7))
- Multiplicacion

			def multi(num: int, num2: int) -> int: return num * num2

			if __name__ == "__main__":
			     print(multi(3, 7))
- Division

			def divisi(num: int, num2: int) -> float: return num / num2

			if __name__ == "__main__":
					print(divisi(3, 7))
- Cuadrado

			def cuadrado(num: int) -> int: return num*num

			if __name__ == "__main__":
					print(cuadrado(3))
- Resta

			def resta(num: int, num2: int) -> int: return num - num2

			if __name__ == "__main__":
					print(resta(3, 7))
---
### 1.11 Programas con listas

			i_lista=[1,2,3,4]
			print(mi_lista)
			lista_vacia=[]
			print(lista_vacia)


			mi_lista2=[1,"Hola",True,3.14,[1,2,3],(1,2,3),{1,2,3}]
			print(mi_lista2)

			print(len(mi_lista))
			print(len(mi_lista2))
			print(f"Mi lista:{mi_lista}")

			print(f"No de elementos:{len (mi_lista)}")
			print(f"Primer elemento:{mi_lista[0]},{mi_lista[1]},{mi_lista[2]},{mi_lista[3]}")
			print(f"Primer elemento:{mi_lista[-1]},{mi_lista[-2]},{mi_lista[-3]},{mi_lista[-4]}")
- Slices: Partes de una lista 

			print(mi_lista[1:-1])
			print(mi_lista[0:3])
			print(mi_lista[0:])
			print(mi_lista[:])
- Modificar listas

			mi_lista[2]="tres"
			print(mi_lista)
			
			ml.extend([6,7,8])
			print(ml)

			ml.insert(4,"cinco")
			print(ml)

			del ml[5]
			print(ml)

			ml.remove(2)
			print(ml)

			ml.reverse()
			print(ml)

			l1=[1,2,3]
			l2=l1[:]
			print(l1)
			l1.reverse()
			print(l1)
			print(l2)
- Insertar elementos en una lista

			new_lista=[5,"seis",7,8]
			mi_lista[len(mi_lista):]=new_lista
			print(mi_lista)

			mi_lista=[1,2,3,4]
			mi_lista.append("cinco")
			print(mi_lista)

			ml=[]
			for i in range(1,5):
					ml.append(i)
			print(ml)
- Programa que ordena elementos en una lista

			ld=[[5,4,6],[7,8,2,1],[3,4,5],[6,7]]
			print(f"Desordenado: {ld}")
			ld.sort()
			print(f"Ordenado: {ld}")

			ld=[5,4,6,7,8,2,1,3,4,5,6,7]
			S1= sorted(ld)
			print(S1)
			ld=[5,4,6,7,8,2,1,3,4,5,6,7]
			S2= sorted(ld,reverse=True)
			print(S2)

			ceros=[0,0,0,0,0,0,0,0,0]
			print(ceros)
			ceros=[0]*9
			print(ceros)

			valor_max=max(ld)
			print(valor_max)

			valor_min=min(ld)
			print(valor_min)

			cuatros=ld.count(4)
			print(cuatros)

			repe=[]
			for i in range (1,9):
					repe.append(ld.count(i))
			print(repe)			
---
### 1.12 Ejercicio de clase
- Escribir un programa...
	
			def tablas(t:int,n:int):
					for i in range(1,t+1):
							tabla(i,n,10)

			def tabla(t:int,n:int,spc:int):
					for i in range (1,n+1):
							print(f"{t:^{spc}}x{i:^{spc}}={t*i:^{spc}}")

			t=int(input("¿Hasta que tablas quieres calcular?"))
			n= int(input("¿Hasta que numero quieres calcular?"))
			tablas(t,n)



