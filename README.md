# 情報通信ネットワーク　通信授業課題
### Git、GitHubについてのリサーチと実践

【出題】
---
### 1.Gitについて調べ、何をするツールで何が便利なのかなどを300～500字程度にまとめてください。


Gitとは、分散型のバージョン管理システム。
プログラミングのソースコードの他、開発用途以外にも、デザインやテキストなどでもバージョン管理のツールとして使用されている。
ソースコードなどファイルのバージョン管理にGitを使うメリットとしては下記が挙げられる。
・古いバージョンから新しいバージョンのファイルまで一元的に管理が可能であり、修正をするたびに新しいファイルを増やす必要がない。
・各ファイルの変更履歴を管理しているため、容易に古いバージョンへ戻すことができる。誤って上書きしてもすぐに任意のバージョンに戻せる。
・ネットワークを経由して、複数人でファイルや変更履歴を共有する機能があるため、チームでの共同開発が効率化。
・共同開発を行う際に役立つ機能が豊富（コピー/ブランチ/マージ等について簡易なコマンドでの実行が可能）。
上記より、Gitによってファイルを管理することで、チームでの開発時にソースコードが編集・上書きされても、
簡単に以前のバージョンへ戻すことができるため作業者は、安心してソースコードの更新作業を行える。
Linuxカーネルの開発者、リーナス・トーバルズが制作。

---

### 2.GitHubについて同様に調べ300～500字程度にまとめてください。

GitHubは、プログラムコードやデザインデータを保存・公開できるソースコード管理プラットフォームであり、世界中で利用が拡大している。
GitHubの本質は「Gitリポジトリのホスティングサービス」としての役割にある。Gitは分散型バージョン管理システムで、GitHubはそれをオンラインで共有・管理するためのプラットフォームという位置づけである。
主なメリットは以下の通りとなる。
開発業務の効率化：GitHubはソースコードの共有や管理を容易にし、複数人での共同作業を支援する。また、複数バージョンの管理や作業スペースの分割も可能で、作業の同時進行がスムーズに行える。
質の高いコード作成：GitHubにはプルリクエストやコメント機能があり、プログラマー同士のコードレビューを促進。フィードバックを得てコードの改善が図れ、プロジェクトマネージャーとの共有も容易なため、進捗管理と質の向上が期待できる。
活発なコミュニティ：GitHubには公式フォーラム「GitHub Community」があり、質問や回答を通じて技術的な課題解決が可能で、他のリポジトリ内でもユーザー同士の交流や協力が行われている。

-------------------------------------------------------------------------

### 3.Markdownについて同様に調べ300～500字程度にまとめてください。

Markdownとは、シンプルで読みやすい書式の記法を用いて、テキストを装飾する軽量マークアップ言語である。
（マークアップ言語：テキストに「構造」や「意味」を付与するための記述方法で、特定の記号やタグを使って文章内の情報に装飾や意味付けを行う言語のこと。マークアップ言語を使うと、見出しや段落、リンク、画像などのレイアウトや装飾を定義できる。代表的な例として、HTMLやXMLがある。）
通常のテキストファイルに記述しやすく、記号や記法を使って見出し、リスト、リンク、強調（太字や斜体）などを簡単に表現できることが特徴。たとえば、「#」を先頭に書くことで見出し、「-」を使ってリストを表現するなど、HTMLのようなタグを使わずに、読みやすい状態で構造を示せる。
MarkdownはGitHubやGitLabなどのプラットフォーム、ブログ、Wiki、ドキュメント作成ツールなど多くの場面で利用されており、書いた内容がそのまま見た目に近い形で確認できることから、特にエンジニアやライターにとって人気がある。


---

### 4.
1～3を1つのテキストREADME.mdとしてまとめ、自分のGitHubアカウントにmau-j2nという名前のレポジトリを作成し
https://github.com/kanoxi/mau-j2n
で閲覧できるように対応。

---

<br><br><br>

### 5.1～4までの実現に必要となった作業（ソフトウェアのインストール、コマンドの入力、実行結果、起こったエラー、自分の立てた仮設、わかったことなど）について記録を下記の順番でREADME.mdに追記しGitHubに公開してください。

### README.md記録の内容と順番
---
- gitとは　→バージョン管理ツール

- gitインストール<br>
gitのインストールの有無を確認
Windowsのコマンドプロンプト"git --version"を確認。
gitのバージョンが表示されずエラーとなったら、インストールされていないため、gitをダウンロードしインストールしていく<br>
gitのインストーラーをダウンロード
ウェブブラウザからgit for windowsで検索、
https://gitforwindows.org
からgitインストーラーをダウンロード
ダウンロードしたファイル（Git-2.47.0.2-64-bit.exe）を開きインストールを実行
<br>


<br>
インストールの確認
インストールができたら、下記いずれかを起動  

