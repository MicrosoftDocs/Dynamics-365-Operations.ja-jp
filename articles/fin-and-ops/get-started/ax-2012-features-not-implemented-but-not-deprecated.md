---
title: "延期された Dynamics AX 2012 機能"
description: "このトピックでは、Microsoft Dynamics AX 2012 の延期された機能と、その機能が AX 7.0 リリース以降に実装されているかどうかを示しています。"
author: sericks007
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21881
ms.assetid: 26793616-9b3f-41f5-8500-6983769c51d8
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 6728ef5bf6dbb380dafb56b108bda8d67e9fba30
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="dynamics-ax-2012-features-that-were-postponed"></a>延期された Dynamics AX 2012 機能

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics AX 2012 の延期された機能を一覧表示します。 これらの機能は、Microsoft Dynamics AX 7.0 では実装されていませんでした。 次の表では、**現在の状態**列は AX 7.0 リリース以降に機能が実装されたかどうかを示します。

製品の各バージョンがリリースされたときの詳細な一覧については、[ソフトウェアのライフ サイクルポリシーおよびクラウド リリース](../../dev-itpro/migration-upgrade/versions-update-policy.md) を参照してください。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>延期された AX 2012 の機能</th>
<th>説明</th>
<th>現在の状態 (2018 年 4 月現在)
</tr>
</thead>
<tbody>

<tr class="even">
<td>人事管理における休暇管理</td>
<td>休暇トランザクションを入力するための機能は Finance and Operations に含まれません。 また、マネージャーとして休暇トランザクションを承認する機能は含まれていません。 他のモジュールとの統合に必要な設定機能は、<strong>Human Resources 2</strong> コンフィギュレーション キーから使用できます。</td>
<td>Dynamics 365 for Talent で実装済み</td>
</tr>

</tr><tr class="odd">
<td>警告</td>
<td>警告はユーザーがシステム内のデータの変更を追跡するのに役立ちます。</td>
<td>プラットフォーム更新 15 で実装済み</td>
</tr>

<tr class="odd">
<td>ラトビアとリトアニア用の支払指図</td>
<td>ラトビアとリトアニア用の支払指図を印刷することができます。 この機能は、将来の更新で利用可能になります。</td>
<td>実装されていません</td>
</tr>

<tr class="even">
<td>スウェーデンの Bankgirot AP 返金形式</td>
<td>Bankgirot の戻り値の形式は、銀行の応答メッセージをインポートするために使用されます。 この機能は、将来の更新で利用可能になります。</td>
<td>実装されていません</td>
</tr>

<tr class="odd">
<td>クライアント ドラッグ アンド ドロップ</td>
<td>Web クライアント コントロールには、ドラッグ アンド ドロップ操作用のアプリケーション プログラミング インターフェイス (API) がありますが、これらの API は非推奨のデスクトップ クライアント テクノロジーに基づいており、新しい Web クライアント プラットフォームで動作するように再設計する必要があります。 ドラッグ アンド ドロップ操作をサポートする API は、将来の更新に含めるためにレビューされます。</td>
<td>実装されていません</td></tr>

<td>クライアント右から左 (右から左) レイアウト</td>
<td>RTL レイアウトがサポートされるようになりました。</td>
<td>プラットフォーム更新 2 で実装済み</td></tr>

<tr class="even">
<td>原価計算</td>
<td><strong>原価計算</strong> モジュールは、複数の組織レベルでの内部原価と収益性レポートの要件を満たすように設計されています。 原価対象レベルを定義するには、モジュールは財務分析コードの適切なマッピングに依存します。 このモジュールでは、総勘定元帳または予算に登録されている経費から原価の詳細割当を実行することができます。 また、これにより実現原価と予算原価を比較することもできます。</td>
<td>バージョン 1611 で実装済み</td>
</tr>

<tr class="odd">
<td>顧客セルフサービス (CSS)</td>
<td>CSS では、承認済の顧客レコードを作成できます。 これにより、選択した製品カタログの表示、品目の注文、および請求書のステータスの表示も可能です。 また、CSS は返品注文を作成およびフォローする機能を提供します。</td>
<td>実装されていません</td>
</tr>

<tr class="odd">
<td>カスタマイズ可能なヘルプ トピック</td>
<td>カスタマイズされたヘルプ トピックを作成する機能は、まだ実装されていません。 カスタム タスク ガイドとカスタム フィールド ヘルプが利用可能です。 この機能は、将来の更新で利用可能になります。 </td>
<td>実装されていません</td></tr>
</td>

