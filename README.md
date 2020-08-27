
rtlwifi_new
===========
### A repo for the newest Realtek rtlwifi codes.
```bash
Este es el codigo que tiene mi maquina una HP-Laptop-15-bw005la y lo subo por que la version oficial actualmente no esta en funcionamiento
Para ver si su modelo es el mismo debes de poner uname -a
Para ver tu controlador sudo lspci -nn
Para ver si esta correcto la configuración: ifconfig 
Este código se basará en cualquier kernel 4.19 y más reciente siempre que la distribución no se haya modificado
cualquiera de las API del kernel. SI USTED EJECUTA UBUNTU, DEBES DE ASEGURARTE DE QUE LAS API NO HAN CAMBIADO.
NO, NO MODIFICARÉ LA FUENTE POR USTED. ¡¡¡¡¡ESTAS POR TU CUENTA!!!!!

Este repositorio incluye controladores para las siguientes tarjetas:

RTL8822BE, RTL8822CE, RTL8821CE y RTL8723DE.
```

### Installation instruction
##### Requirements
Deberá instalar "make", "gcc", "encabezados del kernel", "elementos esenciales de la compilación del kernel" y "git".
Puede instalarlos con el siguiente comando, en ** Ubuntu **:
```bash
sudo apt-get update
sudo apt-get install make gcc linux-headers-$(uname -r) build-essentials git
```
Si no se encuentra alguno de los paquetes anteriores, compruebe si su distribución los instala así.
##### Installation
```bash
PARA TODAS LAS DISTRIBUCIONES
git clone git@github.com:AntzMtz/rtlwifi_new.git
cd rtlwifi_new
make
sudo make install
```
##### How to disable/enable a Kernel module
```bash
sudo modprobe -r rtw_8723de         #para apagar la wifi 
sudo modprobe rtw_8723de ant_sel=2  #Para ensender la WIFI 
```
