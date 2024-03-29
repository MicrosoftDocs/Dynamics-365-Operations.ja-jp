---
title: メンテナンス要求タイプ
description: この記事では、資産管理でメンテナンス要求のタイプを設定する方法について説明します。
author: johanhoffmann
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a2d707cc9c0aa4863968651a8434883cc1322eb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888704"
---
# <a name="maintenance-request-types"></a>メンテナンス要求のタイプ

[!include [banner](../../includes/banner.md)]

 

メンテナンス要求タイプは、メンテナンス要求を分類する目的で使用されます。 たとえば、予防的メンテナンスおよび修繕メンテナンスに関連するメンテナンス要求のタイプがあるとします。 または、資産の修復 (Depot 修復) の管理に使用される特殊メンテナンス要求のタイプもあります。

メンテナンス依頼のタイプは、メンテナンス要求のライフサイクルの状態グループ (メンテナンス ライフサイクル モデル) との所属を定義します。 メンテナンス要求のライフサイクル モデルは、メンテナンス要求に対して設定できるライフサイクルの状態を定義します。 (メンテナンス要求ライフサイクルの状態の例には、**作成済**、**有効**、および **終了済** が含まれます。)

1. **資産管理** \> **設定** \> **メンテナンス要求** \> **メンテナンス要求のタイプ** を選択します。
2. **新規** を選択して、メンテナンス要求のタイプを作成します。
3. **メンテナンス要求のタイプ** フィールドで、メンテナンス依頼のタイプの ID を入力します。
4. **名前** フィールドに、名前を入力します。
5. **一般** クイック タブでは、**メンテナンス要求のライフサイクル モデル** フィールドで、メンテナンス要求のライフサイクル モデルを選択します。
6. **ワーク オーダー タイプ** フィールドで、ワーク オーダー タイプを選択します。 メンテナンス要求がワーク オーダーに変換されると、そのワーク オーダーは、メンテナンス要求のタイプに関連するワーク オーダータイプを自動的に取得します。

次の図は、**メンテナンス要求のタイプ** ページの例を示しています。

![メンテナンス要求のタイプ ページ。](media/07-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]