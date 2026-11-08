# AMAC · Entrega 2: maquetación HTML y CSS

Sitio estático de la bolsa de trabajo AMAC (OT2026-WEB). El prototipo de Figma es la referencia visual. Los datos de vacantes, solicitudes y empresas están escritos en el HTML.

## Cómo verlo

Abra `index.html` en el navegador, o publique la carpeta en Vercel con el ajuste **Other** (HTML puro).

Flujo de demostración: listado → detalle de la vacante → Postularme → Mis solicitudes.

## Páginas

| Archivo | Pantalla |
| --- | --- |
| `index.html` | Listado de vacantes, buscador y filtros |
| `vacante.html` | Detalle de Recepcionista, con Postularme y Llamar |
| `login.html` | Inicio de sesión |
| `registro-candidato.html` | Registro de candidato |
| `mis-solicitudes.html` | Solicitudes con estatus distintos y botón Cancelar |
| `empresa-vacantes.html` | Panel de vacantes de la empresa |
| `404.html` | Página de error (extra) |

En todas hay encabezado, pie, salto al contenido y el botón ¿Necesita ayuda? Llámenos.

## Paleta y tipografía

Definidas en `css/variables.css`, tomadas del sistema de diseño de Figma.

| Token | Valor | Uso |
| --- | --- | --- |
| `--color-primario` | `#202945` | Encabezado, botones principales, texto |
| `--color-primario-oscuro` | `#151c31` | Hover del botón principal |
| `--color-acento` / `--color-ayuda` | `#ff815c` | Foco, ayuda, estados de atención |
| `--color-info` | `#cae4ef` | Mensajes de orientación |
| `--color-borde` | `#a8a8a8` | Bordes de tarjetas y campos |
| `--color-fondo` | `#ffffff` | Fondo |
| `--fuente-base` | Work Sans | Texto de 18 px (`1.125rem`) |
| `--fuente-titulo` | Libre Baskerville | Títulos |

El prototipo usa Work Sans y Libre Baskerville, así que esas son las familias del sitio. El tamaño base sigue en 18 px y en `rem`, para que escale con el navegador.

## Componentes reutilizables

Pensados para convertirse después en componentes de React:

- `marca` y `encabezado`
- `nav-principal` y `menu__boton`
- `pie`
- `boton`, `boton--primario`, `boton--secundario`
- `boton-ayuda`
- `tarjeta-vacante`
- `tarjeta-solicitud`
- `etiqueta-estatus` (enviada, en revisión, aceptada, no seleccionada, activa, pausada, cerrada)
- `campo-formulario`
- `casilla`
- `panel`
- `mensaje-info`
- `resumen`
- `tabla-vacantes`
- `paginacion`
- `saltar-contenido`

## Decisiones respecto al prototipo

1. El registro vive en un solo archivo, como pide la entrega. Los tres pasos de Figma (datos personales, contacto, experiencia) están en la misma página, junto con dirección y la casilla de términos.
2. El encabezado y el pie son los mismos en todas las páginas. En el panel de empresa, Mis vacantes y Cerrar sesión van en una navegación de la sección.
3. El detalle conserva Postularme y Guardar y continuar. También incluye Llamar, porque la entrega lo pide en una vacante.
4. Cancelar aparece en las solicitudes Enviada y En revisión.
5. Los filtros incluyen horario (tipo de jornada del prototipo), categoría, municipio y modalidad.
6. El hover del botón principal usa un azul un poco más oscuro. En Figma el token de primario oscuro repetía el mismo hex.
7. Extra: modo de alto contraste en el pie y página 404.

## Integrantes

Completar con el nombre de cada persona y la parte que realizó.

## Capturas pendientes de la entrega

- `index.html` en celular y en escritorio.
- Puntaje de Lighthouse, categoría Accessibility, sobre `index.html`.

## Accesibilidad incluida

Texto base de 18 px en `rem`, contraste del azul `#202945` sobre blanco, controles de al menos 44 px, etiquetas visibles, un solo `h1` por página, `lang="es"`, foco visible y enlace para saltar al contenido.
