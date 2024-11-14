# [Tarea 1: Integración con Terceros](https://miro.com/app/board/uXjVLHLyKvA=/?openCardPanel=3458764606331717222)

## Objetivo
Integrar la funcionalidad de autenticación de usuarios con servicios de terceros, permitiendo a los usuarios iniciar sesión mediante **Google OAuth 2.0** en la aplicación.

## Descripción
Configurar la autenticación con **Google** mediante el protocolo **OAuth 2.0**.  
Registrar las credenciales de la API en la **Google Cloud Console** siguiendo el enlace: [Google Cloud Console](https://console.cloud.google.com/apis/credentials?project=tms-unab).  
Para orientación visual, consultar la referencia en [Miro](https://miro.com/app/board/uXjVLHLyKvA=/?moveToWidget=3458764606336884985&cot=14).

## Entregable

### 1. **Integración funcional de inicio de sesión con Google:**
- Crear el flujo de autenticación con **OAuth 2.0**.
- En el **front-end**, instalar la biblioteca `react-oauth/google` para el manejo de la autenticación.
- Configuración del componente **GoogleOAuthProvider** en el archivo de rutas principal, pasando el **clientId** generado.

Dicha porción de código podrá ser vista en la siguiente referencia [Miro](https://miro.com/app/board/uXjVLHLyKvA=/?moveToWidget=3458764606857121516&cot=14).

---

# [Tarea 2: Definir Costos de los Servicios de AWS](https://miro.com/app/board/uXjVLHLyKvA=/?openCardPanel=3458764606331717300)

## Objetivo
Se requiere definir los costos de los servicios de **AWS**, incluyendo la implementación de **Auto Scaling**.

## Entregable

### Presupuesto de los servicios en AWS:
- **S3**
- **EC2**
- **CloudWatch**
- **RDS**
- **Cognito**
- **AWS Support**
- **Load Balancing**

### Implementación de los servicios AWS:

1. **S3**  
   Se gestionó el almacenamiento en **S3** para manejar archivos estáticos, como documentos e imágenes, asegurando un escalado automático según el uso. Los costos se cobrarán según el almacenamiento consumido y las solicitudes realizadas.

2. **EC2**  
   Se configuraron instancias de **EC2** para ejecutar la API de logueo, habilitando el **Auto Scaling** para que las instancias se ajusten automáticamente según el volumen de tráfico mensual, con capacidad para manejar **50,000 peticiones nuevas por mes**.

3. **CloudWatch**  
   Se activó **CloudWatch** para monitorear los recursos del sistema, incluyendo el uso de CPU en las instancias EC2, el tráfico de red, y establecer alertas automáticas para la detección temprana de problemas de rendimiento.

4. **RDS**  
   Se gestionó la base de datos **PostgreSQL** con **RDS**, permitiendo que el **Auto Scaling** ajuste la capacidad de la base de datos en función del aumento en el tráfico y la demanda, asegurando un rendimiento óptimo para las **50,000 peticiones mensuales**.

5. **Cognito**  
   Se implementó **Cognito** para manejar la autenticación y autorización de usuarios de manera segura, gestionando los procesos de registro, inicio de sesión y generación de tokens de sesión.

6. **AWS Support**  
   Se activó **AWS Support** para recibir soporte técnico y asesoría continua, garantizando la optimización de costos y el correcto funcionamiento de la infraestructura.

7. **Load Balancing**  
   Se configuró un **Load Balancer** para distribuir de manera eficiente el tráfico entre las instancias de **EC2**, evitando sobrecargas en los servidores y manteniendo el rendimiento del sistema.
