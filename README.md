# Github packages latest image tag

[![test](https://github.com/AlexF4Dev/github-packages-image-tag/actions/workflows/test.yml/badge.svg)](https://github.com/AlexF4Dev/github-packages-image-tag/actions/workflows/test.yml)

This [GitHub Action](https://github.com/features/actions) Gets latest iamge tag from GitHub packages



## Usage

```yaml
steps:
    # - uses: actions/checkout@v3    
    - name: 'Get Version Of the Image'
    uses: AlexF4Dev/github-packages-image-tag@master
    id:  getVersion
    with:
        github-token: ${{ secrets.GHCR_PAT }}
        image-repo: "github"
        image-name: "super-linter"
        tag-pattern: "[0-9]\\.[0-9]+"
        debug: false
    
    - name: Just echo the output
    run: echo '${{ steps.getVersion.outputs.result }}'             

```

## License

This project is released under the [MIT License](LICENSE).