<tr class="even">
<td>従業員セフルサービス (ESS)</td>
<td><p>ESS は、1 ページにタスクの関連情報およびキャリアの関連情報を持つ複数のタイルを従業員に表示します。 従業員は、保留中の作業項目を表示したり、ページが開いているリンクをクリックして、自分のタスクに対処することができます。 また、ESS ページでは、従業員の認定状況、次回の業績レビューが予定されている時期、技能、目標、報酬情報、休暇や病気の時の残高などの情報も表示されます。 従業員は、ESS ページから会社ディレクトリにもアクセスできます。</td>
<td>バージョン 1611 で実装済み</td>
</tr>

<tr class="even">
<td>外部アンケートおよび機能の採用</td>
<td>アンケートの外部公開機能および開いているジョブは、将来の更新で Talent に追加されます。</td>
<td><p>外部アンケートの機能は、実装されていません。</p><p>採用機能は、Talent の Attract アプリケーションで利用可能です。</p></td></tr>

<td>ポーランドの会計プリンター</td>
<td>ポーランドの会計処理用プリンターとの統合により、請求書の転記中に必要な情報を適切な形式で会計処理用プリンターに送信できます。 ポーランドの財政的なプリンターの例には、Posnet Thermal プリンターおよび Elzab Omega プリンターのタイプがあります。 この機能は、将来の更新で利用可能になります。</td>
<td>実装されていません</td></tr>

<tr class="odd">
<td>一般予算引当</td>
<td>一般予算引当はコミットメントと呼ばれることがあります。 公的機関法人はよく、このドキュメントを使用して、予算財源を取置きしたり、他の目的に使用できないようにします。 この機能は、将来の更新に追加されます。</td>
<td>実装されていません</td></tr>

<tr class="even">
<td><strong>固定資産価値モデル</strong>および<strong>減価償却簿プロファイル</strong>ページの<strong>グラフィック</strong>タブ</td>
<td>チャートには時間経過に伴う減価償却費、減価償却累計額および正味簿価額が表示されます。 <strong>データ</strong> タブをクリックすると、グラフよりも詳細な情報を表示できます。 このチャートは、今後の更新で再設計されます。</td>
<td>実装されていません</td>
</tr>

<tr class="odd">
<td>Intelligent Data Management Framework (IDMF)</td>
<td>IDMF は、システム管理者のパフォーマンスを最適化するアドオン ツールです。 IDMF は、アプリケーションの正常性の評価と現在の使用パターンの分析を行い、データベース サイズの削減に役立ちます。</td>
<td>実装されていません</td>
</tr>
 
<tr class="odd">
<td>Microsoft Project クライアント統合</td>
<td>Microsoft Project クライアントは、プロジェクトに統合されます。</td>
<td>バージョン 7.2 (2017 年 7 月更新プログラム) で実装済み</td>
</tr>

<td>調達サイト</td>
<td>以前のバージョンでは、従業員セルフ サービスの調達サイトで、従業員の要求の入力、注文のステータス (作成済、入庫済または入庫確認済) の表示、および新しい仕入先のオンボーディングの要求が可能でした。 ポリシーに応じて異なる調達カタログをサイトに表示するように設定できます。 新しいノードを追加することによっても調達カタログを設計できます。 現在のバージョンでは、調達カタログ機能が縮小され、組織に対して注文できる製品に制限をかける目的にのみ使用されます。 構造は常に、調達カテゴリ階層に基づいています。 また、調達サイトで従業員は仕入先請求書を承認し、要求と派生した発注書に関連して領収書を確認します。</td>
<td>実装されていません</td></tr>


<tr class="odd">
<td>グローバル アドレス帳を保護</td>
<td>法人別のグローバル アドレス帳とアドレス帳のセキュリティ保護に役立つ機能は、まだ実装されていません。 この機能は、将来の更新で利用可能になります。</td>
<td>実装されていません</td></tr>
<tr class="even">

<tr class="odd">
<td>電子申告 (ER) 支払形式の仕様</td>
<td><p>現在、支払いフォーマットの使用を手動で入力する必要があります。 今後の更新プログラムで、リスト内の支払フォーマットの仕様を選択できるようになります。 現在、次の支払詳細が支払形式でサポートされています。</p>
 <p><strong>注記:</strong> これらのサポートされている支払明細の値は、選択された支払方法についての<strong>支払仕様</strong>ページの支払明細パラメータとして使用されます。</p>
