---
title: API スロットリングの監視
description: この記事では、サービスの保護制限に達する場合にアプリケーション プログラミング インターフェイス (API) の監視に使用できるツールについて説明します。
author: jaredha
ms.date: 08/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2022-04-16
ms.dyn365.ops.version: Platform update 52
ms.openlocfilehash: c40b485ee711ade632a0788a1b973355283245e7
ms.sourcegitcommit: 20df336e6483d1537da4cb5c687008c4dde8ed48
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/21/2022
ms.locfileid: "9554315"
---
# <a name="monitor-api-throttling"></a>API スロットリングの監視

[!include [banner](../includes/banner.md)]

この記事では、アプリケーション プログラミング インターフェイス (API) の使用を監視できるツールについて説明します。 これには、[サービス保護制限](service-protection-api-limits.md)に達した場合に調整された API 要求や、統合が API の制限に近づいた時点を管理者が理解するのに役立つ一般的な API の使用に関する情報を表示するクエリが含まれます。

スロットリング機能を含むオンボード エクスペリエンスを成功させるには、Open Data Protocol (OData) およびカスタム サービス統合パターンも監視できる必要があります。 財務と運用アプリの管理センターである Microsoft Dynamics Lifecycle Services (LCS) には、管理している環境を正確に表示できることを保証する監視および診断ツールのコレクションが含まれています。 詳細については、 [Lifecycle Services (LCS) の監視および診断ツール](../lifecycle-services/monitoring-diagnostics.md)を参照してください。

これらのクエリを使用すると、サービスの管理に関連するデータを使用して RAW ログを取得できます。 さらに高度な分析を行うためにログをエクスポートすることができます。

## <a name="requests-throttled"></a>調整済みの要求

定義された **調整済みの要求** を使用すると、サービス保護 API 制限を超過したために特定の日時の範囲で調整された API 要求の一覧を表示できます。

追従する監視と診断ポータルでスロットリング活動を表示するには、次の手順に従います。

1. LCS で、適切なプロジェクトを開きます。
2. **環境** セクションで、表示する環境を選択してから **完全な詳細** を選択します。
3. **環境の詳細** ページで、**環境の監視** を選択して、監視および診断ポータルを開きます。 
4. **環境の監視** ページで、**活動** タブを選択して、**未加工ログ** ページを表示します。 
5. クエリ名を選択し、調整されたすべての OData およびカスタム サービス要求の **調整済みの要求** を選択します。
6. **検索** を選択します。

## <a name="summarized-api-requests-by-application-and-user"></a>アプリケーションとユーザーによる集計済みの API 要求

**アプリケーションとユーザーによる集計済みの API 要求** クエリは、AAD ユーザーおよびアプリケーションに対する API 要求を要約して表示します。 このレポートには、使用状況が示されます。この使用状況は、サービス保護 API 制限と比較できます。 選択したユーザーおよびアプリケーションについて、クエリが次の項目を表示します。
- 選択した日付または時刻の範囲の API 要求の総数。
- 選択した日付または時刻の範囲の API 要求の合計実行時間。

この結果は、[ユーザーベースのサービス保護 API 制限](service-protection-api-limits.md#user-based-service-protection-api-limits) の 5 分のスライド ウィンドウ内と同様に、5 分間隔で集計されます。

集計データを表示するには:

1. LCS で、適切なプロジェクトを開きます。
2. **環境** セクションで、表示する環境を選択してから **完全な詳細** を選択します。
3. **環境の詳細** ページで、**環境の監視** を選択して、監視および診断ポータルを開きます。 
4. **環境の監視** ページで、**活動** タブを選択して、**未加工ログ** ページを表示します。 
5. クエリ名を選択し、**アプリケーションとユーザーによる集計済みの API 要求** を選択します。
6. クエリ オブジェクトで次の項目を入力します。
    - **開始日**: API 使用状況データを表示する範囲の開始日と開始時刻。
    - **終了日**: API 使用状況データを表示する範囲の終了日と終了時刻。
    - **ユーザー オブジェクト ID**: ユーザーの Azure Active Directory (AAD) ユーザー オブジェクト ID。
    - **アプリケーション ID**: API を使用する統合アプリケーションの AAD アプリケーション ID。
7. **検索** を選択します。

## <a name="api-requests-by-application-and-user"></a>アプリケーションとユーザーによる API 要求

**アプリケーションとユーザーによる API 要求** クエリにより、特定の日時範囲の定義済みユーザーおよびアプリケーションに対して行われた API 要求の一覧が表示されます。 各レコードについて、クエリには次の情報が表示されます。
- 要求のタイムスタンプ
- API 要求を行うユーザーの AAD ユーザー ID
- 要求の AAD アプリケーション ID
- 要求が行われた AOS ノード
- API 要求の URL
- 要求の合計実行時間

クエリのデータを表示するには:

1. LCS で、適切なプロジェクトを開きます。
2. **環境** セクションで、表示する環境を選択してから **完全な詳細** を選択します。
3. **環境の詳細** ページで、**環境の監視** を選択して、監視および診断ポータルを開きます。 
4. **環境の監視** ページで、**活動** タブを選択して、**未加工ログ** ページを表示します。 
5. クエリ名を選択し、**アプリケーションとユーザーによる API 要求** を選択します。
6. クエリ オブジェクトで次の項目を入力します。
    - **開始日**: API 使用状況データを表示する範囲の開始日と開始時刻。
    - **終了日**: API 使用状況データを表示する範囲の終了日と終了時刻。
      > [!NOTE]
      > クエリに許容される時間の最大範囲は 20 分です。 **終了日** の値を **開始日** の値から 20 分を超えて設定しないでください。
      
    - **ユーザー オブジェクト ID**: ユーザーの Azure Active Directory (AAD) ユーザー オブジェクト ID。
    - **アプリケーション ID**: API を使用する統合アプリケーションの AAD アプリケーション ID。
7. **検索** を選択します。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

