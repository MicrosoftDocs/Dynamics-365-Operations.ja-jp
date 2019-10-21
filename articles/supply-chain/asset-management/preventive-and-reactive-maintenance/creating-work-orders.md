---
title: 作業指示書の作成
description: このトピックでは、資産管理で作業指示書を作成する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0a348bc9b7f5a24c5a3ac57113d430a92020b893
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922117"
---
# <a name="creating-work-orders"></a>作業指示書の作成

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

予防的メンテナンス ジョブがスケジュールされている場合は、次の手順でジョブの作業指示書を作成します。 これは、メンテナンス スケジュールのいずれかで行われます。 メンテナンス スケジュールのスケジュールされたジョブには、異なる参照タイプがあります。

| 参照タイプ | 説明                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| メンテナンス計画     | 予防的メンテナンス ジョブは、メンテナンス計画タイプの "時間" または "カウンター" に基づきます。                       |
| メンテナンス ラウンド    | 予防的メンテナンス ジョブには、同様のタイプのメンテナンスを必要とする複数の資産が含まれます。           |
| メンテナンス要求   | 手動で作成された資産のメンテナンスまたは修理に対する要求が、ワークオーダーに変換されます。 |


1. **資産管理** > **共通** > **すべてのメンテナンス スケジュール**または**未処理のメンテナンス スケジュール行**または**未処理のメンテナンス スケジュール プール**の順にクリックします。

2. 作業指示書を作成するスケジュール済みメンテナンス ジョブを選択し、**作業指示書**をクリックします。 **作業指示書の作成**ダイアログで、**メンテナンス予測時間**フィールドには、選択した明細行に対する予測時間の合計数が表示されます。

3. **パラメーター** セクションで、作成する必要がある作業指示の数を選択します。 1つのメンテナンス スケジュール行ごとに 1 つの作業指示書、または **1 つの作業指示書ごと**の選択項目に基づいて複数の作業指示書を作成できます。

4. 作成するすべての作業指示書で使用される**作業指示書タイプ**を選択します。 次の図は、**作業指示書の作成**ダイアログの例を示しています。

![図 1](media/18-preventive-maintenance.png)

5. **OK**をクリックします。 1 つ以上の作業指示書が作成されます。

