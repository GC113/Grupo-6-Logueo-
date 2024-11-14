# [Tarea 1: Determinar las necesidades y expectativas del usuario](https://miro.com/app/board/uXjVLHLyKvA=/?openCardPanel=3458764606333314205)

## Objetivo
Identificar y entender a fondo las necesidades y expectativas de los usuarios finales en lo que respecta al sistema de autenticación, asegurando que sea seguro, accesible y fácil de usar. Este análisis permitirá tomar decisiones fundamentadas sobre las funcionalidades que serán esenciales en el sistema de autenticación para maximizar la satisfacción del usuario y la seguridad del producto.

## Entregable

### Descripción de los Usuarios Principales
- **Usuarios Finales**: Personas que requieren acceso rápido y seguro al sistema y valoran la simplicidad en el proceso de autenticación y recuperación de cuentas.
- **Administradores del Sistema**: Personal con permisos especiales para gestionar las cuentas y mantener la seguridad de la plataforma.

### Expectativas Clave de los Usuarios
- **Acceso seguro y rápido**: Un sistema que permita a los usuarios autenticarse sin demoras y con altos estándares de seguridad.
- **Facilidad en la creación y recuperación de cuentas**: La aplicación debe incluir un proceso de registro simple, así como un mecanismo eficaz para la recuperación de contraseñas.

### Requisitos Iniciales del Sistema de Autenticación
- **Registro y Autenticación Segura**
  - Registro de nuevos usuarios con confirmación de identidad mediante email.
  - Login seguro utilizando autenticación con tokens para proteger las sesiones activas.
  - Opciones de autenticación con cuentas de terceros (por ejemplo, Google) para mejorar la accesibilidad y conveniencia.

- **Gestión de Sesiones y Seguridad**
  - Manejo de cookies para almacenar de forma segura los tokens de sesión.
  - Protección contra accesos no autorizados con mecanismos de verificación, como OAuth2.
  - Almacenamiento seguro de contraseñas mediante encriptación con bcrypt.

- **Recuperación de Cuenta**
  - Proceso de restablecimiento de contraseñas a través de un enlace seguro enviado por email.

---

# [Tarea 2: Escalabilidad de la App](https://miro.com/app/board/uXjVLHLyKvA=/?openCardPanel=3458764606333314204)

## Objetivo
Identificar y garantizar que la infraestructura esté diseñada de manera escalable para soportar el crecimiento futuro del sistema, tanto en términos de usuarios como de nuevas funcionalidades. Esto asegura que el sistema no solo cumpla con los requisitos actuales, sino que también pueda evolucionar sin problemas con el tiempo.

## Entregable

### Arquitectura Modular
El sistema será construido con una arquitectura modular, es decir, un enfoque de diseño de sistemas en el que el sistema se divide en componentes o módulos independientes que se pueden desarrollar, mantener y desplegar por separado. Esto permitirá la integración de nuevas funcionalidades o la modificación de las existentes sin necesidad de reestructurar completamente el sistema. Facilitará la incorporación de nuevas opciones de autenticación, como integración con otras plataformas o autenticación multifactor, en el futuro.

### Escalabilidad del Backend
Se garantizará que el sistema sea capaz de manejar un número creciente de usuarios sin comprometer el rendimiento. El uso de tecnologías como JWT para la gestión de sesiones permitirá una autenticación eficiente, incluso con un alto volumen de usuarios.

### Soporte para Expansión
El diseño permitirá la integración futura con sistemas más complejos, como la inclusión de roles de usuario o la implementación de políticas de seguridad más avanzadas. Además, la infraestructura permitirá su escalabilidad en la nube, lo que facilitará el manejo de un aumento en la demanda o de nuevas regiones geográficas en caso de expansión.

### Mantenibilidad y Flexibilidad
Se utilizarán buenas prácticas de desarrollo y documentación clara para que el sistema sea fácil de mantener, actualizar y escalar según sea necesario. Los cambios y mejoras en el sistema podrán implementarse sin causar interrupciones significativas en la operación del sistema.

---

# [Tarea 3: Evaluar el tamaño y crecimiento potencial del mercado](https://miro.com/app/board/uXjVLHLyKvA=/?openCardPanel=3458764606333874337)

