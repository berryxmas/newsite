# 🌐 My Personal Website
This website is used to share information about my current focus, past experiences, blog posts, and recent projects.

## 🚀 Getting Started
### Prerequisites

Make sure you have [Hugo](https://gohugo.io/getting-started/installing/) installed on your machine.

### Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/berryxmas/newsite.git
    cd newsite
    ```

2. Initialize and update submodules:

    ```sh
    git submodule init
    git submodule update
    ```

### Running Hugo

To run the website locally, use the following command:

```sh
hugo server --disableFastRender
```

## 🔧 Troubleshooting
### Updating Submodule
If you need to update the Blowfish theme submodule, run the following commands:
```sh
git submodule init
git submodule update
```
If the submodule is not visible, you might need to remove and re-add it:
```sh
git submodule deinit -f themes/blowfish
git rm -f themes/blowfish
rm -rf .git/modules/themes/blowfish
git submodule add https://github.com/nunocoracao/blowfish themes/blowfish
git submodule update --init --recursive
```
### Deleting Public Folder
To clear the `public` folder, which contains the generated site files, run:
```sh
rm -rf public
hugo server --disableFastRender
```