# QCustomPlot

This is a replica of the official [QCustomPlot](https://gitlab.com/ecme2/QCustomPlot) repo. Because I want to make some changes but don't have a GitLab account to do a proper fork. The repo is used as submodule in projects [reZonator](https://github.com/orion-project/rezonator2), [Beam Inspector](https://github.com/orion-project/beam-inspector), [Spectrum](https://github.com/orion-project/spectrum). There is also an additional [QCPL](https://github.com/orion-project/custom-plot-lab) libary that adds some helper functions and various dialogs for QCustomPlot.

> [!CAUTION]
> Do not modify manually any braches besides of the `orion` branch

## Update original sources

```bash
git clone https://github.com/orion-project/QCustomPlot.git
git remote add upstream https://gitlab.com/ecme2/QCustomPlot
git fetch upstream
git checkout master
git merge upstream/master
```

Update the dev branch:

```bash
git checkout orion
git rebase master
```
