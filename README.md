# Tecnicatura Superior en Telecomunicaciones  

## Asignaturas: 
- Electronica Microcontroada. Profesor **Cristian Gonzalo Vera**
- Sensores y Actuadores. Profesor **Jorge Morales**
- Redes. Profesor **Dante Violi**
  
## Formacion Profesional
**Desarrollador de Dispositivos IoT**

## Descripcion del Respositorio  
Este repositorio es creado con el fin de dar soporte al desarrollo del proyecto final para la obtencion de la FP. 
El mismo esta organizado sobre una estructura de **platformIO** sobre el ide de **Visual Studio Code**. Tambien se agrega la extension de **wokwi** para la simulacion de los dispositivos. Y la carpeta **proteus** para la simulacion de los circuitos electronicos no soportados en wokwi.

## Descripcion del Proyecto
El proyecto consiste en un sistema de control y monitoreo distribuido para optimizar el uso y gestión del agua en diferentes entornos.
Este controlador, tipo célula, es capaz de abarcar el control general y amplio de jardines, plazas, huertas urbanas, así como grandes plantaciones agrícolas en campos rurales.
El sistema se enfoca en la eficiencia y sostenibilidad del riego mediante la gestión y monitoreo inteligente de los recursos hídricos locales.  

El proyecto será llevado a cabo  a lo largo de 4 Sprints:  

- Sprint 1: Planificación y Configuración Inicial
- Sprint 2: Integración y Desarrollo de Software
- Sprint 3: Configuración Avanzada y Optimización
- Sprint 4: Prueba Final, Documentación y Presentación  

