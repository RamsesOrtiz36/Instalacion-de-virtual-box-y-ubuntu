# Instalacion-de-virtual-box-y-ubuntu
Pasos para instalar virtual box y configuración del sistema operativo secundario Ubuntu

## Ubuntu 20.04
El uso de maquina virtual permite el cambio de caracteristicas de hardware más sencillo
Porteje al sistema operativo primario 

## Requisitos de hardware físico
+ Mínmo 2 nucleos
+ RAM 8GB mínimo
+ Disco Duro 60 GB libre 
+ Pantalla 1024x764 pixeles

El procesador debera tener habilitada al virtualización, en dado caso de no tenerla, entrar a BIOS y activarla

## Software 
De la pagina de [virtual box](https://www.virtualbox.org/) descargar el software Virtual box 
De la pagina de [Versiones de Linux](https://releases.ubuntu.com/) descargar la ***imagen .iso*** de Ubuntu 20.04 LTS (64 bits) aprox 3.6 GB

La maquina virtual del software de Virtual Box nos permite ejecutar un segundo sistema operaticvo con recursos asignados.

## Procedimiento para crear maquina virtual.
1. Descargar virtual Box y Ububtu 20.04 lts.
2. Instalar software de vitual box (sigue las instrucciones del asistente de instalación).
![](https://github.com/RamsesOrtiz36/Instalacion-de-virtual-box-y-ubuntu/blob/main/Instalaci%C3%B3n%20Virtual%20Box/Instalaci%C3%B3n%20de%20virtual%20box1.png)
3. Al terminar la instalación ejecutar VirtualBox.
4. Buscar el boton de "crear" o "nueva" y darle clic.
![](https://github.com/RamsesOrtiz36/Instalacion-de-virtual-box-y-ubuntu/blob/main/Instalaci%C3%B3n%20Virtual%20Box/Instalaci%C3%B3n%20de%20virtual%20box2.png)
5. Seguir la instrucciones dandole nombre a la maquina virtual **(Ububtu 20.04 LTS)** y seleccionar el tipo de sistema opertivo **(Linux)** y version de 64 bits
6. Seleccionar desde carpeta la ubicación de la Maquina virtual.
7. Asignarle RAM de 4GB en multiplos de 1024 bytes ![](https://github.com/RamsesOrtiz36/Instalacion-de-virtual-box-y-ubuntu/blob/main/Instalaci%C3%B3n%20Virtual%20Box/Instalaci%C3%B3n%20de%20virtual%20box3.png)
8. Crear disco duro virtual tipo VDI ![](https://github.com/RamsesOrtiz36/Instalacion-de-virtual-box-y-ubuntu/blob/main/Instalaci%C3%B3n%20Virtual%20Box/Instalaci%C3%B3n%20de%20virtual%20box4.png)
![](https://github.com/RamsesOrtiz36/Instalacion-de-virtual-box-y-ubuntu/blob/main/Instalaci%C3%B3n%20Virtual%20Box/Instalaci%C3%B3n%20de%20virtual%20box5.png)
9. Reservar dinamicamente espacio en disco de 48GB ![](https://github.com/RamsesOrtiz36/Instalacion-de-virtual-box-y-ubuntu/blob/main/Instalaci%C3%B3n%20Virtual%20Box/Instalaci%C3%B3n%20de%20virtual%20box6.png)
10. Crear Maquina virtual.

## Configuración de Maquina virtual
Una vez creada hay que configurarla sin iniciarla, desde la ventana de virtual box
1. Seleccionarla y dar clic en boton de configuración
2. En General->Avanzado->Activar portapapeles **Bidireccional** y arrastar y pegar **Bidireccional**
3. Sistema->Procesadores->**2 nucleos** (No seleccionar más de la mitad de la cantidad de nucleos)
4. Pantalla->pantalla->**128 MB**
5. Pantalla-> controlador grafico **VMSVGA** (No activar Acelerador 3D)
6. Red-> **Conecctor puente** en caso de usar red en escuela usar **NAT**
7. Tambien seleccionar la tarjeta de Red, cada cambio entre WiFi a Eternet.

Posteriormente se puede cambiar la configuración de la maquina virtual para adecuarla al uso

## Instalar Ububtu en Maquina vrtual.
Una vez configurada se da clic en el boton de inicializar maquina virtual, es como prender la computadora.
Solamente la primera vez que se inicializa la computadora el softwae te pedira la instalación del sistema operatvo.
Seleccionar desde carpeta la ubicación de la imagen de disco tipo .ISO (el archivo de Ububtu 20.04 de 3.6 Gb).
+ Solicita nombre del usuario y con el asigna nombre de la maquina virtual, aquí se puede dar nombre que uno escoja. 
+ Pedirá contraseña, se recomienda que sea corta, ya que se usará muchas veces.
+ Seguir las instrucciones, solicitará permiso para instalar software de terceros decir que si
+ Tambien hay que seleccionar la opcion de borrar espacio de disco e instalar Ubuntu.
+ Cuando termine de instalarse Ubuntu se pide reiniciar la maquina virtual.
+ Al reiniciar pide el idioma y el idioma de teclado, hay que buscarlos en la lista desplegable, si no se ve en pantalla hay que mover el marco de la ventana para ver los botones de continuar.
+ Acualizar y poner al día al sistema operativo, en una ventana de terminal (ctrl+alt+T)

      sudo apt-get update
      sudo apt-get upgrade

## Instalar Guest additions
Esta instalación ayuda a que la ventana de visualización del sistema operativo de la maquina vritual se ajuste a la redimension del marco de ventana, si no  se queda en un tamaño pequeño y es muy incomodo.
+ Desde terminal (ctrl+alt+T) descargar e instalar 
  
        sudo apt install gcc perl make
        
+ Aceptar la descarga siguiendo las instrucciones que aparecen
+ Insertar el disco de Guest additions, en el menu de la ventana de maquina virtual ir a **Dispositivos** e insertar el CD de Guest Additions.
+ Reiniciar la maquina virtual.
+ Sacar o expulsar el disco de Guest additions.      
+  Acualizar y poner al día al sistema operativo, en una ventana de terminal (ctrl+alt+T)

       sudo apt-get update
       sudo apt-get upgrade






 


