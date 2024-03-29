---
title: Dynamics AX プラットフォーム更新プログラム 1 (2016 年 5 月) の新機能および変更された機能
description: この記事では、Microsoft Dynamics AX プラットフォーム更新プログラム 1 の新機能または変更された機能について説明します。 このバージョンは 2016 年 5 月にリリースされ、ビルド番号は 7.0.4127.16103 です。
author: sericks007
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.custom: 91183
ms.assetid: 259a6844-3675-44bd-a4ea-57a5976628ff
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 4f5d6e839abf29dbc21a55673a84cfff7e7d0d18
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283205"
---
# <a name="whats-new-or-changed-in-dynamics-ax-platform-update-1-may-2016"></a>Dynamics AX プラットフォーム更新プログラム 1 (2016 年 5 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics AX プラットフォーム更新プログラム 1 の新機能または変更された機能について説明します。 このバージョンは 2016 年 5 月にリリースされ、ビルド番号は 7.0.4127.16103 です。

## <a name="platform-compatibility"></a>プラットフォーム互換性

| 何ができますか。 | これは、なぜ重要ですか。 |
|------------------|------------------------|
| アプリケーションをアップグレードせずに、Dynamics AX プラットフォームを新しいリリースにアップグレードします。 | Dynamics AX プラットフォームは、Dynamics AX 7.0 (2016 年 2 月) バージョン以降、Dynamics AX アプリケーションの以前のバージョンと互換性が確保されるようになりました。 したがって、アプリケーション全体をアップグレードしなくても、プラットフォームの最新の機能を最新の状態に保つことができます。 今回のリリースでは、プラットフォームは Dynamics AX 7.0 (2016 年 2 月) リリースと機能的に互換性があります。 ただし、まだ完全にバイナリと互換性があるわけではないため、プラットフォームの更新後に引き続きコードをコンパイルする必要があります。 プラットフォームをアップグレードする機能は、アプリケーション プラットフォーム、アプリケーション ファウンデーション、ディレクトリ、およびテスト エッセンシャルのいずれのモデルにも重ならないアプリケーションでのみ使用できます。 |

## <a name="development-and-customization"></a>開発とカスタマイズ

