# SSTIA-Archive
*🚧development in progress*

## Intro
A repo that served as an archive site for the organization UMJI-SSTIA.

In order to contribute, you may:
- If you have push access to this repo, simply clone this repo, edit the corresponding content, create a commit and push to the master branch. The Gitbook service will automatically fetch your commit and refresh building.
- Otherwise, you may either:
    - log in as `ji-sstia`, or
    - create pull request, or
    - send your patch to `ji_sstia@163.com`

## Gitbook Deployment
See ji-sstia.gitbook.io/ji-sstia/

## Local Build
- Source: [link](https://github.com/GitbookIO/gitbook)
- Config guide: [link](https://github.com/GitbookIO/gitbook/blob/master/docs/config.md)

If you would like to test locally:

### Environment Setup
install nodejs & npm

```shell
sudo apt update
sudo apt install nodejs npm
# upgrade
sudo npm install n -g
sudo n stable npm i -g npm
# change npm source
npm config set registry http://registry.npm.taobao.org/
```

nvm

```shell
# assume using bash
curl https://gitee.com/mirrors/nvm/raw/master/install.sh | bash
source ~/.bashrc
export NVM_NODEJS_ORG_MIRROR=https://npm.taobao.org/mirrors/node
nvm install 12.18.1
nvm use 12.18.1
```

install gitbook

```shell
# install gitbook-cli
sudo npm install -g gitbook-cli
# install gitbook; NOTE: it takes around 20mins
gitbook -V
# verify the installation of gitbook
gitbook -V
# optional for export PDF
sudo apt install calibre
```

### Workflow
- ~~`gitbook init` initialize your local directory~~ no need since we've already got our contents
- `git clone git@github.com:UMJI-SSTIA/ji-sstia-pages.git & cd ji-sstia-pages`
- `gitbook serve` deploy locally
    - by default `localhost:4000`
- `gitbook build` build static website pages into `./_book`