# The Frames Vol. 1, zine digital

Contenido de esta carpeta:
- index.html: el visor (efecto de hoja con la librería StPageFlip, licencia MIT)
- pages/: las 24 páginas en JPG (01.jpg es la portada, 24.jpg la contraportada)

## 1. Publicarlo en GitHub Pages (gratis)
1. En github.com crea un repositorio público llamado `zine-the-frames`.
2. "Add file" > "Upload files": arrastra index.html y la carpeta pages. Commit.
3. Settings > Pages > Source: "Deploy from a branch", rama `main`, carpeta `/ (root)`. Save.
4. En uno o dos minutos queda en: https://loui89.github.io/zine-the-frames/

## 2. Incrustarlo en Squarespace (plan Core o superior)
Edita la página, agrega un bloque "Código", pega esto y guarda:

<div class="loui-zine">
  <iframe src="https://loui89.github.io/zine-the-frames/?embed=1"
          title="The Frames Vol. 1, photo zine by loui.61"
          loading="lazy"
          style="width:100%;border:0;display:block;height:70vw;max-height:880px;background:transparent"></iframe>
</div>
<script>
  window.addEventListener("message", function (e) {
    if (e.origin !== "https://loui89.github.io") return;
    var d = e.data;
    if (!d || d.type !== "loui-zine-height") return;
    document.querySelectorAll(".loui-zine iframe").forEach(function (f) {
      if (f.contentWindow === e.source) f.style.height = d.height + "px";
    });
  });
</script>

Revisa el resultado en una ventana de incógnito: Squarespace no ejecuta los scripts
de los bloques de código mientras estás conectado.

## Opciones de la URL del iframe
- `?embed=1`            fondo transparente (toma el color de tu sección)
- `&ink=light`          botones y contador claros, para secciones oscuras
- `&ink=dark`           botones y contador oscuros, para secciones claras
- `&maxw=800`           ancho máximo del libro en px (por defecto 960)
Ejemplo: https://loui89.github.io/zine-the-frames/?embed=1&ink=light&maxw=900

## Para una próxima zine
Reemplaza las imágenes de pages/ (mismos nombres, 01.jpg en adelante, número par de páginas)
y agrega o quita líneas <div class="page"> en index.html para que coincidan.
