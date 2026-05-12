# GitHub Repo Setup — Step-by-Step Instructions

Estas instrucciones te guían a través de la creación del repo `pmilet/ai-ddd-mainframe-modernization-patterns` con el contenido v0.1 publicado como release. Tiempo total estimado: 20-30 minutos.

---

## Prerequisites

- Cuenta GitHub activa bajo el usuario `pmilet`
- Los siguientes archivos preparados (ya generados en esta sesión):
  - `README.md`
  - `LICENSE`
  - `CHANGELOG.md`
  - `pattern-catalog-v10.md` (renombrar a `catalog.md` al subir)
  - `AI-Assisted-Domain-Driven-Mainframe-Modernization.pdf`
  - `AI-Assisted-Domain-Driven-Mainframe-Modernization.epub`

---

## Paso 1 — Crear el repo (5 minutos)

1. Navega a https://github.com/new (logueado como `pmilet`)
2. **Repository name:** `ai-ddd-mainframe-modernization-patterns`
3. **Description:** `Twenty-eight patterns where Domain-Driven Design meets blackfield mainframe modernization. A pattern catalog from Project Rosetta.`
4. **Visibility:** Selecciona **Public**
5. **Initialize this repository with:**
   - ❌ NO marques "Add a README file" (vamos a subir uno custom)
   - ❌ NO marques "Add .gitignore"
   - ❌ NO marques "Choose a license" (vamos a subir uno custom)
6. Click **Create repository**

GitHub te mostrará la pantalla "Quick setup" con instrucciones de git remote. Ignora esa pantalla por ahora — vamos a subir archivos via web UI para v0.1 launch (más rápido que clone+commit+push).

---

## Paso 2 — Subir los archivos base (5 minutos)

En la pantalla del repo recién creado:

1. Click el botón **uploading an existing file** (link azul en la sección "Quick setup")
2. Drag & drop los siguientes archivos:
   - `README.md`
   - `LICENSE`
   - `CHANGELOG.md`
   - `catalog.md` (renombrar `pattern-catalog-v10.md` a `catalog.md` antes de subir)
3. **Commit message:** `Initial repo content: README, LICENSE, CHANGELOG, catalog`
4. Selecciona **Commit directly to the main branch**
5. Click **Commit changes**

Espera ~10 segundos. La página se refresca y muestra los 4 archivos en root.

---

## Paso 3 — Verificar el README se renderiza bien (2 minutos)

Vuelve a la página principal del repo (`github.com/pmilet/ai-ddd-mainframe-modernization-patterns`). Scroll down para ver el README renderizado.

**Verifica:**
- ✅ Título principal aparece correctamente
- ✅ Status badge muestra "draft v0.1"
- ✅ License badge muestra "CC BY 4.0"
- ✅ Tabla de downloads tiene 3 filas (PDF / EPUB / Markdown)
- ✅ Links internos a `catalog.md` y `LICENSE` funcionan
- ✅ Tabla de Status muestra 15 / 9 / 4
- ✅ Sección "Who this is for" se ve correctamente
- ✅ Cita en bottom usa formato APA-like

**Si algo no se ve bien:** edita el archivo correspondiente directamente desde GitHub UI (botón ✏️ en cada archivo).

---

## Paso 4 — Crear el primer Release v0.1 (10 minutos)

Este paso adjunta el PDF y EPUB al repo como artefactos descargables versionados.

1. En la página principal del repo, mira el panel derecho. Encontrarás una sección **"Releases"** con texto "No releases published — Create a new release".
2. Click **Create a new release**

En la pantalla de creación del release:

3. **Choose a tag:**
   - Click el dropdown "Choose a tag"
   - Escribe `v0.1` en el textbox
   - Click **+ Create new tag: v0.1 on publish**

4. **Target:** Deja `main` (el default)

5. **Release title:** `v0.1 — Initial draft`

6. **Release description:** Copia y pega exactamente lo siguiente:

```markdown
First public release of the catalog. Draft published in-progress to gather feedback while review continues.

## What's in v0.1

- **28 patterns** organised across 4 Parts (Strategic Recovery, Tactical Generation, Verification, Governance)
- **7 antipatterns** naming the failure modes the patterns are built against
- ~41,000 words of body content

## Status distribution

- **15 patterns** marked *working* (validated inside the Rosetta prototype)
- **9 patterns** marked *in progress* (in active construction)
- **4 patterns** marked *next* (designed from validated principles but not yet built)

## Honest disclosure

No pattern has yet been validated against a real customer engagement. That's the next phase, not yet started. Validation to date is inside the Rosetta prototype.

## Known gaps in this draft

- 24 visual placeholders (figures, illustrations, code samples, tables) marked in-text but not yet rendered as production graphics
- 3 code samples sketched as descriptions but not yet implemented in real Roslyn-rendered C#
- 2 reference tables described but not yet rendered

These gaps will close in subsequent releases. The textual content is review-ready as it stands.

## Available formats

- **PDF** (157 pages, 3.4 MB) — print-friendly, attached below
- **EPUB** (3.4 MB) — e-reader format, attached below
- **Markdown source** — `catalog.md` in the repo

## Feedback welcome

Open an issue for specific corrections or suggestions. Discuss broader topics on LinkedIn under the LegacyLabs name.

See [CHANGELOG.md](https://github.com/pmilet/ai-ddd-mainframe-modernization-patterns/blob/main/CHANGELOG.md) for full details.
```

