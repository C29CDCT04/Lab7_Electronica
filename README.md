# Lab7_Electronica

Parte 1. Se diseñó e implementó una función que permitió encender un LED y mantenerlo encendido por cierto tiempo. La función recibió dos parámetros:
- Indicador del LED que debía encenderse (1, 2 o 3 para LED1, LED2 o LED3, respectivamente).
- Tiempo, en milisegundos, que debía permanecer el LED encendido. Luego de que transcurriera ese tiempo, debía apagar el LED.
Ej: Encender_LED(1, 500) -> Encendió LED1 por 500 ms.
Nota: La pausa se pudo realizar con interrupciones o usando la función vTaskDelay.

Parte 2. Se configuró el módulo UART del ESP32 y mostró en una terminal serial un menú con 2 opciones:
1. Lectura ADC.
2. Controlar LEDs.
La opción "Lectura ADC" la escogió el usuario ingresando un "1" en la terminal serial y la opción "Controlar LEDs" ingresando un "2". Si el usuario ingresó una opción diferente, mostró un mensaje de error (Ej: Opción inválida) y volvió a desplegar el menú.

Parte 3. Si el usuario seleccionó la opción 1 (Lectura ADC), realizó una lectura del canal analógico y desplegó el valor de voltaje obtenido (Ej: Voltaje: 2.5V) e imprimió nuevamente el menú.

Parte 4. Si el usuario seleccionó la opción 2 (Controlar LEDs), mostró otro mensaje solicitando: el LED a encender y el tiempo en milisegundos que debía permanecer encendido. El usuario debía indicar esos parámetros separados por coma y sin espacios (Ej: "1,500" -> encendió LED1 por 500 ms).
- Si el usuario ingresó un valor de LED inválido o si el tiempo no era un número, mostró un mensaje de error y solicitó el comando nuevamente.
- Luego de interpretar el comando, llamó la función de la parte 1 y encendió el LED. Al finalizar el tiempo, volvió a desplegar el menú.
