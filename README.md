# jupyterlab-git

<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->

[![All Contributors](https://img.shields.io/badge/all_contributors-4-orange.svg?style=flat-square)](#contributors-)

<!-- ALL-CONTRIBUTORS-BADGE:END -->

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/jupyterlab/jupyterlab-git/master?urlpath=lab/tree/examples/demo.ipynb) [![Build Status](https://travis-ci.org/jupyterlab/jupyterlab-git.svg?branch=master)](https://travis-ci.org/jupyterlab/jupyterlab-git) [![Version](https://img.shields.io/npm/v/@jupyterlab/git.svg)](https://www.npmjs.com/package/@jupyterlab/git) [![Version](https://img.shields.io/pypi/v/jupyterlab-git.svg)](https://pypi.org/project/jupyterlab-git/) [![Downloads](https://img.shields.io/npm/dm/@jupyterlab/git.svg)](https://www.npmjs.com/package/@jupyterlab/git) [![Version](https://img.shields.io/conda/vn/conda-forge/jupyterlab-git.svg)](https://anaconda.org/conda-forge/jupyterlab-git) [![Downloads](https://img.shields.io/conda/dn/conda-forge/jupyterlab-git.svg)](https://anaconda.org/conda-forge/jupyterlab-git)

A JupyterLab extension for version control using git

![](http://g.recordit.co/N9Ikzbyk8P.gif)

To see the extension in action, open the example notebook included in the Binder [demo](https://mybinder.org/v2/gh/jupyterlab/jupyterlab-git/master?urlpath=lab/tree/examples/demo.ipynb).

## Prerequisites

- JupyterLab

## Usage

- Open the git extension from the _Git_ tab on the left panel

## Install

To install perform the following steps:

```bash
pip install --upgrade jupyterlab-git
jupyter lab build
```

### Troubleshooting

Before consulting the following list, be sure the server extension and the frontend extension have the same version by executing the following commands:

```bash
jupyter serverextension list
jupyter labextension list
```

- **Issue**: the Git panel does not recognize that you are in a Git repository.

  Possible fixes:

  - Be sure to be in a Git repository in the filebrowser tab

  - Check the server log. If you see a warning with a 404 code similar to:  
    `[W 00:27:41.800 LabApp] 404 GET /git/server_root?1576081660665`

    Explicitly enable the server extension by running:

    ```bash
    jupyter serverextension enable --py jupyterlab_git
    ```

  - If you are using JupyterHub or some other technologies requiring an initialization script which includes the jupyterlab-git extension, be sure to install both the frontend and the server extension **before** launching JupyterLab.

- **Issue**: the Git panel is not visible.

  Possible fixes:

  - Check that the JupyterLab extension is installed:

    ```bash
    jupyter labextension list
    ```

    If you don't see `@jupyterlab/git v... enabled OK` in the list, explicitly install the jupyter labextension by running:

    ```bash
    jupyter labextension install @jupyterlab/git
    ```

## Development

### Contributing

If you would like to contribute to the project, please read our [contributor documentation](https://github.com/jupyterlab/jupyterlab/blob/master/CONTRIBUTING.md).

JupyterLab follows the official [Jupyter Code of Conduct](https://github.com/jupyter/governance/blob/master/conduct/code_of_conduct.md).

### Install

Requires node 4+ and npm 4+

```bash
# Install new-ish JupyterLab
pip install -U jupyterlab

# Clone the repo to your local environment
git clone https://github.com/jupyterlab/jupyterlab-git.git
cd jupyterlab-git

# Install the server extension in development mode and enable it
pip install -e .[test]
jupyter serverextension enable --py jupyterlab_git

# Build the labextension and dev-mode link it to jlab
jlpm build
jupyter labextension link .
```

To rebuild the package after a change and the JupyterLab app:

```bash
jlpm run build
jupyter lab build
```

To execute the tests

```bash
pytest jupyterlab_git
jlpm run test
```

## Contributors ✨

The Jupyter Git extension is part of [Project Jupyter](http://jupyter.org/) and is developed by an open community of contributors
([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://github.com/ellisonbg"><img src="https://avatars3.githubusercontent.com/u/27600?v=4" width="100px;" alt=""/><br /><sub><b>Brian E. Granger</b></sub></a><br /><a href="#projectManagement-ellisonbg" title="Project Management">📆</a> <a href="#design-ellisonbg" title="Design">🎨</a> <a href="#ideas-ellisonbg" title="Ideas, Planning, & Feedback">🤔</a> <a href="#fundingFinding-ellisonbg" title="Funding Finding">🔍</a></td>
    <td align="center"><a href="https://www.saulshanabrook.com/"><img src="https://avatars1.githubusercontent.com/u/1186124?v=4" width="100px;" alt=""/><br /><sub><b>Saul Shanabrook</b></sub></a><br /><a href="https://github.com/jupyterlab/jupyterlab-git/commits?author=saulshanabrook" title="Code">💻</a> <a href="#projectManagement-saulshanabrook" title="Project Management">📆</a> <a href="https://github.com/jupyterlab/jupyterlab-git/pulls?q=is%3Apr+reviewed-by%3Asaulshanabrook" title="Reviewed Pull Requests">👀</a> <a href="#infra-saulshanabrook" title="Infrastructure (Hosting, Build-Tools, etc)">🚇</a></td>
    <td align="center"><a href="https://github.com/jaipreet-s"><img src="https://avatars1.githubusercontent.com/u/43826141?v=4" width="100px;" alt=""/><br /><sub><b>Jaipreet Singh</b></sub></a><br /><a href="#projectManagement-jaipreet-s" title="Project Management">📆</a> <a href="https://github.com/jupyterlab/jupyterlab-git/pulls?q=is%3Apr+reviewed-by%3Ajaipreet-s" title="Reviewed Pull Requests">👀</a> <a href="https://github.com/jupyterlab/jupyterlab-git/commits?author=jaipreet-s" title="Code">💻</a> <a href="#design-jaipreet-s" title="Design">🎨</a></td>
    <td align="center"><a href="https://github.com/fcollonval"><img src="https://avatars1.githubusercontent.com/u/8435071?v=4" width="100px;" alt=""/><br /><sub><b>Frédéric Collonval</b></sub></a><br /><a href="#projectManagement-fcollonval" title="Project Management">📆</a> <a href="https://github.com/jupyterlab/jupyterlab-git/pulls?q=is%3Apr+reviewed-by%3Afcollonval" title="Reviewed Pull Requests">👀</a> <a href="https://github.com/jupyterlab/jupyterlab-git/commits?author=fcollonval" title="Code">💻</a></td>
  </tr>
</table>

<!-- markdownlint-enable -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!

To add yourself, or someone else, to this list you can either [use the bot](https://allcontributors.org/docs/en/bot/usage) (`@all-contributors please add <username> for <contributions>`) or [the CLI](https://allcontributors.org/docs/en/cli/usage) (`jlpm all-contributors add <username> <contributions>`).

## Attributions

Extension development has been sponsored at various times by the following organizations:

- **[Jupyter Cal Poly](https://github.com/jupytercalpoly)**: [Brian Granger](https://github.com/ellisonbg), [Ji Zhang](https://github.com/zzhangjii), [Hana Zarea](https://github.com/hzarea), [Noah Stapp](https://github.com/NoahStapp), and [Ashutosh Bondre](https://github.com/ashutoshbondre).
- **[Amazon Web Services](https://github.com/aws)**: [Jaipreet Singh](https://github.com/jaipreet-s), [Neelam Gehlot](https://github.com/neelamgehlot), and [Saul Shanabrook](https://github.com/saulshanabrook).
- **[LabShare](https://github.com/LabShare)**: [Konstantin Taletskiy](https://github.com/ktaletsk).
- **[Safran Group](https://www.safran-group.com/)**: [Frédéric Collonval](https://github.com/fcollonval).
- **D. E. Shaw group**: [Max Klein](https://github.com/telamonian) and [Athan](https://github.com/kgryte).
