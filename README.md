# Yachay Box 🌞

**Tutor de inteligencia artificial que funciona sin internet, para escuelas rurales del Perú.**
*Yachay* significa «aprender» en quechua.

Proyecto presentado en **Hack4Edu 2026 · Reto 02 · Aprender sin conexión**.

## Equipo

- **Nicolay Alexander Galecio Sosa**, líder
- **Sandro Manuel Velasquez Chapa**
- **Paul Josue Damian Sarro**

Universidad María Auxiliadora (UMA), Perú.

## El problema

En el Perú, 6 de cada 10 escuelas públicas de primaria no tienen internet, y en el campo solo 1 de cada 4 hogares está conectado. Las herramientas de IA educativa dan por hecho una conexión que esos niños no tienen.

## La solución

Yachay Box lleva la IA **dentro de la escuela**: una laptop o mini-PC ejecuta el modelo **Qwen 2.5 (3B)** con **Ollama**. El modelo se descarga una sola vez y después todo funciona sin internet, sin costo de datos y sin que ninguna pregunta salga del aula.

| Pantalla | Para quién | Qué hace |
|---|---|---|
| Estudiante | Alumnos de 1.º a 6.º de primaria | Responde preguntas por grado y curso, en frases cortas, con estrellas de curiosidad y lectura en voz alta |
| Profe | Docente multigrado | Genera fichas de trabajo por grado, curso y contexto rural, con clave de respuestas, listas para imprimir |
| Panel del aula | Docente | Muestra qué cursos se consultan más, sin nombres de alumnos |
| Próximas mejoras | Jurado y aliados | Vista previa de lo que viene (marcada como maqueta) |

## Cómo probarlo

1. Instala **Ollama**: https://ollama.com
2. Descarga el modelo (una sola vez, con internet):
   ```
   ollama pull qwen2.5:3b
   ```
3. Permite que la página use Ollama (Windows, en la ventana de comandos):
   ```
   setx OLLAMA_ORIGINS "*"
   ```
   Luego cierra y vuelve a abrir Ollama.
4. Abre `app/index.html` con Chrome o Edge.
5. Apaga el WiFi: el aviso verde dice **«Sin internet · ¡funcionando!»** y Yachay sigue respondiendo.

## Pruebas realizadas

- **29 y 30 de octubre de 2026:** con el WiFi apagado, la IA respondió en las versiones 1 y 2.
- **Evaluación de la interfaz** en laptop (1366×768), proyector (1280×720) y celular (390×844): se encontraron 10 problemas y se corrigieron en la versión 3.

Siguiente paso: un **piloto en una escuela rural de Piura**, la primera prueba en campo con alumnos y docentes.

## Estructura del repositorio

```
app/index.html    Sistema Yachay Box (un solo archivo, funciona sin internet)
LICENSE           Licencia MIT
```

## Tecnología

HTML, CSS y JavaScript (sin dependencias externas) · Ollama · Qwen 2.5 (3B).
Tipografía Nunito (SIL Open Font License), incluida dentro del archivo.

## Licencia

Código abierto bajo licencia **MIT** (ver `LICENSE`).
