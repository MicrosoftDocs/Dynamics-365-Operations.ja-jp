---
title: サービス注文の在庫品目要求の作成
description: サービス注文に特定の品目を引き当てる必要がある場合、その在庫品目要求を作成できます。
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc65393f74c6daa008e072cbe3745235fbfd896b
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2019
ms.locfileid: "1743324"
---
# <a name="create-item-requirements-for-service-orders"></a>サービス注文の在庫品目要求の作成 

[!include [banner](../includes/banner.md)]


顧客に提供するサービスを追跡および管理するサービス注文を作成できます。 サービス注文に特定の品目を引き当てる必要がある場合、その在庫品目要求を作成できます。 品目要求を在庫からすぐ消費したり、その品目の製造オーダーを開始できます。

品目トランザクションではなく在庫品目要求を使用することによって、品目が実際に使用される直前の配送を計画したり、発注書を作成したり、品目を売買契約の枠組みに含めたり、在庫品目要求を生産計画に含めたりすることができます。

サービス注文に関する要求はプロジェクトを通じて処理します。 サービス注文に対して在庫品目要求を作成するには、サービス注文をプロジェクトに関連付ける必要があります。 サービス注文に対して在庫品目要求を作成した後、選択したプロジェクトの**プロジェクト**フォームに在庫品目要求を表示できます。

## <a name="create-an-item-requirement-for-a-service-order"></a>サービス注文の在庫品目要求の作成

1.  **サービス管理** \> **共通** \> **サービス注文** \> **サービス注文**の順にクリックします。

2.  在庫品目要求を作成するサービス注文を選択します。

3.  **アクション ウィンドウ**の**出荷**タブで、**在庫品目要求**をクリックします。

4.  **在庫品目要求**フォームで、必要な品目の情報を入力します。 フォームのそれぞれのフィールドについては、[在庫品目要求 (フォーム)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)) を参照してください。

## <a name="create-an-item-requirement-for-a-service-agreement"></a>サービス契約の在庫品目要求の作成

1.  **サービス管理** \> **共通** \> **サービス契約** \> **サービス契約**の順にクリックします。

2.  在庫品目要求を作成するサービス契約を開きます。

3.  **明細行**クイックタブで、**追加**をクリックして明細行を新規作成します。

4.  **トランザクション タイプ**フィールドで、**品目**を選択します。

5.  **項目の設定**フィールドで、**在庫品目要求**を選択します。

6.  **品目番号**フィールドで、サービス契約に必要な品目を選択します。

7.  **サイト**フィールドの、**製品分析コード**タブにおける、**明細行の詳細**クイック タブで、品目の在庫サイトを選択します。

8.  契約項目からサービス注文を作成するには、**明細行**クイック タブで**サービス注文の作成**をクリックし、**サービス注文の作成**フォームに、関連情報を入力します。 


## <a name="see-also"></a>参照

[サービス注文の自動作成](create-service-orders-automatically.md)。

  


