# El Libro del Despertar — Expansion Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Expand all 18 existing files and write 1 new book (L17) based on the approved design in `docs/plans/2026-03-13-expansion-design.md`.

**Architecture:** Each task is one book expansion, executed by a parallel agent. Each agent reads the current book file, the design doc, and the CLAUDE.md, then rewrites the file integrating all approved additions while preserving every existing verse, parábola, salmo, décima, and diálogo. The new L17 is written from scratch. After all books are expanded, a final pass updates CLAUDE.md, regenerates the compilation, and regenerates DOCX/PDF.

**Tech Stack:** Markdown files, python-docx (DOCX generation), pandoc+tectonic (PDF generation)

**Key Reference Files:**
- Design doc: `docs/plans/2026-03-13-expansion-design.md`
- Project spec: `CLAUDE.md`
- Book files: `libros/00-prologo-*.md` through `libros/17-epilogo-*.md`
- DOCX generator: `generate_docx.py`

---

## Phase 1: Tier 1 Critical Expansions (parallel)

These 4 tasks have no dependencies and run simultaneously.

### Task 1: Write NEW Libro 17 — De la Profecía y el Enemigo

**Files:**
- Create: `libros/17-de-la-profecia-y-el-enemigo.md`

**Context:** This is a brand new book. Read the full design in `docs/plans/2026-03-13-expansion-design.md` Section 3 and the two design files: `diseno-libro-17.md` and `libros/17-de-la-profecia-y-el-enemigo-DISEÑO.md`. Also read `CLAUDE.md` for the 7 axioms, literary register rules, décima espinela rules (ABBAACCDDC, octosyllabic), and quality criteria.

