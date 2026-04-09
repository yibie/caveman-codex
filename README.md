<h1 align="center">caveman-codex</h1>

<p align="center">
  Codex-first port of <code>caveman</code> — install as a <strong>Codex Desktop local plugin</strong> and trigger with <code>$caveman</code>.
</p>

---

This repository adapts the original **caveman** prompt/skill into a format that can be installed and used from **OpenAI Codex Desktop** as a local plugin.

For the full project story, examples, and benchmarks, see the upstream README:

- https://github.com/JuliusBrussee/caveman#readme

## Install (Codex Desktop)

### One command (recommended)

Run this in the project folder you want to enable Caveman for:

```bash
curl -fsSL https://raw.githubusercontent.com/yibie/caveman-codex/main/install.sh | bash
```

Or specify the target project explicitly:

```bash
curl -fsSL https://raw.githubusercontent.com/yibie/caveman-codex/main/install.sh | bash -s -- --project "/path/to/your/project"
```

What the installer does:

- Vendors the plugin into `<project>/.codex-plugins/caveman`
- Updates `<project>/.agents/plugins/marketplace.json` to reference `./.codex-plugins/caveman`

Then **restart Codex Desktop** and install `caveman` from the Plugins UI.

### macOS double-click installer (.command)

If you cloned this repo locally, you can also run:

```bash
/path/to/caveman-codex/install-codex-plugin.command "/path/to/your/project"
```

Or double-click `install-codex-plugin.command` in Finder and pick the target folder.

## Usage

- Enable: `$caveman`
- Intensity: `$caveman lite` / `$caveman full` / `$caveman ultra`
- Disable: “stop caveman” / “normal mode”

## Notes

- If your Codex Desktop build/account only allows official plugins, you may not be able to install local plugins via UI even after creating `marketplace.json`. In that case, use the upstream repo for non-Codex environments, or install as a Codex skill (manual).

