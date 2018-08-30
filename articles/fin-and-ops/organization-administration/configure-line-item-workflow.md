---
title: "明細行品目ワークフローのコンフィギュレーション"
description: "このトピックでは、行項目ワークフローの要素をコンフィギュレーションする方法を説明します。"
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 0a57baa3ecae727721f62477cfc5fa41f60ad06d
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="configure-line-item-workflows"></a>明細行品目ワークフローのコンフィギュレーション

[!include [banner](../includes/banner.md)]

このトピックでは、行項目ワークフローの要素をコンフィギュレーションする方法を説明します。

行項目ワークフローの要素をコンフィギュレーションするには、ワークフロー エディターで要素を右クリックし、**プロパティ**をクリックして、**プロパティ**ページを開きます。 次の手順に従って、行項目ワークフローの要素をコンフィギュレーションします。

## <a name="name-the-line-item-workflow-element"></a>行項目ワークフロー要素に名前を付ける
行項目ワークフロー要素の名前を入力するには、次の手順に従います。

1.  左ウィンドウで**基本設定**をクリックします。
2.  **名前**フィールドに、行項目ワークフロー要素の名前を入力します。

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a>同じワークフローですべての行項目を処理するかどうかを指定する
ドキュメントのすべての行項目の処理に、同じワークフローを使用するかどうかを指定するには、次の手順に従います。

1.  左ウィンドウで**基本設定**をクリックします。
2.  ドキュメントのすべての行項目を同じワークフローで処理する場合は、**すべての品目に対して単一のワークフローを呼び出す**をクリックします。 その後、行項目の処理に使用するワークフローを選択します。
3.  ある特定の条件セットを満たす行項目を特定のワークフローで処理する場合は、**それぞれの品目に対してワークフローを呼び出す**をクリックします。 次に条件セットを定義するには、次の手順に従います。
    1.  **追加**をクリックします。
    2.  テーブル内の条件を選択します。
    3.  **条件名**タブで、定義する条件セットの名前を入力します。
    4.  **条件の追加**をクリックして、条件を入力します。
    5.  必要に応じて、追加条件を入力します。
    6.  入力した条件セットが正しく構成されていることを検証するには、**テスト**をクリックします。 **ワークフロー条件のテスト**ページの、**条件の検証**領域で、レコードを選択して、**テスト**をクリックします。 システムによってレコードが評価され、定義した条件を満たすかどうかが判定されます。 **OK**、または**キャンセル**をクリックして、**プロパティ**ページに戻ります。

    **ワークフロー**タブで、定義した条件セットを満たす行項目の処理に使用するワークフローを選択します。