7. **Attach binaries:**
   - Scroll down a la sección **"Attach binaries by dropping them here or selecting them"**
   - Drag & drop:
     - `AI-Assisted-Domain-Driven-Mainframe-Modernization.pdf`
     - `AI-Assisted-Domain-Driven-Mainframe-Modernization.epub`
   - Espera a que ambos archivos se uploadeen (~30-60 segundos cada uno)

8. **Pre-release checkbox:**
   - ❌ NO marques "Set as a pre-release"
   - ✅ MARCA "Set as the latest release" (debería estar marcado por default)

9. Click **Publish release**

---

## Paso 5 — Verificar el release (3 minutos)

GitHub te redirige a la página del release recién creado. URL será:
`github.com/pmilet/ai-ddd-mainframe-modernization-patterns/releases/tag/v0.1`

**Verifica:**
- ✅ Título "v0.1 — Initial draft" se muestra
- ✅ Descripción renderiza correctamente con markdown formatting
- ✅ Sección "Assets" muestra los 3 elementos:
  - `AI-Assisted-Domain-Driven-Mainframe-Modernization.pdf` (con tamaño ~3.4 MB)
  - `AI-Assisted-Domain-Driven-Mainframe-Modernization.epub` (con tamaño ~3.4 MB)
  - `Source code (zip)` (auto-generated por GitHub)
  - `Source code (tar.gz)` (auto-generated por GitHub)

**Prueba los downloads:**
- Click en el PDF link, debería empezar download
- Click en el EPUB link, debería empezar download
- Abre el PDF descargado y verifica que rendea correctamente

---

## Paso 6 — Verificar links del README (2 minutos)

Vuelve a la página principal del repo. En el README, prueba los download links:

- 📄 PDF link → debería abrir la página del release `v0.1`
- 📱 EPUB link → debería abrir la página del release `v0.1`
- 📝 Markdown source link → debería abrir `catalog.md` en GitHub viewer

Si los links están broken, edita el README — los URLs apuntan a `/releases/latest`, que GitHub resuelve automáticamente al release más reciente.

---

## Paso 7 — Configuración optional (5 minutos)

Estas configuraciones son opcionales pero refinan la presentación:

### 7a — About section (panel derecho)

En la página principal del repo, click el ⚙️ icono junto a "About" en el panel derecho:

- **Description:** `Twenty-eight patterns where Domain-Driven Design meets blackfield mainframe modernization. A pattern catalog from Project Rosetta.`
- **Website:** Deja vacío por ahora (o añade tu LinkedIn profile)
- **Topics:** Añade tags para SEO:
  - `ddd`
  - `domain-driven-design`
  - `mainframe`
  - `modernization`
  - `cobol`
  - `cics`
  - `ai-assisted`
  - `software-architecture`
  - `patterns`
  - `legacy-modernization`

Click **Save changes**.

### 7b — Issue templates (opcional, recomendado)

Si quieres feedback estructurado, crea templates para Issues:

1. Navigate to `Settings` → `Features` → **Issues** → **Set up templates**
2. Add a template called **"Pattern feedback"** con campos:
   - Pattern number
   - Specific concern
   - Suggested change
3. Save

Esto guía a los readers a dar feedback más actionable.

### 7c — Discussions (opcional)

Si quieres una surface para discusión más informal:

1. `Settings` → `Features` → ☑️ **Discussions**
2. Esto activa la pestaña "Discussions" en el repo

Recomendado para preguntas conceptuales que no son issues específicos.

---

## Paso 8 — Confirmación final

Tu repo está live en:

**https://github.com/pmilet/ai-ddd-mainframe-modernization-patterns**

El release v0.1 está descargable desde:

**https://github.com/pmilet/ai-ddd-mainframe-modernization-patterns/releases/tag/v0.1**

Tiempo total invertido: ~25-30 minutos.

---

## Siguiente paso después del setup

Una vez el repo está live, los siguientes assets que recomiendo preparar (en orden):

1. **LinkedIn launch post** — Beck-shaped, 3 párrafos, link al primer comentario apuntando al repo
2. **LinkedIn newsletter article** — versión long-form bajo LegacyLabs (1,500-2,500 palabras)
3. **DM templates personalizados** — para outreach a Tune, Alcaraz, Brandolini, Majors, Beck, Böckeler

Avísame cuando hayas completado el setup (idealmente con el URL del repo público), y procedemos con los launch assets.

---

## Si algo sale mal

**Problemas comunes y soluciones:**

| Problema | Solución |
|----------|----------|
| El README no rendea bien | Edita directly desde GitHub UI (botón ✏️), corrige el markdown, commit |
| El PDF no aparece en el release | Tamaño puede haber excedido limit (200 MB es el max por archivo). El nuestro son 3.4 MB, no debería ser issue |
| Los download links del README van a 404 | Verifica que el release v0.1 está realmente publicado (no draft) |
| El repo se ve como private aunque marqué public | `Settings` → `General` → scroll down a "Danger Zone" → "Change visibility" → "Make public" |

Cualquier otra duda durante el setup, escríbeme directamente y resolvemos.
