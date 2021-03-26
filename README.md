# 概要

- [実践Rustプログラミング入門](https://www.amazon.co.jp/%E5%AE%9F%E8%B7%B5Rust%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%9F%E3%83%B3%E3%82%B0%E5%85%A5%E9%96%80-%E5%88%9D%E7%94%B0-%E7%9B%B4%E4%B9%9F/dp/4798061700/ref=pd_lpo_14_t_0/357-0106208-0618610?_encoding=UTF8&pd_rd_i=4798061700&pd_rd_r=9cbd1402-6438-4519-9f3f-5238ec8e60f5&pd_rd_w=fv0Sa&pd_rd_wg=DGyhV&pf_rd_p=cb2cef9d-b0a3-4b58-a575-45abfc5e07e8&pf_rd_r=BV7DJ3R9WGQVKDKWJZ86&psc=1&refRID=BV7DJ3R9WGQVKDKWJZ86) [Chapter8の写経](https://github.com/forcia/rustbook/tree/master/ch08)
- あらかじめクロスコンパイル環境の構築とQEMUでのエミュレータ環境構築(dockerインストール含む)が必要。
- エミュレータ環境はDockerfileで記述。
# クロスコンパイルの環境構築
```sh
$ rustup target add thumbv7em-none-eabi
$ cargo install cargo-binutils
$ rustup component add llvm-tools-preview
$ cargo add cortex-m-rt cortex-m-semihosting panic-halt
```

# 参考
- [Ubuntu 20.04へのDockerのインストールおよび使用方法](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04-ja)
