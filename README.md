
# Proyecto Next.js

Este es un proyecto de [Next.js](https://nextjs.org) inicializado con [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Primeros Pasos

Primero, ejecuta el servidor de desarrollo:

```bash
npm run dev
# o
yarn dev
# o
pnpm dev
# o
bun dev
```

Abre [http://localhost:3000](http://localhost:3000) en tu navegador para ver el resultado.

Puedes comenzar a editar la página modificando `app/page.tsx`. La página se actualizará automáticamente a medida que edites el archivo.

Este proyecto usa [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) para optimizar y cargar automáticamente [Geist](https://vercel.com/font), una nueva familia tipográfica de Vercel.

## Aprende Más

Para aprender más sobre Next.js, consulta los siguientes recursos:

- [Documentación de Next.js](https://nextjs.org/docs) - aprende sobre las funcionalidades y la API de Next.js.
- [Aprende Next.js](https://nextjs.org/learn) - un tutorial interactivo de Next.js.

También puedes revisar el [repositorio de GitHub de Next.js](https://github.com/vercel/next.js) - ¡tu feedback y contribuciones son bienvenidos!

## Despliegue en Vercel

La forma más sencilla de desplegar tu aplicación de Next.js es usando la [plataforma Vercel](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme), creada por los autores de Next.js.

Consulta nuestra [documentación de despliegue de Next.js](https://nextjs.org/docs/app/building-your-application/deploying) para más detalles.

## Configuración de Variables de Entorno

### Settings → Environment Variables

Para la creación de `GOOGLE_CLIENT_ID` y `GOOGLE_CLIENT_SECRET`, sigue estos pasos:

1. Ingresa a la [Consola de APIs de Google](https://console.cloud.google.com/).
2. Crea un **OAuth Client ID** (tipo **Aplicación Web**).
3. Como URI de redirección, añade:

   ```
   http://[reemplaza por tu dominio de app]/api/auth/callback/google
   ```

4. Cuano despliegues en Vercel configura esto en las variables de entorno:

```bash
GOOGLE_CLIENT_ID=tu_CLIENT_ID_de_Google
GOOGLE_CLIENT_SECRET=tu_CLIENT_SECRET_de_Google
NEXTAUTH_SECRET=tu_clave_secreta_generada (puedes usar `openssl rand -base64 32` o una clave larga similar, por ejemplo: s9f1H3KdL9jYw5vPq8rVzXgN+ADDe1aB1c4D6eF7hI=)
```

## Configuración de API

En el archivo:

```
src/app/api/agent/route.ts
```

Reemplaza `[API]` por la URL de tu API desplegada.

---

**Autor: MAC**
