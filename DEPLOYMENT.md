
## Manus publishing contract

The project uses Vite. The verified production command is `npm ci --no-audit --no-fund && npm run build`, and the explicit Vite output directory is `dist`. The publish configuration uses `build.command` equal to that clean-install/build command and `build.outputDirectory` equal to `dist`. A clean build was run successfully and produced `dist/index.html`, `dist/manus-routes.json`, `dist/sitemap.xml`, `dist/robots.txt`, and hashed CSS/JavaScript assets.
