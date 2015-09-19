Key Words:Shared memory, Interprocess communication, boost, C++.

boostライブラリを利用したプロセス間通信をします．

<動作確認した環境>
Windows 7 Professional SP1，CPU 3.40GHz，RAM 8.00GB，64bit，Visual C++ 2010．

<使用するための初期設定>
プロパティシート"boost.props"の[共通プロパティ]→[ユーザーマクロ]の"BOOSTROOT"を，お使いの環境におけるboostのディレクトリ("stage"というファイルが存在する位置)に変更してください．
ビルド環境をDebugにすると次のエラーが発生し，正常な動作をしません．Releaseに設定してください．
	IntelliSense: #error ディレクティブ: "Incompatible build options"

<ソースファイル>
include\shared_memory.h

<サンプルプログラム>
<アプリケーション間の通信>
Release\app1.exe
Release\app2.exe
異なるアプリケーション間でデータを相互通信します．
片方を実行すると待機状態になり，もう一方を起動するとデータの相互通信が実行されます．
	
<スレッド間の通信>
Release\multi_thread.exe
マルチスレッド処理において，スレッド間でデータを相互通信します．
アプリケーションを実行すると2つのスレッドごとにデータの送信・受信を一定周期で行い，コンソールに出力します．
