# Agent instructions

- This is a dependency-free HTML5 Canvas game; `index.html` is the entrypoint and loads the classic script `game.js` (not a module).
- Run it with `npx serve .` and open `http://localhost:3000`; opening `index.html` directly also works, but use the local server for browser verification.
- There is no package manifest, build step, test suite, linter, formatter, CI, or codegen. For a lightweight syntax check, run `node --check game.js`; verify gameplay manually in a browser.
- All gameplay, rendering, input, and mutable game state live in `game.js`; preserve its browser globals and `requestAnimationFrame` loop unless intentionally changing the page architecture.
- Keep the canvas dimensions synchronized between `index.html` (`800x600`) and the `W`/`H` constants in `game.js`.
