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
## Configuracion de git

1. Configurar usuario y correo
```bash
git config --global user.name "Usuario"
git config --global user.email "correo@gmail.com"
```
### Configuracion de SSH
1. Generar llave SSH
```bash
ssh-keygen -t rsa -b 4096 -C "tu@email.com"
```
2. Activar servidor de SSH
```bash
eval $(ssh-agent - s)
```
3. Incluir SSH
```bash
ssh-add ~/.ssh/id_rsa
```

## Instalacion de Node JS y NPM

[Instalacion](https://github.com/nvm-sh/nvm#installing-and-updating)

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
```

Es posible, que necesites cerrar la terminal y abrirla de nuevo para poder ejecutar el siguiente comando:

```bash
nvm install version-node-lts
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



