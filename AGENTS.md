# AGENTS.md

## Cursor Cloud specific instructions

This repository is a **GitHub profile README** repo (the special repo whose `README.md`
renders on the owner's GitHub profile page). Its only tracked content is `README.md`.

- There is **no application, build system, package manager, dependencies, tests, or services**.
  Do not look for `package.json`, `Makefile`, CI workflows, etc. — none exist.
- "Development" here means **editing Markdown** in `README.md` and checking how it renders.
- Nothing needs to be installed for the repo itself; the startup update script is a no-op.

### Previewing the README (optional)

GitHub renders `README.md` server-side, so there is no local server in the repo. To preview
rendering locally you can convert the Markdown to HTML with any renderer, e.g.:

```bash
python3 -m pip install --user markdown   # one-off; not a repo dependency
python3 -c "import markdown,pathlib;pathlib.Path('/tmp/readme.html').write_text(markdown.markdown(pathlib.Path('README.md').read_text(encoding='utf-8'),extensions=['extra','nl2br']),encoding='utf-8')"
python3 -m http.server 8080 -d /tmp     # then open http://localhost:8080/readme.html
```

Note: this is only a rough preview. GitHub Flavored Markdown (emoji, alerts, etc.) may render
slightly differently on the actual profile page than in a generic Markdown renderer.
