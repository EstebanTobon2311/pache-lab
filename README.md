![Built with AI](https://img.shields.io/badge/Built%20with-AI-blue.svg)

# PACHE — Laboratorio de Análisis Colaborativo Heurístico
## *Protocolo de Análisis Colaborativo Heurístico con Validación Empírica*


## ¿Qué se va a hacer? / *What this lab is about*

Se replicará un experimento real que ocurrió entre el 5 y 7 de abril de 2026 desde un pueblo de Colombia durante Semana Santa.

Un solo operador humano — sin credenciales especializadas en geopolítica, sin presupuesto, usando solo prensa abierta e IA — construyó modelos predictivos (*predictive models*) sobre un evento geopolítico complejo que acertaron entre el **68% y el 92%** de sus predicciones ponderadas (*weighted predictions*).

**El objetivo NO es adivinar qué pasó.** Los hechos ya ocurrieron y están completamente documentados en este repositorio — incluyendo el *scoring* final en `contexto/commit_v4.md`.

**El objetivo ES** reproducir el proceso de razonamiento, registrar predicciones propias, y comparar cómo se llegó a ellas versus cómo llegó el operador original — con el mismo contexto disponible, pero sin haber leído el resultado aún.

> [!important]
> Todos los archivos están disponibles desde el inicio. La integridad del experimento no depende de ocultar información — depende de registrar las predicciones **antes** de leer el v4. El *template* de resultados tiene el orden correcto.

---

## Contexto del experimento original / *Original experiment context*

| Campo | Detalle |
|---|---|
| **Problema analizado** | Guerra EEUU-Israel vs Irán — plazo crítico del 6 de abril de 2026 |
| **Duración** | ~38 horas (domingo 5 Abr ~2pm → martes 7 Abr ~4am, hora Colombia) |
| **Instrumentos** | Claude Sonnet 4.6 (Anthropic) + Gemini (Google) |
| **Método** | PACHE — *Protocolo de Análisis Colaborativo Heurístico con Validación Empírica* |
| **Fuentes barridas** | CNN, BBC, Al Jazeera, Reuters, EFE, NPR, Times of Israel, Iran International, CFR, Arms Control Association, entre otras |
| **Repositorio original** | [github.com/ensayos-aaad/analisis-colaborativo-heuristico](https://github.com/ensayos-aaad/analisis-colaborativo-heuristico) |

El experimento produjo cuatro modelos predictivos sucesivos (*commits* v1 → v4), cada uno más refinado que el anterior. Los *commits* están en la carpeta `/contexto/` de este repositorio.

---

## Objetivos de aprendizaje / *Learning objectives*

Al completar esta práctica, el estudiante será capaz de:

1. **Aplicar razonamiento heurístico** (*heuristic reasoning*) para construir modelos predictivos sobre sistemas complejos a partir de información incompleta
2. **Identificar el rol del humano como sensor primario** en un sistema de cognición distribuida (*distributed cognition*) humano-IA
3. **Ejecutar triangulación dialéctica** (*dialectical triangulation*) entre fuentes y modelos con sesgos distintos: tesis + antítesis = síntesis (*Hegelian synthesis*)
4. **Ejercer metacognición activa** (*active metacognition*) — detectar y cuestionar sesgos propios y de la IA en tiempo real
5. **Diseñar predicciones falsificables** (*falsifiable predictions*) con criterios de verificación explícitos y *scoring* ponderado
6. **Conectar el proceso** con conceptos del curso: ACO (*Ant Colony Optimization*), grafos de decisión, *feedback loops*, búsqueda heurística (*heuristic search*)

---

## Resultados de aprendizaje esperados / *Expected learning outcomes*

| Al finalizar | Se deberá demostrar |
|---|---|
| **Proceso** | Descripción del ciclo completo: observación → modelo → predicción → verificación (*observation → model → prediction → verification*) |
| **Método** | Explicación de por qué la síntesis de dos modelos divergentes supera a cualquier modelo individual (*ensemble reasoning*) |
| **IA crítica** | Identificación de al menos un sesgo (*bias*) o error en los *outputs* de la IA cargada |
| **Conocimiento emergente** | Nombramiento de algo concreto aprendido del proceso que no estaba en ninguno de los *inputs* |
| **Conexión técnica** | Al menos una conexión explícita con un algoritmo o estructura de datos del curso |

---

## Instrucciones / *Step-by-step instructions*

### Antes de empezar — la única regla

> [!caution]
> **No leer el `commit_v4.md` hasta haber completado las Secciones 2 y 3 del *template*.**  
> Todos los archivos son públicos y accesibles. No hay trampa posible — solo proceso honesto o proceso deshonesto. El valor del ejercicio está en registrar el razonamiento antes de ver el *ground truth*.

---

### Paso 1 — *Fork* del repositorio

1. Hacer *fork* de este repositorio a la cuenta personal de GitHub
2. Crear una carpeta con el nombre del estudiante dentro de `/resultados/`:  
   `resultados/nombre-apellido/`
3. Copiar el archivo `resultados/resultados_template.md` a esa carpeta y renombrarlo:  
   `resultados/nombre-apellido/nombre-apellido_resultados.md`

---

### Paso 2 — Cargar los *commits* en Claude (modo incógnito, sin cuenta)

> [!warning]
> **¿Por qué modo incógnito sin cuenta? / *Why incognito without account?***  
> Para garantizar *zero context* — que Claude no tenga memoria de sesiones anteriores ni contexto personal. El experimento original fue diseñado así y la replicación debe mantener esa condición.

1. Abrir **claude.ai** en una ventana de incógnito (`Ctrl+Shift+N` / `Cmd+Shift+N`)
2. Usar Claude **sin iniciar sesión** (versión gratuita disponible)
3. Copiar el contenido completo de `contexto/commit_v1.md` y pegarlo como primer mensaje
4. Leer la respuesta — **no hacer preguntas todavía**
5. Continuar con `commit_v2.md` y luego `commit_v3.md` en mensajes sucesivos
6. **Detenerse aquí. El v4 se leerá después.**

En este punto se tiene el mismo contexto que tenía el operador original la noche del 5 de abril, antes de que ocurrieran los eventos del 6.

---

### Paso 3 — Construir predicciones propias (*build your own predictions*)

Con el contexto v1 + v2 + v3 cargado, hacer a Claude **esta pregunta exacta**:

> *"Basándote en todo el contexto que tienes, ¿cuáles son tus predicciones para el 6 de abril de 2026? Dame predicciones específicas con probabilidades asignadas para cada una."*

Luego preguntar:

> *"¿Cuál es la predicción más falsificable — la que más claramente puede resultar verdadera o falsa?"*

**Registrar en el *template*** antes de continuar:
- Las predicciones que Claude generó
- Las probabilidades asignadas
- La predicción más falsificable identificada
- Algo que no convenza o que se cambiaría

---

### Paso 4 — El ancla de razonamiento / *The reasoning anchor*

Antes de ver el v4, responder en el *template*:

- ¿Hay algo en las predicciones de Claude que no convence? ¿Por qué?
- Si se tuviera que cambiar una probabilidad, ¿cuál sería y a qué valor?
- ¿Se detectó algún sesgo (*bias*) en los *outputs*?

Este paso no tiene respuesta correcta. Es donde el razonamiento propio entra como sensor primario del sistema.

---

### Paso 5 — Leer el v4 y comparar / *Read v4 and compare*

1. Abrir `contexto/commit_v4.md`
2. Leer el *scoring* final y los hechos verificados del 6 de abril
3. Completar la sección de comparación en el *template*

---

### Paso 6 — Reflexión y entrega / *Reflection and submission*

1. Completar todas las secciones de reflexión en el *template*
2. Subir el archivo al *fork* personal (este será la evidencia de trabajo de este laboratorio)

> [!caution]   
> El siguente procedimiento se realizara despues (cuando lo indique el profesor). Abstengase por ahora de seguirlo.
> 
> 3. Abrir un *Pull Request* al repositorio original con el nombre:  
   **`[Nombre del estudiante] — Replicación PACHE`**

---

## Estructura de entrega / *Submission structure*

```
resultados/
└── nombre-apellido/
    └── nombre-apellido_resultados.md    ← completado con todas las secciones
```

---

## Criterios de evaluación / *Evaluation criteria*

| Criterio | Peso | Descripción |
|---|---|---|
| Predicciones registradas antes del v4 | 30% | Evidencia de proceso en orden. Las predicciones **no necesitan ser correctas** — necesitan existir antes de la comparación |
| Calidad del ancla de razonamiento (Paso 4) | 25% | ¿Se detectó algo que Claude no vio? ¿Se cuestionó una probabilidad con argumento propio? |
| Comparación honesta con el *scoring* original | 20% | ¿En qué convergió o divergió del operador original? ¿Por qué? |
| Conocimiento emergente (*emergent knowledge*) | 15% | Algo concreto aprendido del proceso que no estaba en ninguno de los *inputs* |
| Conexión con estructuras de datos | 10% | Al menos una conexión explícita con un algoritmo o estructura del curso |

> [!important]
> **Importante:** El porcentaje de acierto de las predicciones vs el *ground truth* **no cuenta para la nota**. Un estudiante que acertó el 40% pero ejerció *metacognición activa* y documentó su razonamiento obtiene mejor nota que uno que acertó el 90% sin reflexión.

---

## Conexión con estructuras de datos / *Connection to data structures*

| Concepto del curso | Cómo aparece en el PACHE |
|---|---|
| **ACO — *Ant Colony Optimization*** | Cada sesión deja "feromona" (contexto acumulado). El modelo óptimo emerge sin planificación central — exactamente como una colonia de hormigas |
| **Grafo dirigido** (*directed graph*) | Los *commits* son nodos. Cada nuevo *commit* es una arista que actualiza el estado del sistema |
| **Árbol de decisión** (*decision tree*) | Cada predicción es un nodo hoja. Las probabilidades son los pesos de las ramas |
| ***Feedback loop* — lazo cerrado** | El ciclo predicción → hecho real → corrección → nueva predicción es un sistema de control de lazo cerrado (*closed-loop control*) |
| **Búsqueda heurística** (*heuristic search*) | El protocolo completo es búsqueda heurística: no explora todo el espacio, usa señales locales para converger al resultado |
| ***Ensemble method*** | La síntesis hegeliana (Modelo C) es un *ensemble* de dos modelos débiles que supera a cualquiera individual — mismo principio que *Random Forest* |

---

## Referencia conceptual / *Conceptual reference*

> [!tip]
> *"The Big Short"* — Michael Lewis / Adam McKay (2015).  
> * Misma estructura: datos públicos disponibles para todos + método riguroso + tolerancia a la incertidumbre = hipótesis probabilística accionable (*actionable probabilistic hypothesis*).  
> * La diferencia es que Michael Burry necesitó meses, equipo y capital.  
> * Este experimento replicó la estructura del razonamiento en una tarde, desde un pueblo de Colombia, con acceso libre a internet.

---

## Declaración de autoría / *Authorship declaration*

Los *commits* de este repositorio fueron redactados por Claude Sonnet 4.6 (Anthropic) siguiendo instrucciones explícitas del operador humano. El crédito intelectual del diseño metodológico corresponde al operador. Las IAs fueron instrumentos del método, no agentes autónomos.

De conformidad con las políticas de uso responsable de IA, ningún documento debe citarse como trabajo de autoría humana sin declarar que su redacción fue ejecutada por un modelo de lenguaje.

---

* Tiempo estimado / *Estimated time*: 90–120 minutos  
* Práctica diseñada como experimento de replicación metodológica.  
* Los hechos del 6 de abril de 2026 ya ocurrieron. El valor del ejercicio está en el proceso, no en el resultado.


> [!important]
> Este material fue desarrollado con apoyo de herramientas de IA como asistente de redacción y estructuración. El contenido ha sido supervisado, validado y refinado por intervención humana para garantizar su precisión técnica y coherencia pedagógica. No obstante, pueden haber errores.