# msa-example

자세한 설명은 👉 [MSA-Example WIKI](https://github.com/Gyeom/msa-example/wiki/1.-Overview)

### Download

##### Clone Main Project
```bash
$ git clone {main_repository_url}
```
##### Clone Sub Project
```bash
# in main project root folder
# git local config에 submodule을 인지시킴
# 명령 전후로 'git config --list --local'를 확인해 보자
$ git submodule init
# clone submodules
$ git submodule update
# checkout master each sub project ... (*)
git submodule foreach git checkout master
```
※ 마지막 명령은, 각 sub project를 master branch로 checkout 하기 위한 것이다. 처음 submodule update를 통해 sub project를 받으면, sub project는 detached HEAD 상태로 어떤 branch에도 속하지 않는 상태이기 때문이다.

##### Clone Main and Sub Project at the same time
```bash
$ git clone --recurse-submodules {main_repository_url}
# git submodule foreach git checkout master
```
