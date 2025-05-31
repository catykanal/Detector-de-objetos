# Detector-de-objetos
Proyecto para detectar el nivel de comida para un perro y notificación en Telegram sobre el nivel de comida actual
Crea una alarma que te notifique cuando se le terminara la comida a tu perro en Telegram
Link del tutorial comlpeto: https://youtu.be/yMTSmL99j5Q


Con esta tarjeta puedes conectar un sensor ultrasonico HCSR04 al microcontrolador ESP 32 C3 (yo utilizo la versión Supermini) y así poder enviar una notificación a un grupo de Telegram cuando se detecte un objeto.
Te propongo utilizar este sistema para adaptarlo a un dispensador de alimento para perros pues así sera muy fácil saber aunque estés lejos cuando se terminara la comida y poder tomar tus precauciones y no se quede con hambre tu amigo peludo.
Aquí encuentras todo lo que necesitas para llevar a cabo la practica en protoboard o en circuito hecho en PCB.
Para la creación del código me apoye de la AI (DeepSeek), y en el tutorial te muestro como hacer la vinculación paso a paso con Telegram para que tengas las notificaciones sin falla.

Materiales para practica:
1 Esp 32 C3
1 Sensor HCSR04
Jumpers

Materiales circuito PCB:
1 Esp32 C3
2 Borneras
1 Resistencias THT
4 Pines hembra
1 Porta pilas AA
1 Regulador voltaje AMS1117
1 Switch cola raton SMD

Promp DeepSeek:
Necesito que crees un programa en ide arduino para un circuito que tiene un sensor ultrasonico HCSR04 y que es controlado por el ESP32 C3,en donde el trigger esta conectado al gpio9, y el eco esta en el GPIO10, este programa enviara una señal para encender un led que esta integrado en el GPIO8 si y solo si se detecto un objeto desde los 16 cm hasta los 40cm,después se apagara el led y posteriormente a la detección del objeto esperara 4 segundos y deja de censar y posteriormente continua con el ciclo para volver a detectar, pero si el objeto detectado esta a 15 cm o menos no encenderá el led y estará detectando el sensor sin pausas solo en este caso, si se sale de rango mayor a 40 cm deberá estar apagado el led y por ultimo se repite el ciclo después de cada detección y eso MISMO QUE HACE EL LED también lo hará AHORA CON EL ENVÍO DE UNA NOTIFICACIÓN QUE LLEGARA A UN GRUPO DE TELEGRAM UTILIZANDO LAS LIBRERÍAS <WiFi.h> <HTTPClient.h> <WiFiClientSecure.h>, IMPORTANTE!!!! ESTA NOTIFICACIÓN tiene que hacer exactamente lo mismo que realiza el led y posteriormente continua con el resto del programa y solo se tiene que enviar la notificación de los 16 a 40cm, el SSID es , el password , el botToken (TU BOT TOKEN AQUI )y el ChatId (TU CHATID)

![photo_5012842260752084418_y](https://github.com/user-attachments/assets/c6068f4c-711a-49a3-aa0e-13f57714f128)

Link para generar el ID del chat
https://api.telegram.org/botTU_TOKEN_AQUI/getUpdates
