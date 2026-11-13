# SeguimIA

La revisión del resultado y de los efectos adversos en medicina estética. Aplicación web de un solo fichero.

**Usar la app:** https://fborrasumh.github.io/seguimia/

**Idiomas:** español (por defecto), inglés, portugués; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL).

## Qué hace

Quinta app del [Kit EstéticIA](https://fborrasumh.github.io/kitesteticia/): la revisión tras el tratamiento.

- **Lee la sesión de [PautIA](https://fborrasumh.github.io/pautia/)** (formato `kitesteticia-sesion/1`): paciente, fecha, productos con su lote, zonas tratadas e incidencias inmediatas.
- **Calendario orientativo** por técnica: fecha de revisión y del siguiente paso (retoque, nueva sesión o valoración final).
- **Antes y después**: dos fotos comparadas con un deslizador y lista de fotografía estandarizada. Las fotos se ven en el navegador y **no se guardan ni se envían**; la comparación se puede descargar como imagen para la historia clínica.
- **Resultado**: escala de mejoría estética global (GAIS) del médico y del paciente, satisfacción de 0 a 10 e intensidad por zona antes y ahora (escala sencilla de cinco grados, no validada).
- **Efectos adversos tardíos** propios de cada técnica, con fecha de inicio, intensidad, producto y lote, actuación y evolución. Los graves se marcan.
- **Notificación preparada**: según el producto, sospecha de reacción adversa a medicamento (Sistema Español de Farmacovigilancia, notificaram.es) o incidente con producto sanitario (AEMPS), con los datos listos para copiar. La app avisa de los graves sin notificar.
- **Informe de revisión** con las próximas citas, en Word o impreso.

No usa IA y no hace ninguna llamada de red. Español, inglés y portugués.

## Privacidad

Las revisiones y los efectos adversos se guardan en el navegador. Las fotos no se guardan. Nada sale hacia ningún servidor: la notificación la envía el médico en la web oficial.

## Límites

Las fechas son orientativas. La intensidad por zona no es una escala validada. La app no decide si un efecto es una reacción adversa ni sustituye a la valoración clínica, y no envía notificaciones.

## Pruebas

`node tests/test_nucleo.js` (calendario, sesión, escalas, efectos adversos, vía de notificación e informe) y `python3 tests/smoke.py` (lee una sesión descargada de PautIA; fotos y deslizador, escalas, efectos adversos y notificación, informe, persistencia sin fotos, tres idiomas, accesibilidad WCAG 2.2 AA, CSP y móvil).

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche) y Elena Caride Miana (Dra. Caride Medicina Estética & Antiaging).

Quinta app del Kit EstéticIA, diseñado para el alumnado del Máster de Formación Permanente en Medicina Estética Integral y Antienvejecimiento (UMH).

ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573) · Elena Caride Miana [0000-0002-7620-4857](https://orcid.org/0000-0002-7620-4857)

## Cómo citar

Borrás Rocher, F. y Caride Miana, E. (2026). *SeguimIA* (v1.0.0) [Software]. (DOI en trámite)

## Licencia

MIT. Véase [LICENSE](LICENSE).
