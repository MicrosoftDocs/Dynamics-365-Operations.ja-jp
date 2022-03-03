---
title: B2B Web サイトの注文を迅速に実行する
description: このトピックでは、企業間 (B2B) サイト ユーザーがバルク注文やリピート注文を迅速に実行できる Microsoft Dynamics 365 Commerce の機能について説明します。
author: shajain
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 4909056435425f251efb45f5a4355f103a420ba8
ms.sourcegitcommit: 4d52c67f52ad0add63cd905df61367b344389069
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/16/2022
ms.locfileid: "8312605"
---
# <a name="place-b2b-website-orders-quickly"></a>B2B Web サイトの注文を迅速に実行する

[!include [banner](../../includes/banner.md)]

このトピックでは、企業間 (B2B) サイト ユーザーがバルク注文やリピート注文を迅速に実行できる Microsoft Dynamics 365 Commerce の機能について説明します。

Dynamics 365 Commerce B2B eコマースの Web サイトを使用すると、ユーザーは、検索や閲覧による新製品の検出、製品詳細の表示、品目のカートへの追加、チェックアウトなどの標準的な操作を実行できます。ただし、企業間 (B2C) サイトの顧客は、通常、品目を少量で 1 回だけ注文しますが、通常、B2B 顧客は品目を大量に複数回注文します。 通常、このような顧客は購入したい品目をよく把握しているため、製品の検出フェーズをスキップして、直接注文に移動します。 Commerce B2B eコマースの Web サイトは、顧客のニーズを満たすために役立つさまざまな機能を提供します。

## <a name="bulk-order-by-item-number"></a>品目番号でのバルク注文

Commerce B2B eコマースの Web サイトでは、サイト ユーザーが必要な数量と製品品目番号を入力して、品目をカートに追加できます。

次の図は、製品品目番号でのクイック注文入力の例を示しています。

![製品品目番号でのクイック注文入力。](../media/QuickAddByItem.png)

## <a name="bulk-order-by-variant"></a>バリアント別バルク注文

Commerce B2B eコマース Web サイトを使用すると、サイト ユーザーは、サイズ、色、およびスタイル別に在庫状態を表示する単一のビューで、同じ製品の異なるバリアントを簡単に追加できます。 さらに、サイト ユーザーは、**すべての数量を入力** を選択して、すべての在庫製品の同じ数量を簡単に入力することができます。

次の図は、"すべての数量の入力" 機能を使用したクイック注文入力の例を示しています。

!["すべての数量を入力" 機能を使用したクイック注文入力。](../media/MatrixView.png)

## <a name="use-order-templates-for-quick-order-entry"></a>クイック注文入力で注文テンプレートを使用する

B2B Web サイトの購入担当者は、特定の品目をまとめて注文することがよくあります。 たとえば、建設現場で必要な注文を行う場合は、シャツ、ジャケット、ズボン、靴、帽子などを一緒に注文することがあります。 医者、看護師、清掃スタッフなどへの異なるユニフォームが必要な病院のために注文を行う場合は、各ユニフォームのタイプをグループ化すると、注文が簡単になることもあります。 このタイプのシナリオでは、Commerce B2B サイトを使用して注文テンプレートを作成できます。 サイト ユーザーは、任意の数のカスタム テンプレートを作成した後、そのテンプレートからすべてまたは一部の品目を必要に応じて注文できます。

次の図は、注文テンプレートのの例を示しています。

![注文テンプレートの例。](../media/OrderTemplateHeader.png)

次の図は、注文テンプレートの例を表示しています。

![注文テンプレートの詳細ビューの例。](../media/OrderTemplateLines.png)

## <a name="reorder-from-order-history"></a>注文履歴から再注文する

Commerce B2B eコマース Web サイトを使用すると、サイト ユーザーは注文履歴から品目をすばやく再注文できます。 サイト ユーザーは、注文履歴から選択した品目を購入するか、以前に購入した品目をカートに追加することができます。

次の図は、ユーザーの注文履歴と、その履歴から品目を再注文するオプションの例を示しています。

![注文履歴から再注文する。](../media/Reorder.png)

このトピックでは、Commerce B2B サイトを使用すると、ユーザーが必要な製品をすばやく見つけて注文、再注文することができます。 バルク注文のキャプチャ プロセスを簡素化するために、さらなる機能が開発中です。
