# Dr. Adrián Fernández — Urólogo en Guadalajara

Sitio del **Dr. Adrián Fernández Arzate**, urólogo en Guadalajara: especialidades, sobre el doctor y contacto. Dominio: <https://urologoadrianfernandez.com>.

**Stack:** React 19 (JavaScript) + Vite 6 + Tailwind CSS 3 + React Router 7.

## Requisitos

- Node.js 20.19 o superior (recomendado 22 LTS) y npm.
- Git.

## Instalación

```bash
git clone https://github.com/PrimerotuwebTeam/urologoadrianfernandez-web.git
cd urologoadrianfernandez-web
npm install
```

## Ejecutar en local

```bash
npm run dev
```

Vite levanta el sitio en <http://localhost:5173> con recarga en caliente.

## Scripts

| Comando | Qué hace |
|---|---|
| `npm run dev` | Servidor de desarrollo |
| `npm run build` | Compila a `dist/` |
| `npm run lint` | ESLint |
| `npm run preview` | Sirve el build en local |

## Estructura

- `src/pages/` — `mainpage`, `specialties`, `aboutUs`, `contact`.
- `src/routes/` — definición de rutas.
- `src/components/` — componentes compartidos.
- `public/` — imágenes, SEO y `.htaccess`.

## Despliegue

El sitio es estático: `npm run build` genera la carpeta `dist/` y ese contenido es lo que se publica en **urologoadrianfernandez.com** (hosting compartido tipo Hostinger/Apache).

1. Compila:

   ```bash
   npm run build
   ```

2. Prueba el build en local (opcional): `npm run preview`.
3. Sube **el contenido** de `dist/` (no la carpeta `dist` en sí) a `public_html/` del dominio, por el Administrador de archivos de hPanel o por FTP.
4. Comprueba que se subió el `.htaccess` (es un archivo oculto y algunos clientes FTP lo omiten). Viene de `public/.htaccess`, Vite lo copia a `dist/` y es el que hace que las rutas internas no den 404 al recargar.

El repositorio no tiene despliegue automático: cada publicación es un build y una subida manual.

## Ramas

La rama por defecto en GitHub es `master` (publicado). Se trabaja en `develop` y se fusiona a `master` para publicar.
