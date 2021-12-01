# Personal helm repository
## Repository
    helm repo add nenych https://nenych.github.io/helm-charts/

## Add a new chart
- Add charts to the charts directory.
- Commit a new chart.
- Package a new chart:
    ```bash
    cd <repo_root>
    helm package <path_to_chart>
    ```
- Stash:
    ```bash
    git stash
    ```
- Checkout to the "gh-pages" brach and unstash files:
    ```bash
    git checkout gh-pages
    git stash pop
    ```
- Move your package to the packages folder:
    ```bash
    mv <package>.tgz packages
    ```
- Index all helm packages:
    ```bash
    helm repo index --url https://nenych.github.io/helm-charts packages/
    ```
