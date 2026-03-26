# 🐳 Laboratorio 3 – Docker

## 📌 Información general

* **Materia:** Sistemas Operativos
* **Alumno:** Facundo Rodríguez
* **Laboratorio:** Laboratorio 3 – Docker

---

## 🎯 Objetivo

El objetivo de este laboratorio es comprender el funcionamiento de Docker, incluyendo el uso de contenedores, imágenes y Dockerfiles. Además, se busca experimentar con distintos sistemas operativos dentro de contenedores y ejecutar aplicaciones en entornos aislados.

---

## ⚙️ Tecnologías utilizadas

* Docker Desktop
* Nginx
* Ubuntu (contenedor)
* Alpine (contenedor)
* Visual Studio Code

---

## 🚀 Ejecución del proyecto

### 1. Clonar el repositorio

```bash
git clone https://github.com/cfacu23/Lab03-Docker-Facundo.git
cd Lab03-Docker-Facundo/web-docker
```

---

### 2. Construir la imagen

```bash
docker build -t facu-web .
```

---

### 3. Levantar el contenedor

```bash
docker run -d --name facu-web-contenedor -p 8090:80 facu-web
```

---

### 4. Abrir en el navegador

```
http://localhost:8090
```

Se visualizará una página web simple creada con HTML dentro del contenedor.

---

## 📂 Estructura del proyecto

```
web-docker/
│
├── Dockerfile
└── index.html
```

---

## 🐳 Dockerfile utilizado

```dockerfile
FROM nginx:alpine
COPY index.html /usr/share/nginx/html/index.html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
```

---

## 🧪 Pruebas realizadas

Durante el laboratorio se realizaron las siguientes pruebas:

* Ejecución de contenedores básicos (`hello-world`)
* Uso de comandos Docker (`ps`, `logs`, `exec`, `rm`, `rmi`)
* Creación de imagen personalizada con Dockerfile
* Levantamiento de un servidor web con Nginx
* Pruebas con distintos sistemas operativos:

  * Ubuntu (uso de `apt-get`)
  * Alpine (uso de `apk`)

---

## 🧠 Conclusión

Este laboratorio permitió comprender el funcionamiento de Docker y la diferencia entre imágenes y contenedores. Se logró crear y ejecutar un contenedor personalizado que levanta un servidor web, además de experimentar con distintos sistemas operativos dentro de entornos aislados. Docker facilita la portabilidad y ejecución de aplicaciones de forma consistente en distintos entornos.

---

## 🔗 Repositorio

https://github.com/cfacu23/Lab03-Docker-Facundo

---