<table>
<thead>
<tr>
<th>何ができますか。</th>
<th>これは、なぜ重要ですか。</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>InternalsVisibleToAttribute</strong> 属性を適用して、他のモデルからの消費のために内部を開きます。</td>
<td>超過レイヤーのモデルをロックすると、コンポーネントがモデルの内部になり実装の詳細を外部呼び出しからより確実に分割されます。 ただし、他のモデルを内部へのアクセス権を持つ「フレンド」としてマークするのは有利な場合があります。 この機能は、主にテスト シナリオに役立ちます。 このためには、<strong>InternalsVisibleTo</strong> タグが、内部コードを含むモデルの記述子 XML ファイルに適用されます。</td>
</tr>
<tr>
<td>オーバーレイを禁止するモジュールを有効にします。</td>
<td>ソフト ロックとハード ロックの 2 つのフェーズで、超過レイヤーのモデルをロックできるようになりました。 ソフト ロックを行うと、オーバーレイヤーの発生が警告として扱われます。 ハード ロックはエラーとして扱われるオーバーレイの発生を引き起こし、モデルのビルドがブロックされます。 ハード ロックを使用するときは、オーバーレイを実行できません。</td>
</tr>
<tr>
<td><strong>カスタマイズ分析</strong>レポートで、カスタマイズ分析のベスト プラクティス ルールを文書化します。</td>
<td><strong>カスタマイズ分析</strong>レポートの新しい列では、独立系ソフトウェア ベンダー (ISV) によって、特定のルールが非表示になっている理由を文書化できます。</td>
</tr>
<tr>
<td><strong>InternalUseOnly</strong> 属性を使用して、将来的に内部としてマークすべきアーティファクトを特定します。</td>
<td>新しい <strong>InternalUseOnly</strong> 属性が X++ 言語に追加されました。 X++ コンパイラは、この属性で修飾されたコンポーネントが現在のモデルの外部で参照される状況に警告の診断を下します。 この属性は、成果物を<strong>内部</strong>キーワードでマークする代わりに、チームがまだビルドを行っている間に不正な参照を取り除く時間をチームに与えるという利点があります。</td>
</tr>
<tr>
<td>X++ コードの編集用に Microsoft Visual Studio 2015 ダーク テーマを選択します。</td>
<td>ダーク テーマでは、コード編集の視覚的品質が向上しました。 <strong>ツール</strong> &gt; <strong>オプション</strong> &gt; <strong>環境</strong> &gt; <strong>一般</strong> &gt; <strong>色のテーマ</strong> でテーマを選択します。</td>
</tr>
<tr>
<td>拡張機能を通じて拡張データ型 (EDT) をカスタマイズします。</td>
<td>拡張機能によって EDT をカスタマイズすることができるようになりました。 ただし、現在の配列要素を追加します。</td>
</tr>
<tr>
<td>フォーム拡張のコントロール上にある<strong>テキスト</strong> プロパティをカスタマイズします。</td>
<td>一部のコントロール (ボタンなど) には、<strong>ラベル</strong> プロパティの代わりに <strong>テキスト</strong> プロパティがあります。 拡張機能によってこれらのプロパティをカスタマイズすることができるようになりました。</td>
</tr>
<tr>
<td>既存のメニュー項目または拡張機能によって埋め込まれたメニューを非表示にします。</td>
<td>拡張機能で <strong>表示</strong> プロパティを設定できるようになりました。</td>
</tr>
<tr>
<td>クエリを拡張します。</td>
<td>以下の方法で、クエリを拡張することができるようになりました。
<ul>
<li>既存のデータ ソースに範囲を追加します。</li>
<li>既存のデータ ソースに新しい (埋め込み) のデータ ソースを追加します。</li>
<li>既存のデータ ソースに新しいフィールドを追加します。</li>
</ul></td>
</tr>
<tr>
<td>クラスの拡張機能に、インスタンスと静的メソッド、インスタンスと静的状態を追加します。</td>
<td>拡張メソッドが拡張され、インスタンス メソッド、静的メソッド、インスタンス状態、および静的状態を Dynamics  AX コンポーネントに追加することができます。 今回のリリースでは、サポートはクラスの強化に限定されます。</td>
</tr>
<tr>
<td><strong>グローバル</strong> 拡張機能を使用して、最上位レベルの機能を追加します。</td>
<td>クラスの新しい拡張モデルにより、静的メソッドを追加できます。 静的メソッドが<strong>グローバル</strong> クラスの拡張に追加された場合、そのメソッドは X++ 言語の関数として使用可能になります。 したがって、その結果を達成するために、オーバーレイは必要なくなりました。</td>
</tr>
<tr>
<td>会社切り替え警告のオプトアウト。</td>
<td>DataAreaID でサポートされているテーブルからの会社間データを表示するフォーム上の行を切り替えると、会社を変更することに関する警告が表示されます。 デザイナーでのデザイン時に、または API メソッド介した実行時に、フォームごとの動作を選択することができます。</td>
</tr>
<tr>
<td>最終的な検証を実行するイベントをサブスクライブします。</td>
<td>新しいイベント FinalDataValidation は、FinalDataValidation イベントを順番に呼び出します。 このイベントは、AOS によってデータベースに適用される前に、データとアクションの最終的な検証として機能します。</td>
</tr>
</tbody>
</table>

## <a name="monitoring-and-telemetry"></a>モニタリングとテレメトリー

| 何ができますか。 | これは、なぜ重要ですか。 |
|------------------|------------------------|
| システム上で実行される最も高価なクエリについて把握します。 | **環境の監視** ページの **SQL インサイト** ビューには、期間、論理入出力 (I/O)、CPU 時間、および実行カウントに基づいて、最もコストのかかるクエリの履歴データが表示されます。 追加の分析とクエリのチューニングを行うことができるように、実行計画をダウンロードするオプションがあります。 |
| 事前に定義されたクエリを使用して、問題をすばやくトラブルシューティングします。 | **環境監視ページ** の **未加工のログの表示** ビューには、システム障害、デッドロック、エラー、バッチの調整の問題、**管理レポート** モジュールの問題など、特定の問題のトラブルシューティングに使用できる新しいクエリがあります。 |
| 環境内で発生したシステムの失敗に関する情報を取得します。 | LCS 内の **監視** セクションに、**推奨される修正方法を表示** リンクが追加され、発生回数と問題を修正する修正プログラムをダウンロードするオプションと共に、環境で発生したシステム障害の一覧が表示されます。 |

## <a name="web-client"></a>Web クライアント

