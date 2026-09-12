# Kairos - Disponibilidad de citas

Página pública que muestra la disponibilidad de citas (slots libres, ocupados y restringidos).

## Despliegue en GitHub Pages

La página se publica desde la rama `main` en la raíz del repo.

1. Subir cambios a `main`.
2. Activar Pages: Settings → Pages → Source: "Deploy from a branch", rama `main`, carpeta `/ (root)`.
3. URL: `https://sajaldi.github.io/kairos-disponibilidad/`

## Cómo funciona

- Consulta la Realtime Database de Firebase por REST:
  - `https://kairos-112e3-default-rtdb.firebaseio.com/citas.json`
  - `https://kairos-112e3-default-rtdb.firebaseio.com/restricciones.json`
- Requiere que las reglas de la base permitan lectura pública de los nodos `citas` y `restricciones`.
- Horarios: 07:00 a 19:00 en bloques de 30 min.
- Estados por slot: Libre / Ocupado / Restringido.
- Se actualiza automáticamente cada 60 segundos y con el botón "Actualizar horarios".