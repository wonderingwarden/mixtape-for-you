# Mixtape for You

A browser-based mixtape maker for creating a personalized cassette-style gift. Choose a cassette design, decorate it with stickers, search for songs, write a note, and export a standalone HTML mixtape.

> **Status:** Static frontend project. No account, backend, build step, or API key is required for the core experience.

## Features

- **Cassette themes** — pastel, vivid, vintage, and dark palettes.
- **Sticker editor** — place, drag, resize, rotate, and remove decorative stickers.
- **Song search** — search the iTunes Search API and add up to eight tracks.
- **30-second previews** — play preview clips when the API provides them.
- **Rich-text note** — personalize the note with basic formatting and text colors.
- **Shareable export** — download a self-contained HTML page for the finished mixtape; song previews and web fonts still require an internet connection.
- **Responsive layout** — designed for desktop and mobile screens.

## Preview

After publishing with GitHub Pages, add a screenshot or short screen recording here. Keep the image in the repository (for example, `assets/preview.png`) and reference it with a relative path.

## Run locally

No dependencies or build tools are required.

1. Download or clone this repository.
2. Open `index.html` in a modern browser.
3. To use song search, run the page from a local web server if your browser blocks requests from `file://` URLs.

Example local server with Python:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploy to GitHub Pages

1. Push the repository to GitHub.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Select `main` and `/(root)`, then save.
5. Wait for GitHub Pages to publish the site.

The entry point is `index.html`; no build command is needed.

## How it works

The project is implemented in plain HTML, CSS, and JavaScript. The browser handles the interface, canvas-based sticker placement, SVG cassette illustrations, preview audio, and export generation.

### External services

- **iTunes Search API** — retrieves song metadata, artwork, track links, and preview URLs. Search results and preview availability depend on the service.
- **Google Fonts** — loads decorative and interface typefaces when internet access is available.
- **Apple-hosted preview media and artwork** — may be requested by the browser when a user searches or plays previews.

The app does not include a custom backend or require an API key. Requests to these third parties can expose ordinary request metadata such as IP address and browser/network information to the relevant service. Do not put private or sensitive information into a public demo.

## Privacy and security

- Mixtape content is handled in the browser and is not sent to a project-owned server.
- Song searches are sent to the iTunes Search API.
- The exported HTML file contains the recipient name, note, chosen tracks, and design needed to recreate the mixtape. Review it before sharing.
- Rich-text notes are sanitized before being displayed in the finished card or included in the exported page.
- Only HTTPS media and track links are accepted for playback/export.
- Never commit credentials, private personal data, private media, or API tokens.

This is a client-side project, not a security-audited application. Review changes and test it in current browsers before using it for sensitive information.

## Accessibility and compatibility

The app uses standard browser controls and responsive CSS. Some interactions—especially canvas-based sticker editing and the rich-text toolbar—may be less convenient with assistive technology or keyboard-only navigation. Accessibility improvements and testing are welcome.

Test on current versions of Chrome, Firefox, Safari, and Edge, including a mobile viewport.

## Known limitations

- Song search requires a network connection and availability of the external API.
- Preview clips are not full tracks and may not be available for every result.
- Google Fonts and remote artwork may not load offline.
- The exported HTML is portable, but remote fonts and audio previews still rely on external services.
- The app does not upload, host, or grant rights to copyrighted music or artwork.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for development and pull request guidelines. Please report security concerns privately using GitHub's repository security reporting features where available; see [SECURITY.md](SECURITY.md).

## License

The project source is licensed under the MIT License; see [LICENSE](LICENSE). This license applies to the original project code, not third-party trademarks, song recordings, cover art, fonts, or API content. Those remain subject to their respective owners' terms.
