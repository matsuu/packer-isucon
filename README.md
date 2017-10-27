matsuu/packer-isucon
====================

## これはなに

[Packer](https://www.packer.io/)でISUCON環境を構築するためのTemplateです。


## 必要なもの

- git
- packer
- 以下のいずれかの実行環境
    - VirtualBox
    - VMware Fusion
    - Parallels Desktop

## 使い方

### ISUCON7予選

```
git clone --recursive --depth=1 https://github.com/matsuu/packer-isucon
cd packer-isucon/bento/ubntu
# parallels
packer build --only=parallels-iso ../../isucon7-qualifier.json
# virtualbox
packer build --only=virtualbox-iso ../../isucon7-qualifier.json
# vmware
packer build --only=vmware-iso ../../isucon7-qualifier.json
```

生成されたイメージはbento/builds/配下に出力されます。

## 参考

- [ISUCON](https://www.isucon.net)
- [matsuu/ansible-isucon](https://github.com/matsuu/ansible-isucon)
- [Packer](https://www.packer.io/)
- [bento](http://chef.github.io/bento/)
