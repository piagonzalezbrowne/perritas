# 🐕🐶 Lisa & Caluga — Cómo publicar e instalar la app

## Paso 1: Subirla a GitHub Pages (gratis, ~5 minutos)

Ya tienes cuenta de GitHub (piagonzalezbrowne), así que:

1. Entra a github.com y crea un repositorio nuevo → nómbralo `perritas` → **Public** → Create repository.
2. En el repo, haz clic en **"uploading an existing file"** y arrastra estos 5 archivos:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon-192.png`
   - `icon-512.png`
3. Commit changes.
4. Ve a **Settings → Pages** → en "Source" elige **Deploy from a branch** → branch `main`, carpeta `/ (root)` → Save.
5. Espera 1-2 minutos. Tu app quedará en:
   **https://piagonzalezbrowne.github.io/perritas/**

Ese es el link que le mandas a tu hermano.

## Paso 2: Instalarla en el celular de tu hermano

**Android (Chrome):**
1. Abrir el link en Chrome.
2. Aparecerá un aviso "Agregar a pantalla de inicio" (o menú ⋮ → **Instalar aplicación**).
3. Listo: queda con ícono de patita como cualquier app.
4. Al abrirla, tocar **"Activar notificaciones"** y aceptar.

**iPhone (Safari):**
1. Abrir el link en Safari.
2. Botón compartir □↑ → **"Agregar a pantalla de inicio"**.

## Sincronización entre teléfonos 🔄

La app está conectada a una base de datos gratuita (Firebase, proyecto "pewitas" en tu cuenta de Google). Eso significa:

- **Todos los que instalen la app desde el mismo link ven y marcan lo mismo**, al instante: actividades, radar de pipí, agua, registros de caca, todo.
- No hay que crear cuentas ni iniciar sesión — basta con abrir el link.
- Si alguien queda sin internet un rato, la app sigue funcionando y se sincroniza al reconectarse.
- Nota de seguridad: la base está en "modo de prueba", abierta para quien tenga el link. Para una agenda de perritas el riesgo es mínimo, pero no guardes ahí información sensible. Firebase puede pedirte renovar el modo de prueba pasados unos meses (te llega un correo); se extiende con un clic en la pestaña "Reglas" de Realtime Database.

## Cómo funcionan las notificaciones (importante ⚠️)

- **Android:** las notificaciones llegan mientras la app esté abierta o en segundo plano reciente. Recomendación para tu hermano: dejar la app abierta durante el día (aunque esté con la pantalla apagada o usando otras apps, Chrome suele mantenerla un buen rato). Si el teléfono la "mata" por ahorro de batería, basta con abrirla de nuevo.
  - Tip: en Ajustes del teléfono → Batería → poner Chrome (o la app instalada) **sin restricciones** ayuda mucho.
- **iPhone:** las notificaciones de apps web son más limitadas; la app igual sirve como agenda con el radar de pipí visible al abrirla.

## Qué guarda la app

- Todo se guarda en el teléfono automáticamente (aunque la cierre o se quede sin internet).
- El registro dura **de lunes a lunes**: cada lunes se limpia la semana anterior y parte de cero.
- La pestaña **🗓 Semana** muestra el resumen de cada día: actividades completadas y las cacas de Lisa en cada paseo (normal / blanda / no hizo).

## Cómo funcionan las alertas

- Las alertas aparecen **solo cuando toca hacer algo** (hora cumplida, pipí vencido, ventana de caca abierta, agua vencida). El resto del tiempo se ven como chips pequeños arriba.
- Cada alerta tiene dos botones: hacerla ✔ o **"Ahora no · 15 min"** para aplazarla.
- Los mensajes vienen "en voz" de las pewitas para que den ganas de responder 🥺
- Pipí: aviso cada **2 horas** (solo entre 8:00 y 22:00).
- Caca: se predice según cuánto suele demorar Caluga después de comer, jugar o pasear. Usa valores típicos de cachorra hasta juntar 4 registros de cada señal, y ahí pasa a usar los suyos. Se ve el detalle en la sección "🔮 Predicción de caca".
- Si una comida se marca a una hora distinta de la programada, la predicción se ajusta a esa hora real.

## Editar horarios

Si cambia algún horario, edita el archivo `index.html` en GitHub (lápiz ✏️): la agenda está al principio del `<script>`, en la lista `AGENDA`. Cambias la hora o la nota, guardas, y en un par de minutos la app se actualiza sola.
