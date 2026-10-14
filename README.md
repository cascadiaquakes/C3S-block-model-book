# CRESCENT Block Model Book

[![License: BSD-3-Clause](https://img.shields.io/badge/License-BSD_3--Clause-blue.svg)](LICENSE)

A minimal Jupyter Book template for the CRESCENT block model. Add notebooks to build out the book.

Repository: [c3S-block-model-book](https://github.com/cascadiaquakes/c3S-block-model-book)

Published book (after deployment): https://cascadiaquakes.github.io/c3S-block-model-book/

## Install and preview

Install Python 3.11 or newer and Node.js LTS. From the repository root, install the book dependencies into your Python environment:

```bash
pip install -r requirements.txt
jupyter book start
```

Open the local URL printed by the preview server. This book uses Jupyter Book 2 and MyST, configured in `myst.yml`.

Alternatively, preview with Node.js alone:

```bash
npx --yes mystmd start
```

## Add your notebooks

1. Copy `notebooks/example.ipynb` or place your own `.ipynb` file under `notebooks/`.
2. Give it a descriptive filename and begin with a Markdown heading and introduction.
3. Add it to `project.toc` in `myst.yml`, in the order it should appear:

```yaml
  toc:
    - file: index.md
    - file: notebooks/example.ipynb
    - file: notebooks/my-notebook.ipynb
```

4. Run the notebook in your preferred notebook editor and save it if you want its outputs published. The website build does not execute notebooks by default.
5. Preview the book and check the new chapter. Remove the example notebook and its TOC entry when you no longer need them.

Notebook execution dependencies are separate from the book builder. Document them alongside your notebook and add shared Python dependencies to `requirements.txt` when needed.

## Build HTML

```bash
jupyter book build --html --strict
```

The website is written to `_build/html/`. The equivalent Node.js command is `npx --yes mystmd build --html --strict`.

## Publish with GitHub Pages

In the repository's **Settings > Pages**, select **GitHub Actions** as the build and deployment source.

The deployment workflow builds and publishes on pushes to `main`, and can also be run manually from the Actions tab. It derives the website base path from the repository name, so renamed repositories and forks use their own asset paths.

If you fork this template, update the repository and published-book links above for your GitHub owner and repository name.

## License and feedback

This project is licensed under the BSD 3-Clause License. See [LICENSE](LICENSE).

For corrections or suggestions, [open an issue](https://github.com/cascadiaquakes/c3S-block-model-book/issues).

## Acknowledgments

<table>
  <tr>
    <td align="center" valign="middle">
      <img src="https://raw.githubusercontent.com/cascadiaquakes/.github/main/assets/crescent-circle.png" alt="CRESCENT Logo" width="150" />
    </td>
    <td align="center" valign="middle">
      <img src="https://raw.githubusercontent.com/cascadiaquakes/.github/main/assets/nsf-logo.png" alt="NSF Logo" width="450" />
    </td>
  </tr>
</table>

This project is supported by the National Science Foundation through the Cascadia Region Earthquake Science Center (CRESCENT), Cooperative Agreement EAR-2225286.

