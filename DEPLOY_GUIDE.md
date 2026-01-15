# Guía de Despliegue en GitHub Pages

## 1. Repositorio Local
En tu terminal:
```bash
git init
git add .
git commit -m "Inicio documentación"
```

## 2. GitHub
1. Crea un nuevo repositorio en [Global GitHub](https://github.com/new).
2. Sigue las instrucciones para "push an existing repository":
```bash
git remote add origin https://github.com/TU_USUARIO/NOMBRE_REPO.git
git branch -M main
git push -u origin main
```

## 3. GitHub Pages
1. Ve a **Settings > Pages** en tu repo.
2. En **Branch**, elige `main` y `/ (root)`.
3. Guarda.
4. Tu sitio estará en el link que aparece ahí en unos minutos.
