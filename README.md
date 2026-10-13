# PM MVP

Una skill en español para pasar de una idea a un experimento, construir lo mínimo y revisarlo antes de probarlo con usuarios. Pensada para personas que no saben programar.

Se basa en tres prompts: **definir → construir → auditar**. También ayuda a interpretar resultados sin confundir interés, pago, uso y utilidad.

## Empezar

Después de instalar la skill en Codex, escribe:

```text
Usa $pm-mvp. Mi idea es [idea]. Quiero ayudar a [usuario].
Tengo esta evidencia: [evidencia o ninguna todavía].
Puedo contactar a [personas o canal].
Dispongo de [tiempo], [presupuesto] y [herramientas].
Ayúdame a definir y ejecutar el primer experimento.
```

También puedes pedir «Usa $pm-mvp para construir el MVP de esta ficha» o «Usa $pm-mvp para auditar este prototipo» y adjuntar el material correspondiente.

## Instalar en Codex

La carpeta instalable es [`skills/pm-mvp`](skills/pm-mvp). Contiene `SKILL.md` y la presentación opcional para Codex en `agents/openai.yaml`. No requiere API keys ni dependencias propias.

Para instalar desde GitHub, pide a Codex:

```text
Usa $skill-installer para instalar la skill de este repositorio: https://github.com/johny-Payeras/pm-mvp.
La ruta de la skill dentro del repositorio es skills/pm-mvp.
```

Para instalar manualmente, copia la carpeta completa `pm-mvp` que está dentro de `skills/` a `~/.agents/skills/`. Para limitarla a un proyecto, cópiala a `.agents/skills/` dentro de ese proyecto. En instalaciones que utilicen `~/.codex/skills/`, utiliza la ruta que indique su instalador. Si no aparece en el selector, reinicia Codex.

El formato y la instalación se documentan en la [guía oficial de skills de OpenAI](https://learn.chatgpt.com/docs/build-skills).

## Usar en otras IA

- **Si admiten Agent Skills:** importa la carpeta `skills/pm-mvp` siguiendo las instrucciones de esa herramienta. La compatibilidad depende de cada aplicación.
- **Si solo aceptan texto o adjuntos:** abre [`USAR-EN-OTRA-IA.md`](USAR-EN-OTRA-IA.md), copia su contenido como instrucciones o adjúntalo, y añade tu contexto. Es una versión autocontenida del flujo.
- **Si quieres un paso específico:** copia uno de los [tres prompts](prompts/01-definir.md). Los otros dos son [construcción](prompts/02-construir.md) y [auditoría](prompts/03-auditar.md).

Una IA sin herramientas puede redactar propuestas, formularios, prompts y código, pero no necesariamente crear archivos, conectar servicios o publicar. Debe distinguir lo realizado de lo pendiente. No se ha comprobado esta skill en todas las IA.

## Publicar este paquete en GitHub sin programar

1. Inicia sesión en GitHub y crea un repositorio llamado `pm-mvp` con visibilidad **Public**.
2. Si usas el ZIP, descomprímelo primero.
3. Usa la opción para subir archivos y arrastra **el contenido** de la carpeta `pm-mvp`, conservando sus subcarpetas. No subas solo el ZIP.
4. Guarda los cambios y comprueba que `README.md`, `skills/pm-mvp/SKILL.md` y `skills/pm-mvp/agents/openai.yaml` aparecen en las rutas indicadas.
5. Copia la URL real del repositorio para usarla con el instalador.

Publicar el repositorio distribuye las instrucciones; no instala la skill automáticamente ni publica los MVP que se creen con ella.

## Archivos

```text
pm-mvp/
├── README.md
├── LICENSE
├── USAR-EN-OTRA-IA.md
├── prompts/
│   ├── 01-definir.md
│   ├── 02-construir.md
│   └── 03-auditar.md
└── skills/
    └── pm-mvp/
        ├── SKILL.md
        └── agents/openai.yaml
```

`SKILL.md` es la fuente principal de instrucciones. Si lo modificas, actualiza también su versión de texto para otras IA. Los prompts son puntos de entrada independientes.

## Licencia

[MIT](LICENSE): permite reutilizar, modificar y distribuir el paquete conservando el aviso de licencia.
