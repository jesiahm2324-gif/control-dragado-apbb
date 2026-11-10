# Control de Operaciones de Dragado – APBB

Sistema de la **Administración Portuaria Bluff** (Bluefields, Nicaragua) para registrar, controlar y analizar la producción diaria de las dragas.
Es una App web instalable en iPhone, Android, tabletas y computadoras. Funciona sin internet y sincroniza con GitHub al reconectarse.

Dirección de la App: **https://jesiahm2324-gif.github.io/control-dragado-apbb/**

## Cómo funciona la seguridad
- Los datos se guardan **cifrados** (AES-256) en los *Issues* de este repositorio. Aunque el repositorio sea público, nadie sin un código de acceso puede leerlos.
- Cada usuario tiene un **código de acceso personal** y su **propia contraseña**, que nunca sale de su dispositivo.
- Cada registro va **firmado digitalmente**. Los permisos (Administrador, Operador o Consulta) se verifican en cada dispositivo, así que nadie puede modificar ni borrar registros sin autorización.
- GitHub conserva todas las versiones, y cada cambio queda en el historial de modificaciones de la App.

## Publicación (una sola vez)
1. En GitHub cree el repositorio **público** `control-dragado-apbb` (Issues activado, viene así por defecto).
2. Toque **Add file → Upload files**, arrastre **todo el contenido** de esta carpeta (son 11 archivos, todos al mismo nivel) y toque **Commit changes**.
3. Vaya a **Settings → Pages**. En *Branch* elija `main` y `/ (root)` y toque **Save**. En 1 o 2 minutos la App estará en la dirección de arriba.

## Llave de GitHub (token)
1. Abra https://github.com/settings/personal-access-tokens/new
2. *Token name*: `Dragado APBB`. *Expiration*: la mayor duración disponible (anote la fecha).
3. *Repository access*: **Only select repositories** → `control-dragado-apbb`.
4. *Permissions → Repository permissions → Issues*: **Read and write**.
5. Toque **Generate token** y copie la llave (empieza con `github_pat_`).

## Configuración inicial (administrador)
1. Abra la dirección de la App en su teléfono.
2. Toque **Configuración inicial del sistema**, escriba su nombre, pegue la llave y cree su contraseña.
3. La App le mostrará **su código de administrador**. Guárdelo en un lugar seguro: lo necesita para entrar desde otro equipo.
4. Las dragas Rama y Rama Kay y el proyecto Bluff-Pescanica (ancho de 30 m) se crean automáticamente.

## Instalar en el teléfono
- **iPhone:** abra la dirección en **Safari**, toque **Compartir** y luego **Agregar a pantalla de inicio**.
- **Android:** abra la dirección en **Chrome** y toque **Instalar App** (o el menú ⋮ → *Instalar aplicación*).
- **Computadora:** en Chrome o Edge, toque el ícono de instalar en la barra de direcciones.

## Agregar usuarios
En **Administración de usuarios → + Agregar usuario**, elija el tipo de usuario y entregue el código por un mensaje privado. La persona instala la App, pega el código y crea su contraseña.

## Si la llave de GitHub vence
Cree una nueva llave con los mismos permisos y genere códigos nuevos para los usuarios (**Reemplazar código**).

## Actualizaciones
Cuando se suban versiones nuevas de `index.html` y `sw.js` a GitHub, la App mostrará el aviso **"Hay una nueva versión – Actualizar"**.