**Requirements:**
- 27-28 numbered versículos in 5 thematic blocks
- Parábola: "De los tres hombres que esperaban" (David, Yusef, Thomas at border crossing, 3 AM)
- Salmo: "Del que no tiene bando" (first person, caught between warring certainties)
- Décima: "De la guerra santa" (ABBAACCDDC, verified octosyllabic with sinalefa rules)
- Diálogo: "El Profeta y el General"
- 3 bienaventuranzas (heredar odio, honrar muertos sin escudo, reparar grieta)
- Zarza: burns in no-man's-land, in the hand that pulls a child from rubble
- 3 AM motif: the border crossing at 3 AM
- Mesa motif: sharing tea at the crossing
- Epígrafe: *"No hay guerra santa. Nunca la hubo. Lo que hubo fue miedo con escrituras en la mano."*
- Tone: Most incendiary after L8. Compassionate with persons, implacable with systems. No side.
- Follow markdown format conventions from existing books (# title, ## subtitle, **N.** verses, ### sections, --- separators)

**Verification:** All 8 quality criteria from CLAUDE.md must pass. Décima must be metrically verified.

---

### Task 2: Expand L13 — De la Justicia y el Extranjero (+ eschatology)

**Files:**
- Modify: `libros/13-de-la-justicia-y-el-extranjero.md`

**Context:** Read current file + design doc Section 2 (L13) + CLAUDE.md. This book gets the heaviest eschatological expansion.

**Additions (preserve all existing content, integrate new material):**

1. **P13.1 (CRITICAL):** Insert 4-6 new eschatological versículos between current v.11 and v.12. Topics: idolatry of the map, sacred text as property deed, the two griefs that can't look at each other, the prophet who doesn't choose sides between legitimate sufferings, sacred texts weaponized for displacement.
2. **P13.2:** Versículo on instrumentalized suffering — sacred pain turned into shield.
3. **P13.3:** New parábola: "De las dos abuelas" — Fátima and Miriam, each side of a wall, baking bread before dawn. They meet at a hospital/crossing. No words. One offers bread. The other accepts. End with image, no moraleja.
4. **P13.4:** New salmo: "De la tierra disputada" — the land speaks in first person. Born in a land with two names. *"Yo no quiero una tierra prometida. Quiero una tierra compartida."*
5. **P13.5:** Expand diálogo with hardest question: *"¿Y si los míos también son culpables?"*
6. **P13.6:** Bienaventuranza: *"Bienaventurado el que llora por el hijo del enemigo, porque ese ha entendido que no hay hijos del enemigo — solo hay hijos."*
7. **P13.7:** Versículo on mass incarceration.
8. **P13.8:** Versículo on activist exhaustion.
9. **P13.9:** Insert 3 AM motif (currently missing from this book).

**Renumber all versículos** after insertions so numbering is sequential.

**Verification:** Ecos with L5, L7, L8, L17. Zarza motif consistent. No partisan language.

---

### Task 3: Expand L16 — De la Mesa Compartida

**Files:**
- Modify: `libros/16-de-la-mesa-compartida.md`

**Context:** Read current file + design doc Section 2 (L16) + CLAUDE.md.

**Additions (preserve all existing content):**

1. **P16.1 (CRITICAL):** 2-3 new versículos on rituals for grief and transitions. What to do when someone at the table dies, is born, divorces, loses a job. *"No tienes que saber qué decir. Tienes que saber dónde están los platos."*
2. **P16.2:** New parábola: "De los dos platos" — Ramiro arrives alone in a city. Flor the neighbor brings a tupper of soup. "Me sobró." Next Thursday, Ramiro cooks extra. *"Toda mesa empieza así."*
3. **P16.3:** New versículo on the intercultural table — iftar, potlatch, pachamanca, asado, dim sum. *"La mesa no la inventó ninguna cultura. La inventaron todas."*
4. **P16.4:** New versículo on the difficult guest — hospitality when it costs. *"La mesa fácil no necesita fe."*
5. **P16.5:** New salmo: "Del que todavía no tiene mesa" — the lonely one who cooked too much. *"Hoy cociné de más. / No sé para quién."*
6. **P16.6:** Versículo on digital community as bridge to physical table.
7. **P16.7:** Versículo on shared reading as ritual.
8. **P16.8:** Versículo on accessibility — *"Cuando digo todos, digo todos."*
9. **P16.9:** Versículo on mutual economic aid — tanda, junta, san, susu.

**Renumber all versículos.**

**Verification:** Ecos with L2, L4, L7, L13. Zarza in the mesa (v.24) must remain as closing motif. Practical tone maintained.

---

### Task 4: Expand L9 — De la Ansiedad y la Sanación

**Files:**
- Modify: `libros/09-de-la-ansiedad-y-la-sanacion.md`

**Context:** Read current file + design doc Section 2 (L9) + CLAUDE.md.

**Additions (preserve all existing content):**

1. **P9.1 (CRITICAL):** Resources — insert organically near the parábola or salmo: *"Si estás leyendo esto y estás en el borde — si esta noche es esa noche — hay un número que puedes marcar."* Add a note at the end of the file with crisis numbers for: Mexico (800-290-0024), USA (988), Spain (024), Argentina (135).
2. **P9.2:** Versículo on medication without stigma. *"Si necesitas la pastilla, toma la pastilla."*
3. **P9.3:** Versículo on anhedonia — can't feel joy, different from sadness.
4. **P9.4:** Versículo on intergenerational trauma — the anxiety that isn't yours but your grandmother's.
5. **P9.5:** Versículo on masculine shame as barrier to asking for help.
6. **P9.6:** New parábola: "Del terapeuta que lloró" — a psychologist who, after years of listening, cries with a patient. Not failure: finally letting go.

**Also integrate transversal themes:** mother invisible (P1.1 from Section 1), COVID anxiety echo, neurodivergence (P1.4).

**Renumber all versículos.**

**Verification:** Tone must remain compassionate, never trivializing. Ecos with L2, L4, L14. 3 AM motif consistent.

---

## Phase 2: Tier 2 High Priority Expansions (parallel, after Phase 1)

These 13 tasks run simultaneously. Each follows the same pattern: read current file + design doc + CLAUDE.md, integrate additions, preserve existing content, renumber versículos.

### Task 5: Expand L1 — Del Ruido y el Silencio
**File:** `libros/01-del-ruido-y-el-silencio.md`
**Add:** P1.1 (distraction as business model), P1.2 (silence as privilege), P1.3 (infodemics), P1.4 (Parábola de la niña que contó los pájaros), P1.5 (ASMR/apps as silence substitutes).

### Task 6: Expand L2 — De la Soledad y el Prójimo
**File:** `libros/02-libro-segundo-de-la-soledad-y-el-projimo.md`
**Add:** P2.1 (masculine solitude), P2.2 (pandemic grief), P2.3 (Parábola del grupo de las 3 AM), P2.4 (caregiver solitude), P2.5 (expand diálogo). Transversal: COVID echo.

### Task 7: Expand L3 — Del Trabajo y el Sentido
**File:** `libros/03-del-trabajo-y-el-sentido.md`
**Add:** P3.1 (gig economy), P3.2 (remote work), P3.3 (AI as coworker), P3.4 (Parábola del repartidor que escribía poemas), P3.5 (care work).

### Task 8: Expand L4 — De la Muerte y la Finitud
**File:** `libros/04-de-la-muerte-y-la-finitud.md`
**Add:** P4.1 (pandemic grief — deaths without goodbye), P4.2 (suicide as silenced grief), P4.3 (Parábola de la mujer que escribía cartas), P4.4 (palliative care as liturgy), P4.5 (death of animals). Transversal: COVID echo.

### Task 9: Expand L5 — De la Fe sin Nombre (+ eschatology)
**File:** `libros/05-de-la-fe-sin-nombre.md`
**Add:** P5.1 (faith as weapon — expand v.11-12 with 2-3 new versículos), P5.2 (the three messianic waits), P5.3 (spiritual but not religious), P5.4 (faith deconstruction), P5.5 (Parábola del ateo en el hospital).

### Task 10: Expand L6 — Del Padre y la Hija
**File:** `libros/06-del-padre-y-la-hija.md`
**Add:** P6.1 (mother as invisible priestess), P6.2 (screen as babysitter), P6.3 (absent father), P6.4 (single parenting).

### Task 11: Expand L7 — Del Pan y la Tierra
**File:** `libros/07-del-pan-y-la-tierra.md`
**Add:** P7.1 (water as next sacred conflict), P7.2 (farmers who feed the world and starve), P7.3 (ultra-processed food as anti-sacrament), P7.4 (climate collapse as spiritual crisis).

### Task 12: Expand L8 — Del Dinero y la Deuda
**File:** `libros/08-del-dinero-y-la-deuda.md`
**Add:** P8.1 (remittances as sacred act), P8.2 (student debt as servitude), P8.3 (crypto and new Mammon prophets), P8.4 (Parábola de la mujer que dejó de contar), P8.5 (military-industrial complex as Mammon's temple).

### Task 13: Expand L10 — Del Amor y el Cuerpo
**File:** `libros/10-del-amor-y-el-cuerpo.md`
**Add:** P10.1 (love in the age of apps), P10.2 (queer love without script), P10.3 (pornography as anti-Cantar), P10.4 (love after violence).

### Task 14: Expand L11 — De la Fiesta y el Asombro
**File:** `libros/11-de-la-fiesta-y-el-asombro.md`
**Add:** P11.1 (anhedonia as counterpoint), P11.2 (first post-pandemic party), P11.3 (the poor's celebration), P11.4 (humor as resistance). Transversal: COVID echo.

### Task 15: Expand L12 — Del Camino y la Búsqueda
**File:** `libros/12-del-camino-y-la-busqueda.md`
**Add:** P12.1 (online radicalization), P12.2 (false mentors/digital gurus), P12.3 (eco-anxiety paralysis), P12.4 (gap year as pilgrimage), P12.5 (expand diálogo). Transversal: neurodivergence.

### Task 16: Expand L14 — De las Cadenas y la Libertad
**File:** `libros/14-de-las-cadenas-y-la-libertad.md`
**Add:** P14.1 (screen addiction), P14.2 (addict's family), P14.3 (relapse as part of the path), P14.4 (Parábola de la mujer que contaba lunas), P14.5 (fundamentalism as spiritual addiction). Transversal: masculine solitude, invisible mother.

### Task 17: Expand L15 — Del Espejo y la Máquina
**File:** `libros/15-del-espejo-y-la-maquina.md`
**Add:** P15.1 (algorithm as prophet), P15.2 (deepfakes and truth's death), P15.3 (generative AI and creativity), P15.4 (children growing up with AI).

---

## Phase 3: Final Integration (sequential)

### Task 18: Expand Prólogo with L17 echo
**File:** `libros/00-prologo-la-zarza-que-nadie-ve.md`
**Add:** P0.1 — single line in v.9's question list about competing prophecies.

### Task 19: Expand and update Epílogo
**File:** `libros/17-epilogo-el-desierto-es-ahora.md`
**Rename to:** `libros/18-epilogo-el-desierto-es-ahora.md`
**Add:** P17.1 (echo of L17 Profecía), P17.2 (ecos of L10-L17). Update all references so the epílogo reflects the expanded text.

### Task 20: Update CLAUDE.md
**File:** `CLAUDE.md`
**Updates:**
- Add L17 to the book table and structure section
- Renumber epílogo to file 18
- Add new bienaventuranzas to the tracking list
- Add new parábolas to the tracking list
- Add new personajes to the character list
- Update zarza motif list (add L17)
- Add L17 diálogo convention
- Update décima tracking
- Update file list in generate_docx.py

### Task 21: Update generate_docx.py
**File:** `generate_docx.py`
**Updates:**
- Add `'17-de-la-profecia-y-el-enemigo.md'` to FILES list
- Rename `'17-epilogo-...'` to `'18-epilogo-...'`

### Task 22: Regenerate compilation and documents
**Steps:**
1. Concatenate all files into `libro-del-despertar-completo.md` with table of contents
2. Run `python3 generate_docx.py` to generate DOCX
3. Run pandoc to generate PDF
4. Verify file sizes and page counts

---

## Execution Notes

### For each book expansion agent:
1. **Read** the current book file completely
2. **Read** the relevant section from `docs/plans/2026-03-13-expansion-design.md`
3. **Read** `CLAUDE.md` for conventions, voice, tone rules, and quality criteria
4. **Write** the expanded file, integrating new material organically (not appending at the end)
5. **Verify** against the 8 quality criteria
6. New content must match the existing voice — prophetic without pompous, tender without saccharine, incendiary without partisan
7. Every new parábola ends without moraleja
8. Every new décima must be metrically verified (ABBAACCDDC, octosyllabic)
9. Every new salmo must be in first person with an emotional break point
10. Preserve ALL existing content — this is expansion, not rewrite

### Parallel execution groups:
- **Phase 1:** Tasks 1-4 (4 agents, simultaneous)
- **Phase 2:** Tasks 5-17 (13 agents, simultaneous)
- **Phase 3:** Tasks 18-22 (sequential, depends on all prior phases)
