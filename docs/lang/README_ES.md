<nav align="center" aria-label="Elegir idioma del README">
  <a href="../../README.md">English</a> ·
  <a href="README_ZH.md">简体中文</a> ·
  <a href="README_ZH_TW.md">繁體中文</a> ·
  <a href="README_JA.md">日本語</a> ·
  <a href="README_KO.md">한국어</a> ·
  <strong>Español</strong>
</nav>

<h1 align="center">
  Compositor
  <br />
  <sub>Edición comunitaria multilingüe</sub>
</h1>

<p align="center">
  <a href="https://github.com/MJorgin/Compositor-i18n/releases/latest"><strong>Descargar DMG</strong></a>
  ·
  <a href="https://github.com/robbietilton/Compositor">Compositor oficial</a>
</p>

Compositor es un editor de imágenes nativo y gratuito para macOS. Esta edición comunitaria está basada en **Compositor 1.3.7** y añade seis idiomas de interfaz, un selector de idioma dentro de la app y un DMG ya compilado.

## Datos rápidos

- 6 idiomas de interfaz: inglés, chino simplificado, chino tradicional, japonés, coreano y español
- 715 cadenas de interfaz en cada idioma traducido
- Sigue el idioma del sistema o se puede cambiar manualmente dentro de la app
- El DMG comunitario tiene una firma ad-hoc, pero **no está notarizado por Apple**; el primer arranque requiere una confirmación adicional
- Las imágenes existentes y los proyectos `.comp` se guardan fuera de la app y no cambian al reemplazarla

## Idiomas disponibles

| Idioma | Código | Cobertura | Mantenimiento |
|---|---|---|---|
| English | `en` | idioma de origen | proyecto oficial |
| 简体中文 | `zh-Hans` | completo, 715 cadenas | comunidad |
| 繁體中文 | `zh-Hant` | completo, 715 cadenas | comunidad |
| 日本語 | `ja` | completo, 715 cadenas | comunidad |
| 한국어 | `ko` | completo, 715 cadenas | comunidad |
| Español | `es` | completo, 715 cadenas | comunidad |

## Instalar por primera vez

1. Descarga `Compositor-1.3.7-multilingual.dmg` desde la [última Release](https://github.com/MJorgin/Compositor-i18n/releases/latest).
2. Abre el DMG y arrastra **Compositor** a Aplicaciones.
3. La primera vez, haz clic con el botón secundario en la app, elige Abrir y vuelve a elegir Abrir.
4. Si macOS la bloquea, ve a Configuración del Sistema → Privacidad y seguridad → Abrir de todos modos.

## Reemplazar la versión oficial

1. Sal del Compositor oficial.
2. Abre el DMG comunitario y arrastra Compositor a Aplicaciones.
3. Elige Reemplazar cuando macOS lo pregunte.
4. La primera vez que abras la app reemplazada, haz clic con el botón secundario y elige Abrir.

No edites directamente las cadenas dentro de la app oficial instalada. Cambiar los recursos de una app firmada invalida su firma y puede hacer que Gatekeeper se comporte de forma confusa. Sustituirla por esta compilación comunitaria completa es más sencillo.

Para volver a la versión oficial, descárgala de nuevo desde el [proyecto original](https://github.com/robbietilton/Compositor).

## Cambiar de idioma

Menú Compositor → **Language…** → elige Seguir el sistema, English, 简体中文, 繁體中文, 日本語, 한국어 o Español. Reinicia la app para aplicar el cambio.

## Compilar desde el código fuente

Requiere macOS 26.5 o superior y Xcode 26 o superior.

```sh
git clone https://github.com/MJorgin/Compositor-i18n.git
cd Compositor-i18n
open Compositor.xcodeproj      # después pulsa ⌘R
```

## Contribuir con un idioma

Todas las cadenas están en `Compositor/Localizable.xcstrings`. Las traducciones deben usar textos de interfaz breves, coincidir con la terminología de Photoshop en ese idioma y ser revisadas por una persona que lo hable con fluidez. La IA puede preparar un borrador inicial, pero no debe enviarse una traducción automática sin revisar.

```text
Estás localizando un editor de imágenes nativo de macOS al [idioma de destino]. Traduce las entradas adjuntas del catálogo de cadenas conservando todos los marcadores, incluidos %@, %lld y %%. Usa textos de interfaz breves y adapta los términos técnicos a Photoshop en [idioma de destino], como capa, máscara, calar, niveles, curvas, relleno según contenido, contraer y expandir. No añadas explicaciones ni signos de puntuación que no estén en el origen. Si un término suele dejarse en inglés, mantenlo y sepáralo en una lista. Devuelve solo JSON combinable.
```

Después del borrador con IA, revisa la naturalidad y los atajos, valida los marcadores, compila la app y abre una pull request.

## Relación con el proyecto original

Se ofreció una localización al chino simplificado mediante la PR #113. El mantenedor explicó que el mantenimiento continuo en varios idiomas todavía no es viable para este proyecto inicial mantenido por una sola persona. Este fork conserva las mismas funciones, añade la capa de idiomas y sigue el proyecto original. Muchas gracias al autor original.