## Objetivo
Evaluar el tamaño y crecimiento potencial del mercado de aplicaciones de autenticación y logueo, entendiendo las tendencias de adopción de tecnologías de seguridad, las necesidades de los usuarios y las oportunidades de expansión en distintos sectores. Este análisis permitirá identificar oportunidades clave para mejorar y expandir la app de logueo y adaptarla a las necesidades de un mercado en crecimiento.

## Entregable

### Proyecciones de Crecimiento del Mercado
- Según un informe de **Markets and Markets**, el mercado global de la autenticación multifactor está proyectado a alcanzar los **USD 24,8 mil millones para 2025**, con un crecimiento anual compuesto (CAGR) de 15,4% desde 2020.
- Estudios de crecimiento en **tecnologías de ciberseguridad** indicaron un incremento en la inversión en autenticación en la nube, que representa un área clave para la expansión de apps de logueo.

### Análisis de Oportunidades de Innovaciones Tecnológicas
- Se recogió información sobre tendencias emergentes, como el uso de **blockchain** para mejorar la seguridad del logueo, la integración con **redes sociales** para simplificar el proceso de registro, y el uso de **inteligencia artificial** para detectar intentos de fraude.
- Informes sobre la implementación de **autenticación sin contraseña**, que está ganando tracción como una opción más segura y conveniente.

### Segmentación de Mercado
- **Usuarios Individuales**: El 56% de los usuarios de internet en Norteamérica y Europa utilizan autenticación multifactor para proteger sus cuentas bancarias en línea, según un estudio de **Cybersecurity Ventures**.
- **Empresas y Organizaciones**: Según **IDC**, el 83% de las empresas están implementando soluciones de autenticación avanzada debido al aumento de ciberataques.

### Oportunidades de Expansión
- La expansión hacia nuevos mercados en **Asia y África**, donde la adopción de soluciones de seguridad está en auge debido a un aumento en las transacciones móviles y la digitalización de servicios financieros.

---

# [Tarea 4: Tecnología de Logueo Back](https://miro.com/app/board/uXjVLHLyKvA=/?openCardPanel=3458764606333874361)

## Objetivo
Evaluar el tamaño y crecimiento potencial del mercado de aplicaciones de autenticación y logueo, entendiendo las tendencias de adopción de tecnologías de seguridad, las necesidades de los usuarios y las oportunidades de expansión en distintos sectores. Este análisis permitirá identificar oportunidades clave para mejorar y expandir la app de logueo y adaptarla a las necesidades de un mercado en crecimiento.

## Entregable

### Proyecciones de Crecimiento del Mercado
- Según un informe de **Markets and Markets**, el mercado global de la autenticación multifactor está proyectado a alcanzar los **USD 24,8 mil millones para 2025**, con un crecimiento anual compuesto (CAGR) de 15,4% desde 2020.
- Estudios de crecimiento en **tecnologías de ciberseguridad** indicaron un incremento en la inversión en autenticación en la nube, que representa un área clave para la expansión de apps de logueo.

### Análisis de Oportunidades de Innovaciones Tecnológicas
- Se recogió información sobre tendencias emergentes, como el uso de **blockchain** para mejorar la seguridad del logueo, la integración con **redes sociales** para simplificar el proceso de registro, y el uso de **inteligencia artificial** para detectar intentos de fraude.
- Informes sobre la implementación de **autenticación sin contraseña**, que está ganando tracción como una opción más segura y conveniente.

### Segmentación de Mercado
- **Usuarios Individuales**: El 56% de los usuarios de internet en Norteamérica y Europa utilizan autenticación multifactor para proteger sus cuentas bancarias en línea, según un estudio de **Cybersecurity Ventures**.
- **Empresas y Organizaciones**: Según **IDC**, el 83% de las empresas están implementando soluciones de autenticación avanzada debido al aumento de ciberataques.

### Oportunidades de Expansión
- La expansión hacia nuevos mercados en **Asia y África**, donde la adopción de soluciones de seguridad está en auge debido a un aumento en las transacciones móviles y la digitalización de servicios financieros.

---

# [Tarea 5: Tecnología de Logueo Front](https://miro.com/app/board/uXjVLHLyKvA=/?openCardPanel=3458764606333874383)

## Objetivo
Evaluar el tamaño y crecimiento potencial del mercado de aplicaciones de autenticación y logueo, entendiendo las tendencias de adopción de tecnologías de seguridad, las necesidades de los usuarios y las oportunidades de expansión en distintos sectores. Este análisis permitirá identificar oportunidades clave para mejorar y expandir la app de logueo y adaptarla a las necesidades de un mercado en crecimiento.

