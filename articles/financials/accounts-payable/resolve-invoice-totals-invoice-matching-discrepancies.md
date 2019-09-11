---
title: 請求合計の照合における差異の解決の概要
description: 合計請求書の照合により、合計請求書金額が、許容差を超えて予測金額から逸脱していないことを確認できます。
author: abruer
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4a20368385ec43547ee3d29770bd83cdec47e4a
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864945"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching-overview"></a>請求合計の照合における差異の解決の概要

[!include [banner](../includes/banner.md)]

請求書照合の検証の一つのタイプは、請求合計の照合です。 システムが請求合計の照合をするよう指定するには、**買掛金勘定パラメータ** ページの **請求書の検証** タブで **請求合計の照合** オプションを **はい** に設定します。 

合計請求書の照合により、合計請求書金額が、許容差を超えて予測金額から逸脱していないことを確認できます。 6 つの合計が **請求合計照合の詳細** ページで比較されます。 合計のいずれかが、対応する発注書の合計予想金額から逸脱すると、照合不一致にフラグが立ちます。 

合計の照合不一致のある請求書を確認するには、**仕入先請求書の入力** ワークスペースで **保留中の請求書** のタイルをクリックします。 その後、アクション ペインの **確認** タブで **照合の詳細** をクリックします。 照合不一致が検出された場合に、警告アイコンが請求金額の横に表示されます。 請求合計照合の詳細を表示して合計に関する詳細を表示できます。 

不一致を識別した後で、請求書の情報が間違っていると思う場合には、仕入先に連絡する必要があるかもしれません。 その結果の仕入先との合意に応じて、次のいずれかのアクションを実行できます。

-   価格差異を受け入れ、照合不一致のある請求書を転記する。 照合不一致がある場合、転記する前に承認を要求するようにシステムが設定されている場合があります。 この場合、照合不一致を承認し、必要に応じて承認コメントを入力できます。 その後、請求書を転記する選択ができます。
-   請求書金額を想定される金額に改訂し、請求書を転記する。
-   仕入先にフル クレジットと訂正した新しい請求書を要求する。

詳細については、「[例外の調査または解決](tasks/research-resolve-exceptions.md)」を参照してください。


