---
title: 作業指示書タイプ
description: このトピックでは、資産管理における作業指示書タイプについて説明します。
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3e813bd4f2d47b928b6184bb063d9afa45695727
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569734"
---
# <a name="work-order-types"></a>作業指示書タイプ

[!include [banner](../../includes/banner.md)]

 

作業指示書タイプは、作業指示書を分類するために使用されます。 例えば、予防的メンテナンスおよび修繕メンテナンスに関連する作業指示書があるとします。

作業指示書タイプは、作業指示書ライフサイクル モデルとの所属を定義します。 作業指示書のライフサイクル モデルでは、作業指示書に対して設定できる作業指示書ライフサイクルの状態が定義されます。 (作業指示書のライフサイクルの状態の例として**作成**、**処理中**、**完了済**があります)。

作業指示書ライフサイクルの状態とプロジェクト ステージの詳細については、[作業指示書ライフサイクルの状態](work-order-lifecycle-states.md) を参照してください。

1. **資産管理** \> **設定** \> **作業指示書** \> **作業指示書タイプ**を選択します。
2. **新規作成**を選択して作業指示書タイプを作成します。
3. **作業指示書タイプ** フィールドで、作業指示書タイプの ID を入力します。
4. **名前**フィールドに、名前を入力します。
5. **作業指示書ライフサイクル モデル** フィールドで、ライフサイクル モデルを選択します。
5. このタイプの作業指示書に関連するすべての作業指示書ジョブを同じメンテナンス作業者にスケジュールする必要がある場合は、**1 人のメンテナンス作業者**オプションを**はい**に設定します。
6. **原価タイプ** フィールドで該当する場合、**修正**、**予防的**、または**投資**を選択します。 作業指示書のすべての作業指示書ジョブは必ず同じ原価タイプを持つ必要があります。
7. **必須**セクションで、関連するオプションを**はい**に設定し、このタイプの作業指示書に追加される障害関連またはメンテナンス ダウンタイムなどの関連情報を指定します。

    > [!NOTE]
    > **必須**セクションのオプションは、**作業指示書のライフサイクルの状態**ページで**検証**クイックタブのオプションに関連しています (**資産管理** \> **設定** \> **作業指示書** \> **ライフサイクルの状態**)。

8. **保存** を選択します。

![作業指示書タイプ](media/16-setup-for-work-orders.png)
