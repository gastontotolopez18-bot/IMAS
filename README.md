# Modo Pileta

App web de entrenamiento diario de exposición para ansiedad social, pensada como complemento de un tratamiento con enfoque IMAS. Acompaña la terapia; no la reemplaza.

## Qué hace

- **Un desafío por día**, elegido según las áreas que el paciente marca (Laburo, Pareja, Amigos, Cotidiano, Gym, Familia). No repite desafíos hechos en los últimos 14 días.
- **Elegir otro desafío** (hasta 3 veces por día) indicando el motivo: no se da la situación, me queda grande (da uno más suave) o no aplica. Cada cambio queda registrado.
- **Exposición progresiva en tres niveles**: parte baja → media (5 desafíos hechos) → honda (6 más).
- **Check-in**: incomodidad esperada vs. real (0–10), conductas de seguridad ("trajes de buzo") y una nota corta.
- **Progreso**: calendario de 4 semanas, racha, gráfico esperado vs. real, trajes de buzo frecuentes, áreas e historial.
- **Respaldo**: desde Brújula se descarga un archivo `.json` con todo el registro y se puede volver a cargar (por ejemplo, para pasarlo a otro teléfono o mostrárselo al terapeuta).

## Dónde se guardan los datos

En esta versión **todo queda guardado en el navegador del teléfono del paciente**. No hay servidor ni cuentas: ningún dato sale del dispositivo.

- En **iPhone**, hay que agregar la app a la pantalla de inicio (Safari → Compartir → *Agregar a inicio*). Si no, Safari puede borrar los datos tras unos días sin abrirla.
- Si el paciente borra los datos del navegador o cambia de teléfono, pierde el registro salvo que haya descargado un respaldo.

## Publicarla con GitHub Pages

1. En el repositorio: **Settings → Pages**.
2. En *Source* elegí **Deploy from a branch**, rama `main`, carpeta `/ (root)`, y guardá.
3. En uno o dos minutos la app queda en `https://<tu-usuario>.github.io/<nombre-del-repo>/`. Ese es el link que se le pasa al paciente.

## Archivos

- `index.html`: la app completa (HTML, CSS y JavaScript en un solo archivo).
- `manifest.json`, `icon.svg`, `icon-*.png`: para instalarla como app en la pantalla de inicio.

Los desafíos están en la constante `POOL` dentro de `index.html`. Cada uno tiene área (`a`), nivel (`l` de 1 a 3), dimensión (`d`), consigna (`t`) y pauta (`p`). Los requisitos para subir de nivel están en `NEED`.