- <u>コマンドプロンプト</u>　基本的なCLI操作。歴史が長いが、機能が限定的。  
- <u>PowerShell</u>　Windows管理タスクに強い。オブジェクト指向のコマンドが使える。  
- <u>Git Bash</u>　Gitのインストール時に付属するUnixライクなシェル。Linuxコマンドも使える。  


git --versionと入力、バージョン情報が表示される

※インストール時に、Gitの実行ファイルgit.exeみたいなファイルの、どこかに置かれたパスが、PATH環境変数に書き込まれたから、コマンドプロンプト、パワーシェル、あるいはgit bashでgit と打ち込むだけで、そのプログラムを実行できる
参考:PATHを通すとは  
https://qiita.com/sta/items/63e1048025d1830d12fd


<br>

- gitセットアップ
Gitへユーザー名とメールアドレスの設定

設定  
git config --global user.name "ユーザー名は任意"  
git config --global user.email "メールアドレス"  
確認  
git config user.name
git config user.email
git config --list
cat ~/.gitconfig

※変更したい場合、同様の作業をすることで上書き  
ここでは、それぞれ、Kano、kanoysyk@gmail.comに設定  
Git BashとPower Shellで登録されたことを確認



- gitの使い方  
         git init　リポジトリを初期化（新しいGitプロジェクトを作成）  
         git add　変更したファイルをステージングエリアに追加  
         git commit　ステージングエリアの変更を履歴として記録  
         git push　ローカルの変更をリモートリポジトリに反映  
<br>

---
<br>  
  
- githubアカウントの作成  
下記サイトからサインアップしアカウントを作成  
https://github.com    
  
    
<br>

--- 


- ### githubへのREADME.mdの公開方法
基本的な流れ

1. #### ローカルリポジトリの新規作成
対象のディレクトリに移動してからgit initコマンドにて初期化  
そうするとローカルに.gitという隠しフォルダのリポジトリが作成される


2. #### ファイルを編集
今回はVSCodeを用いマークダウン形式で記述  


3. #### ファイルの変更をステージングエリアへ追加
git add ファイル名  
git add .指定するとディレクトリの全部のファイルが追加されて便利  
例：git add hello.txt


4. #### ローカルリポジトリにコミットを作成
git commit<br>
コミットメッセージを入力する画面が開かれる（Vim、VSCodeなどインストール時に選択したエディター）  
git commit -v だと、変更箇所がわかりやすい

その他、git commit -m "Added hello.txt"　コミットメッセージ（変更の説明）を直接コマンドラインで指定

1行目：変更内容の要約  
2行目：空行  
3行目：変更した理由  
cf.Gitのコミットメッセージには何を書くべきか？  
https://www.engilaboo.com/git-commit-message/  
コードには How  
テストコードには What  
コミットログには Why  
コードコメントには Why not  
○○を追加、などと見てわかる自明を記載するな、理由を書き残せ！


5. リモートリポジトリにプッシュ
例：git push origin main

GitHubにログイン
New repositoryをクリックしてGitHubにリポジトリを作成  
…or push an existing repository from the command line　このメッセージの下記を実行  

git remote add origin https://github.com/kanoxi/GitTest.git　※gitにGitHubを登録するコマンド  

git branch -M main　※現在のブランチの名前をmainに変更するコマンド  

git push -u origin main　※プッシュする（はじめてプッシュする場合）  
-u とすると、今後このリポジトリでgit pushと入力するだけで、このリモート（origin）とブランチ（main）にプッシュされるよう追跡設定を行う。
つまり次回からは短縮コマンド git pushでOK。

GitHubのブラウザをリロードし、プッシュされたか確認

---
---

<br>

以下メモ  

<br>

#### gitインストーラーのメッセージ
1. Welcome to the Git Setup Wizard　GNU General Public License　GNU（グヌー）ライセンスの同意　Next
2. Select Destination Location　インストール先フォルダの選択。　特に問題なければNext
3. Select Components　Gitに含まれる機能を選択。　デフォルトで問題なければNext
4. Select Start Menu Folder　スタートメニューのフォルダ選択。　デフォルトで問題なければNext
5. Choosing the default editor used by Git　Gitで使用するデフォルトエディターの選択
　　デフォルトではVim、Use Visual Studio Code as Git's default editorを選択、Next
6. Adjusting the name of initial branch in new repositolies　新しいレポジトリ作成時のブランチ名の選択
　　Override the default name and specifyで自分で好きな名前を指定でるほうを選択、Next
7. Adjusting your PATH environment　WindowsのPATH環境変数の設定
　　デフォルトの真ん中を選択　Git from the command line and also from 3rd-party software: コマンドプロンプトやPowerShellでもGitを使えるようにする。
8. Choosing the SSH executable　Gitのインストール中にSSH（Secure Shell）接続を行うためのプログラム（実行ファイル）を選択する画面です。これは、リモートリポジトリ（例：GitHub、GitLabなど）との通信にSSHを使う際に使用されるSSHクライアントを指定する設定です。
　　Use bundled OpenSSH　デフォルトのまま選択。
　　Gitに付属しているOpenSSHを使用。Git for Windowsに標準で含まれるSSHクライアント。
　　SSHとは？
　　**SSH（Secure Shell）**は、安全にリモートサーバーと通信するためのプロトコルです。
		- Bashはシステム操作やスクリプト実行に使うシェルで、主にローカルで利用します。
		- SSHはリモートコンピュータやサーバーに安全に接続し、リモートでBashなどのシェルを操作するために使うプロトコルです。
		- 両者は補完的な関係にあり、SSHを使ってリモートサーバーに接続し、その先でBashを利用することが一般的です。
	Gitでは、HTTPSまたはSSHを使ってリモートリポジトリと通信しますが、SSHは認証やセキュリティの面でよく利用されます。  
