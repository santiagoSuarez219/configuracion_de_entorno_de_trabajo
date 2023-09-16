# Configuracion entorno de trabajo

## Instalando Python y PIP
```bash
sudo apt update
sudo apt -y upgrade
python3 -V
sudo apt install -y python3-pip
pip3 -V
sudo apt install -y build-essential libssl-dev libffi-dev python3-dev
```
## Instalacion de git
1. Abre WSL y ejecuta el siguiente comando
```bash
sudo apt-get install git-all
```
2. Una vez instalado, debes configurar tu usuario y correo electronico
```bash
git config --global user.name "Tu nombre"
git config --global user.email "Tu correo"
```
3. Para verificar que se haya instalado correctamente, ejecuta el siguiente comando
```bash
git --version
```

## Creacion de una cuenta en GitHub
1. Ingresa a la pagina oficial de GitHub
2. Crea una cuenta

## Configuracion de SSH
1. Abre WSL y ejecuta el siguiente comando
```bash
ssh-keygen -t rsa -b 4096 -C "tu@email.com"
```
2. Una vez ejecutado el comando, se te pedira que ingreses una ruta para guardar la llave, puedes dejar la ruta por defecto o bien, ingresar una ruta personalizada
3. Se te pedira que ingreses una contraseña, puedes dejarla en blanco o bien, ingresar una contraseña
4. Una vez creada la llave, debes ejecutar el siguiente comando
```bash
eval "$(ssh-agent -s)"
```
5. Ahora, debes agregar la llave a ssh
```bash
ssh-add ~/.ssh/id_rsa
```
6. Para obtener la llave, debes ejecutar el siguiente comando
```bash
cat ~/.ssh/id_rsa.pub
```
7. Copia la llave y pegala en tu cuenta de GitHub

## Instalacion de Node JS con NVM
1. Abre WSL y ejecuta el siguiente comando
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
```
2. Una vez instalado, debes cerrar y abrir WSL
3. Para verificar que se haya instalado correctamente, ejecuta el siguiente comando
```bash
nvm --version
```
4. Ahora, debes instalar la version de Node JS que desees, en este caso, se instalara la version 18.17.0
```bash
nvm install 18.17.0
```
5. Para verificar que se haya instalado correctamente, ejecuta el siguiente comando
```bash
node --version
```
6. Debes verificar la version de npm que se instalo, para ello, ejecuta el siguiente comando
```bash
npm --version
```
## Instalacion de Nest JS
```bash
npm install -g @nestjs/cli
```

## Instalacion de Angular CLI
```bash
npm install -g @angular/cli
```

### Creacion de un proyecto de angular
```bash
ng new my-project
```

### Correr un proyecto de angular en ambiente de desarrollo
```bash
ng serve
```
Lanzar servidor y abrir el navegador por defecto automáticamente:
```bash
ng serve -o
```
Angular utiliza por defecto el puerto 4200. Si quieres utilizar otro, podemos hacer:
```bash
ng serve --port=3500
```

Finalmente, si quieres analizar la versión de Angular y la versión de todas las dependencias instaladas, puedes hacer:
```bash
ng version
```
### Componentes en angular
```bash
ng g c components/component-name
```

### Servicios en angular
```bash
ng g s test-name
```

## Instalacion de docker
[Instalacion](https://docs.docker.com/engine/install/ubuntu/)

## Instalacion de ESP-IDF en Windows
1. Descargar el instalador desde la documentacion oficial de espressif [aqui](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/windows-setup.html)
2. Ejecutar el instalador.
3. Ejecute la powershell desde la terminal
4. Ubiquese en la carpeta \examples\get-started\hello_world
5. Puedes compilar el archivo con el comando:
```bash
idf.py build
```

## Instalacion de Docker en WSL
1. Descargar el instalador desde la documentacion oficial de docker [aqui](https://docs.docker.com/desktop/install/windows-install/)
2. Ejecutar el instalador.
3. Cuando ya tienes instalado Docker Desktop dentro de tus programas debes abrirlo y debes asegurarte que la opción “Use the WSL 2 based engine” está habilitada:

![01](https://i.imgur.com/COPXJpw.png)

4. Luego debes ir a la opción “Resources” y luego a “WSL Integration” y asegurarte que la opción “Enable integration with my default WSL distro” está habilitada:

![02](https://i.imgur.com/g20OhlL.png)

## Acceder a un servidor local hosteado en WSL 2.0 por medio de dispositivos de la misma red local
1. En la terminal de WSL vas a escribir lo siguiente y vas a copiar tu direccion IPv4
```bash
ifconfig
```
2. Luego ejecutaras la terminal de windows "PowerShell" como administrador
3. Dentro de la PS escribiras el siguiente comando
```bash
netsh interface portproxy add v4tov4 listenport=[Puerto del servidor] listenaddress=0.0.0.0 connectport=[Puerto del servidor] connectaddress=[Tu dirección IPv4]
```
4. Para finalizar, debemos habilitar estos puertos en el firewall de Windows
  1. Firewall de Windows Defender
  2. Configuracion Avanzada
  3. Reglas de entrada (Lateral izquierda)
  4. Nueva regla (Lateral derecha)
  5. Puerto
  6. TCP y puertos locales especificos (Puerto)
  7. Nombre: WSL
  8. Finalizar
5. ahora podremos acceder a nuestro servidor local desde cualquier dispositivo que este dentro de la misma red local. Cabe aclarar que la dirección IPv4 de la maquina WSL se cambia cada vez que reiniciamos el PC. Lo único de que debemos de hacer es volver a realizar los pasos 1, 2 y 3 con la nueva dirección IPv4 que se le asigno a la maquina WSL.

# Herramientas de IA y otras
## Generadores de codigo
1. [Phind](https://www.phind.com/)

## Creacion de paginas Web
1. [Dora](https://www.dora.run/ai)
2. [Wishpond](https://www.wishpond.com/ai/)