<table>
<thead>
<tr>
<th>何ができますか。</th>
<th>これは、なぜ重要ですか。</th>
</tr>
</thead>
<tbody>
<tr>
<td>フィールドまたはボタンのラベルの上にマウス ポインターを置くにことによって、ページ上のフィールドやボタンの便利な説明を参照してください。</td>
<td>この機能により、ユーザーはページ フィールドに関連する重要なビジネス情報をより簡単に学習し理解できます。 したがって、Dynamics AX を使用すると生産性が向上します。</td>
</tr>
<tr>
<td>フィールドの説明をカスタマイズおよび追加する。</td>
<td>ソリューションに固有のフィールド説明を追加、または会社のポリシーに関連する情報を追加することができます。</td>
</tr>
<tr>
<td>強化グリッドを使用して &quot;ヘッド ダウン&quot; データ入力を実行します。</td>
<td>Dynamics AX グリッド コントロールには、実行時に使用可能な <strong>fastEdit</strong> プロパティが追加されました。 このプロパティが有効になると、グリッドと前後のページは、ユーザー入力の承認と検証のみに特化します。 したがって、このプロパティを使用して最適化された「ヘッドダウン」データ入力エクスペリエンスを作成できます。 アプリケーション コードが、通常は、グリッドの <strong>init()</strong> メソッドで、実行時に <strong>fastEdit</strong> プロパティを設定すると (たとえば、<strong>MyGridInstance.fastEdit(true)</strong>)、クライアント側のグリッドはユーザー入力の受け入れの処理に専念します。 検証はキューに追加され、ユーザーがインタラクティブな一時停止を指定する場合にのみ実行されます。 このモードでは、<strong>gotFocus()</strong>、<strong>lostFocus()</strong>、<strong>enter()</strong>、<strong>leave()</strong> などは呼び出されず、ルックアップ制御をエンド ユーザーは使用できません。 <strong>fastEdit</strong> プロパティは、特殊なアプリケーション定義の既定値エントリまたは複数の依存フィールド検証を提供しないグリッドでのみ使用してください。</td>
</tr>
<tr>
<td>個人用設定を通じてワークスペースを作成します。</td>
<td>ダッシュ ボードからは、<strong>個人用設定</strong> &gt; <strong>ワークスペースの追加</strong>を右クリックし選択できるようになります。 ワークスペース タイルは、ダッシュ ボードに追加されます。 ワークスペースの名前を入力することにより、このタイルを個人用に設定することができます。 次に、タイルをクリックして、他のワークスペースのコンテンツをパーソナライズできるように、コンテンツをパーソナライズできる新しい空のワークスペースを開きます。</td>
</tr>
<tr>
<td>詳細ページからワークスペースへのリンクを追加します。</td>
<td>以前は、リスト ページからワークスペースにフィルター処理されたリストまたはタイルを保存できました。 また、リストをワークスペース上のリンクとして保存することができるようになりました。</td>
</tr>
<tr>
<td>ページ情報とコントロール情報を表示します。</td>
<td>ショートカット メニューにより要素の技術詳細を表示できます。 ショートカット メニューに、<strong>フォーム名</strong> と <strong>コントロール名</strong> のメニュー項目がある <strong>フォーム情報</strong> メニュー項目が追加されました。 <strong>フォーム名</strong>をクリックすると、現在のコントロールと現在のページに関する情報を提供するダイアログ ボックスが開きます。 開発者が<strong>コントロール名</strong>をクリックすると、Microsoft Visual Studio が起動し、現在のページとコントロールのメタ定義が開きます。</td>
</tr>
<tr>
<td>デバイスとブラウザー ビューポートの間でのページ要素の反応性の改善を参照してください。</td>
<td>Dynamics AX はさまざまなサイズのビューポートで実行されるため、使用可能な領域に対してページ コンテンツを正しく配置することが重要です。 次の点が変更されています。
<ul>
<li>オーバーフロー ボタンが、ツールバーや、ビューポートの使用可能な幅に合わないアクションのナビゲーション バーで使用可能になりました。</li>
<li>メッセージ ボックス コンテンツは、利用可能な幅に基づいてサイズ変更されるようになりました。</li>
<li>利用可能な幅に基づいて、さまざまなウィンドウ (ナビゲーション ウィンドウ、フィルター ナビゲーション、ナビゲーション リスト、FactBox ナビゲーション、別のナビゲーション) が自動的に折りたたまれます。</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="data-management-and-integration"></a>データの管理および統合

| 何ができますか。 | これは、なぜ重要ですか。 |
|------------------|------------------------|
| 同じ Dynamics AX 配置内の複数の企業間で参照データおよびグループ データを複製することで、企業間のデータ共有をコンフィギュレーションします。 | この機能により、複数の企業の設定プロセスをはるかに簡単にできます。 たとえば、すべての会社が同じ支払日オプションを使用する場合、1 つの会社でのグループ設定をコンフィギュレーションし、それから展開内の他の会社に複製できます。 |
| ファイルまたはデータ パッケージを使用してデータをインポートする前に、エンティティ内のデータを切り詰めるように選択します。 | データ シナリオのインポートについては、管理者は、ファイルまたはデータ パッケージを使用してデータをインポートする前に、エンティティ内のデータを切り詰めるように選択できます。 この機能により、顧客はどの環境でも構成データを元のデータセットに簡単にリセットできます。 |