<p><strong>オランダの BTL91</strong></p>
<table>
<thead>
<tr class="header">
<th>支払仕様 (ER で利用)</th>
<th>フォーマットの説明をエクスポート</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ChqBen</td>
<td>小切手、Begunstigde</td>
</tr>
<tr class="even">
<td>ChqOff</td>
<td>小切手、Kantoor opdrachtgever</td>
</tr>
<tr class="odd">
<td>ChqPri</td>
<td>小切手、Opdrachtgever</td>
</tr>
<tr class="even">
<td>TrfBenBen</td>
<td>Overboeking Begunstigde/Begunstigde</td>
</tr>
<tr class="odd">
<td>TrfBenBenUrg</td>
<td>Overboeking Begunstigde/Begunstigde Spoed</td>
</tr>
<tr class="even">
<td>TrfEurBen</td>
<td>Overboeking Euro/Begunstigde</td>
</tr>
<tr class="odd">
<td>TrfEurBenUrg</td>
<td>Overboeking Euro/Begunstigde Spoed</td>
</tr>
<tr class="even">
<td>TrfEurEur</td>
<td>Overboeking Euro/Euro</td>
</tr>
<tr class="odd">
<td>TrfEurEurUrg</td>
<td>Overboeking Euro/Euro Spoed</td>
</tr>
<tr class="even">
<td>TrfForBen</td>
<td>Overboeking VV-rekening/Begunstigde</td>
</tr>
<tr class="odd">
<td>TrfForBenUrg</td>
<td>Overboeking VV-rekening/Begunstigde Spoed</td>
</tr>
<tr class="even">
<td>TrfForFor</td>
<td>Overboeking VV-rekening/VV-rekening</td>
</tr>
<tr class="odd">
<td>TrfForForUrg</td>
<td>Overboeking VV-rekening/VV-rekening Spoed</td>
</tr>
</tbody>
</table>
<p><strong>デンマークの Betalingsservice</strong></p>
<table>
<thead>
<tr class="header">
<th>支払仕様 (ER で利用)</th>
<th>フォーマットの説明をエクスポート</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>B0112</td>
<td>BS-B 0112: Lang tekst &amp; adresse</td>
</tr>
<tr class="even">
<td>B0113</td>
<td>BS-B 0113: Erstat. bet. lang tekst</td>
</tr>
<tr class="odd">
<td>T0112</td>
<td>BS-T 0112: Lang tekst &amp; adresse</td>
</tr>
<tr class="even">
<td>T0117</td>
<td>BS-T 0117:FIK;kort frist;lang tekst&amp;adr.</td>
</tr>
</tbody>
</table>
<p><strong>デンマーク用の Nordea 仕入先</strong></p>
<table>
<thead>
<tr class="header">
<th>支払仕様 (ER で利用)</th>
<th>フォーマットの説明をエクスポート</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>56</td>
<td>デンマークでの Nordea 勘定の間の通貨勘定の移動</td>
</tr>
<tr class="even">
<td>47</td>
<td>国内小切手</td>
</tr>
<tr class="odd">
<td>45</td>
<td>国内移動</td>
</tr>
<tr class="even">
<td>50</td>
<td>速達振替</td>
</tr>
<tr class="odd">
<td>55</td>
<td>会社間転送 (国内)</td>
</tr>
<tr class="even">
<td>51</td>
<td>外国の銀行への会社間転送</td>
</tr>
<tr class="odd">
<td>54</td>
<td>外国小切手</td>
</tr>
<tr class="even">
<td>52</td>
<td>Nordea 会社間支払</td>
</tr>
<tr class="odd">
<td>43</td>
<td>転送依頼</td>
</tr>
<tr class="even">
<td>46</td>
<td>振込用紙/郵便振替</td>
</tr>
</tbody>
</table>
<p><strong>ISO20022 口座振替 (CH)</strong></p>
<table>
<thead>
<tr class="header">
<th>支払仕様 (ER で利用)</th>
<th>フォーマットの説明をエクスポート</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tp1.ESROPS</td>
<td>タイプ 1 - ESR オレンジの支払伝票</td>
</tr>
<tr class="even">
<td>Tp21.ISR1SPS</td>
<td>タイプ 2.1 - IS 赤 1 ステージ支払伝票</td>
</tr>
<tr class="odd">
<td>Tp22.ISR2SPS</td>
<td>タイプ 2.2 - IS 赤 2 ステージ支払伝票</td>
</tr>
<tr class="even">
<td>Tp7.Dmstc</td>
<td>タイプ 7 - 国内郵便為替</td>
</tr>
<tr class="odd">
<td>TpE1.PSWR</td>
<td>タイプ E1 - 参照付き支払伝票</td>
</tr>
<tr class="even">
<td>TpE2.PSWN</td>
<td>タイプ E2 - 通知付き支払伝票</td>
</tr>
</tbody>
</table>
<p><strong>AvtaleGiro (NO)</strong></p>
<table>
<thead>
<tr class="header">
<th>支払仕様 (ER で利用)</th>
<th>フォーマットの説明をエクスポート</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Varsling</td>
<td>通知付き AvtaleGiro トランザクション</td>
</tr>
</tbody>
</table>
<p><strong>AutoGiro (NO)</strong></p>
<table>
<thead>
<tr class="header">
<th>支払仕様 (ER で利用)</th>
<th>フォーマットの説明をエクスポート</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>溶接</td>
<td>通知付き Autogiroトランザクション</td>
</tr>
</tbody>
</table>
<p><strong>eFaktura (NO)</strong></p>
<table>
<thead>
<tr class="header">
<th>支払仕様 (ER で利用)</th>
<th>フォーマットの説明をエクスポート</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Reklame</td>
<td>広告フラグを含む</td>
</tr>
</tbody>
</table>
<p><strong>ISO20022 口座振替 (DK)</strong></p>
<table>
<thead>
<tr class="header">
<th>支払仕様 (ER で利用)</th>
<th>フォーマットの説明をエクスポート</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EasyAccountTransfer</td>
<td>CVR (NKV) の簡単なアカウント</td>
</tr>
<tr class="even">
<td>Paym_slip</td>
<td>振込用紙 (OCR)</td>
</tr>
</tbody>
</table>
<p><strong>ISPAG-CNAB240 形式 (BR)</strong></p>
<table>
<thead>
<tr class="header">
<th>支払仕様 (ER で利用)</th>
<th>フォーマットの説明をエクスポート</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>A</td>
<td>口座の OP (支払オーダー)、DOC (電子送金)、TED (その他の種類の電子送金)、および直接貸方</td>
</tr>
<tr class="even">
<td>J</td>
<td>バーコード支払 (バーコード付きの請求書またはバーコード付きの他のタイプのドキュメント)</td>
</tr>
<tr class="odd">
<td>O</td>
<td>税金の支払またはその他の公的サービスの支払</td>
</tr>
</tbody>
</table></td>
<td>実装されていません</td></tr>
<tr class="even">



