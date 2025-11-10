Nombre del proyecto: Documentación QA para Instagram Lite


Integrante: Maria Celeste Paredes


Objetivo del testing: El objetivo es asegurar que cada requisito o funcionalidad del software esté cubierto por una o más pruebas


Alcance: El Alcance para Instagram Lite
Las áreas que sí se probarán incluyen el registro y logueo, asegurando que el proceso sea rápido y eficiente, con redirección inmediata a la pantalla del feed tras el acceso exitoso, sin animaciones gráficas complejas o transiciones pesadas, y que se muestren mensajes de error claros y no ambiguos al ingresar credenciales no válidas. Respecto a la Publicación de Contenido, se verificará el acceso directo a la galería y se validará estrictamente la limitación clave de la versión Lite: la selección de una única foto o un único video corto a la vez, además de la capacidad de añadir texto descriptivo y su correcta visualización en el feed y perfil. Las interacciones sociales como dar 'Me Gusta' y Guardar Publicaciones serán probadas, exigiendo un cambio de estado visual inmediato y una ejecución ágil

Ambiente de Ejecución: Pruebas (Test QA).
Plataforma de la Aplicación : Android (Instagram Lite es una aplicación Android).
Herramientas de Testing Funcional: Casos de Prueba manuales para validar la lógica del negocio.

Conclusión general
NO, el producto no está listo para ser liberado a Producción basándose en los resultados de la ejecución de pruebas funcionales.
La conclusión se basa en los siguientes puntos:
1. Fallos Críticos de las Funcionalidades Base
De los 15 casos de prueba funcionales ejecutados, se encontraron tres fallos (FAIL) que comprometen la funcionalidad esencial y los requerimientos no funcionales (eficiencia y limitaciones) del producto:
• Registro Fallido (TC-001): El caso de registro exitoso con correo electrónico y contraseña válidos NO PASÓ. Aunque se esperaría que el usuario fuera redirigido inmediatamente a la pantalla del feed (CA 1.2), el resultado obtenido fue que se mostró un aviso de información.
• Fallo de Seguridad/Validación (TC-003): La verificación del mensaje de error al usar una contraseña que NO cumple con los requisitos mínimos de seguridad NO PASÓ. El sistema no permitió continuar la prueba por el botón de siguiente, lo que indica un error en la validación o el flujo.
• Violación de la Limitación Lite (TC-007): Este es un fallo crucial. La prueba buscaba verificar que el sistema NO permitiera la selección de más de un elemento para publicación simultánea (un requerimiento clave de Instagram Lite, CA 2.2). El resultado obtenido fue que el sistema SÍ permite selección múltiple, lo que viola la limitación funcional conocida de la versión Lite de ahorrar datos y espacio.
