# 2025BeginnerTrainingGit
株式会社MIXI 新卒向けGit研修リポジトリ

Gitの内部構造の説明に使用します。
本リポジトリをcloneした後に、以下のコマンドを実行して、packファイルを解凍してください。ファイル名などは適宜読み替えてください。

```cmd
mkdir temp && cd temp
git init
git unpack-objects <  ../2025BeginnerTrainingGit/.git/objects/pack/pack-xxx.pack
find .git/objects -not -name 'pack' -a -not -name 'info' -type d -mindepth 1 | xargs -I {} mv {} ../2025BeginnerTrainingGit/.git/objects/
cd ../2025BeginnerTrainingGit
```

これにより、packファイルに圧縮された内容が、.git/objects下に展開されます。
