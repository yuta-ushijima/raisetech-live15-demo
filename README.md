# raisetech-live15-demo
CircleCIで下記のworkflowを実行するサンプルリポジトリです。

## Workflow
1. リポジトリにコードをpush
2. CircleCIがリポジトリにpushされたことをイベントトリガーとして、workflowを実行
3. 最初のworkflowとしてCloudformationを実行
4. 2番目のworkflowとしてCloudformationによって作成されたAWS環境に対して、ansibleを実行
5. 3番目のworkflowとしてServerspecで自動テストを実行する

## 環境
### aws cli
```
$ aws --version
aws-cli/2.9.8 Python/3.9.11 Linux/5.15.0-1021-aws exe/x86_64.ubuntu.22 prompt/off
```

### ansible
```
$ ansible --version
ansible 2.10.7
```

### ruby
```
image: 'cimg/base:stable'
```
