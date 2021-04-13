---
title: ユーザー サインインの追跡
description: このトピックでは、Microsoft Dynamics 365 Finance and Operations アプリにサインインして使用するユーザーの監査ログを作成する方法について説明します。
author: manalidongre
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2017-10-31
ms.dyn365.ops.version: Platform update 12
ms.openlocfilehash: f7ddf99ae90fea7e320608108e2a63ad8b88f4a7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750534"
---
# <a name="track-user-sign-ins"></a>ユーザー サインインの追跡 
 
[!include [banner](../includes/banner.md)]

多くの組織は、システムを使用したユーザーの監査証跡を管理する必要があります。 この要件は、コンプライアンス上の理由から、または不適切な使用が発生した場合にトラックバックを有効にできます。 

Microsoft Dynamics AX 2012 では、**監査ログ** フォームが Microsoft Dynamics AX 環境にアクセスしたユーザーを記録していました。 Microsoft Dynamics 365 Finance and Operations アプリでは、この情報はテレメトリでキャプチャされます。 IT 管理者は、Microsoft Dynamics Lifecycle Services (LCS) を使用して、この情報をダウンロードし、サインインしているユーザーの監査証跡を維持するためにオフライン ストレージに移動することができます。

システムを使用したユーザーの監査ログを生成するには、次の手順を実行します。

1. LCS でサインインし、実装に関連付けられているプロジェクトを開きます。
2. 実稼働環境に移動して、**環境の詳細** ページを開きます。
3. **監視** タブで、**環境の監視** リンクを選択して、監視ダッシュボードを開きます。
4. **活動** タブで、**未加工のログの表示** を選択します。
5. **クエリ** フィールドで、**ユーザー ログイン イベント** を選択します。 開始日が **終了日 - 7日** に設定されている期間を参照します。
6. 終了日を設定し、**検索** を選択します。 返される検索結果には、選択した終了日より 7 日前にシステムにサインインしたすべてのユーザーが含まれます。
7. 検索結果には、ユーザーのセッションの **AADUserID** 値と、サインインの開始時刻と終了時刻が表示されます。 **AADUserID** の値をユーザーのユーザー名と電子メールアドレスにマップするには、**ユーザー** ページ (**システム管理** > **ユーザー**) を使用します。
8. レコードをエクスポートして長期間保存するには、**エクスポート グリッド** を選択します。

完全な監査証跡を保証するために、IT 管理者は 7 日ごとにこの手順を完了する必要があります。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]