**Propósito**:

Construir un sistema de registro, refinamiento y aplicación del aprendizaje técnico.\
Evitar dispersión, redundancia y pérdida de contexto.\
Convertir la experiencia diaria en conocimiento estructurado y reutilizable.

***

**Estructura General del Vault**

Organizar el vault en cinco áreas:
- **Inbox** — Ideas y notas rápidas.
- **Registro Diario** — Registros diarios de aprendizaje.
- **Repositorio de Conceptos** — Conocimiento depurado. 
- **Área de Práctica** — Ejecución y experimentos.
- **Backlog de Aprendizaje** — Pendientes a investigar.
- **MOC (Map of Content)** — Índice estructural del sistema

Cada área cumple una función distinta dentro del ciclo cognitivo: capturar, estructurar, aplicar, revisar.

***

**1. Registro Diario**

**Función:** Capturar conocimiento en bruto y observaciones cotidianas.\
**Formato:**
```
YYYY-MM-DD.md
---

tags: [diario]

---

Tema: 

Aprendido: 

Confuso: 

Derivado: 
```
**Reglas:**

- No editar el mismo día; solo registrar hechos o aprendizajes.
- Usar lenguaje propio, sin copiar texto externo.
- Limitar a una entrada por día.
- Revisar semanalmente para extraer conceptos relevantes hacia el repositorio.

**Ejemplo:**

2025-10-20

Tema: Docker + Node

Aprendido: configuración de volúmenes para hot reload en desarrollo.

Confuso: diferencia entre bind mounts y named volumes.

Derivado: investigar docker compose profiles.

***

**2. Repositorio de Conceptos**

**Función:** Consolidar y explicar cada concepto aprendido.\
Cada archivo representa una unidad de conocimiento autocontenida.

**Formato base:**

```
---

title: <% tp.file.title %>

date: <% tp.date.now("YYYY-MM-DD") %>

tags: [<% tp.file.cursor() ? tp.file.cursor() : "concept" %>]

status: evergreen

related: []

---

# <% tp.file.title %>

 

## Explicación

Descripción en tus palabras.

 

## Ejemplo

Código o configuración mínima.

 

## Aplicación

Dónde y cómo se usa en tus proyectos.


## Referencias
- enlace a documentación
- notas relacionadas
```
**Reglas:**

- Nombrar los archivos con el concepto principal.
- Mantener independencia entre notas; vincular con \[\[ ]] solo si hay relación conceptual directa.
- Revisar periódicamente para actualizar con nueva comprensión.

***

**3. Área de Práctica**

**Función:** Transformar teoría en experiencia.\
Contiene fragmentos de código, configuraciones o proyectos de prueba.

**Estructura sugerida:**

```
/practice/
  ├─ ejemplo-1.md
  ├─ ejemplo-2.md
```

**Contenido mínimo:**

- Propósito del experimento.
- Pasos ejecutados.
- Resultado obtenido.
- Lecciones derivadas.

**Reglas:**

- Evitar copiar código sin comprensión.
- Documentar la intención antes de ejecutar.
- Registrar errores y correcciones.

***

**4. Backlog de Aprendizaje**

**Función:** Mantener control de los temas pendientes por investigar.
**Formato:**

```
# Backlog de Aprendizaje

## Tema

- [ ] Pendiente

- [ ] Pendiente
```

**Reglas:**

- Revisar semanalmente.
- Al completar un ítem, moverlo al registro diario con fecha.
- Priorizar por impacto en proyectos actuales.
---
**5. MOC (Map of Content)**

Mapa de Contenido: nodo central que agrupa y organiza notas relacionadas.  
Funciona como índice manual para navegar entre áreas conceptuales.  
Ejemplo:

```
/moc/
  ├─ index.md                → MOC raíz del sistema
  ├─ devops.md               → MOC temático
  ├─ backend.md              → MOC temático
  ├─ frontend.md             → MOC temático
  ├─ aprendizaje.md          → MOC metacognitivo

```


El MOC no contiene teoría, solo enlaces estructurados.  
Cada dominio (DevOps, Backend, Frontend, Arquitectura) mantiene su propio MOC.  
El MOC raíz vincula todos los secundarios.

**La cantidad depende de la densidad del conocimiento; el criterio es navegabilidad, no cantidad.**

***

**Ciclo Cognitivo**

1. **Captura** — Registrar lo aprendido cada día.
2. **Refinamiento** — Extraer y formalizar conceptos relevantes.
3. **Aplicación** — Experimentar mediante práctica dirigida.
4. **Revisión** — Integrar lo nuevo y depurar lo redundante.
5. Integración (en MOC) — Reflejar el estado global del conocimiento.

El ciclo mantiene el vault en evolución constante y evita acumulación de datos inútiles.

***

**Convenciones de Archivo y Enlace**

- Nombres en minúscula, guiones medios, sin espacios.
- Evitar redundancia de etiquetas; cada archivo debe tener máximo tres tags.
- Usar \[\[ ]] solo para relaciones conceptuales firmes.
- Crear alias para términos equivalentes.

***

**Uso en Obsidian**

- Activar **Daily Notes** para capturar registros.
- Usar **Dataview** o **Templater** para generar vistas dinámicas de conceptos y pendientes.
- Activar **Graph View** para observar conexiones entre áreas.
- Mantener sincronización local o en Git para versionar conocimiento.