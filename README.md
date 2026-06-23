# API Intiza Cobranzas — Documentación

Documentación de la API v2 de Intiza Cobranzas, migrada desde Stoplight y renderizada con [Stoplight Elements](https://github.com/stoplightio/elements).

## Contenido

- `reference/api-v2-auth.yaml` — Autenticación (obtención de token)
- `reference/api-v2.yaml` — API v2: clientes, facturas, pagos, cotizaciones
- `index.html` — Visor navegable (Stoplight Elements)

## Ver la documentación

### Online (GitHub Pages)

Una vez activado Pages, la doc queda disponible en:

```
https://<usuario>.github.io/<repo>/
```

### Local

Como `index.html` carga los YAML por fetch, necesitás un servidor local (no abrir el archivo directo):

```bash
python3 -m http.server 8080
# luego abrir http://localhost:8080
```

## Editar la documentación

Editá los archivos `.yaml` en `reference/`. Al hacer push a `main`, el GitHub Action republica Pages automáticamente.

Para validar los specs antes de pushear:

```bash
npx @redocly/cli lint reference/api-v2.yaml reference/api-v2-auth.yaml
```
