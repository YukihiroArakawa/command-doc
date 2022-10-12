# NeoVim
- configの場所は ~/.config/nvim/init.vim
- 起動コマンド: nvim
- vi, vimを起動してもnvimが起動するように設定すると便利

```
$ vim ~/.zshrc

# 以下を追加
alias vi="nvim"
alias vim="nvim"
alias view="nvim -R"

$ exec zsh
```

- view pathで開くとread onlyで開くことが可能
- ctrl + rでredo
- number ddでnumber行削除
- yyで1行コピー
- Pで現在行にコピー
- pで下にペースト
- 2 yyで2行コピー
- .でrepeat
- :!!で前のコマンドを実行
- :!でコマンド実行
- ブラケットを２回押しすると段落・セクションにジャンプできる
- ctrl + oで移動前に戻る
- Jで行の連結. 下の行が上に来る
- コメントの挿入
  - 先頭に  :norm I# (ノーマルモードでインサート#)
  - 行末    :norm A# 

- コンフィグ設定
  - vim ~/.config/nvim/init.vim

## Vimのプラグイン
- vim-plug入れればOK https://github.com/junegunn/vim-plug
- :PlugInstallでプラグインをインストールできる
- nerd tree, ツリー表示をterminalの横っちょに出すプラグイン
  - :NERDTreeでツリーに入る, 
  - ctrl + w + wで開いたファイルからツリーに戻る
  - :qで戻る
- FizzyFinder
  - ファイルを高速に検索するプラグイン
  - https://github.com/junegunn/fzf 
  - terminalからfzfで実行して検索できる
  - nvimの場合は:FZFで呼び出せる
  - カレントディレクトリ以下を検索することに注意
- vim-fugitive: gitをnvimから使えるようにするプラグイン
  - https://github.com/tpope/vim-fugitive
  - installation
  ```terminal
    mkdir -p ~/.config/nvim/pack/tpope/start
    cd ~/.config/nvim/pack/tpope/start
    git clone https://tpope.io/vim/fugitive.git
    vim -u NONE -c "helptags fugitive/doc" -c q
  ```
  - :Git blameでgit blameを開ける
  - 他にも開ける
- vim-gitgutter
  - nvimから簡単にdiffを見れる？
- vim-commentary
  - 複数行コメントアウトするプラグイン
  - installation
  ```terminal
    mkdir -p ~/.config/nvim/pack/tpope/start
    cd ~/.config/nvim/pack/tpope/start
    git clone https://tpope.io/vim/commentary.git
    vim -u NONE -c "helptags commentary/doc" -c q
  ```
  - vimのビジュアルモードでgcとうつとコメントアウトできる
- vim-polyglot
  - 見た目を変えられるやつ
  - https://github.com/sheerun/vim-polyglot 
- coc.nvim
  - 補完をしてくれるやつ
  - :CocInstall coc-pythonみたいな感じで言語毎の補完を入れられる
