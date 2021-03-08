# 6-2. 軽量で多機能なフルスタックフレームワークMicronaut

## 必要なもの

- Micronaut CLI
    - SDKMANを使ったインストールが推奨されている。


# 準備手順

## SDKMANのインストール

参考: https://sdkman.io/install

Bashが使える環境で下記を実行する。
```
$ curl -s "https://get.sdkman.io" | bash
$ source "$HOME/.sdkman/bin/sdkman-init.sh"
```
最後に`$ sdk version`を実行して、  
`sdkman 5.0.0+51`等のバージョン情報が表示されればOK.

Windows環境の場合、通常ではBashが使えないので以下の何れかで対応します。

- Windows Subsystem for Linux (WSL)を利用する。
- CygwinやGit Bash forWindowsといったツールを導入する。

## Micronaut CLIのインストール

参考: https://micronaut-projects.github.io/micronaut-starter/latest/guide/#installation

sdkmanが使える環境で下記を実行する。
```
$ sdk update
$ sdk install micronaut
```

## アプリケーションの雛形を生成

Micronaut CLIが使える環境で下記を実行する。
```
mn create-app minjava.frameworks.micronaut.micronaut-samples
./gradlew shadowJar
java -jar build/libs/micronaut-sample-0.1-all.jar
```