## <a name="analytics"></a>分析

<table>
<thead>
<tr>
<th>何ができますか。</th>
<th>これは、なぜ重要ですか。</th>
</tr>
</thead>
<tbody>
<tr>
<td>大量のデータに対して Power BI Desktop を使用して Microsoft Power BI レポートを作成します。</td>
<td>Dynamics AX 7.0 (2016 年 2 月) のリリースでは、データ エンティティで公開される OData エンド ポイントを使用して Power BI レポートを作成できます。 この方法は引き続きサポートされていますが、Power Users はエンティティ格納にステージングされた Dynamics AX データを使用することにより Power BI DirectQuery レポートを作成できます。 Dynamics AX プラットフォーム更新プログラム 1 で導入されたエンティティ格納は、高度な分析用に最適化された拡張可能な運用データ ウェアハウスです。 Power BI Desktop は、Power Users 用に用意されている強力なオーサリング ツールです。 Power BI Desktop では、エンティティ格納に接続することにより、レポートおよびデータのモデルを作成できます。</td>
</tr>
<tr>
<td>Dynamics AX 環境間で Power BI レポートを移行します。</td>
<td>ほとんどの場合、レポートはデータ量が少ない開発者環境またはテスト環境で作成されます。 また、テスト環境には、実際の顧客名またはその他の非常に個人的なデータが含まれていない場合があります。 レポートが作成された後、運用環境に移行する必要があります。 管理者は、レポート用の .pbix ファイルを LCS にアップロードできます。 次に、接続文字列などを手動で更新することなく、別の Dynamics AX 環境に移行できます。</td>
</tr>
<tr>
<td>エンティティ格納の更新をスケジュールします。</td>
<td>エンティティ格納は、Dynamics AX の運用環境のデータを定義されたスケジュールで更新する必要があります。 管理者は、Dynamics AX バッチ フレームワークを使用してスケジュールを作成できます。</td>
</tr>
<tr>
<td>Power BI タイルを追加することで、ワークスペースをカスタマイズします。</td>
<td>以前のリリースでは、Power BI のビジュアルは開発者によって作成されるいくつかのワークスペースにのみ追加できます。 現在のリリースではパーソナライズ機能が追加されているため、どのユーザーも新しいワークスペースを作成したり、既存のワークスペースに Power BI タイルを追加することができます。</td>
</tr>
<tr>
<td>フル ページの対話型 Power BI レポートを追加することにより、ワークスペースをカスタマイズします。</td>
<td>Power BI フル ページ レポートでは、ユーザーがデータを対話的に調べることができます。 パワー ユーザーが、作成したレポートを使用・調整したり、豊富なレポートを作成したりできます。 個人用設定として選択したワークスペースにレポートを追加することもできます。</td>
</tr>
<tr>
<td>Dynamics AX ソリューションのコンポーネントとして Power BI レポートをリリースします。</td>
<td>Dynamics AX 7.0 (2016 年 2 月) リリースでは、パートナーおよび ISV は Power BI マーケットプレースを使用して、Dynamics AX Power BI のコンテンツ パックを公開することができます。 これらのコンテンツ パックは、PowerBI.com 上のサービスとして表示されます。 Power BI マーケットプレース経由でコンテンツを公開することができますが、パートナーおよび ISV は LCS の Dynamics AX ソリューションと共に Power BI レポート (.pbix ファイル) もリリースできるようになりました。 また、この方法により、パートナーは、1 対 1 で、またはソリューションの更新として、通常の頻度で顧客に Power BI レポート パックおよび更新をリリースできます。</td>
</tr>
<tr>
<td>ほぼリアルタイムの Power BI レポートおよび Microsoft Cortana Intelligence Suite (CIS) とエンティティ格納の統合を活用します。</td>
<td>エンティティ格納は、高度な分析シナリオ用に最適化された、拡張可能で豊富な運用データ ウェアハウスです。 エンティティ格納は、Dynamics AX のすべてのインスタンスと共に配置されるようになりました。 管理者またはパワー ユーザーは Dynamics AX 集計測定をエンティティ格納内で実施して更新スケジュールを設定することができます。 エンティティ格納のデータは、Power BI DirectQuery モデルを使用してレポートできます。 したがって、ほぼリアルタイムの Power BI レポートを生成することができます。 エンティティ格納は、CIS との統合に対しても使用されます。 Dynamics AX データは、高度な予測のために Microsoft Azure 機械学習に送信されます。 結果はクライアント ユーザー インターフェイスに表示されます。</td>
</tr>
<tr>
<td>SQL Server Reporting Services 統合のフレームワークの改善点を活用します。</td>
<td>改善点の一部は以下のとおりです。
<ul>
<li>大量のデータ セットを照会するときのパフォーマンスの向上。</li>
<li>レンダリングがファイルに報告したときのパフォーマンスの向上。</li>
<li>インストルメンテーションとエラー処理の改善。</li>
</ul>
</td>
</tr>
<tr>
<td>Dynamics AX が配置されたテナントに、検証済み AAD ドメインとしてドメインを追加します。</td>
<td>Azure AD ポータルを使用すると、ドメインを検証済み AAD ドメインとして、Dynamics AX が配置されているテナントに追加できるようになります。 そうすることで、ログインしてドメイン電子メール アカウントを使い Dynamics AX にログインできるようになりますが、これらの同じアカウントを使い Dynamics AX クライアント内の Power BI タイルと Power BI レポートを固定することもできます。</td>
</tr>
</tbody>
</table>