<tr class="odd">
<td>米国の給与</td>
<td>米国の給与計算では、米国内の従業員に対して総計-純処理が提供されます。 給与で、すべての給与レコードおよびトランザクションを設定、入力、および管理できます。 </td>
<td>バージョン 1611 で実装済み</td>
</tr>



<td>仕入先コラボレーション (仕入先ポータル)</td>
<td>Dynamics AX 2012 では、Enterprise Portal を介して仕入先のポータル機能を提供しました。 これらの機能は、Financial and Operations にポートされています。 バージョン 7.1 (Dynamics 365 for Operations 1611 とも呼ばれます) で、仕入先は発注書の表示および対応が可能になりました。
</p><p>バージョン 7.3 では、仕入先は RFQ のものを表示および対応できます。 仕入先は、アドレス、連絡先情報、連絡担当者などの仕入先レコードから選択した情報を表示および編集し、証明書に関連したドキュメントをアップロードすることもできます。<p/>
</td>
<td>バージョン 7.3 で実装済み</td></tr>

<tr class="odd">
<td>仕入先要求 - 新しい仕入先になるための外部要求</td>
<td>Dynamics AX 2012 では、匿名ユーザーがシステムに仕入先として登録する機能を提供しました。これにより、仕入先のマスターに新しい仕入先を追加するための仕入先要求が発生する可能性があります。 バージョン 7.3 では、見込み仕入先からの匿名要求をエンティティ (データ管理/OData) 経由でインポートでき、仕入先 (または仕入先の連絡担当者) を招待して、見込み仕入先に関する追加情報を登録できました。 提供される情報は、ワークフロー プロセスを通じて確認および承認できる新しい仕入先要求に含まれています。 ベンダーの要求を承認すると、Finance and Operations に新しい仕入先勘定の作成をします。
</td>
<td>バージョン 7.3 で実装済み</td></tr>

<td>一般的な仕入先要求</td>
<td>Dynamics AX 2012 には、仕入先の新しい調達カテゴリへの要求や新しい仕入先を要求する社内従業員に関すること、または別の企業に仕入先を追加することを要求するなど、仕入先関連情報の更新に関する様々な目的に役立つ仕入先要求の概念がありました。 仕入先として追加される仕入れ先の要求のみバージョン 7.3 で実装済みです。</td>
<td>実装されていません</td>
</td></tr>






</tbody>
</table>

