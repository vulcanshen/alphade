# Alphade

Quita marcas de agua semitransparentes, logotipos y textos superpuestos de tus propios vídeos, en tu Mac. Alphade recupera la imagen que había debajo en lugar de difuminarla.

[English](README.md) | [Deutsch](README-de.md) | Español | [Français](README-fr.md) | [日本語](README-ja.md) | [한국어](README-ko.md) | [繁體中文](README-zh_TW.md)

![Alphade comparando el vídeo original y el procesado](images/compare.png)

## Qué hace

Dibuja un recuadro alrededor de la marca de agua. Alphade analiza el vídeo completo, averigua cómo se mezcló la marca y lo revierte en cada fotograma. Si la marca es opaca y está sobre un fondo sencillo, rellena la zona de forma suave a partir de lo que la rodea.

- **Restaura, no difumina**: la marca de agua semitransparente se elimina de la imagen y vuelve a verse lo que había debajo.
- **Te avisa antes de exportar**: tras el análisis, Alphade indica si la marca «Se elimina limpiamente», «Se elimina rellenando» o «Quedará borroso».
- **Revisa cada fotograma**: avanza fotograma a fotograma, compara con el original lado a lado y reproduce desde cualquier punto.
- **Solo cambia el recuadro**: exporta con el tamaño original o reducido a 1080p o 720p, en H.264 o HEVC. El audio se copia tal cual.
- **Privado**: todo se procesa en tu Mac. Los vídeos nunca se suben, no hace falta cuenta, Alphade no se conecta a la red y no recopila ningún dato.
- **Gratis**.

## Instalación

Requiere macOS 26 o posterior. Probado en Mac con Apple silicon. Alphade está firmado con un Developer ID y notarizado por Apple.

### Descarga

1. Descarga [`Alphade.zip`](../../releases/latest/download/Alphade.zip) de la [última versión](../../releases/latest).
2. Abre el zip y arrastra **Alphade** a la carpeta Aplicaciones.
3. Abre Alphade. macOS te preguntará si quieres abrir una app descargada de internet; haz clic en **Abrir**.

Para desinstalarlo, arrastra Alphade a la Papelera. Sus ajustes y archivos temporales están en `~/Library/Containers/app.vulcanshen.alphade`, que también puedes eliminar.

### Homebrew

```sh
brew install --cask vulcanshen/tap/alphade
```

Actualiza con `brew upgrade --cask alphade`. Desinstala con `brew uninstall --cask alphade`, o añade `--zap` para borrar también sus ajustes y archivos temporales.

## Primeros pasos

1. Haz clic en **Elegir vídeo…** (o suelta un vídeo en la ventana).
2. Arrastra un recuadro alrededor de la marca de agua, con un poco de margen por todos los lados.
3. Haz clic en **Analizar**.
4. Revisa el resultado con **Original**, **Procesado** y **Comparar**.
5. Haz clic en **Exportar…** y elige dónde guardarlo. El nombre aparece como `<nombre original>_nowm.mp4`.

La interfaz sigue el idioma del sistema: English, Deutsch, Español, Français, 日本語, 한국어 o 繁體中文. Puedes cambiarlo en Ajustes.

## Teclado

| Teclas | Acción |
|---|---|
| ⌘O | Abrir un vídeo |
| ⌘E | Exportar |
| ⌘1 / ⌘2 / ⌘3 | Original / Procesado / Comparar |
| ← / → | Fotograma anterior / siguiente |
| Espacio | Reproducir o pausar (sin sonido) |
| Mantener O | Mostrar el original mientras se mantiene pulsada |
| ⌘+ / ⌘− | Ampliar / reducir (después de dibujar el recuadro) |
| ⌘, | Ajustes (idioma) |

## Funciona mejor con

- Marcas de agua, logotipos y textos semitransparentes que permanecen en el mismo sitio durante todo el vídeo
- Logotipos opacos sobre fondos sencillos, como colores lisos, degradados y diapositivas
- Vídeos MP4, MOV y M4V de 8 bits (SDR)

## No compatible

- Marcas de agua que se mueven o cambian de posición
- Marcas de agua opacas sobre fondos detallados o imágenes reales (la zona queda borrosa)
- Vídeos de 10 bits y HDR

## Úsalo en tus propios vídeos

Edita solo vídeos que te pertenezcan o que tengas permiso para modificar. Quitar la marca de agua de otra persona puede infringir las leyes de propiedad intelectual de tu país, y eres responsable del uso que hagas de Alphade.

## Comentarios

Informa de problemas e ideas en [Issues](../../issues). El código fuente no es público.

## Colaboradores

<a href="https://github.com/vulcanshen"><img src="https://github.com/vulcanshen.png" width="48" alt="Vulcan Shen"></a>
<a href="https://github.com/claude"><img src="https://github.com/claude.png" width="48" alt="Claude"></a>

Creado por [Vulcan Shen](https://github.com/vulcanshen) y [Claude](https://github.com/claude) con Claude Code.

## Licencia

Alphade se puede descargar y usar gratis. © 2026 Vulcan Shen. Todos los derechos reservados. Alphade se ofrece «tal cual», sin garantía de ningún tipo.