## <a name="office-integration"></a>Office 統合

| 何ができますか。 | これは、なぜ重要ですか。 |
|------------------|------------------------|
| 新しいフィード コントロールを使用して、ページに Yammer または Twitter 会話フィードを追加します。 | 管理者は、Yammer フィードをワークスペースにコンフィギュレーションして、ユーザーが関連する会話を表示して参加することができます。 たとえば、Yammer フィード コントロールは、開発者により **販売処理** ワークスペースに追加され、それから「販売ディスカッション」 Yammer グループを指すようにコンフィギュレーションされます。 |
| 新しい Microsoft Exchange メール プロバイダー経由で送信されるようにメールをコンフィギュレーションします。 | 管理者は、新しいエクスチェンジ メール プロバイダー経由で送信されるようにメールを設定できます。 Microsoft 365 ライセンスがテナント (ドメイン) に関連付けられている場合、Exchange メール プロバイダーは複数の理由から優れたオプションとなります。 たとえば、単一の保存されたアカウントを使用する代わりに、現在のユーザーとして電子メールを送信します。 また、Simple Mail Transfer Protocol (SMTP) プロバイダーとは異なり、Exchange メール プロバイダーは送信済フォルダーに電子メールを保存します。 最後に、任意のコンフィギュレーションを有効にすること以外は、必要ありません。 |
| **SysEmailAddress** または **EmailBase** EDT を使用するメール フィールドの横にある Skype for Business プレゼンス インジケータを参照してください。 (この機能は、編集モードではない非グリッドフィールドにのみ適用されます。) | Skype for Business を使用して、連絡先がオンラインか、質問に回答できるかどうかをすぐに確認できます。 |
| Word アドインを使用してラベルとして、Word テンプレートにバインドされていないテキストを追加します。 | テンプレート デザイナーは、ドキュメントが生成されたときに現在使用されている言語に応じて、テキストが適切に翻訳されるようにバインドされていないテキストにラベルを使用できます。 |
| 会社で ADFS を使用している場合でも、Office アドインにログインします。 | Office アドインは、アドインが一部のアクセス許可の問題を回避できるようにする特殊なダイアログ内で ADFS (Active Directory フェデレーション サービス) のサインインを行うことができるようにする、Office チームから新しい API を利用できるようになりました。 このサポートを利用するには、Office のインストールを可能な限り最新の状態にする必要があります。 |

## <a name="task-guides"></a>タスク ガイド

| 何ができますか。 | これは、なぜ重要ですか。 |
|------------------|------------------------|
| 新規または更新されたタスク ガイドへのアクセス | タスク ガイドでは、ガイド付きでインタラクティブな方法によって、タスクまたは業務プロセスの手順が説明されています。 Microsoft が提供するタスク ガイドをダウンロードおよびカスタマイズできます。 新規または更新されたタスク ガイドの一覧を表示するには、「[新規または更新されたタスク ガイド (2016 年 5 月)](new-updated-task-guides-available-may-2016.md)」を参照してください。 |

## <a name="additional-resources"></a>追加リソース

[財務と運用ホーム ページの新機能および変更された機能](whats-new-changed.md)

[新規または更新されたタスク ガイド (2016 年 5 月)](new-updated-task-guides-available-may-2016.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
