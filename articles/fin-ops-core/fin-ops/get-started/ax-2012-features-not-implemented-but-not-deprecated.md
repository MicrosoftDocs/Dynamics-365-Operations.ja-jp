---
title: 延期された AX 2012 の機能
description: このトピックでは、Microsoft Dynamics AX 2012 の延期された機能と、その機能が AX 7.0 リリース以降に実装されているかどうかを示しています。
author: sericks007
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 21881
ms.assetid: 26793616-9b3f-41f5-8500-6983769c51d8
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: 79bf0c9db4531679fb21b1d31c6cd484f100d19f0f0924e2a7217bdea26bf26d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775952"
---
# <a name="ax-2012-features-that-were-postponed"></a>延期された AX 2012 の機能

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics AX 2012 の延期された機能を一覧表示します。 これらの機能は Microsoft Dynamics AX 7.0 では実装されませんでした。 次の表では、**現在の状態** 列は AX 7.0 リリース以降に機能が実装されたかどうかを示します。

各バージョンのリリース データの詳細一覧については、[ソフトウェアのライフ サイクルポリシーおよびクラウド リリース](../../dev-itpro/migration-upgrade/versions-update-policy.md) を参照してください。

<table>
<thead>
<tr>
<th>延期された AX 2012 の機能</th>
<th>説明</th>
<th>現在の状態 (2019 年 2 月現在)</th>
</tr>
</thead>
<tbody>
<tr>
<td>人事管理における休暇管理</td>
<td>休暇トランザクションを入力するための機能は含まれていません。 また、マネージャーとして休暇トランザクションを承認する機能は含まれていません。 他のモジュールとの統合に必要な設定機能は、<strong>Human Resources 2</strong> コンフィギュレーション キーから使用できます。</td>
<td>Dynamics 365 Human Resources で実装済み</td>
</tr>
<tr>
<td>警告</td>
<td>警告はユーザーがシステム内のデータの変更を追跡するのに役立ちます。</td>
<td>プラットフォーム更新 15 で実装済み</td>
</tr>
<tr>
<td>ラトビアとリトアニア用の支払指図</td>
<td>ラトビアとリトアニア用の支払指図を印刷することができます。 この機能は、将来の更新で利用可能になります。</td>
<td>実装されていません</td>
</tr>
<tr>
<td>スウェーデンの Bankgirot AP 返金形式</td>
<td>Bankgirot の戻り値の形式は、銀行の応答メッセージをインポートするために使用されます。 この機能は、将来の更新で利用可能になります。</td>
<td>実装されていません</td>
</tr>
<tr>
<td>クライアント ドラッグ アンド ドロップ</td>
<td>Web クライアント コントロールには、ドラッグ アンド ドロップ操作用のアプリケーション プログラミング インターフェイス (API) がありますが、これらの API は非推奨のデスクトップ クライアント テクノロジーに基づいており、新しい Web クライアント プラットフォームで動作するように再設計が必要です。 ドラッグ アンド ドロップ操作をサポートする API は、将来の更新に含めるためにレビューされます。</td>
<td>実装されていません</td>
</tr>
<tr>
<td>クライアント右から左 (右から左) レイアウト</td>
<td>RTL レイアウトがサポートされるようになりました。</td>
<td>プラットフォーム更新 2 で実装済み</td>
</tr>
<tr>
<td>原価計算</td>
<td><strong>原価計算</strong> モジュールは、複数の組織レベルでの内部原価と収益性レポートの要件を満たすように設計されています。 原価対象レベルを定義するには、モジュールは財務分析コードの適切なマッピングに依存します。 このモジュールでは、総勘定元帳または予算に登録されている経費から原価の詳細割当を実行することができます。 また、これにより実現原価と予算原価を比較することもできます。</td>
<td>バージョン 1611 で実装済み</td>
</tr>
<tr>
<td>顧客セルフサービス (CSS)</td>
<td>CSS では、承認済の顧客レコードを作成できます。 これにより、選択した製品カタログの表示、品目の注文、および請求書のステータスの表示も可能です。 また、CSS を使用すると、返品注文を作成して追跡できます。</td>
<td>実装されていません</td>
</tr>
<tr>
<td>カスタマイズ可能なヘルプ トピック</td>
<td>カスタマイズされたヘルプ トピックを作成する機能は、まだ実装されていません。 カスタム タスク ガイドとカスタム フィールド ヘルプが利用可能です。 この機能は、将来の更新で利用可能になります。</td>
<td>実装されていません</td>
</tr>
<tr>
<td>従業員セフルサービス (ESS)</td>
<td>ESS は、1 ページにタスクの関連情報およびキャリアの関連情報を持つ複数のタイルを従業員に表示します。 従業員は、保留中の作業項目を表示したり、ページが開いているリンクをクリックして、自分のタスクに対処することができます。 また、ESS ページでは、従業員の認定状況、次回の業績レビューが予定されている時期、技能、目標、報酬情報、休暇や病気の時の残高などの情報も表示されます。 従業員は、ESS ページから会社ディレクトリにもアクセスできます。</td>
<td>バージョン 1611 で実装済み</td>
</tr>
<tr>
<td>外部アンケートおよび機能の採用</td>
<td>アンケートの外部公開機能および開いているジョブは、将来の更新で人事管理に追加されます。</td>
<td>外部アンケートの機能は、実装されていません。
<p>採用機能は、Microsoft Dynamics 365 Talent: Attract で利用可能です。</p>
</td>
</tr>
<tr>
<td>ポーランドの会計プリンター</td>
<td>ポーランドの会計処理用プリンターとの統合により、請求書の転記中に必要な情報を適切な形式で会計処理用プリンターに送信できます。 ポーランドの財政的なプリンターの例には、Posnet Thermal プリンターおよび Elzab Omega プリンターのタイプがあります。 この機能は、将来の更新で利用可能になります。</td>
<td>実装されていません</td>
</tr>
<tr>
<td>一般予算引当</td>
<td>一般予算引当はコミットメントと呼ばれることがあります。 公的機関法人はよく、このドキュメントを使用して、予算財源を取置きしたり、他の目的に使用できないようにします。</td>
<td>バージョン 8.1 で実装済み</td>
</tr>
<tr>
<td><strong>固定資産価値モデル</strong>および<strong>減価償却簿プロファイル</strong>ページの<strong>グラフィック</strong>タブ</td>
<td>チャートには時間経過に伴う減価償却費、減価償却累計額および正味簿価額が表示されます。 <strong>データ</strong> タブをクリックすると、グラフよりも詳細な情報を表示できます。 このチャートは、今後の更新で再設計されます。</td>
<td>実装されていません</td>
</tr>
<tr>
<td>Intelligent Data Management Framework (IDMF)</td>
<td>IDMF は、システム管理者のパフォーマンスを最適化するアドオン ツールです。 IDMF は、アプリケーションの正常性の評価と現在の使用パターンの分析を行い、データベース サイズの削減に役立ちます。</td>
<td>実装されていません</td>
</tr>
<tr>
<td>Microsoft Project クライアント統合</td>
<td>Microsoft Project クライアントは、プロジェクトに統合されます。</td>
<td>バージョン 7.2 (2017 年 7 月更新プログラム) で実装済み</td>
</tr>
<tr>
<td>調達サイト</td>
<td>以前のバージョンでは、従業員セルフ サービスの調達サイトで、従業員の要求の入力、注文のステータス (作成済、入庫済または入庫確認済) の表示、および新しい仕入先のオンボーディングの要求が可能でした。 異なる調達カタログを設定し、ポリシーに応じてサイトに表示できます。 新しいノードを追加することによって、調達カタログを設計することもできます。 現在のバージョンでは、調達カタログ機能が縮小され、組織に対して注文できる製品に制限をかける目的にのみ使用されます。 構造は常に、調達カテゴリ階層に基づいています。 また、調達サイトで従業員は仕入先請求書を承認し、要求と派生した発注書に関連して領収書を確認します。</td>
<td>実装されていません</td>
</tr>
<tr>
<td>グローバル アドレス帳を保護</td>
<td>法人別のグローバル アドレス帳とアドレス帳のセキュリティ保護に役立つ機能は、利用できません。 この機能は、将来の更新で利用可能になります。</td>
<td>実装されていません</td>
</tr>
<tr>
<td>電子申告 (ER) 支払形式の仕様</td>
<td>現在、支払いフォーマットの使用を手動で入力する必要があります。 今後の更新プログラムで、リスト内の支払フォーマットの仕様を選択できるようになります。 現在、次の支払詳細が支払形式でサポートされています。
<blockquote>[!NOTE] これらのサポートされている支払明細の値は、選択された支払方法についての<strong>支払仕様</strong>ページの支払明細パラメータとして使用されます。</blockquote>
<p><strong>オランダの BTL91</strong></p>
<table>
<thead>
<tr>
<th>支払仕様 (ER で利用)</th>
<th>フォーマットの説明をエクスポート</th>
</tr>
</thead>
<tbody>
<tr>
<td>ChqBen</td>
<td>小切手、Begunstigde</td>
</tr>
<tr>
<td>ChqOff</td>
<td>小切手、Kantoor opdrachtgever</td>
</tr>
<tr>
<td>ChqPri</td>
<td>小切手、Opdrachtgever</td>
</tr>
<tr>
<td>TrfBenBen</td>
<td>Overboeking Begunstigde/Begunstigde</td>
</tr>
<tr>
<td>TrfBenBenUrg</td>
<td>Overboeking Begunstigde/Begunstigde Spoed</td>
</tr>
<tr>
<td>TrfEurBen</td>
<td>Overboeking Euro/Begunstigde</td>
</tr>
<tr>
<td>TrfEurBenUrg</td>
<td>Overboeking Euro/Begunstigde Spoed</td>
</tr>
<tr>
<td>TrfEurEur</td>
<td>Overboeking Euro/Euro</td>
</tr>
<tr>
<td>TrfEurEurUrg</td>
<td>Overboeking Euro/Euro Spoed</td>
</tr>
<tr>
<td>TrfForBen</td>
<td>Overboeking VV-rekening/Begunstigde</td>
</tr>
<tr>
<td>TrfForBenUrg</td>
<td>Overboeking VV-rekening/Begunstigde Spoed</td>
</tr>
<tr>
<td>TrfForFor</td>
<td>Overboeking VV-rekening/VV-rekening</td>
</tr>
<tr>
<td>TrfForForUrg</td>
<td>Overboeking VV-rekening/VV-rekening Spoed</td>
</tr>
</tbody>
</table>
<p><strong>デンマークの Betalingsservice</strong></p>
<table>
<thead>
<tr>
<th>支払仕様 (ER で利用)</th>
<th>フォーマットの説明をエクスポート</th>
</tr>
</thead>
<tbody>
<tr>
<td>B0112</td>
<td>BS-B 0112: Lang tekst &amp; adresse</td>
</tr>
<tr>
<td>B0113</td>
<td>BS-B 0113: Erstat. bet. lang tekst</td>
</tr>
<tr>
<td>T0112</td>
<td>BS-T 0112: Lang tekst &amp; adresse</td>
</tr>
<tr>
<td>T0117</td>
<td>BS-T 0117:FIK;kort frist;lang tekst&amp;adr.</td>
</tr>
</tbody>
</table>
<p><strong>デンマーク用の Nordea 仕入先</strong></p>
<table>
<thead>
<tr>
<th>支払仕様 (ER で利用)</th>
<th>フォーマットの説明をエクスポート</th>
</tr>
</thead>
<tbody>
<tr>
<td>56</td>
<td>デンマークでの Nordea 勘定の間の通貨勘定の移動</td>
</tr>
<tr>
<td>47</td>
<td>国内小切手</td>
</tr>
<tr>
<td>45</td>
<td>国内移動</td>
</tr>
<tr>
<td>50</td>
<td>速達振替</td>
</tr>
<tr>
<td>55</td>
<td>会社間転送 (国内)</td>
</tr>
<tr>
<td>51</td>
<td>外国の銀行への会社間転送</td>
</tr>
<tr>
<td>54</td>
<td>外国小切手</td>
</tr>
<tr>
<td>52</td>
<td>Nordea 会社間支払</td>
</tr>
<tr>
<td>43</td>
<td>転送依頼</td>
</tr>
<tr>
<td>46</td>
<td>振込用紙/郵便振替</td>
</tr>
</tbody>
</table>
<p><strong>ISO20022 口座振替 (CH)</strong></p>
<table>
<thead>
<tr>
<th>支払仕様 (ER で利用)</th>
<th>フォーマットの説明をエクスポート</th>
</tr>
</thead>
<tbody>
<tr>
<td>Tp1.ESROPS</td>
<td>タイプ 1 - ESR オレンジの支払伝票</td>
</tr>
<tr>
<td>Tp21.ISR1SPS</td>
<td>タイプ 2.1 - IS 赤 1 ステージ支払伝票</td>
</tr>
<tr>
<td>Tp22.ISR2SPS</td>
<td>タイプ 2.2 - IS 赤 2 ステージ支払伝票</td>
</tr>
<tr>
<td>Tp7.Dmstc</td>
<td>タイプ 7 - 国内郵便為替</td>
</tr>
<tr>
<td>TpE1.PSWR</td>
<td>タイプ E1 - 参照付き支払伝票</td>
</tr>
<tr>
<td>TpE2.PSWN</td>
<td>タイプ E2 - 通知付き支払伝票</td>
</tr>
</tbody>
</table>
<p><strong>AvtaleGiro (NO)</strong></p>
<table>
<thead>
<tr>
<th>支払仕様 (ER で利用)</th>
<th>フォーマットの説明をエクスポート</th>
</tr>
</thead>
<tbody>
<tr>
<td>Varsling</td>
<td>通知付き AvtaleGiro トランザクション</td>
</tr>
</tbody>
</table>
<p><strong>AutoGiro (NO)</strong></p>
<table>
<thead>
<tr>
<th>支払仕様 (ER で利用)</th>
<th>フォーマットの説明をエクスポート</th>
</tr>
</thead>
<tbody>
<tr>
<td>溶接</td>
<td>通知付き Autogiroトランザクション</td>
</tr>
</tbody>
</table>
<p><strong>eFaktura (NO)</strong></p>
<table>
<thead>
<tr>
<th>支払仕様 (ER で利用)</th>
<th>フォーマットの説明をエクスポート</th>
</tr>
</thead>
<tbody>
<tr>
<td>Reklame</td>
<td>広告フラグを含む</td>
</tr>
</tbody>
</table>
<p><strong>ISO20022 口座振替 (DK)</strong></p>
<table>
<thead>
<tr>
<th>支払仕様 (ER で利用)</th>
<th>フォーマットの説明をエクスポート</th>
</tr>
</thead>
<tbody>
<tr>
<td>EasyAccountTransfer</td>
<td>CVR (NKV) の簡単なアカウント</td>
</tr>
<tr>
<td>Paym_slip</td>
<td>振込用紙 (OCR)</td>
</tr>
</tbody>
</table>
<p><strong>ISPAG-CNAB240 形式 (BR)</strong></p>
<table>
<thead>
<tr>
<th>支払仕様 (ER で利用)</th>
<th>フォーマットの説明をエクスポート</th>
</tr>
</thead>
<tbody>
<tr>
<td>A</td>
<td>口座の OP (支払オーダー)、DOC (電子送金)、TED (その他の種類の電子送金)、および直接貸方</td>
</tr>
<tr>
<td>J</td>
<td>バーコード支払 (バーコード付きの請求書またはバーコード付きの他のタイプのドキュメント)</td>
</tr>
<tr>
<td>O</td>
<td>税金の支払またはその他の公的サービスの支払</td>
</tr>
</tbody>
</table>
</td>
<td>実装されていません</td>
</tr>
<tr>
<td>米国の給与</td>
<td>米国の給与計算では、米国内の従業員に対して総計-純処理が提供されます。 給与で、すべての給与レコードおよびトランザクションを設定、入力、および管理できます。</td>
<td>バージョン 1611 で実装済み</td>
</tr>
<tr>
<td>仕入先コラボレーション (仕入先ポータル)</td>
<td>Dynamics AX 2012 では、エンタープライズ ポータルを介して仕入先のポータル機能を提供しました。 また、これらの機能は Financial and Operation によって提供されます。 バージョン 7.1 (Dynamics 365 for Operations 1611 とも呼ばれます) で、仕入先は発注書の表示および対応が可能になりました。
<p>バージョン 7.3 では、仕入先が RFQs を表示および応答できます。 仕入先は、アドレス、連絡先情報、連絡担当者などの仕入先レコードから選択した情報を表示および編集し、証明書に関連したドキュメントをアップロードすることもできます。</p>
</td>
<td>バージョン 7.3 で実装済み</td>
</tr>
<tr>
<td>仕入先要求 - 新しい仕入先になるための外部要求</td>
<td>Dynamics AX 2012 では、匿名ユーザーがシステムに仕入先として登録する機能を提供しました。これにより、仕入先のマスターに新しい仕入先を追加するための仕入先要求が発生する可能性があります。 バージョン 7.3 では、見込み仕入先からの匿名要求をエンティティ (データ管理/OData) 経由でインポートでき、仕入先 (または仕入先の連絡担当者) を招待して、見込み仕入先に関する詳細を登録できました。 提供される情報は、ワークフロー プロセスを通じて確認および承認できる新しい仕入先要求に含まれています。 ベンダーの要求を承認すると、新しい仕入先勘定が作成されます。</td>
<td>バージョン 7.3 で実装済み</td>
</tr>
<tr>
<td>一般的な仕入先要求</td>
<td>Dynamics AX 2012 には、仕入先の新しい調達カテゴリへの要求や新しい仕入先を要求する社内従業員に関すること、または別の企業に仕入先を追加することを要求するなど、仕入先関連情報の更新に関する様々な目的に役立つ仕入先要求の概念がありました。 仕入先として追加される仕入れ先の要求のみバージョン 7.3 で実装済みです。</td>
<td>実装されていません</td>
</tr>
<tr>
<td>[ロシア] 税登録</td>
<td>法人は、レジスターを使用して、収益と経費を開示できます。 レジスターは、売上請求書や配送メモなどの基本ドキュメントが、生産の原価価格の計算を使って最初に入力されたときからの収益および経費データを追跡するために使用されます。 レジスターからのデータは、法人の宣言された利益を確認するために使用されます。 この機能には次の機能が含まれています。
<ul>
<li>現在の期間の収入</li>
<li>税経費</li>
<li>現在の期間の他の経費</li>
<li>現在の期間の未実現経費</li>
<li>その他の未実現経費</li>
<li>売掛金勘定の貸方 - 在庫</li>
<li>貸倒損失引当の計算</li>
<li>不良債務引当移動</li>
<li>売掛金勘定振替</li>
<li>AR 不良債務損金処理の手順</li>
<li>買掛金勘定の借入金 - 一覧</li>
<li>買掛金勘定の借入金移動</li>
<li>AP 不良債務損金処理の手順</li>
<li>商品原価計算</li>
<li>FA オブジェクト情報</li>
<li>IA オブジェクト情報</li>
<li>FA 減価償却</li>
<li>IA 減価償却</li>
<li>FA/IA 販売</li>
<li>減価償却特別復旧</li>
</ul>
</td>
<td>バージョン 8.1.3 で実装済み</td>
</tr>
<tr>
<td>[ロシア] クライアント銀行インターフェイスおよび調整手順の電子エクスポート/インポート形式</td>
<td>入金される支払のエクスポートおよび送信の支払のインポートの電子形式。</td>
<td>バージョン 8.1.3 で実装済み</td>
</tr>
<tr>
<td>[ロシア] VAT申告</td>
<td>VAT 申告の電子形式。</td>
<td>バージョン 10.0.1 で実装済み</td>
</tr>
<tr>
<td>[ロシア] キャッシュ フロー管理</td>
<td>キャッシュ フロー予測を取得して分析を実行し、支払スケジュールの仕訳帳を使用して日次ベースで支払を管理し、会社の現金の位置を制御し、集中コントロールを使用して会社のキャッシュ フローを維持する機能。</td>
<td>バージョン 10.0.1 で実装済み</td>
</tr>
<tr>
<td>[ロシア] 会計報告形式</td>
<td>次の会計報告の電子形式: バランス_シート、BalanceSheet、IncomeStatement、CashFlow、EquityStatement、TargetUsageMoney</td>
<td>バージョン 10.0.1 で実装済み</td>
</tr>
<tr>
<td>[ロシア] 評価税レポート</td>
<td>評価税申告。</td>
<td>バージョン 10.0.1 で実装済み</td>
</tr>
<tr>
<td>[ロシア] 土地税レポート</td>
<td>土地税申告。 別の部署による土地税申告の作成。</td>
<td>バージョン 10.0.1 で実装済み</td>
</tr>
<tr>
<td>[ロシア] 輸送税レポート</td>
<td>輸送税申告。</td>
<td>バージョン 10.0.1 で実装済み</td>
</tr>
<tr>
<td>[ロシア] 輸入品の間接税返還 (VAT および物品税)</td>
<td>関税同盟の州メンバーからの輸入品における間接 (源泉徴収) 税還付 (VAT および物品税)。</td>
<td>バージョン 10.0.1 で実装済み</td>
</tr>
<tr>
<td>[ロシア] アルコール小売販売の仕訳帳</td>
<td>日次アルコール仕訳帳。</td>
<td>バージョン 10.0.1 で実装済み</td>
</tr>
<tr>
<td>[ロシア] オプションの一般会計への移動オーダーの転記</td>
<td>移動オーダーを転記する場合に、総勘定元帳に転記する、または転記しないというオプション。</td>
<td>バージョン 8.1.2 で実装済み</td>
</tr>
<tr>
<td>[ロシア] 在庫所有者</td>
<td>在庫 (委託在庫、寄託、輸送料金、など) の所有者を追跡する場合に使用される在庫分析コード。</td>
<td>バージョン 10.0.1 で実装済み</td>
</tr>
<tr>
<td>[ロシア] AP/AR - 第三者の雑費</td>
<td>第三者の雑費の登録および次の管理体制に基づいた分配: 購入済商品の原価に含める (ほかの仕入先からの請求書明細行に配賦)、ほかの当事者への再振出、およびほかの経費勘定への再配分。</td>
<td>バージョン 8.1.1 で実装済み</td>
</tr>
<tr>
<td>[ロシア] 仕入先からの輸送中の商品</td>
<td>品目タイプが "輸送の間の購買済品目" の特別な転記プロファイルによる仕入先からの輸送中の商品の登録。 輸送中の在の保有法の作成。 (INV-6)</td>
<td>バージョン 8.1.2 で実装済み</td>
</tr>
<tr>
<td>[ロシア] 輸送中の商品 - プロパティの受け渡しが延期された顧客への販売</td>
<td>延期されたプロパティの移動を含む販売後の請求書: 顧客債務が転記されず、すべての支払税が転記され、品目は流通倉庫に転送されます。 負債が転記されたプロパティの受け渡し、および流通倉庫からの品目の販売を登録します。</td>
<td>バージョン 8.1.2 で実装済み</td>
</tr>
<tr>
<td>[ロシア] 寄託 - 受託者側の会計</td>
<td>法律によって必要とされる、委託の場合の在庫受領書の会計および基本フォーム MX-1 の生成。 委託された在庫入庫の会計、基本フォーム MX-3 の委託と生成。 受託者側の委託原価計算。</td>
<td>バージョン 8.1.2 で実装済み</td>
</tr>
<tr>
<td>[ロシア] 寄託 - 所有者側の会計</td>
<td>寄託への在庫移動、および寄託サービス契約に基づく商品の所有者側での寄託から在庫への返品の会計。</td>
<td>バージョン 8.1.2 で実装済み</td>
</tr>
<tr>
<td>[ロシア] Process Industries ソリューションのローカライズ</td>
<td>2 つの地域での基本ローカライズ: すべての新しい総勘定元帳転記の勘定の対応、および Process Industries 機能とロシアの国コンテキストの機能的共存 (Process Industries とロシアの国コンテキストの両方が有効な場合は問題なし)。</td>
<td>バージョン 10.0.1 で実装済み</td>
</tr>
<tr>
<td>[ロシア] アルコール販売の申告: 卸売申請書 6、7、8。 小売申請書 11、12</td>
<td>生産者、測定単位、小売ライセンス、および卸売取引を含む、アルコール飲料のタイプを追跡。 次のアルコール飲料の活動データを準備: 印刷済みの申告、電子報告書経由で Excel 形式にエクスポートした申告。</td>
<td>バージョン 10.0.1 で実装済み</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]