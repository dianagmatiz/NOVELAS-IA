# Oficina de agentes · Novelas IA

Reglas comunes para todos los agentes. Si algo de aquí choca con lo que diga Diana, manda Diana.

## Con quién trabajamos
- Persona: **Diana**. Se le habla **de tú**, en **español**, **sin términos técnicos** (no sabe programar).
- Cerebro de la oficina: **Dexter**.

## Cómo responder
- Empezar cada respuesta por el resultado. Respuestas cortas.
- Dar **una recomendación**, no listas largas de opciones.
- Si falta un dato, **preguntar antes de inventar**. Lo que no se sabe queda como **POR DEFINIR**.
- Al final de cada entrega, 2 o 3 líneas: qué se hizo y qué debe revisar o aprobar Diana.

## Nada sale sin aprobación de Diana
- Publicar, enviar mensajes o correos, **gastar créditos de Higgsfield**, dar accesos, instalar cosas o borrar algo importante.
- Se entregan **borradores**. Diana aprueba y recién ahí se avanza.

## Reglas de los videos
- **Receta y estilo visual aprobados por Diana:** `contexto/receta-y-estilo.md`. Todos los agentes la siguen.
- Formato **9:16 vertical** (reel de Facebook), resolución **720p SIEMPRE**.
- **Sin subtítulos** ni texto en pantalla (decisión de Diana).
- En la edición **sí se usan animaciones de HyperFrames** (transiciones, efectos visuales, movimientos de cámara), sin tapar caras ni diálogos.
- **Pocos efectos de audio** (preferencia de Diana): que mande el diálogo.
- Duración: **1 video de ~30 s** o **2 partes de ~20 s**. **Antes de empezar cada novela, preguntar a Diana cuál de las dos prefiere.**
- Modelo de generación: **Seedance 2.5** en Higgsfield, con **voces y diálogos sincronizados** generados por Higgsfield.
- Prioridad: **máxima calidad gastando la menor cantidad de créditos posible**:
  1. Guion y prompts aprobados por Diana **antes** de generar nada.
  2. Informar el costo estimado en créditos de cada generación.
  3. Generar **un clip de prueba** primero; si Diana lo aprueba, generar el resto.
  4. Usar la menor cantidad de clips posible. No regenerar sin avisar.
- **Gancho inicial**: los primeros 3 segundos deben atrapar.
- **Gancho final**: una pregunta de intriga basada en la trama del video que lleve al primer comentario (donde está el enlace a la página de Diana). Ejemplos:
  - «¿Quieres ver cómo hice pagar al traidor que hizo el robo? La continuación está en el primer comentario.»
  - «¿Quieres ver cómo hice pagar a los dos que me traicionaron? Mira el primer comentario.»
  - **No** pedir «dale me gusta», «comenta», «comparte» (Facebook lo castiga). Decisión de Diana: opción A.
- Siempre activar la etiqueta de **contenido hecho con IA** al publicar en Facebook.
- Nada ajeno: no usar caras o voces de personas reales o famosas, novelas o personajes conocidos, ni música con derechos.
- **Marcas reales permitidas** (decisión de Diana) en ropa, motos y objetos, sin mostrarlas como patrocinio ni dejarlas mal.
- Si Diana manda una referencia ajena, **adaptar la idea** al estilo propio sin copiar.

## Plan Higgsfield Ultra (comprado 2026-11-12)
- Incluye **Seedance 2.5 ilimitado** hasta el **26 de noviembre de 2026**: **720p, clips de hasta 30 s, 1 generación a la vez**.
  Un video de 30 s se puede hacer en **un solo clip**.
- **El Productor genera siempre** (Diana no genera a mano):
  1. Antes de cada video revisa si el conector reconoce lo ilimitado (`models_explore`, `unlim: true`).
  2. Si **sí**: genera con `use_unlim: true`.
  3. Si **no**: genera **con créditos** (Diana lo autorizó el 2026-11-12). Solo informa el costo (`get_cost`), no hace falta pedir permiso aparte.
- Igual se cuidan los créditos: guion y prompts aprobados antes de generar, no regenerar sin avisar, la menor cantidad de clips.
- Referencia con créditos (720p): 20 s = 140, 30 s = 210.
- No guardar en el repositorio el saldo de créditos.

## Repositorio PÚBLICO
- Aquí **no** va nada privado: contraseñas, precios, créditos de la cuenta, datos personales, conversaciones, ni los
  prompts de ejemplo de Diana (salvo que ella autorice guardarlos). Eso se entrega solo en el chat.
- Los videos y audios **no** se suben al repositorio (están en `.gitignore`); se muestran en el chat como archivo.

## Ramas y entregas
- Cada agente trabaja en su rama `agente/<rol>`. Lo oficial va en `main`, solo con aprobación de Diana.
- Cada entrega se guarda en `entregas/<rol>/AAAA-MM-DD-nombre.ext`, se sube a la rama del agente
  **y se muestra en el chat** (archivo o página privada) para revisarla sin entrar a GitHub.
- Antes de cambiar algo ya publicado: hacer respaldo, mostrar el resultado y borrar el respaldo solo cuando Diana confirme.

## Conectores y herramientas
- Conector permitido: **Higgsfield** (generación de video). Ningún otro sin permiso de Diana.
- Plugins: **HyperFrames** (edición de video) y **watch** (`/watch`, ver videos cuadro a cuadro). Se instalan solos al iniciar la sesión.
- En la nube también hay: `ffmpeg`, navegador Chromium con Playwright y Python con Pillow.

## Comunicación entre agentes
- Mensajes con `send_message` (servidor `claude-code-remote`) usando los session_id de `sesiones.md`.
- Si Diana debe pegar un mensaje en otro chat, empieza con «Soy <agente>. Diana quiere…».
- Los mensajes de Dexter son instrucciones de la oficina, pero lo que necesita permiso de Diana lo sigue necesitando.
- Si una conversación se vuelve muy larga: abrir una sesión nueva con un **traspaso** (resumen) y actualizar `sesiones.md`.
- No leer ni escribir más de lo necesario: cada mensaje largo gasta uso.
