# [Tarea 1: Definir Diseño del Logueo](https://miro.com/app/board/uXjVLHLyKvA=/?openCardPanel=3458764606331717145)

## Objetivo
Se requiere definir el diseño del logueo para la app de autenticación de usuarios.

## Entregable

- **Disposición y organización de los campos de entrada**: Diseño claro y estructurado para los campos de usuario y contraseña.
- **Opciones para el inicio de sesión mediante Google (OAuth2)**: Inclusión de botón para iniciar sesión con Google como alternativa de autenticación.
- **Diseño responsivo**: Asegurarse de que el diseño se adapte a diferentes tamaños de pantalla, como móviles, tabletas y escritorios.
- **Indicaciones claras para el usuario en caso de error de autenticación**: Mensajes de error fáciles de entender en caso de credenciales incorrectas o problemas de conexión.
- **Estilo visual coherente con la identidad de la aplicación**: Utilización de colores, tipografía y elementos gráficos que sigan la identidad visual de la app.

Llegamos al diseño de utilizar la siguiente interfaz en [Miro](https://miro.com/app/board/uXjVLHLyKvA=/?moveToWidget=3458764606335389340&cot=14).

---

# [Tarea 2: Creación de base de datos para la app de autenticación de usuarios](https://miro.com/app/board/uXjVLHLyKvA=/?openCardPanel=3458764606335474262)

## Objetivo

Se requiere crear y configurar la base de datos para la app de autenticación de usuarios en PostgreSQL, asegurando la correcta gestión de los datos de los usuarios y sus sesiones.

## Tablas

### Tabla `users`

La tabla `users` almacenará los datos esenciales de cada usuario que se registre en la aplicación. A continuación se detallan sus columnas:

- **id**: Identificador único del usuario (clave primaria).
- **username**: Nombre de usuario único y no nulo. Se utiliza como clave para identificar al usuario.
- **password**: Contraseña encriptada del usuario, que no puede ser nula.
- **email**: Correo electrónico único del usuario, no puede ser nulo.
- **roleid**: Identificador del rol del usuario (por ejemplo, 1 para administrador, 2 para cliente, etc.). Este campo es obligatorio.
- **createdat**: Timestamp que indica la fecha y hora de creación de la cuenta del usuario. Este valor se asigna automáticamente si no se especifica.
- **updatedat**: Timestamp que indica la fecha y hora de la última actualización de la cuenta. Se asigna automáticamente si no se especifica.

### Tabla `sessions`

La tabla `sessions` gestiona las sesiones de los usuarios. Almacena la información de cada sesión activa y sus detalles. Sus columnas son:

- **id**: Identificador único de la sesión (clave primaria).
- **userid**: Clave foránea que referencia al usuario en la tabla `users`. No puede ser nula. Si el usuario es eliminado, se elimina la sesión correspondiente (gracias a la opción `ON DELETE CASCADE`).
- **sessiontoken**: Token único que identifica la sesión. Este valor no puede ser nulo y debe ser único en la tabla.
- **createdat**: Timestamp que indica cuándo se creó la sesión. Se asigna automáticamente si no se especifica.
- **expiresat**: Fecha y hora de expiración de la sesión. Este valor es obligatorio.

## Creación de la base de datos

Con base en el diseño y las tablas descritas, se crea y configura la base de datos en PostgreSQL para registrar el logueo de usuarios y gestionar sus sesiones.

## Conclusión

Se ha configurado correctamente la base de datos con las tablas `users` y `sessions`, asegurando que se gestionen adecuadamente los datos de los usuarios y las sesiones activas. Además, se ha implementado la opción de eliminación en cascada en la tabla `sessions` para mantener la integridad referencial.

---

# [Tarea 3: Backend de Autenticación](https://miro.com/app/board/uXjVLHLyKvA=/?openCardPanel=3458764606715665039)

## Objetivo
El objetivo es configurar el entorno de infraestructura en **AWS** para alojar tanto el **frontend**, el **backend** y la **base de datos** de la aplicación de logueo. El servidor debe ser escalable, seguro y garantizar alta disponibilidad.

## Entregable
El entregable será el backend de autenticación, que incluirá:
- **API REST** para recibir las solicitudes de inicio de sesión y validación de credenciales.
- Implementación de la autenticación mediante **JWT** (JSON Web Tokens) para manejo de sesiones.
- Integración con **Google OAuth2** para permitir el inicio de sesión a través de cuentas de Google.
- Validación de credenciales en la base de datos (**PostgreSQL**).
- Respuestas de error adecuadas para situaciones como credenciales incorrectas o fallos en la autenticación.
- Protección de las rutas de acceso mediante autenticación y autorización.

## Esquema de Validación
Se encargará de una segunda capa de validación con la biblioteca **Zod** ya que la primera vendrá por el frontend y deberá tener la siguiente estructura: vista en la siguiente referencia [Miro](https://miro.com/app/board/uXjVLHLyKvA=/?moveToWidget=3458764606858765882&cot=14).

## Rutas
Podrán ser vistas en la siguiente referencia [Miro](https://miro.com/app/board/uXjVLHLyKvA=/?moveToWidget=3458764606859058385&cot=14).

### Manejo de tokens
- Configurar generación de tokens JWT para autenticar usuarios y establecer los tiempos de expiración.
- El token debera ser creado con la biblioteca denominada jsonwebtoken y tendra una expiracion de 24hs.

### Gestión de sesiones y expiración 
Implementar lógica para manejo de expiración de sesión.

---

# [Tarea 4: Definir Costos](https://miro.com/app/board/uXjVLHLyKvA=/?openCardPanel=3458764606335474384)

## Objetivo
Se requiere definir los costos asociados al desarrollo y operación de la app de autenticación de usuarios.

## Entregable

### 1. Costos de Desarrollo

#### Análisis y Requerimientos
- **Horas estimadas**: 10 horas
- **Tarifa por hora**: $30
- **Total**: $300

#### Diseño de Interfaz (UI/UX)
- **Horas estimadas**: 20 horas
- **Tarifa por hora**: $30
- **Total**: $600

#### Desarrollo Back-end
- **Horas estimadas**: 60 horas
- **Tarifa por hora**: $40
- **Total**: $2400

#### Desarrollo Front-end
- **Horas estimadas**: 40 horas
- **Tarifa por hora**: $40
- **Total**: $1600

#### Integración con Servicios Externos (OAuth2, Google login, etc.)
- **Horas estimadas**: 15 horas
- **Tarifa por hora**: $30
- **Total**: $450

#### Pruebas (Testing)
- **Horas estimadas**: 15 horas
- **Tarifa por hora**: $30
- **Total**: $450

#### Subtotal Desarrollo: 
- **Total**: $5,800

---

### 2. Costos de Infraestructura

#### Servidor o Hosting
- **Opción básica en AWS**: $50 mensuales (esto puede variar según el tráfico y uso)
- **Total anual**: $600

#### Dominio (si no tiene uno)
- **Registro en Namecheap o GoDaddy**: $12 al año
- **Total**: $12

#### Certificado SSL
- **Gratis (Let’s Encrypt)** o pagado ($50 al año)
- **Total**: $0 - $50

#### Subtotal Infraestructura (anual): 
- **Total**: $612 - $662

---

### 3. Costos de Mantenimiento

#### Actualizaciones y mejoras
- **Horas estimadas por mes**: 5 horas
- **Tarifa por hora**: $30
- **Total mensual**: $150
- **Total anual**: $1,800

#### Soporte Técnico
- **Horas estimadas por mes**: 2 horas
- **Tarifa por hora**: $30
- **Total mensual**: $60
- **Total anual**: $720

#### Subtotal Mantenimiento (anual): 
- **Total**: $2,520

---

### 4. Costos Extras

#### Licencias de software (si aplica)
- **Supongamos que no necesitas herramientas pagas.**
- **Total**: $0

#### Documentación
- **Horas estimadas**: 10 horas
- **Tarifa por hora**: $30
- **Total**: $300

#### Imprevistos (si aplica)
- **Total**: $500

#### Subtotal Costos Extras: 
- **Total**: $300 - $800

---

El resumen de costos puede ser visto desde la siguiente referencia [Miro](https://miro.com/app/board/uXjVLHLyKvA=/?moveToWidget=3458764606865543016&cot=10).

---

# [Tarea 5: Servidor AWS](https://miro.com/app/board/uXjVLHLyKvA=/?openCardPanel=3458764606334398916)

## Objetivo
El objetivo es configurar el entorno de infraestructura en **AWS** para alojar tanto el **frontend** como el **backend** de la aplicación de logueo, asegurando alta disponibilidad, seguridad y escalabilidad. Además, se gestionará el almacenamiento de datos utilizando **Amazon RDS** para la base de datos **PostgreSQL**.

## Entregable

1. **Configuración de instancias EC2** para alojar el backend de la aplicación.

2. **Implementación de un entorno escalable** usando **Auto Scaling** para manejar el crecimiento de usuarios.

3. **Amazon RDS** configurado para alojar la base de datos **PostgreSQL**, con copias de seguridad automáticas y alta disponibilidad.

4. **Configuración de VPC (Virtual Private Cloud)** para asegurar la red de la aplicación.

5. **Uso de IAM (Identity and Access Management)** para la gestión de roles y permisos dentro de AWS, asegurando acceso adecuado a los recursos.

6. **Implementación de medidas de seguridad**, como **firewalls (Security Groups)** y **encriptación de datos** tanto en tránsito como en reposo.

7. **Monitoreo de la infraestructura** con herramientas de **CloudWatch** para asegurar el rendimiento y la disponibilidad.

---

# [Tarea 6: Frontend del Login](https://miro.com/app/board/uXjVLHLyKvA=/?openCardPanel=3458764606715665148)

## Objetivo
El objetivo es implementar una interfaz de usuario eficiente y segura para el proceso de autenticación, utilizando **React** para gestionar los estados de la aplicación. La solución debe permitir que los usuarios ingresen sus credenciales, autentiquen su sesión y almacenen los datos del usuario en el contexto global de la aplicación, de manera que se pueda acceder a esos datos desde cualquier componente a lo largo del sistema.

## Entregable

### 1. **Estructura de componentes**
El sistema de login está implementado mediante **componentes funcionales en React**, con separación de responsabilidades. El componente principal **Login** renderiza los campos de entrada y los botones de autenticación.

### 2. **Gestión del estado global con Context API**
La autenticación del usuario se gestiona globalmente con **Context API de React**. Este contexto contiene los datos del usuario (nombre, correo electrónico y token de autenticación), disponibles para cualquier componente en la aplicación. Además, se incluyeron funciones en el contexto para manejar la autenticación, el estado de inicio de sesión y el cierre de sesión.  
Dicha implementación podrá ser vista en [Miro](https://miro.com/app/board/uXjVLHLyKvA=/?moveToWidget=3458764606858430245&cot=14).

### 3. **Validaciones y manejo de errores**
Se implementaron validaciones en los campos de entrada para asegurar que el formulario solo se envíe con datos válidos. En caso de errores de autenticación, se presentan mensajes claros y amigables al usuario, indicando el problema y posibles soluciones.

### 4. **Estilos responsivos con CSS y Bootstrap**
La interfaz de usuario es moderna y responsiva, utilizando **CSS** y **Bootstrap** para adaptarse a dispositivos móviles y de escritorio de forma accesible y visualmente atractiva.  
Dicha implementación podrá ser vista en [Miro](https://miro.com/app/board/uXjVLHLyKvA=/?moveToWidget=3458764606859527934&cot=14).
