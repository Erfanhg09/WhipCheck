# WhipCheck
Crack a whip at wrong AI answers to make them re-check themselves — canvas whip physics, synthesized crack sound, streaming Markdown, works with any OpenAI-compatible API.


Inspired by that viral video of someone whipping Claude to make it work faster. Built the same idea a different way — the whip actually triggers something real instead of being a gimmick.

Ask an AI a question. If it's wrong, hit one of three whip buttons. Each one sends a genuinely different re-check prompt: a quick sanity check, a step-by-step re-verification, or a full rebuild from scratch. The whip follows your cursor (or finger, on mobile) with real rope physics and cracks when you press Ask or one of the three recheck buttons — moving the whip around never triggers a crack by itself. The whip itself is cosmetic — the accuracy comes from the prompt behind it.

Single HTML file. No backend, nothing to install. Works with any OpenAI-compatible API — Groq, OpenAI, OpenRouter, a local Ollama server, whatever. Renders Markdown and LaTeX math properly, and streams answers in live.

## Getting a key

Groq's free tier is the easiest: console.groq.com/keys → sign in → Create API Key. No card, no region lock.

Any other provider works too — grab a key and pick "Custom" (or the matching preset) in the app.

## Running it

Download `WhipCheck.html`, open it in a browser. Pick a provider preset, paste your key, adjust the model if you want, ask something. Everything's saved in local storage so you're not re-entering it each time.


## Worth knowing

- **The key lives in your browser.** Fine for personal use, don't put this exact page in front of strangers.
- **"Any API" = OpenAI-compatible ones.** Anthropic's and Google's native APIs use a different format and won't work without a gateway.
- **Markdown and math render via innerHTML.** A light sanitizer strips scripts/inline handlers, and LaTeX (`$...$`, `$$...$$`, `\(...\)`, `\[...\]`) is rendered with KaTeX. Fine for personal use, not hardened for public deployment.
- **Model names change.** If a default stops working, check console.groq.com/docs/models and type the new name into the Model field.



Built with Claude as a coding partner — idea and decisions were mine.
