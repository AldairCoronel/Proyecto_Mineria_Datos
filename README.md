# Proyecto Integrador - Almacenes y Minería de Datos

**Anticipación de saturación y recomendación de rutas alternas en la red del STC Metro y Metrobús de la CDMX**

Facultad de Ciencias, UNAM · Profesora: Jessica Santizo Galicia
Ayudante de teoría: Diego Antonio Villalba González · Ayudante de laboratorio: Emma Alicia Jiménez Sánchez

## 🌐 Sitio desplegado

**https://fernando-bm.github.io/Proyecto_Mineria_Datos**

## Equipo

| Integrante | Rol |
|------------|-----|
| Aldair Coronel Ruiz | Analista / traductor técnico |
| Fernando Bernal Martínez | Relator y verificación de fuentes |
| Luis Alberto Hernández Aguilar | Exploración de datos |
| Tania Ramírez Plascencia | Factibilidad y calendario de eventos |

## Entregas

| # | Fase CRISP-DM | Entrega | Estado |
|---|---------------|---------|--------|
| 1 | Comprensión del negocio | E0 | ✅ |
| 2 | Comprensión de los datos | E1 | ⏳ |
| 3 | Preparación de los datos | E2 | ⏳ |
| 4 | Modelado | E3 | ⏳ |
| 5 | Evaluación | E4 | ⏳ |
| 6 | Despliegue | Reporte y presentación final | ⏳ |

### E0 - Comprensión del Negocio

| Página | Archivo |
|--------|---------|
| Bitácora del stakeholder | `entregas/E0_comprension_negocio/bitacora.qmd` |
| Business Understanding Canvas | `entregas/E0_comprension_negocio/canvas.qmd` |
| Preguntas de investigación | `entregas/E0_comprension_negocio/preguntas.qmd` |
| Criterio de éxito | `entregas/E0_comprension_negocio/criterio_exito.qmd` |
| Supuestos y riesgos | `entregas/E0_comprension_negocio/riesgos_supuestos.qmd` |
| Uso de herramientas de IA | `entregas/E0_comprension_negocio/uso_ia.qmd` |
| Fuentes consultadas | `entregas/E0_comprension_negocio/fuentes.qmd` |

## Estructura del repositorio

```
Proyecto_Mineria_Datos/
├── _quarto.yml                    # configuración del sitio (output-dir: docs)
├── index.qmd                      # portada
├── styles.css                     # estilos, incluido el Canvas
├── entregas/
│   └── E0_comprension_negocio/
│       ├── bitacora.qmd
│       ├── canvas.qmd
│       ├── preguntas.qmd
│       ├── criterio_exito.qmd
│       ├── riesgos_supuestos.qmd
│       ├── uso_ia.qmd
│       ├── fuentes.qmd
│       └── fuentes/               # evidencia archivada del stakeholder simulado
├── docs/                          # sitio compilado (lo genera Quarto)
└── README.md
```

## Cómo compilar el sitio

Requiere [Quarto](https://quarto.org/docs/get-started/) instalado.

```bash
# Vista previa con recarga automática mientras editas
quarto preview

# Compilar el sitio en docs/
quarto render
```

`quarto render` escribe en `docs/`, que es la carpeta que sirve GitHub Pages.

## Cómo publicar en GitHub Pages

```bash
git init
git add .
git commit -m "E0: comprensión del negocio"
git branch -M main
git remote add origin https://github.com/Fernando-BM/Proyecto_Mineria_Datos.git
git push -u origin main
```

Después, en GitHub: **Settings → Pages → Source: Deploy from a branch → Branch: `main` / carpeta `/docs` → Save**.

El sitio tarda uno o dos minutos en aparecer. Verifica que la URL cargue **antes** de la fecha límite y pégala arriba en este README.

> `docs/` debe subirse al repositorio (no ignorarlo), porque es lo que GitHub Pages publica.

## Pendientes antes de entregar

- [ ] Sustituir todos los campos entre corchetes: nombres, fechas, usuario de GitHub.
- [ ] Completar en `bitacora.qmd` el **intento real de contacto** con un stakeholder (a quién, cuándo, por qué medio, qué respuesta se obtuvo). Sin esto, la modalidad simulada no está justificada.
- [ ] Completar `uso_ia.qmd` con el uso real de IA y las correcciones que hizo el equipo.
- [ ] Archivar en `fuentes/` las capturas o PDF de respaldo de las trece fuentes citadas.
- [ ] Verificar que el Canvas se lea de forma autónoma y **quepa en una página** al imprimirse.
- [ ] Confirmar que **todos** los integrantes puedan explicar el criterio de éxito, los riesgos R1 y R3 y por qué se descartó el objetivo horario: la entrega puede anularse si alguien no responde.

## Datos y licencia

Conjuntos de datos del [Portal de Datos Abiertos de la CDMX](https://datos.cdmx.gob.mx), publicados por la **Secretaría de Movilidad (SEMOVI)** bajo licencia **CC-BY-4.0-ESP**. La atribución es obligatoria.

Este proyecto **no utiliza scraping**. Los datos de Waze quedan explícitamente fuera de alcance: no existe API pública y su programa Waze for Cities restringe la republicación de los datos compartidos con socios gubernamentales.
