# Configuracion entorno de trabajo de Linux

## Configuracion de git

1. Configurar usuario y correo
```bash
git config --global user.name "Usuario"
git config --global user.email "correo@gmail.com"
```
## Instalacion de Node JS y NPM

[Instalacion](https://github.com/nvm-sh/nvm#installing-and-updating)

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
```

Es posible, que necesites cerrar la terminal y abrirla de nuevo para poder ejecutar el siguiente comando:

```bash
nvm install lts
```

## Instalacion de docker

[Instalacion](https://docs.docker.com/engine/install/ubuntu/)

# Configuracion entorno de trabajo de Windows

# Git 
## Configuracion SSH 
1. Generar llave SSH
```bash
ssh-keygen -t rsa -b 4096 -C "tu@email.com"
```
2. Agregar la llave publica a GitHub

## Instalacion de ESP-IDF
1. Descargar el instalador desde la documentacion oficial de espressif [aqui](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/windows-setup.html)
2. Ejecutar el instalador.
3. Ejecute la powershell desde la terminal
4. Ubiquese en la carpeta \examples\get-started\hello_world
5. Puedes compilar el archivo con el comando:
```bash
idf.py build
```

## Instalacion de Node JS y NPM




