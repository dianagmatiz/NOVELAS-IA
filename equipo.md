# Equipo

| Agente | Sesión | Rama | Qué hace | Qué pasarle |
|---|---|---|---|---|
| Dexter | Dexter | `claude/new-session-3ps98d` | Cerebro: arma y mejora la oficina | Cambios a la oficina, problemas |
| Coordinador | AGENTE · Coordinador | `agente/coordinador` | Ordena ideas y pendientes, reparte el trabajo | Ideas nuevas, datos pendientes, dudas |
| Guionista | AGENTE · Guionista | `agente/guionista` | Escribe el capítulo (1×30 s o 2×20 s) | Idea de la novela + formato elegido |
| Gancho | AGENTE · Gancho | `agente/gancho` | Gancho de los 3 primeros segundos y gancho final | Guion borrador |
| Prompts | AGENTE · Prompts | `agente/prompts` | Prompts para Seedance 2.5 según los ejemplos de Diana | Guion aprobado con ganchos |
| Productor Higgsfield | AGENTE · Productor Higgsfield | `agente/productor-higgsfield` | Genera los clips en Higgsfield cuidando créditos | Prompts aprobados |
| Editor | AGENTE · Editor | `agente/editor` | Arma el reel final 9:16 con HyperFrames | Clips generados + guion |
| Publicación Facebook | AGENTE · Publicación Facebook | `agente/publicacion-facebook` | Texto del reel, hashtags, portada, revisión de reglas | Reel final + guion |

## Flujo típico
1. Diana le cuenta una idea al **Coordinador**, que le pregunta: ¿1×30 s o 2×20 s?
2. **Guionista** escribe → **Gancho** ajusta inicio y final → **Prompts** arma los prompts. Diana aprueba guion y prompts.
3. **Productor Higgsfield** avisa el costo, genera un clip de prueba y, con el visto bueno, el resto (720p).
4. **Editor** une todo con HyperFrames → **Publicación Facebook** prepara el texto. Diana revisa y publica.
