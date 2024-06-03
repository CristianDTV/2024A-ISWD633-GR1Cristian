# COMPLETAR  
Comparando sus conocimientos antes de hacer la práctica con sus conocimientos después de hacer la tarea, explicar los principales aprendizajes logrados para beneficio de su formación profesional.  
Si solucionó un problema presentado al realizar la práctica también se debe documentar.
## Reflexión y Aprendizajes Logrados

### Antes de la Práctica

Antes de realizar esta práctica, mis conocimientos sobre Docker y la gestión de contenedores eran básicos. Tenía una comprensión general de cómo crear y ejecutar contenedores, pero carecía de experiencia práctica en la configuración avanzada de redes de Docker, la persistencia de datos y la gestión de variables de entorno para aplicaciones complejas como WordPress y MySQL.

### Después de la Práctica

Después de completar esta práctica, he adquirido una comprensión más profunda y práctica de varios aspectos clave de Docker. Aquí están los principales aprendizajes que he logrado:

1. **Creación y Gestión de Redes Docker**:
   - Aprendí a crear redes de tipo `bridge` y cómo conectar y desconectar contenedores de estas redes. Esto es crucial para gestionar la comunicación entre contenedores de forma segura y organizada.
   - Comprendí cómo inspeccionar redes y contenedores para verificar sus conexiones y configuraciones de red.

2. **Configuración de Contenedores con Variables de Entorno**:
   - Adquirí la habilidad para configurar contenedores con variables de entorno, lo cual es esencial para la configuración de aplicaciones como WordPress y MySQL. Esto me permite manejar configuraciones sensibles de manera segura y reutilizable.
   - Utilicé archivos de variables de entorno para simplificar y estandarizar la configuración de contenedores.

3. **Persistencia de Datos**:
   - Entendí la importancia de usar volúmenes de Docker para la persistencia de datos. Esto es vital para mantener los datos de aplicaciones a través de reinicios y recreaciones de contenedores.
   - Aprendí a crear y usar volúmenes para asegurar que los datos de WordPress y MySQL se mantengan a salvo incluso si los contenedores son eliminados.

4. **Despliegue de Aplicaciones Complejas**:
   - Adquirí experiencia en el despliegue de una aplicación web completa con un backend de base de datos. Configuré un entorno de WordPress con MySQL y manejé la comunicación entre ambos contenedores.
   - Aprendí a mapear puertos para permitir el acceso externo a aplicaciones web alojadas en contenedores Docker.

### Problemas Solucionados

Durante la práctica, enfrenté y resolví varios problemas:

1. **Problemas con la Resolución de Nombres de Contenedor**:
   - Inicialmente, tuve problemas con la resolución de nombres de contenedores cuando intenté conectar WordPress a MySQL. Aprendí a usar direcciones IP y finalmente resolví el problema configurando correctamente las variables de entorno.

2. **Persistencia de Datos**:
   - Descubrí que al eliminar y recrear contenedores, los datos se perdían. Resolví esto utilizando volúmenes de Docker, asegurando que los datos de WordPress y MySQL se mantuvieran persistentes a través de recreaciones de contenedores.

3. **Configuración y Conexión de Redes**:
   - Tuve que aprender cómo conectar y desconectar contenedores a múltiples redes y cómo verificar estas conexiones. Esto fue crucial para asegurar que los contenedores de WordPress y MySQL pudieran comunicarse correctamente en la red `net-wp`.

### Conclusión

Esta práctica ha sido extremadamente beneficiosa para mi formación profesional. No solo he mejorado mis habilidades técnicas en Docker, sino que también he adquirido un enfoque más sistemático para la resolución de problemas y la configuración de entornos de desarrollo complejos. Estos conocimientos me permitirán gestionar aplicaciones de manera más efectiva y segura.
