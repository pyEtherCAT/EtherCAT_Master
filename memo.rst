=============================================================
EtherCAT 開発用メモ
=============================================================


冗長性について
-----------------------------------------------------------

- EtherCATの冗長性はLANをループする形で得ることが出来るが、ただ単にLANケーブルを２分岐する形では駄目っぽい。謎。

各フレームについて　まとめメモ
-----------------------------------------------------------

:自動インクリメント: 自動でインクリメントされたアドレスにアクセスすることが出来る。
:設定アドレス: EtherCATが起動後にマスターから渡されたアドレスすることが出来る。
:ブロードキャスト: 接続されているスレーブ全体にアクセスすることが出来る。
:理論メモリ: 接続されたスレーブを一つのメモリ空間としてアクセスすることが出来る。
:マルチライト: よくわからん

:APRD: 自動インクリメント物理リード
:APWR: 自動インクリメント物理ライト
:APRW: 自動インクリメント物理リードライト
:ARMW: 自動インクリメント物理リード・マルチライト

:FPRD: 設定アドレス物理リード
:FPWR: 設定アドレス物理ライト
:FPRW: 設定アドレス物理リードライト
:FRMW: 設定アドレス物理リード・マルチライト

:BRD: ブロードキャストリード
:BWR: ブロードキャストライト
:BRW: ブロードキャストリードライト

:LRD: 理論メモリリード
:LWR: 理論メモリライト
:LRW: 理論リードライト

自動インクリメント時のアドレスについて
-----------------------------------------------------------

Master -> Slave1 -> Slave2 -> Slave3

Master 
Slave1 = 0x0000
Master = 0xFFFF
Master = 0xFFFE

