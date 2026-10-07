# ESPECIFICACION DEL PROYECTO: IVAN MORATILLO (ARQUITECTURA & ARTE)

## 1. Vision y Proposito
Crear el portal web oficial y nodo digital (Nivel 5 Agent-Native) para Ivan Moratillo, arquitecto y artista plastico peruano con base itinerante entre Lima y Berlin. 

El sitio web tiene como objetivo primordial proyectar su estatus de artista-arquitecto ante coleccionistas privados, instituciones culturales, museos y editoriales internacionales, sirviendo a la vez como canal directo para la comercializacion de obras originales y series de impresiones digitales de coleccion (Giclee Fine Art Prints) con envios internacionales.

## 2. Publico Objetivo (Target)
- Coleccionistas de arte contemporaneo (ticket medio y alto).
- Museos, galerias y curadores en Peru y Europa (especialmente Berlin).
- Editoriales y estudios de arquitectura / interiorismo de alto standing.
- Compradores particulares de arte y laminas de archivo.

## 3. Requerimientos Funcionales
1. **Portada Editorial (Home):**
   - Declaracion de autor y presentacion visual de gran formato.
   - Navegacion bifurcada: Colecciones de Arte (Originales y Prints) vs. Estudio de Arquitectura.
   - Muestra destacada de obras con estetica de galeria de arte europea.
2. **Galeria de Arte (Originales):**
   - Fichas completas de piezas originales: tecnica (tinta, plumilla, acuarela, pastel), dimensiones, soporte (papel de archivo), ano y certificado de autenticidad firmado.
   - Estado: Disponible / Coleccion privada / En exhibicion.
   - Boton de contacto confidencial para coleccionistas.
3. **Tienda de Giclee Prints (Impresiones Fine Art):**
   - Reproducciones seriadas y numeradas sobre papel de algodon (Hahnemuhle / BFK Rives).
   - Selector interactivo de formatos (A3, A2, A1) y opciones de enmarcado.
   - Canales de adquisicion: Pasarela directa (Stripe Payment Links) y boton de asistencia personalizada por WhatsApp.
4. **Manifiesto & Biografia (El Autor):**
   - Manifiesto conceptual del vinculo indisoluble entre la disciplina arquitectonica y el dibujo visionario.
   - Trayectoria, exposiciones y presencia en Lima y Berlin.
5. **Estudio de Arquitectura (Portafolio):**
   - Espacio sobrio para proyectos arquitectonicos seleccionados.
6. **Capa Agendica y GEO (Playbook Nivel 5):**
   - Archivos `llms.txt`, `llms-full.txt` y `robots.txt` con Content Signals.
   - Grafo JSON-LD estructurado (`Person`, `VisualArtwork`, `ArtGallery`).
   - Formulario de contacto via Web3Forms con entrega cifrada a correo.

## 4. Direccion de Diseno (Directivas Soft-Skill)
- **Paleta:** Blanco roto / papel grabado (`#FBFBF9`), tinta negra profunda (`#111827`) y matices tierra/sepia (`#78350F`, `#9A3412`).
- **Tipografia:** Serif de alto contraste para titulares (*Cormorant Garamond* / *Playfair Display*) y sans-serif geometrica neutra (*Plus Jakarta Sans*) para cuerpos y fichas.
- **Espaciado:** Secciones amplias (`py-24` a `py-32`) con margenes generosos y sensacion de sala de exposicion.
