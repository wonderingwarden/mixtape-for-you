# Contributing

Contributions are welcome.

## Before opening a pull request

1. Describe the problem or improvement clearly.
2. Keep changes focused and avoid adding dependencies without a clear need.
3. Do not commit secrets, private user content, copyrighted music files, or API credentials.
4. Test the main flow in a current browser:
   - Choose a theme.
   - Add, move, resize, rotate, and remove stickers.
   - Search for songs and test an available preview.
   - Format a note and complete a mixtape.
   - Export and open the downloaded HTML.
5. Check desktop and mobile layouts.
6. Include screenshots for visual changes and note any known limitations.

## Code conventions

- Prefer readable, small functions and descriptive names.
- Keep the project build-free unless a documented need justifies a build system.
- Treat data returned by external services and user-entered rich text as untrusted.
- Validate external URLs and avoid unsafe HTML insertion.
- Preserve keyboard access and reduced-motion preferences where possible.

## Pull requests

Use the pull request template. Explain what changed, why it changed, how it was tested, and whether any third-party service or privacy behavior changed.