## Entregable

### Proyecciones de Crecimiento del Mercado
- Según un informe de **Markets and Markets**, el mercado global de la autenticación multifactor está proyectado a alcanzar los **USD 24,8 mil millones para 2025**, con un crecimiento anual compuesto (CAGR) de 15,4% desde 2020.
- Estudios de crecimiento en **tecnologías de ciberseguridad** indicaron un incremento en la inversión en autenticación en la nube, que representa un área clave para la expansión de apps de logueo.

### Análisis de Oportunidades de Innovaciones Tecnológicas
- Se recogió información sobre tendencias emergentes, como el uso de **blockchain** para mejorar la seguridad del logueo, la integración con **redes sociales** para simplificar el proceso de registro, y el uso de **inteligencia artificial** para detectar intentos de fraude.
- Informes sobre la implementación de **autenticación sin contraseña**, que está ganando tracción como una opción más segura y conveniente.

### Segmentación de Mercado
- **Usuarios Individuales**: El 56% de los usuarios de internet en Norteamérica y Europa utilizan autenticación multifactor para proteger sus cuentas bancarias en línea, según un estudio de **Cybersecurity Ventures**.
- **Empresas y Organizaciones**: Según **IDC**, el 83% de las empresas están implementando soluciones de autenticación avanzada debido al aumento de ciberataques.

### Oportunidades de Expansión
- La expansión hacia nuevos mercados en **Asia y África**, donde la adopción de soluciones de seguridad está en auge debido a un aumento en las transacciones móviles y la digitalización de servicios financieros.

---

# [Tarea 6: Tecnología de Almacenamiento de Datos](https://miro.com/app/board/uXjVLHLyKvA=/?openCardPanel=3458764606333874422)

## Objetivo
Determinar la tecnología de almacenamiento para la gestión de usuarios y autenticación de la app de logueo.

## Entregable

Se ha seleccionado **PostgreSQL** como tecnología de almacenamiento de datos debido a su fiabilidad, escalabilidad y capacidad para gestionar grandes volúmenes de datos. PostgreSQL es un sistema de gestión de bases de datos relacional (RDBMS) que proporciona potentes características de seguridad, como la **encriptación de datos** y el **control de acceso**, lo que lo convierte en una opción ideal para almacenar la información sensible de los usuarios, incluidas las **credenciales de acceso** y los **tokens generados para la autenticación**.

---

# [Tarea 7: Tecnología de Infraestructura](https://miro.com/app/board/uXjVLHLyKvA=/?openCardPanel=3458764606333874447)

## Objetivo
Determinar la tecnología de infraestructura para el despliegue y operación de la app de logueo.

## Entregable

Se ha seleccionado **AWS (Amazon Web Services)** como la infraestructura en la nube para el despliegue de la aplicación debido a su fiabilidad, escalabilidad y amplia gama de servicios. AWS ofrece herramientas como **EC2** para el alojamiento de servidores, **S3** para almacenamiento de archivos estáticos, y **RDS** para bases de datos gestionadas, lo que facilita la administración de los recursos y asegura un rendimiento óptimo. Además, AWS proporciona opciones de seguridad avanzadas, como **IAM** para la gestión de accesos y **VPC** para redes privadas, lo que garantiza un entorno seguro para la aplicación.

---

# [Tarea 8: Plataforma para la Creación de un Repositorio](https://miro.com/app/board/uXjVLHLyKvA=/?openCardPanel=3458764606335291802)

## Objetivo
Se requiere crear un repositorio privado en GitHub para la gestión del código fuente de la app de logueo.

## Entregable

Se creó un repositorio privado en **GitHub** donde se almacenará todo el código fuente del proyecto. El repositorio permitirá una gestión adecuada de las versiones mediante el uso de **ramas (branches)**, **commits** y **pull requests**. Además, se establecerán las políticas de acceso necesarias para que solo los miembros autorizados puedan contribuir al proyecto.

GitHub también proporcionará herramientas de **integración continua (CI/CD)** para automatizar el proceso de pruebas y despliegue del código, asegurando un flujo de trabajo eficiente y sin interrupciones.

Dicho repositorio podrá ser observado en la siguiente referencia de [Miro](https://miro.com/app/board/uXjVLHLyKvA=/?moveToWidget=3458764606859813806&cot=14).
