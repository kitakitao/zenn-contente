---
title: "非情報系神経科学者の初Zenn投稿。バイブコーディングを添えて"
emoji: "🧠"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["python", "chatgpt", "github", "vscode", "neuroscience", "初心者向け"]
published: false
---

# バイブコーディングって？

以下chatGPT先生の回答

「**バイブコーディング**」とは、**自分のノリ（vibe）で楽しくコードを書く**スタイル。  
完璧さや理論から入るのではなく、音楽を聴きながら直感的に手を動かすのが特徴です。


私は普段、神経科学系の研究で行動実験や電気生理データ解析をしています。  
その解析を少しでも自動化したいと思い、最近Pythonを触り始めました。  
どうせなら楽をしたいと思い、ChatGPTとGitHubを組み合わせて「バイブコーディング」的にやってみた体験をまとめます。

---

# 環境構築

## 1. VS Code セットアップ
- [VS Code](https://code.visualstudio.com/) をインストール  
- 拡張機能を追加：
  - Python  
  - GitHub Pull Requests and Issues  
  - （お好みで）GitLens  

## 2. GitHub リポジトリ作成
1. GitHubで新しいリポジトリを作成（例：`vibe-coding-python`）  
2. VS Codeからクローン  

リポジトリ名が微妙なのはご愛敬

```bash
git clone https://github.com/your-username/vibe-coding-python.git
cd vibe-coding-python
````


## 3. Python 仮想環境

```bash
python -m venv venv
source venv/bin/activate   # Mac/Linux
# venv\Scripts\activate    # Windows
```

これで解析やスクリプトをまとめる環境ができました。

---

# ChatGPTでコードを書いてみる

まずは練習として「リストの平均値を出すプログラム」を作成。

ChatGPTに聞いたら、こんなコードを提案してくれました：

```python
numbers = [10, 20, 30, 40, 50]
avg = sum(numbers) / len(numbers)
print("平均:", avg)
```

保存して実行すると：

```
平均: 30.0
```

一発で動く。このテンポ感が最高です。
研究でちょっとした計算をするときにも便利そう。

---

# 応用してみる

次は「ユーザー入力から平均値を出す」コード。

```python
def calculate_average():
    numbers = []
    print("数字を入力してください（終了するには'q'を入力）:")
    
    while True:
        user_input = input("数字: ")
        if user_input.lower() == 'q':
            break
        try:
            numbers.append(float(user_input))
        except ValueError:
            print("無効な入力です。数字を入力してください。")
    
    if numbers:
        avg = sum(numbers) / len(numbers)
        print(f"\n入力された数字: {numbers}")
        print(f"平均値: {avg:.2f}")
    else:
        print("数字が入力されませんでした。")

if __name__ == "__main__":
    calculate_average()
```

実行結果：

```
数字: 15
数字: 25
数字: 35
数字: q

入力された数字: [15.0, 25.0, 35.0]
平均値: 25.00
```

こういう簡単なツールを積み重ねていけば、解析の自動化に繋がると感じました。

---

# GitHubで記録を残す

コードができたらGitHubへコミット：

```bash
git add .
git commit -m "平均計算プログラムを追加"
git push origin main
```

リポジトリに反映され、学習や試行錯誤の記録が残ります。
研究ノート的に使えるのも魅力。

---

# やってみて思ったこと

* **良かった点**

  * ChatGPTで「とりあえず動くコード」がすぐ手に入る
  * GitHubに残すと成長の可視化になって達成感がある
  * VS Codeで補完もGit操作も完結できる

* **課題**

  * 仮想環境の有効化を忘れがち
  * コードを理解せずにコピペすると学びが薄い

---

# まとめ

* **バイブコーディングは「楽しく続ける」ためのマインドセット**
* **Python + ChatGPT** で「思いついたら即実行」が可能
* **GitHub + VS Code** で「積み重ねが見える化」

研究の本番解析にいきなり導入するのは難しいですが、
小さなツールから試すことでPythonに慣れつつ、解析自動化にも近づけると感じました。

ちなみにこの記事もLLMで7割くらい生成しました。
便利な世の中になりましたね。

```



