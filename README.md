# tarea-1_sistemas_operativos_1

# Tarea 1 - Sistemas Operativos 1

## Autor
- **Nombre:** Luis Pablo Manuel García López  
- **Carnet:** 202200129  
- **Curso:** Sistemas Operativos 1  
- **Universidad San Carlos de Guatemala**  

---

## 📌 Introducción
En esta tarea se aplicaron comandos básicos de Linux y scripting en Bash para simular la creación de contenedores simples mediante archivos de texto generados de forma aleatoria.  
El objetivo fue familiarizarse con la línea de comandos y la automatización mediante scripts.

---

## 📂 Evidencia de Comandos

### 🔹 Navegación de directorios
```bash
pwd
ls
cd practica
pwd
```


---

### 🔹 Manipulación de archivos
```bash
touch archivo1.txt
ls
cp archivo1.txt copia_archivo1.txt
mv copia_archivo1.txt archivo_renombrado.txt
rm archivo_renombrado.txt
```



---

### 🔹 Visualización de contenido
```bash
echo "Hola, este es un archivo de prueba" > archivo1.txt
cat archivo1.txt
more archivo1.txt
less archivo1.txt
```


---

### 🔹 Gestión de permisos
```bash
ls -l archivo1.txt
chmod 700 archivo1.txt
ls -l archivo1.txt
sudo chown root archivo1.txt
ls -l archivo1.txt
```



---

## 📜 Script Bash: simulacion_crear_contenedores.sh
```bash
#!/bin/bash
# Script: simulacion_crear_contenedores.sh
# Autor: Luis Pablo Manuel García López
# Carnet: 202200129
# Curso: Sistemas Operativos 1
# Descripción: Simula la creación de contenedores con archivos de texto aleatorios.

# Número aleatorio entre 1 y 4
num_archivos=$(( (RANDOM % 4) + 1 ))

echo "Se crearán $num_archivos contenedores..."

# Lista de nombres aleatorios
nombres=("alpha" "beta" "gamma" "delta" "omega" "sigma" "lambda")

for (( i=1; i<=num_archivos; i++ ))
do
    # Seleccionar nombre aleatorio
    nombre=${nombres[$RANDOM % ${#nombres[@]}]}
    archivo="contenedor_202200129_${nombre}.txt"

    # Crear archivo y escribir su propio nombre dentro
    echo "$archivo" > "$archivo"

    echo "Archivo creado: $archivo"
done
```


---

## ✅ Conclusiones
- Se practicó el uso de comandos básicos de Linux para manejo de archivos, directorios, permisos y visualización de contenido.  
- Se implementó un script Bash que simula la creación de contenedores con nombres y contenido aleatorios.  
- La experiencia permitió reforzar el trabajo en la terminal de Linux dentro de WSL.  

---

## 📎 Entrega
- Carpeta del proyecto: `tarea-1/`  
- Archivos incluidos:  
  - `README.md` (este documento)  
  - `simulacion_crear_contenedores.sh`  
  - Carpeta `capturas/` con imágenes de evidencia  

