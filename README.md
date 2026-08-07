# dtrabogados-holding

Landing "en construcción" para `dtrabogados.com` mientras iteramos el sitio real en [`dtrabogados-site`](https://github.com/corak149/dtrabogados-site).

## Qué es

Un **único HTML estático** (~7 KB) sin build ni dependencias. Se sirve directo desde Cloudflare Pages. Mismo lenguaje visual que el sitio principal (navy + dorado + papiro, Cormorant Garamond + Source Sans 3).

## Estructura

```
index.html         página completa (HTML + CSS inline)
logo-dtr.svg       logo placeholder (reemplazar por SVG oficial cuando esté)
favicon.svg
```

## Cómo desplegar en Cloudflare Pages

1. **dash.cloudflare.com → Workers & Pages → Create → Pages**
2. **Connect to Git** → autorizar GitHub → repo `dtrabogados-holding`, branch `main`
3. **Framework preset:** None
4. **Build command:** (vacío)
5. **Build output directory:** `/` (raíz)
6. **Save and Deploy** — deploy en 15 segundos, URL `dtrabogados-holding.pages.dev`

## Conectar dtrabogados.com

Tab **"Custom domains"** del proyecto → **Set up a custom domain** → `dtrabogados.com`.
Cloudflare detecta que el dominio ya está en la misma cuenta y actualiza el registro DNS automáticamente.

## Cuando la V1 del sitio real esté lista

1. En `dtrabogados-holding` → Custom domains → **Remove** `dtrabogados.com`
2. En `dtrabogados-site` (proyecto principal) → Custom domains → **Add** `dtrabogados.com`
3. Cloudflare actualiza DNS solo. En 1-2 min el dominio sirve el sitio real.

Este repo se puede archivar o dejar como plan B para futuros mantenimientos.

## TODOs

- [ ] Reemplazar `logo-dtr.svg` por el oficial exportado del `.ai`
- [ ] Confirmar número real de WhatsApp (hoy placeholder `50700000000`)
- [ ] Confirmar `info@dtrabogados.com` activo (o cambiar por otro correo)
