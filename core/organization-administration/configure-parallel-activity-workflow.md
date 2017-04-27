---
title: "ワークフロー内の並列活動のコンフィギュレーション"
description: "並列活動をコンフィギュレーションするには、ワークフロー エディターで次の手順を実行します。"
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
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
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 818fb054742b935d002a7341e54a37eca0bb4761
ms.lasthandoff: 03/31/2017


---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>ワークフロー内の並列活動のコンフィギュレーション

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
    | **メモ **                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | 並列活動の分岐はすべて同時に実行されるため、分岐の順序は重要ではありません。 |

3.  各分岐をコンフィギュレーションするには、[並列分岐のコンフィギュレーション](http://axhelp.dynamics.com/en/wiki/configure-a-parallel-branch/)を参照してください。




