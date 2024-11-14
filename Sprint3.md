# [Tarea 1: Definir Tipos de Alertas en CloudWatch](https://miro.com/app/board/uXjVLHLyKvA=/?openCardPanel=3458764606331717301)

## Objetivo
Se requiere definir los tipos de alertas en **Amazon CloudWatch** para monitorear el rendimiento y la salud de la infraestructura.

## Entregable

### 1. Intentos Fallidos de Inicio de Sesión
Se monitorea la seguridad detectando intentos de inicio de sesión fallidos que puedan indicar posibles ataques o problemas de usabilidad.

**Configuración en CloudWatch:**
- **Log Events:** Se configura la aplicación para que registre cada intento de inicio de sesión, especificando si fue exitoso o fallido.
- **Metric Filter:** Se crea un filtro de métricas en CloudWatch para contar los eventos de inicio de sesión fallido en los logs de la aplicación.
- **Alarmas:** Se configuran alarmas para que se dispare si la cantidad de intentos fallidos en un período corto (por ejemplo, 5 minutos) supera un umbral definido. Esta alerta puede enviarse por correo electrónico o SMS para que el equipo de seguridad actúe rápidamente.

### 2. Errores HTTP 500
Detectar y responder rápidamente a errores de servidor (HTTP 500), que pueden indicar problemas con el backend, errores de código, o problemas en la base de datos.

**Configuración en CloudWatch:**
- **Log Events:** Se configura la aplicación para registrar errores HTTP 500 en los logs o directamente en las métricas.
- **Metric Filter:** Se crea un filtro de métricas en CloudWatch para contar las respuestas HTTP 500.
- **Alarmas:** Se configura una alarma para activarse cuando la cantidad de errores HTTP 500 supere un umbral en un período de tiempo determinado (como 5 o 10 minutos). Esto permite al equipo de desarrollo detectar y corregir problemas antes de que afecten gravemente a los usuarios.

### 3. Tasa Baja de Intentos de Login
Detectar una reducción anormal en la cantidad de intentos de inicio de sesión, lo que podría indicar que el sistema de autenticación está fallando o que la aplicación no está accesible para los usuarios.

**Configuración en CloudWatch:**
- **Metric Filter:** Se configura una métrica en CloudWatch para contar los intentos de inicio de sesión en el sistema.
- **Alarmas:** Se crea una alarma que se dispare si el número de intentos de inicio de sesión en un período (como 1 hora) cae por debajo de un umbral mínimo esperado. Esto podría indicar problemas en el frontend, la red, o con la funcionalidad de login en el backend.

---

# [Tarea 2: Casos de prueba](https://miro.com/app/board/uXjVLHLyKvA=/?openCardPanel=3458764606331717299)

## Objetivo
Se requiere definir y documentar los casos de prueba para verificar el correcto funcionamiento de la aplicación de login y la autenticación de usuarios.

## Entregable

### Casos de prueba

#### Verificación de credenciales
- **Caso de prueba para autenticación con credenciales válidas:** Verificar que el usuario pueda iniciar sesión con las credenciales correctas.
- **Caso de prueba para autenticación con credenciales incorrectas:** Verificar que el sistema muestre un mensaje de error adecuado si las credenciales no son correctas.

#### Generación de tokens
- **Caso de prueba para la generación y validez del token JWT:** Verificar que se genere un token válido tras la autenticación exitosa y que caduque cuando sea necesario.

#### Autenticación con Google OAuth2
- **Caso de prueba para el flujo de autenticación con Google:** Verificar que el usuario pueda iniciar sesión usando su cuenta de Google y que el sistema reciba la respuesta adecuada.
- **Caso de prueba para la respuesta errónea de OAuth2:** Verificar que el sistema maneje correctamente los errores si hay problemas con la autenticación de Google.

### Casos de prueba de usabilidad

#### Mensajes de error y éxito
- **Caso de prueba para la claridad de los mensajes:** Verificar que los mensajes de error sean claros y útiles para el usuario, por ejemplo, "Usuario o contraseña incorrectos".
- **Caso de prueba para la confirmación de login exitoso:** Verificar que, tras un login exitoso, el usuario vea un mensaje claro que lo indique.

En el siguiente apartado, podrá encontrar los casos de prueba realizados hasta la fecha en [Miro](https://miro.com/app/board/uXjVLHLyKvA=/?moveToWidget=3458764606868436391&cot=10).


---

# [Tarea 3: Definir costos de DNS](https://miro.com/app/board/uXjVLHLyKvA=/?openCardPanel=3458764606335829816)

## Objetivo
Se requiere definir los costos asociados con la utilización de servicios DNS en AWS para la gestión de nombres de dominio.

## Entregable
Para el proyecto se eligió usar **AWS Route 53** para gestionar los DNS de la plataforma, es una excelente opción, ya que ofrece escalabilidad, alta disponibilidad y funciones avanzadas.

En el gráfico se muestran dos conceptos clave de los costos de AWS Route 53:

### 1. Zona DNS (1 dominio)
Se refiere al costo mensual por la gestión de una zona DNS, que es el dominio principal bajo el cual gestionas los subdominios (por ejemplo, tms.com). El costo por cada zona DNS hospedada es de **$0.50 USD al mes**. Solo necesitas pagar una vez por el dominio principal, y puedes crear subdominios como `cliente1.tms.com` sin costo adicional en términos de zonas.

### 2. Consultas DNS (5 millones)
Cada vez que un usuario accede a tu plataforma, se realiza una consulta DNS para resolver el dominio o subdominio hacia una dirección IP específica. AWS cobra **$0.40 USD por cada millón de consultas**. En este ejemplo, se han estimado 5 millones de consultas al mes, lo que genera un costo de **$2.00 USD**. Este número puede variar según el tráfico de tu plataforma y el número de clientes.

- Después de las primeras mil millones de consultas, el costo es de **$0.20 USD por millón de consultas al mes**.

### Costo final:
- **Zona DNS:** $0.50 USD por la zona principal.
- **Consultas DNS:** $0.40 USD x 5 millones = $2.00 USD.
- **Total mensual:** $2.50 USD.

Gráfico referenciado en [Miro](https://miro.com/app/board/uXjVLHLyKvA=/?moveToWidget=3458764606336517211&cot=14).
