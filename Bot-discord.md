Aquí te doy un ejemplo de cómo hacerlo utilizando un bot de Python con la biblioteca `discord.py`. Asegúrate de tener Python instalado en tu sistema antes de seguir estos pasos.

Paso 1: Configuración del Bot en Discord:
1. Ve a [https://discord.com/developers/applications](https://discord.com/developers/applications) y crea una nueva aplicación. Esto te dará acceso a un token que se utilizará para autenticar el bot en tu servidor de Discord.

2. Dentro de tu aplicación, ve a la sección "Bot" y presiona el botón "Add Bot" para convertir tu aplicación en un bot. Luego, copia el token del bot.

Paso 2: Creación del Bot en Python:
3. Crea un nuevo archivo Python, por ejemplo, `bot.py`, y utiliza un editor de texto o un IDE de Python para editarlo.

4. Instala la biblioteca `discord.py` si aún no la tienes instalada. Puedes hacerlo utilizando pip:
   ```
   pip install discord.py
   ```

5. Escribe el código para el bot Discord que imprimirá "Hola Mundo" en un canal de texto. Aquí tienes un ejemplo:

```python
import discord

# Crea un cliente de Discord
intents = discord.Intents.default()
intents.typing = False
intents.presences = False
client = discord.Client(intents=intents)

# Cuando el bot se conecta
@client.event
async def on_ready():
    print(f'Conectado como {client.user.name}')

# Cuando el bot recibe un mensaje
@client.event
async def on_message(message):
    if message.author == client.user:
        return

    if message.content == '!saludo':
        await message.channel.send('Hola Mundo')

# Inicia el bot con su token
token = 'TU_TOKEN_AQUÍ'  # Reemplaza con el token de tu bot
client.run(token)
```

Reemplaza `'TU_TOKEN_AQUÍ'` con el token de tu bot.

Paso 3: Ejecución del Bot:
6. Guarda el archivo `bot.py`.

7. Ejecuta el bot desde la línea de comandos:
   ```
   python bot.py
   ```

El bot se unirá a tu servidor de Discord y responderá con "Hola Mundo" cuando alguien escriba `!saludo` en un canal de texto.

Ten en cuenta que este es solo un ejemplo básico. Puedes personalizar la funcionalidad de tu bot y agregar más características según tus necesidades. Asegúrate de que tu bot tenga los permisos adecuados en tu servidor de Discord para enviar mensajes en los canales.
