## Aspectos de la programación
### Lenguajes de Programación:
Los robots NAO pueden ser programados utilizando varios lenguajes de programación, lo que ofrece flexibilidad y accesibilidad tanto para principiantes como para programadores avanzados. Los principales lenguajes de programación utilizados para programar los robots NAO son:

- Python: Uno de los lenguajes más populares debido a su simplicidad y versatilidad.
- C++: Utilizado para tareas que requieren un alto rendimiento y control detallado del hardware.
- JavaScript: Utilizado en algunas aplicaciones específicas y en combinación con otras herramientas de desarrollo.

### Entorno de Desarrollo:
El entorno de desarrollo principal para los robots NAO es Choregraphe, un software visual que permite a los usuarios programar los robots mediante una interfaz de arrastrar y soltar. Choregraphe facilita la creación de comportamientos complejos sin necesidad de escribir código extenso. Además de Choregraphe, se utilizan otros entornos de desarrollo y herramientas:

- Choregraphe: Un entorno de programación visual que permite a los usuarios crear secuencias de comportamiento para los robots NAO mediante bloques de construcción visuales.
- Python: Se puede utilizar en combinación con Choregraphe para escribir scripts personalizados y controlar el robot a través de módulos de Python.
- NAOqi SDK: Proporciona bibliotecas y herramientas para programar en Python y C++, facilitando el acceso a las funciones y capacidades del robot.

### Ejemplos de Código
A continuación se presentan algunos fragmentos de código en Python, que es uno de los lenguajes más utilizados para programar los robots NAO.

Ejemplo 1: Saludo Simple

````
from naoqi import ALProxy

# Conexión con el robot
ip = "192.168.1.1"  # Dirección IP del robot
port = 9559
motion_proxy = ALProxy("ALMotion", ip, port)
tts_proxy = ALProxy("ALTextToSpeech", ip, port)

# Hacer que el robot se levante
motion_proxy.wakeUp()

# Hacer que el robot salude
tts_proxy.say("Hola, bienvenidos al laboratorio de robots humanoides")

# Hacer que el robot realice un gesto de saludo
motion_proxy.angleInterpolationWithSpeed("RShoulderPitch", -1.0, 0.2)
motion_proxy.angleInterpolationWithSpeed("RShoulderPitch", 1.0, 0.2)
````

Función: Este código conecta con el robot NAO y lo programa para decir "Hola, bienvenidos al laboratorio de robots humanoides" mientras realiza un gesto de saludo.

Ejemplo 2: Rutina de baile

![rutina](https://github.com/mobile-robotics-unal/humanoid-robots-NAO/assets/49196698/68cca956-0767-4e14-a01e-9aca5044e27e)

Función: Este código es generado con los códigos predeterminados de choregraphe, y nos permite unir las líneas de código para crear una rutina personalizada.
