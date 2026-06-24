# API Intiza Cobranzas — Documentación

Documentación de la API v2 de Intiza Cobranzas, migrada desde Stoplight y renderizada con [Stoplight Elements](https://github.com/stoplightio/elements).

## Contenido

- `reference/intiza-api.yaml` — **Spec unificado** que se publica. Dos secciones en el menú lateral: **Autenticación** y **API** (clientes, facturas, pagos, cotizaciones).
- `reference/api-v2-auth.yaml` — spec original de autenticación (referencia).
- `reference/api-v2.yaml` — spec original de la API v2 (referencia).
- `index.html` — visor navegable (Stoplight Elements).
- `vendor/elements/` — assets de Stoplight Elements **alojados localmente** (CSS + JS). La doc no depende de CDNs externos: todo se sirve desde el propio dominio.

> El menú lateral se agrupa por los `tags` del spec. El orden de los grupos sigue el orden de la sección `tags` en `intiza-api.yaml` (primero Autenticación, luego API). Cada endpoint conserva su `servers` propio (auth usa `authc.intiza.com`, el resto `backc.intiza.com`).

## Ver la documentación

### Online (GitHub Pages)
```
https://<usuario>.github.io/<repo>/
```

### Local
```bash
python3 -m http.server 8080
# abrir http://localhost:8080
```

## Editar

Editá `reference/intiza-api.yaml`. Para agregar/mover endpoints entre secciones, cambiá su `tags`. Al pushear a `main`, Pages se republica solo.

Validar antes de pushear:
```bash
npx @redocly/cli lint reference/intiza-api.yaml
```