　　特徴
	- Gitに付属のOpenSSHを使用するため、追加の設定やソフトウェアのインストールが不要です。
	- 多くのチュートリアルやドキュメントで説明されている標準的な方法。
	メリット
	- 簡単に使える。
	- 他のソフトに依存しないため、動作が安定しています。
	デメリット
	- Windows特有のソフト（例：PuTTY）を使いたい場合には適しません。
	- 初心者や標準的な使い方をする場合、「Use bundled OpenSSH」を選択するのが最適です。Gitに付属しているSSHクライアントは、GitHubやGitLabとの接続で十分に機能します。
	サーバーを操作したい場合、まずはSSHを使ってリモートサーバーに接続したら、その先でBashを利用してコードで指示する
9. Chooseing HTTPS transport backend　リモートリポジトリに接続する際の設定。
	HTTPS通信の設定
	画面内容
	Use the OpenSSL library（OpenSSLを使用）: 独自のSSL証明書管理。
	Use the native Windows Secure Channel library（Windowsの証明書ストアを使用）: Windowsのセキュリティ設定を利用。
	デフォルトのUse the OpenSSL libraryを選択、Next
	ただしAI曰く、初心者には「Use the native Windows Secure Channel library」を選ぶのがおすすめです。
10. Configuring line ending conversions
    改行コードの設定
    画面内容
    Checkout Windows-style, commit Unix-style: WindowsでCRLF、UnixでLFに変換。
    Checkout as-is, commit Unix-style: チェックアウト時はそのまま、コミット時にLFに変換。
    Checkout as-is, commit as-is: 変換しない。
    一番下の変換しないを選択、Next
    ただしAI曰く、Windowsユーザーは「Checkout Windows-style, commit Unix-style」が一般的です。選択後、Nextをクリックします。
11. Configuring the terminal emulator to use with Git Bash　Git bashで使用するターミナルの選択
	ターミナルエミュレーターの設定
	画面内容
	Use MinTTY (default terminal): Git BashでUnix風のターミナルを使用。
	Use Windows' default console window: Windows標準のコマンドプロンプトを使用。
	「Use MinTTY (default terminal)」を選ぶのがおすすめです。選択後、Nextをクリックします。
12. Choose the default behavior of 'git pull'　git pullの挙動の設定
	特別な理由がなければDefaultのままでNext
13. Choose a credential helper　資格情報マネージャーの選択
	特別な理由がなければDefaultのままでNext
14. Configuring extra options
	Gitの構成に関する追加オプションの設定
	Enable file system caching（ファイルシステムキャッシュの有効化）
	Enable symbolic links（シンボリックリンクを有効化）
	特別な理由がなければDefaultのままでNext
15. Configuring experimental options
	現在開発段階の機能を追加するかどうかの選択、意図しない動作の可能性があるため、チェックをしない


<br>

#### echoコマンドを使ったテキストファイル作成方法
例：echo"Hello, World!" > hello.txt  
echo ：文字列を出力するコマンド  
1. echo "Hello, Git!"　→ ターミナルに "Hello, Git!" と表示  
2. echo "Hello, Git!" > file1.txt　→リダイレクト記号（>）があると  
-  指定したファイルに新しく内容を書き込みます（既存の内容は上書きされます）。  
-  ファイルが存在しない場合は、新しく作成されます。

3. echo "Another line" >> file1.txt　→>>だと、既存のファイルに追記します（上書きしません）。
file1.txt の最後に "Another line" が追加されます。

<br>

#### Powershellについて
Powershellで ls -aとするとエラー  
PowerShellはUnix系システムと同じコマンドを模倣するように設計されていますが、実際にはWindows環境に特化しているため、完全に同じ挙動にはなりません。  
そのため、-Forceや-AttributesのようなPowerShell特有のオプションを覚えて使うことが重要です。

---
以上


