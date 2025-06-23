# 🧠 Personalizá tu terminal Ubuntu (ideal para Claude Code)

Esta guía te muestra cómo personalizar tu terminal Ubuntu con un mensaje de bienvenida, tabla de comandos útiles y pequeños detalles para mejorar tu productividad al usar asistentes como Claude Code o simplemente trabajar más cómodo desde la terminal.

> ✅ Compatible con Ubuntu o WSL (Windows Subsystem for Linux)

---

## ✨ ¿Qué vas a lograr?

- Un mensaje de bienvenida con tu nombre, fecha y ruta actual.
- Una tabla de comandos útiles cada vez que abrís la terminal.
- Un entorno más amigable para quienes usan la terminal todos los días.

---

## ⚙️ Pasos para configurar tu terminal

### 1️⃣ Editá tu archivo `.bashrc` o `.zshrc`

```bash
nano ~/.bashrc
```

Y pegá al final del archivo el siguiente bloque:

```bash
# 👋 Mensaje de bienvenida personalizado
echo ""
echo -e "\e[1;33m👋 ¡Hola, $USER! Bienvenido a tu terminal Ubuntu WSL 🚀"
echo -e "\e[1;36m📅 Hoy es: $(date)"
echo -e "\e[1;34m📂 Estás en el directorio: \e[0;33m$(pwd)"
echo -e "\e[1;35m💡 Comandos básicos que podés usar:"
echo ""

# 📋 Tabla de comandos
echo -e "\e[1;36m+----------------------+---------------------------------------------+"
echo -e "| Comando              | Descripción                                 |"
echo -e "+----------------------+---------------------------------------------+"
echo -e "| ls                   | Listar archivos y carpetas                  |"
echo -e "| cd /mnt/c/           | Entrar al disco C: de Windows               |"
echo -e "| pwd                  | Mostrar ruta actual                         |"
echo -e "| clear                | Limpiar la pantalla                         |"
echo -e "| nano archivo.txt     | Editar o crear un archivo de texto          |"
echo -e "| cat archivo.txt      | Ver contenido del archivo                   |"
echo -e "| bash script.sh       | Ejecutar un script                          |"
echo -e "+----------------------+---------------------------------------------+\e[0m"
echo ""
```

### 2️⃣ Aplicá los cambios

```bash
source ~/.bashrc
```

### 3️⃣ Opcional: Desactivar el mensaje diario de Ubuntu

```bash
touch ~/.hushlogin
```

---

## 🧩 ¿Por qué hacerlo?

Claude Code funciona exclusivamente desde terminal, y si tu entorno no está optimizado, la experiencia puede resultar frustrante. Esta pequeña mejora visual y funcional hace que trabajar con IA (y sin ella) sea mucho más fluido.

---

## 🧑 Autor

**Javier Morrón**  
*IA, automatización y propósito: ese es mi lenguaje.*

📩 Contacto: [javiermorron.com](https://javiermorron.com)

---

## 📜 Licencia

MIT License
