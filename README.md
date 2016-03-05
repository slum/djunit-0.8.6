djunit 0.8.6 for eclipse 4.5.2 with osgi
====
# 説明
* "djunit 0.8.6 for eclipse 4.5.2"版を"Eclipse 2.0 Style Plugin Support" pluginなしで動くように修正したものです。
* djunit実行、coverage出力について確認済みです。
* djunit実行時には、「プロジェクトのプロパティ」→「djUnit」→「djUnit ClassLoader」タブ→「-noverify(VMオプション)を使用する」にチェックをいれてください。

# 動作条件
* "Eclipse IDE for Java Developers 4.5.2"

# インストール方法
* ZIPダウンロードして解凍後、「ecilpse/dropins」に配置してください。

```
dropins
└─djunit-0.8.6
    └─eclipse
        └─plugins
            └─jp.co.dgic.eclipse.jdt.djunit_0.8.6.xxxxxxxx
```

# 修正内容
* プラグインエクスポート時に日付を付けるように修正。
* eclipse project設定追加
* "plugin.xml"の一部を"META-INF/MANIFEST.MF"へ移動
* "META-INF/MANIFEST.MF"から"org.eclipse.core.boot"の削除
* "jp.co.dgic.eclipse.jdt.internal.junit.ui.DJUnitPlugin"引数なしのコンストラクタ追加。プラグインロード失敗に対応するため。
* メッセージリソースを"OSGI-INF/l10n"へ移動。

# 開発環境
* Eclipse for RCP and RAP Developers 4.5.2(mars2)

# 確認環境
* Eclipse IDE for Java Developers 4.5.2(mars2)

# ダウンロード先
* [eclipse mars2 ダウンロード](http://www.eclipse.org/downloads/packages/eclipse-ide-java-developers/mars2)
