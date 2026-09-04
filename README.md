# Portafolio — Entrega 1

## Estructura

```
portfolio/
├── index.html
├── css/
│   └── styles.css
├── js/
│   └── main.js
├── assets/
│   ├── favicon.svg
│   └── eventoshub-preview.svg
└── README.md
```

## Antes de subirlo, edita esto

- `index.html`: reemplaza `tucorreo@ejemplo.com` y el placeholder de LinkedIn en la sección **Contacto**.
- `index.html`: si tienes foto o una captura real de EventosHub, reemplaza `assets/eventoshub-preview.svg` por tu imagen (expórtala en `.webp`, mantén el `width`/`height` y el atributo `loading="lazy"` para que la carga siga siendo rápida).
- Cuando actives GitHub Pages en el repo de EventosHub, cambia el botón "Demo (próximamente)" por el link real.

## Cómo subirlo con Git Flow + Conventional Commits

Trabaja en una rama de feature y ve haciendo commits pequeños y descriptivos, por ejemplo:

```bash
git checkout -b develop
git checkout -b feature/portfolio-onepage

git add index.html
git commit -m "feat: agregar estructura semántica del one page"

git add css/styles.css
git commit -m "style: agregar diseño responsive y paleta de color"

git add js/main.js
git commit -m "feat: agregar menú móvil y navegación activa"

git add assets/
git commit -m "feat: agregar imágenes optimizadas del proyecto EventosHub"

git add README.md
git commit -m "docs: agregar instrucciones de despliegue"
```

Luego integra a `develop` y de ahí a `main`:

```bash
git checkout develop
git merge feature/portfolio-onepage
git checkout main
git merge develop
```

## Desplegar en GitHub Pages

1. Sube el proyecto a un repositorio en GitHub (puede ser este mismo repo o uno nuevo llamado, por ejemplo, `portafolio`).

   ```bash
   git remote add origin https://github.com/tu-usuario/tu-repo.git
   git push -u origin main
   ```

2. En GitHub, ve a **Settings → Pages**.
3. En **Source**, selecciona la rama `main` y la carpeta `/ (root)`.
4. Guarda. En un par de minutos tu sitio estará disponible en:
   `https://tu-usuario.github.io/tu-repo/`

## Prefijos de Conventional Commits usados

- `feat`: una funcionalidad nueva
- `fix`: una corrección
- `style`: cambios de estilos/CSS que no alteran la lógica
- `docs`: cambios en documentación (como este README)
- `refactor`: reorganizar código sin cambiar su comportamiento
