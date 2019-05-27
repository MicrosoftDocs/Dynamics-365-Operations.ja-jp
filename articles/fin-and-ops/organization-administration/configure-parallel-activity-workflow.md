---
title: ワークフローでの並列活動のコンフィギュレーション
description: 並列活動をコンフィギュレーションするには、ワークフロー エディターで次の手順を実行します。
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01c1fa876dd66ba6f0e1cdcecff56f424e117bd9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563322"
---
# <a name="configure-parallel-activities-in-a-workflow"></a>ワークフローでの並列活動のコンフィギュレーション

[!include [banner](../includes/banner.md)]

並列活動をコンフィギュレーションするには、ワークフロー エディターで次の手順を実行します。

並列活動は、同時に実行されるワークフロー分岐から構成されます。

## <a name="name-a-parallel-activity"></a>並列活動の名前の設定

並列活動の名前を入力するには、次の手順に従います。

1. 並列活動を右クリックし、**プロパティ**をクリックして、**プロパティ**フォームを開きます。
2. 左ウィンドウで**基本設定**をクリックします。
3. **名前**フィールドに、並列活動の一意な名前を入力します。
4. **閉じる**をクリックします。

## <a name="configure-the-branches-of-a-parallel-activity"></a>並列活動の分岐のコンフィギュレーション

この並列活動の分岐を追加およびコンフィギュレーションするには、次の手順に従います。

1. 並列活動の分岐を表示する並列活動をダブルクリックします。
2. 分岐を追加するには、**分岐**要素を**ワークフロー要素**領域からキャンバス上の挿入ポイントにドラッグします。 次の図に、挿入ポイントを示します。

    ![挿入ポイント](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > 並列活動の分岐はすべて同時に実行されるため、分岐の順序は重要ではありません。

3. 各分岐をコンフィギュレーションするには、[並列分岐のコンフィギュレーション](configure-parallel-branch-workflow.md)を参照してください。
