---
title: Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 23 (2019 年 1 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operation プラットフォーム更新プログラム 23 (2019 年 1 月) の新機能または変更された機能について説明します。
author: tonyafehr
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Platform 23
ms.openlocfilehash: 24146818c0e8d3cb1b65c3e9e01c59d80fef4d32
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752220"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-platform-update-23-january-2019"></a>Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 23 (2019 年 1 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 23 の新機能または変更された機能について説明します。 このバージョンは、7.0.5126 のビルド番号を持ちます。

### <a name="dynamics-365-october-18-release-notes"></a>Dynamics 365 2018 年 10 月リリース ノート

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[2018 年 10 月リリース ノートを確認](https://go.microsoft.com/fwlink/?linkid=870424). あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="platform-update-23-bug-fixes"></a>プラットフォーム アップデート 23 のバグ修正プログラム

プラットフォーム更新 23 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、この [KB 資料](https://go.microsoft.com/fwlink/?linkid=2049368)を参照してください。

## <a name="legal-entity-filtering-using-grid-column-headers"></a>グリッド列ヘッダーを使用した法人のフィルター処理

プラットフォーム更新プログラム 23 以降、会社間クエリを含むグリッドでは、グリッド内の他の列と同様、列ドロップダウン メニューを使用して、ユーザーが *法人* 列をフィルター処理できます。 たとえば、ユーザーが特定の顧客のグローバル トランザクションを見ているとき、会社の小さいサブセット内のトランザクションを検索することがあります。 この機能が追加される前は、フィルターまたは並べ替えの編集ダイアログ ボックスの顧客範囲タブを使用してフィルター処理するか、ページ固有のカスタム フィルターを使用する必要がありました。

![法人によるフィルター](media/legalEntityFiltering.png "法人によるフィルター")

## <a name="export-to-excel"></a>Excel にエクスポート

プラットフォーム更新プログラム 22 では、Excel へのエクスポート機能は、Finance and Operations のグリッドから最大 100 万行をエクスポートできるように強化されました。以前の 10,000 行の制限から大幅に上昇しました。

プラットフォーム更新プログラム 23 では、この機能の強化を継続しました。 エクスポートが完了すると、エクスポートが完了したことを知らせる通知がアクション センターに届くようになりました。 通知には、エクスポートされたデータを含む Excel ファイルをダウンロードするためのリンクが含まれています。 リンクと通知には、エクスポートが完了した後、約 3 日間アクセスできます。

## <a name="manage-access-to-network-printers-across-legal-entities"></a>法人間でのネットワーク プリンターへのアクセスの管理

プラットフォーム更新プログラム 23 には、ネットワーク プリンターを Dynamics 365 for Finance and Operations に登録するためのドキュメント回覧エージェント (DRA) と共に、システム管理者が使用できる **システム ネットワーク プリンター管理** フォームが含まれています。

この機能を有効にすると、**プレビュー** リンクが **システム ネットワーク プリンター** フォームに表示されます (**組織管理** \> **設定** \> **ネットワーク プリンター** で **システム ネットワーク プリンター** をクリック)。

DRA を使用してネットワーク プリンターをサービスに登録すると、組織の各法人の構成情報が表示されます。

## <a name="enabling-index-hints-in-x-again"></a>X++ でのインデックス ヒントの再有効化

Microsoft Dynamics AX 2009 以前のバージョンでは、X++ からのインデックス ヒントがサポートされていました。 ただし、Dynamics AX 2012 のリリース時にこれは非推奨になりました。 詳細については、[非推奨: X++ インデックス ヒント句](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/deprecated-x-index-hint-clause)を参照してください。

これが非推奨になった主な理由は、誤ったインデックス ヒットによってクエリが破損し、クエリを解決するまでほとんど実行できないことでした。 現在では、数百のテナントに数千のクエリが表示され、一部のシンプルなクエリのあまり最適でないプランと共に SQL が表示されると、Finance and Operations が X++ ヒントを戻したことになります。 ただし、X++ ヒントは特別な注意を払って使用してください。

既定の動作 **False** を持つ一般的な **allowIndexHint** の新しい API を追加しました。 これにより、開発者はインデックス ヒントをオプトインして明示的に有効にできます。 インデックス ヒントを指定するための select ステートメントの古い構文が再利用されます。

インデックス ヒントを指定する既存の X++ コードがある場合、新しい API が呼び出されるまで現在の動作は変更されません。 詳細については、次の例を参照してください。

```xpp
public void testIndexHintRegularTable()
{
    SysDataAccessDBLogTestTable tbl1;
    tbl1.allowIndexHint(true);
    select generateonly tbl1 index hint PrimaryKeyIdx where tbl1.description == ''; // Send index hint to SQL server
    ...
}
```

> [!NOTE]
> インデックス ヒントは、悪影響よりもメリットの方が多いことが確信できるときのみ、慎重に使用してください。 新しい API により、知識と経験が豊富な開発者が必要なときに適切なヒントを渡すことができるようになります。 経験豊富な開発者は、注意してこの新しい機能を使用してください。 疑わしい場合は、インデックス ヒントを使用しないでください。

## <a name="automated-refresh-of-entity-store-opt-in"></a>エンティティ格納の自動化更新 (オプトイン)
更新を自分でスケジュールする代わりに、システムにエンティティ格納の更新を管理させることができます。 有効にすると、更新パターン (1 時間毎、1 日 2 回、毎日、または毎週) を選択できます。 指定すると、システムは選択されたパターンでエンティティ格納を更新します。 システムはまた、新しい更新フォームに切り替え、ここでステータスと更新の問題が通知されます。 詳細については、[エンティティ格納の自動化更新](../../dev-itpro/analytics/automated-entity-store-refresh.md)を参照してください。

## <a name="entity-store-as-a-data-lake-private-preview"></a>Data Lake としてのエンティティ格納 (プライベート プレビュー)
プラットフォーム更新プログラム 23 では、エンティティ格納を Data Lake として選択できます。 この機能が有効になると、エンティティ格納データは、Microsoft サブスクリプションでリレーショナル エンティティ格納データベースに入力されません。 代わりに、独自のサブスクリプションの Azure Data Lake Storage Gen2 アカウントに入力されます。 PowerBI.com およびその他の Azure ツールのすべての機能をエンティティ格納で使用できます。 この機能をプレビューして使用するには、[Insider プログラム](https://experience.dynamics.com/insider)に是非ご参加ください。

## <a name="extensibility-enhancements"></a>拡張性の強化
プラットフォーム更新プログラム 23 に含まれる[プラットフォーム拡張機能の 4 番目の波](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/platform-extensibility4)は、2018 年 10 月リリース ノートにドキュメントされています。 6 つの強化機能が詳細に説明されており、ハイライトの 1 つはクエリ データソースへの新しいリレーションの追加です。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]