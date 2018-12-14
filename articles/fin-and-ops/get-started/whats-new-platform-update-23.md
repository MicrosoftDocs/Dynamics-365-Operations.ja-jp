---
title: "Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 23 (2018 年 12 月) の新機能および変更された機能"
description: "このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 23 (2018 年 12 月) の新機能または変更された機能について説明します。"
author: tonyafehr
manager: AnnBe
ms.date: 12/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Platform 23
ms.translationtype: HT
ms.sourcegitcommit: 99c10649d7683265fcac86c1825c5a965bbdb415
ms.openlocfilehash: 9dd6394133890bbc9a97c6cb512313e4052c1e4b
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-platform-update-23-december-2018"></a>Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 23 (2018 年 12 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 23 の新機能または変更された機能について説明します。 このバージョンは、7.0.5126 のビルド番号を持ちます。

### <a name="dynamics-365-october-18-release-notes"></a>Dynamics 365 2018 年 10 月リリース ノート
当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか? 

[2018 年 10 月リリース ノートを確認](https://go.microsoft.com/fwlink/?linkid=870424). あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。 

### <a name="platform-update-23-bug-fixes"></a>プラットフォーム アップデート 23 のバグ修正プログラム
プラットフォーム更新 23 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、この [KB 資料](https://go.microsoft.com/fwlink/?linkid=) (**未公開**) を参照してください。

## <a name="legal-entity-filtering-using-grid-column-headers"></a>グリッド列ヘッダーを使用した法人のフィルター処理
プラットフォーム更新プログラム 23 以降、会社間クエリを含むグリッドでは、グリッド内の他の列と同様、列ドロップダウン メニューを使用して、ユーザーが *法人* 列をフィルター処理できます。 たとえば、ユーザーが特定の顧客のグローバル トランザクションを見ているとき、会社の小さいサブセット内のトランザクションを検索することがあります。 この機能が追加される前は、[フィルターまたは並べ替えの編集] ダイアログ ボックスの [顧客範囲] タブを使用してフィルタ処理するか、ページ固有のカスタム フィルターを使用する必要がありました。

![法人によるフィルター処理](media/legalEntityFiltering.png  "法人によるフィルター処理")

## <a name="export-to-excel"></a>Excel にエクスポート
プラットフォーム更新プログラム 22 では、Excel へのエクスポート機能は、Finance and Operations のグリッドから最大 100 万行をエクスポートできるように強化されました。以前の 10,000 行の制限から大幅に上昇しました。 

プラットフォーム更新プログラム 23 では、この機能の強化を継続しました。 エクスポートが完了すると、エクスポートが完了したことを知らせる通知がアクション センターに届くようになりました。 通知には、エクスポートされたデータを含む Excel ファイルをダウンロードするためのリンクが含まれています。 リンクと通知には、エクスポートが完了した後、約 3 日間アクセスできます。 

## <a name="manage-access-to-network-printers-across-legal-entities"></a>法人間でのネットワーク プリンターへのアクセスの管理
新しいシステム管理ユーティリティへのアクセスは、Carbon Flighting Service によって管理されます。 プラットフォーム更新プログラム 23 には、ネットワーク プリンターを Dynamics 365 for Finance and Operations に登録するためのドキュメント回覧エージェント (DRA) と共に、システム管理者が使用できる**システム ネットワーク プリンター管理**フォームが含まれています。

この機能を有効にすると、**プレビュー** リンクが **システム ネットワーク プリンター** フォームに表示されます (**組織管理** > **設定** > **ネットワーク プリンター** で **システム ネットワーク プリンター** をクリック)。 DRA を使用してネットワーク プリンターをサービスに登録すると、組織の各法人の構成情報が表示されます。

## <a name="enabling-index-hints-in-x-again"></a>X++ でのインデックス ヒントの再有効化
Microsoft Dynamics AX 2009 以前のバージョンでは、X++ からのインデックス ヒントがサポートされていました。 ただし、Dynamics AX 2012 のリリース時にこれは非推奨になりました。 詳細については、[非推奨: X++ インデックス ヒント句](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/deprecated-x-index-hint-clause)を参照してください。

これが非推奨になった主な理由は、誤ったインデックス ヒットによってクエリが破損し、クエリを解決するまでほとんど実行できないことでした。 現在では、数百のテナントに数千のクエリが表示され、一部のシンプルなクエリのあまり最適でないプランと共に SQL が表示されると、Finance and Operations が X++ ヒントを戻したことになります。 しかし、X++ ヒントは特別な注意を払って使用してください。  

既定の動作 **False** を持つ一般的な **allowIndexHint** の新しい API を追加しました。 これにより、開発者はインデックス ヒントをオプトインして明示的に有効にできます。 インデックス ヒントを指定するための select ステートメントの古い構文が再利用されます。
インデックス ヒントを指定する既存の X++ コードがある場合、新しい API が呼び出されるまで現在の動作は変更されません。 詳細については、次の例を参照してください。

    public void testIndexHintRegularTable()
        {
            SysDataAccessDBLogTestTable tbl1;
            tbl1.allowIndexHint(true);
            select generateonly tbl1 index hint PrimaryKeyIdx where tbl1.description == ''; // Send index hint to SQL server
         ………..

        }

> [!NOTE]
> インデックス ヒントは、悪影響よりもメリットの方が多いことが確信できるときのみ、慎重に使用してください。 新しい API により、知識と経験が豊富な開発者が必要なときに適切なヒントを渡すことができるようになります。 経験豊富な開発者は、注意してこの新しい機能を使用してください。 疑わしい場合は、インデックス ヒントを使用しないでください。

