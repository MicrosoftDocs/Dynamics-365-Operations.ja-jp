---
title: Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 21 (2018 年 11 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operation プラットフォーム更新プログラム 21 の新機能または変更された機能について説明します。 このバージョンは 2018 年 11 月にリリースされました。
author: tonyafehr
manager: AnnBe
ms.date: 01/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: ''
ms.assetid: a765a61c-52a3-47c5-b579-68b9249c592b
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-09-30
ms.dyn365.ops.version: Platform 21
ms.openlocfilehash: e99994c7ed3e930ebf4f25bc312640d51596ac34
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191729"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-platform-update-21-november-2018"></a>Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 21 (2018 年 11 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 21 の新機能または変更された機能について説明します。 このバージョンは 2018 年 11 月にリリースされ、ビルド番号は 7.0.5073 です。

## <a name="dynamics-365-october-18-release-notes"></a>Dynamics 365 2018 年 10 月リリース ノート

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[2018 年 10 月リリース ノートを確認](https://go.microsoft.com/fwlink/?linkid=870424). あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

## <a name="bug-fixes"></a>バグ修正

プラットフォーム更新 21 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://go.microsoft.com/fwlink/?linkid=2033925)を参照してください。

## <a name="extensibility-enhancements"></a>拡張性の強化

リリース ノートには、[2018 年 10 月リリースのプラットフォーム拡張機能の 2 番目の波](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/platform-extensibility2)に関する情報が含まれています。これは、プラットフォーム更新 21 に付属しています。 11 個の拡張機能が詳細に説明されており、ハイライトの 1 つは、標準例外処理を容易にするため、try-finally ブロック内のコマンド メソッド チェーン内に次の呼び出しを配置する新しい機能です。

## <a name="transientsqlconnectionerror-x-exception"></a>TransientSqlConnectionError X++ 例外

X++ SQL クエリの実行中、サーバー側で一時的な SQL 接続エラーが発生すると、TransientSqlConnectionError X++ 例外が発生します。 アプリケーションの要件に応じて、アプリケーションは例外をキャッチして処理する必要があります。

この例外は通常、大規模なトランザクションの際に、またはデータベースに大きな処理負荷がかかっている場合に発生します。

TransientSqlConnectionError 例外は、トランザクション内ではキャッチできません。 この例外が検出された X++ トランザクションは、例外が発生する前にキャンセルされます (**ttsAbort** を呼び出す)。 つまり、汎用 X++ エラー例外ではなく一時的な SQL 接続エラーを特定するためにキャッチ ブロックを使用した後、最上位のトランザクションを再試行するか、新しいセッションでアプリケーション コード ロジックを再試行する必要があります。 この例外は、一時的なサーバーの障害時にアプリケーションの設計を許可します。

アプリケーション トランザクションの処理に時間がかかる場合、複数の増分遅延を使用して TransientSqlConnectionError 例外をキャッチできます。 新しいセッションでアプリケーション コードを再実行すると、例外をキャッチした後に成功する可能性が最も高くなります。

詳細については、[SQL 接続エラー X++ 例外](../../dev-itpro/dev-ref/sql-connection-error.md)を参照してください。

## <a name="sticky-default-actions-in-grids"></a>グリッド内の既定の付箋アクション

Finance and Operations の多くのグリッドで*既定のアクション*が定義されています。 これは、すべての行の値がハイパーリンクとして表示されるグリッド内の 1 つの列です。それに対して、その他の列ではアクティブな行の値だけがハイパーリンクとして表示されます。 この既定のアクションは常に、ユーザー個人設定が適用される前に、グリッド内の最初のテキスト列に表示されます。 たとえば、以下の **顧客** 一覧の **アカウント** 列を考えます。

![顧客リスト](media/customerGrid.png "顧客リスト")

プラットフォーム更新 21 から利用可能な **既定の付箋アクション** 機能は、列の順序または表示設定を変更する個人用設定が適用された後に、既定のアクション列がグリッドのどこに表示されるかを制御します。

既定の付箋アクションをオフにすると (プラットフォーム更新 21 より前で既定のアクションがどのように動作したかに対応します)、既定のアクション ハイパーリンクが、個人用設定の適用後に最初のテキスト列に表示される列に変更されます。 たとえば、**アカウント** 列をグリッドの 4 番目の列に移動する場合 (または **アカウント** 列を非表示にした場合)、既定のアクションを表すハイパーリンクは **名前** 列に移動します。

![既定の付箋アクションがオフ](media/stickyDAOff.png "既定の付箋アクションがオフになると、[アカウント] 列が最初の列に移動されない場合、[名前] 列が既定のアクション列になります。")

既定の付箋アクションがオンになると、既定のアクション ハイパーリンクは、フォームに適用される個人用設定に関係なく同じ列になります。 つまり、この顧客リストについて、**アカウント** 列が移動されるか非表示になるか関係なく、**アカウント** 列は引き続き既定のアクション列です。

![既定の付箋アクションがオフ](media/stickyDAOn.png "既定の付箋アクションがオンになると、[アカウント] 列は個人用設定にかかわらず既定のアクション列です。")

プラットフォーム更新 21 では、既定の付箋アクション機能がオフですが、システム管理者が環境で有効にできます。 この機能を有効にするには、**システム管理** で **クライアント パフォーマンス オプション** ページに移動し、**既定の付箋アクションを有効にする** オプションを見つけます。

## <a name="batch-active-periods"></a>バッチ アクティブ期間

プラットフォーム更新 21 のリリースでは、バッチ ジョブがいつ実行されるかの制御の追加レベルが使用できるようになりました。 以前は、一定の時間数または特定の日付までの 1 時間ごとにバッチ ジョブが実行されるようにスケジュールすることのみ可能でした。 管理者は、次のシナリオなど、追加のアクティブ期間の情報を指定できるようになりました。

- バッチ グループ内のジョブが実行を開始できる期間を指定します。
- 営業時間外にのみバッチ ジョブを実行する場合に選択します。
- アクティブ期間内で任意の回数の繰り返しを設定します。 たとえば、管理者は、午後 6 時から午前 8 時の間のみ、毎時間バッチ ジョブを実行することを選択できます。

詳細については、「[バッチ アクティブ期間](../../dev-itpro/sysadmin/activeperiod.md)」を参照してください。
