⚙️ Eventos Click — Backend
📌 Descripción
eventos-click-backend es el proyecto backend desarrollado en Spring Boot que expone la API REST para la plataforma Eventos Click, permitiendo la gestión de usuarios, eventos, localidades, compras, cupones y reportes.

Está diseñado para ser seguro, escalable y modular, integrándose con una base de datos MongoDB, servicios externos de almacenamiento de imágenes y pasarelas de pago en modo prueba.

🛠 Tecnologías
Java 21
Spring Boot 3.x
MongoDB
Spring Security (JWT)
Maven / Gradle
Git + GitHub para control de versiones
📂 Estructura principal
src/main/java/        # Código fuente (controladores, servicios, repositorios, modelos)
src/main/resources/   # Configuración, application.properties
src/test/             # Pruebas unitarias e integración
pom.xml / build.gradle # Gestión de dependencias y build
README.md             # Documentación y guía de uso
🌿 Flujo de ramas
master → versión estable del proyecto (solo producción)

dev → integración de nuevas funcionalidades (rama de equipo)

yovany, daniela, camilo → ramas personales de desarrolladores

👉 Cada desarrollador trabaja en su rama personal y luego integra sus cambios en dev.
👉 master contiene únicamente versiones estables y probadas.

🚀 Primeros pasos para nuevos desarrolladores
1️⃣ Clonar el repositorio

bash
Copiar código
git clone https://github.com/TU_USUARIO/eventos-click-backend.git
cd eventos-click-backend
2️⃣ Cambiar a tu rama personal

bash
Copiar código
git checkout tu-rama-personal
git pull origin tu-rama-personal
3️⃣ Configurar variables de entorno en application.properties o .env

properties
Copiar código
spring.data.mongodb.uri=mongodb://localhost:27017/eventosclick
spring.mail.username=tu_correo@gmail.com
spring.mail.password=tu_password
jwt.secret=clave_secreta_segura
4️⃣ Compilar y ejecutar con Maven o Gradle

bash
Copiar código
./mvnw spring-boot:run
# o con Gradle
./gradlew bootRun
La API estará disponible en:
👉 http://localhost:8080

🔄 Flujo de trabajo recomendado
1. Crear o trabajar en tu rama personal
   bash
   Copiar código
   git checkout yovany   # ejemplo
2. Hacer cambios y commits claros
   bash
   Copiar código
   git add .
   git commit -m "feat: agregar entidad Evento con su repositorio"
   👉 Usa prefijos:

feat: nueva funcionalidad

fix: corrección de bug

chore: tareas varias

3. Subir cambios al remoto
   bash
   Copiar código
   git push origin yovany
   📥 Integración de cambios
   De rama personal → dev
   Crear un Pull Request (PR) en GitHub.

Revisar y aprobar cambios.

Merge a dev.

De dev → master
Solo cuando dev esté estable y probada:

bash
Copiar código
git checkout master
git pull origin master
git merge dev
git push origin master
👩‍💻 Flujo de trabajo detallado para desarrolladores
Ejemplo: Daniela
1️⃣ Preparación inicial

bash
Copiar código
git clone https://github.com/TU_USUARIO/eventos-click-backend.git
cd eventos-click-backend
git checkout daniela
git pull origin daniela
2️⃣ Desarrollo en local

bash
Copiar código
git add .
git commit -m "feat: agregar endpoint de registro de usuario"
3️⃣ Subir cambios al remoto

bash
Copiar código
git push origin daniela
4️⃣ Integración en dev

Opción A: Pull Request (PR) desde GitHub.

Opción B: Merge manual en local:

bash
Copiar código
git checkout dev
git pull origin dev
git merge daniela
git push origin dev
5️⃣ De dev a master (solo cuando está probado y estable):

bash
Copiar código
git checkout master
git pull origin master
git merge dev
git push origin master
🔹 Flujo recomendado para Yovany
bash
Copiar código
git checkout dev
git pull origin dev
git checkout yovany
git merge dev
# resolver conflictos si hay
git add .
git commit -m "fix: resolver conflictos con dev"
git push origin yovany
👉 Ahora Yovany puede seguir trabajando en su rama personal con lo más reciente.

🔹 Resumen gráfico del flujo
java
Copiar código
Rama personal (ej: daniela, yovany) → dev → master
dev: integración y pruebas.

master: solo versiones estables de producción.

✅ Todos los desarrolladores trabajan alineados.
✅ dev siempre actualizado.
✅ Los conflictos se resuelven pronto y no se acumulan.

📏 Buenas prácticas
Trabajar siempre en ramas personales (nunca directo en master ni en dev).

Actualizar tu rama personal con dev antes de trabajar:

bash
Copiar código
git checkout dev
git pull origin dev
git checkout tu-rama
git merge dev
Hacer commits frecuentes y claros.

Probar localmente antes de subir cambios.

Usar mensajes de commit consistentes (feat:, fix:, chore:).

📚 Recursos adicionales
Documentación oficial de Spring Boot

Documentación oficial de MongoDB

Guía de Git y GitHub

yaml
Copiar código

🚀 Arranque rápido (Quickstart)
1️⃣ Clonar el repositorio
git clone https://github.com/TU_USUARIO/eventos-click-backend.git
cd eventos-click-backend

2️⃣ Configurar base de datos MongoDB

Asegúrate de tener MongoDB corriendo en local en el puerto por defecto (27017).
Edita src/main/resources/application.properties y añade:

spring.data.mongodb.uri=mongodb://localhost:27017/eventosclick

3️⃣ Ejecutar la aplicación

Con Gradle Wrapper:

./gradlew bootRun


En Windows (PowerShell o CMD):

gradlew.bat bootRun

4️⃣ Verificar que la API está corriendo

La aplicación se levanta en:
👉 http://localhost:8080

5️⃣ Acceder a la documentación Swagger

👉 http://localhost:8080/swagger-ui/index.html