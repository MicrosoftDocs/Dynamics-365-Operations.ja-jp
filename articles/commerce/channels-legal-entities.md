---
title: 法人を作成します
description: このトピックでは、Microsoft Dynamics 365 Commerce で法人を作成する方法について説明していますが、チャネルを作成する前に作成してコンフィギュレーションする必要があります。
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 225fd6a07fee29414ac30a4602b4dfccdc4d742b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800618"
---
# <a name="create-legal-entities"></a>法人を作成します

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce で法人を作成する方法について説明していますが、チャネルを作成する前に作成してコンフィギュレーションする必要があります。

法人とは、登記または法的手続きを済ませた法律上の構造を持つ組織です。 法人には、法的契約の締結が認められており、業績を報告する収支報告書の作成が義務付けられています。

会社とは、法人の 1 つのタイプです。 現在、会社はユーザーが作成できる唯一の法人であり、個々の法人は会社 ID と関連付けられています。 この関連付けは、プログラム内の一部の機能エリアで法人 ID (データモデルでは *DataAreaId*) が使用されているために設けられています。 これらの機能エリアでは、データのセキュリティ区分として法人が使用されています。 ユーザーは、現在ログオン中の会社のデータにのみアクセスできます。 

チャネルを作成するときは、チャネルが属している法人を指定する必要があります。

## <a name="create-a-new-legal-entity"></a>新しい法人の作成

Dynamics 365 Commerce に新しい法人を作成するには、次の手順を実行します。

1. ナビゲーション ウィンドウで、**モジュール \> 本社の設定 \> 法人** の順に移動します。
1. アクション ウィンドウで、**新規** を選択します。 **新しい法人** ウィンドウが右側に表示されます。
1. **名前** フィールドに値を入力します。
1. **会社** フィールドに値を入力します。
1. **国/地域** フィールドで、値を入力または選択します。
1. **OK** を選択します。 

   ![法人の作成](media/legal-entities.png)

1. **一般** セクションで、法人に関する次の一般情報を提供します。 
   1. 検索名が必要な場合、検索名を入力します。 検索名は、この法人を検索するために使用できる代替名です。 
   1. この法人が連結会社として使用されているかどうかを選択します。
   1. この法人が削除会社として使用されているかどうかを選択します。 
   1. エンティティの **既定の言語** を選択します。 
   1. エンティティの **タイム ゾーン** を選択します。
1. **住所** セクションで、**編集** を選択して、番地、郵便番号、市区町村名などの住所情報を入力します。
1. **連絡先情報** セクションで、電子メール アドレス、URL と電話番号など通信方法に関する情報を入力します。
1. **法定レポート** セクションで、法定レポートに使用される登録番号を入力します。
1. **登録番号** セクションで、法人に必要な情報を入力します。
1. **銀行口座情報** セクションで、法人の銀行口座と処理番号を入力します。
1. **対外貿易およびロジスティクス** セクションで、法人の出荷情報を入力します。
1. **番号順序** セクションで、法人に関連付けられている番号順序を表示できます。 開始時は空になります。
1. **ダッシュボードの画像** セクションで、法人に関連するロゴまたはダッシュボードの画像を表示または変更します。
1. **税登録** セクションで、税務当局に報告するために使用される登録番号を入力します。
1. **税金 1099** セクションで、法人の 1099 情報を入力します。
1. **税情報** セクションで、法人の税情報を入力します。
1. **保存** を選択します。

次の図は、法人の例の詳細を示しています。

![法人の一般セクション](media/legal-entities-general.png)
   
## <a name="additional-resources"></a>追加リソース

[組織と組織階層の概要](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[組織階層の計画](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[組織階層](channels-org-hierarchies.md)

[チャネルの概要](channels-overview.md)

[チャネル設定の前提条件](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