## Integrantes del Proyecto
- Jose Marquez, GitHub: [@marquezjose](https://github.com/marquezjose).
- Luciano Lujan, GitHub: [@lucianoilujan](https://github.com/lucianoilujan).
- Vittorio Durigutti, GitHub: [@vittoriodurigutti](https://github.com/vittoriodurigutti).
- Fernando Gimenez Coria, GitHub: [@FerCbr](https://github.com/FerCbr).
- Tiziano Paez, GitHub: [@tpaez](https://github.com/tpaez).
- Marcos Bordón, GitHub: [@Marcos-BR-03](https://github.com/Marcos-BR-03).
- Karina Jazmin Barbero, GitHub: [@karina-lolis](https://github.com/karina-lolis).
- Nicolás Nahuel Barrionuevo, GitHub: [@NicolasBa27](https://github.com/NicolasBa27).
- Macarena Aylen Carballo, GitHub: [@MacarenaAC](https://github.com/MacarenaAC).
- Diego Ares, GitHub: [@diegote7](https://github.com/diegote7).
- Lisandro Juncos, GitHub: [@Lisandro-05](https://github.com/Lisandro-05).
- Raul Antonio Jara, GitHub: [@r-j28](https://github.com/r-j28).
- Joaquin Zalazar, GitHub: [@breaakerr](https://github.com/breaakerr).  
- Patricio Leandro Roldan, Github: [@pleroldan](https://github.com/pleroldan).
- Romina Huk,  Github: [@RoHu17](https://github.com/RoHu17).
- Nahuel Vélez, GitHub: [@Nahuelvelez](https://github.com/Nahuelvelez).
- Paola Natalia Alejandra Pantoja, Github: [@PaolaaPantoja](https://github.com/PaolaaPantoja).
- Laura Analia Brizuela, GitHub: [@gerbena03](https://github.com/gerbena03).
- Joaquin Garzón, GitHub: [@Joacogarzonn](https://github.com/Joacogarzonn)  

---  
### El stack tecnologico utilizado en el proyecto es el siguiente:
- **Plataforma de Hardware:** ESP32
- **ide:** Visual Studio Code
- **Lenguaje de Programacion:** C++, basado en el framework de arduino
- **Plataforma de Software:** PlatformIO, con el framework de arduino
- **Simulacion:** Wokwi y proteus
- **Control de Versiones:** GitHub
- **Documentacion:** Markdown
- **Gestion de Proyecto:** kanban en GitHub
- **Comunicacion:** Discord

### Etapa del Proyecto  
- **Sprint 1:** Planificacion y Configuracion Inicial
- **Fecha de Inicio:** 31/08/2024

#### Actividades a completar:  

- Realización de pruebas iniciales de sensores.
- Realización de pruebas iniciales de actuadores.
- Configuración de librerías necesarias en ESP32.
- Documentación de los pasos de instalación.
- Registro de resultados de pruebas iniciales.
- Ajustes y calibraciones necesarias.
- Preparación de un informe de pruebas iniciales.
- Presentación de los resultados de pruebas al equipo.  



### Consideraciones sobre la Simulacion con wokwi  
Para la simulacion de los dispositivos se utiliza la extension de **wokwi** en **Visual Studio Code** debe tener en cuenta lo siguiente: 
- Tener instalada la extension wokwi en su Visual Studio Code.
- El archivo diagram.json corre la simulacion y es cambiado a .txt, para anularla. Si quiere correr la simulacion debe cargar apropiadamente el .json y cambiar la extension. 
- El archivo wokwi.toml es el archivo de configuracion de la extension wokwi.  

### Consideraciones sobre la Simulacion con Proteus  
Para la simulacion de los circuitos electronicos no soportados en wokwi se utiliza el software **Proteus**. En dicha carpeta se encuentra el proyecto, cargado en la version 8.12. Ademas se agrega la organizacion de los tests correspondientes a cada dispositivo. 
Se debe tener en cuenta que proteus no simula a la fecha agosto/2024 los dispositivos ESP32, por lo que la simulacion se basa en el arduino uno. Y se utiliza luego el firmware desarrollado para el ESP32.

### Lista de sensores y actuadores utilizados en el proyecto:  
 
Se debe actualizar la informacion de las carpetas de acuerdo a los siguientes detalles (datasheet de sensores y actuadores. Protocolos spi, i2c):  

![Conexiones](./assets/Conexion%20fp_controlador_cultivo.png)

**Entradas Analógicas y Digitales:**  

1.	Sensores de Humedad del Suelo (HW-080) (x3):
o	Sensor 1: GPIO36 (ADC1_CHANNEL_0)
o	Sensor 2: GPIO39 (ADC1_CHANNEL_3)
o	Sensor 3: GPIO34 (ADC1_CHANNEL_6)
2.	DHT11 (Temperatura y Humedad):
o	GPIO14 (Digital)
3.	Sensor de Lluvia (AB119):
o	GPIO33 (Digital)
4.	Sensor Ultrasónico (HC-SR04):
o	Trigger: GPIO12
o	Echo: GPIO13
5.	LDR (Luz Ambiente):
o	GPIO32 (ADC1_CHANNEL_4)
6.	Micrófono Electret:
o	GPIO35 (ADC1_CHANNEL_7)
7.	Sensores PIR (HCSR501) (x3):
o	Sensor 1: GPIO25
o	Sensor 2: GPIO26
o	Sensor 3: GPIO27  

**Salidas:**
1.	Tira LED WS2812B:
o	GPIO15 (Digital)
2.	Módulo de Relé de 4 Canales:
o	Canal 1 (Bomba de Agua): GPIO4
o	Canal 2 (Válvula 1): GPIO16
o	Canal 3 (Válvula 2): GPIO17
o	Canal 4 (Válvula 3): GPIO0  

**Interfaces de Comunicación:**
SPI:  
-	MOSI: GPIO23
-	MISO: GPIO19
-	SCK: GPIO18
-	SS (NSS): GPIO5  
I2C:  
-	SCL: GPIO22
-	SDA: GPIO21  
  
**Distribucion de Componentes**  

![Distribucion de componentes](./assets/Instalacion%20Fisica%20de%20Sensores%20y%20Actuadores.png)