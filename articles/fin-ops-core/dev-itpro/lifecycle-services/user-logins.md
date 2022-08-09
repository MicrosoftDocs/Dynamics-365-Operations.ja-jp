---
title: ユーザー サインインの追跡
description: この記事では、財務と運用アプリにサインインして使用するユーザーの監査ログを作成する方法について説明します。
author: angelmarshall
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2017-10-31
ms.dyn365.ops.version: Platform update 12
ms.openlocfilehash: 3f81b104f57b902529f9cecf9b909ef58f594b08
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103574"
---
# <a name="track-user-sign-ins"></a>ユーザー サインインの追跡 
 
[!include [banner](../includes/banner.md)]

多くの組織は、システムを使用したユーザーの監査証跡を管理する必要があります。 この要件は、コンプライアンス上の理由から、または不適切な使用が発生した場合にトラックバックを有効にできます。 

Microsoft Dynamics AX 2012 では、**監査ログ** フォームが Microsoft Dynamics AX 環境にアクセスしたユーザーを記録していました。 Microsoft Dynamics 365 財務と運用アプリでは、この情報はテレメトリでキャプチャされます。 IT 管理者は、Microsoft Dynamics Lifecycle Services (LCS) を使用して、この情報をダウンロードし、サインインしているユーザーの監査証跡を維持するためにオフライン ストレージに移動することができます。

システムを使用したユーザーの監査ログを生成するには、次の手順を実行します。

1. LCS でサインインし、実装に関連付けられているプロジェクトを開きます。
2. 運用環境に移動して、**環境の詳細** ページを開きます。
3. **監視** タブで、**環境の監視** リンクを選択して、監視ダッシュボードを開きます。
4. **活動** タブで、**未加工のログの表示** を選択します。
5. **クエリ** フィールドで、**ユーザー ログイン イベント** を選択します。 開始日が **終了日 - 7日** に設定されている期間を参照します。
6. 終了日を設定し、**検索** を選択します。 返される検索結果には、選択した終了日より 7 日前にシステムにサインインしたすべてのユーザーが含まれます。
7. 検索結果には、ユーザーのセッションの **AADUserID** 値と、サインインの開始時刻と終了時刻が表示されます。 **AADUserID** の値をユーザーのユーザー名と電子メールアドレスにマップするには、**ユーザー** ページ (**システム管理** > **ユーザー**) を使用します。
8. レコードをエクスポートして長期間保存するには、**エクスポート グリッド** を選択します。

完全な監査証跡を保証するために、IT 管理者は 7 日ごとにこの手順を完了する必要があります。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

