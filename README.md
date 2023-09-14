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



