---
title: 資産サービス レベル
description: この記事では、資産管理の資産サービス レベルについて説明します。
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f7429b30253f540925e67ff9239667a0a404f26
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908688"
---
# <a name="asset-service-levels"></a>資産サービス レベル

[!include [banner](../../includes/banner.md)]

 

この記事では、資産管理の資産サービス レベルについて説明します。 資産サービス レベルは資産に関連し、メンテナンス要求およびワーク オーダーに転送されます。 これらは、ワーク オーダー スケジューリング中にワーク オーダーの優先順位を計算するために使用されます。 変更が必要な場合、資産サービス レベルを変更できます。

ワーク オーダー スケジューリングの評価スコアの計算に関連する設定の詳細については、[資産管理パラメーター](../setup-for-objects/enterprise-asset-management-parameters.md) を参照してください。 資産サービス レベルに対して、少なくとも 1 つの既定レコードを設定する必要があります。 この既定のレコードは、ワーク オーダー スケジューリング中に他の一致が見つからない場合に使用されます。

**例 1:** 他の一致が見つからない場合に使用される既定のサービス レベル。 このレコードでは、サービス レベルのみを選択します。

**例 2:** ボルボ トラック エンジンのジョブ スケジュールに使用される高サービス レベル。 このレコードでは、関連する資産タイプ (**トラック エンジン** など)、メーカー (**ボルボ**) 、およびサービス レベルを選択します。

## <a name="set-up-asset-service-levels"></a>資産サービス レベルの設定

1. **資産管理** \> **設定** \> **資産サービス レベル** を選択します。
2. **新規** を選択してレコードを作成します。
3. 資産サービス レベルに必要な詳細レベルに応じて、**機能場所**、**資産タイプ**、**メーカー**、**モデル**、**資産**、**ワーク オーダー タイプ**、および **サービス レベル** フィールドで関連する選択を行います。

    > [!NOTE]
    > 資産サービス レベルがメンテナンス要求およびワーク オーダーに使用される場合、資産管理はすべての資産サービス レベル レコードを調べて、一致の可能性をチェックします。 常に最も限定的な組み合わせを最初にチェックします。 つまり、資産管理は、まず **ワーク オーダー タイプ** フィールドの一致をチェックします。 一致するものが見つからない場合は、**資産** フィールドなどの一致がチェックされます。 **資産 サービス レベル** ページのレイアウトで分かるように、この動作は、最も限定的な組み合わせを見つけるために、資産管理が各レコードを右から左に一致をチェックすることを意味します。 一致するものが見つからない場合は、これらのフィールドに選択がない既定のレコードが使用されます。

4. **サービス レベル** フィールドで、サービス レベル (優先順位) を示す番号を選択します。


> [!NOTE]
> ワーク オーダーで既に使用した後に **資産サービス レベル** ページで資産 サービス レベル レコードを変更した場合、メンテナンス要求とワーク オーダーにあるサービス レベルは適宜更新されません。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]