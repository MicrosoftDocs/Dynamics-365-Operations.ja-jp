---
title: "ワークフロー内の並列活動のコンフィギュレーション"
description: "並列活動をコンフィギュレーションするには、ワークフロー エディターで次の手順を実行します。"
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: ce3fca9d2dbca046232365b1375bfd920d5b10fd
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>ワークフロー内の並列活動のコンフィギュレーション

[!include[banner](../includes/banner.md)]


並列活動をコンフィギュレーションするには、ワークフロー エディターで次の手順を実行します。

並列活動は、同時に実行されるワークフロー分岐から構成されます。

## <a name="name-a-parallel-activity"></a>並列活動の名前の設定
並列活動の名前を入力するには、次の手順に従います。
1.  並列活動を右クリックし、[**プロパティ**] をクリックして、[**プロパティ**] フォームを開きます。
2.  左ウィンドウで [**基本設定**] をクリックします。
3.  [**名前**] フィールドに、並列活動の一意な名前を入力します。
4.  [**閉じる**] をクリックします。

## <a name="configure-the-branches-of-a-parallel-activity"></a>並列活動の分岐のコンフィギュレーション
この並列活動の分岐を追加およびコンフィギュレーションするには、次の手順に従います。
1.  並列活動の分岐を表示する並列活動をダブルクリックします。
2.  分岐を追加するには、[**分岐**] 要素を [**ワークフロー要素**] 領域からキャンバス上の挿入ポイントにドラッグします。 次の図は、挿入ポイントを示しています。![Insertion point](./media/workflow_insertionpoint.gif)
    | **メモ**                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | 並列活動の分岐はすべて同時に実行されるため、分岐の順序は重要ではありません。 |

3.  各分岐をコンフィギュレーションするには、[並列分岐のコンフィギュレーション](configure-parallel-branch-workflow.md)を参照してください。






