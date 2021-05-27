---
title: 需要予測レコードをインポートする際に予測単位原価を更新できない
description: データ エンティティを使用して需要予測レコードをインポートする場合、既存のレコードの原価価格はインポートされたデータに一致するようには更新されません。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026681"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a><span data-ttu-id="02bcd-103">需要予測レコードをインポートする際に予測単位原価を更新できない</span><span class="sxs-lookup"><span data-stu-id="02bcd-103">You can't update the forecasted unit cost when you import demand forecast records</span></span>

<span data-ttu-id="02bcd-104">KB 番号: 4614109</span><span class="sxs-lookup"><span data-stu-id="02bcd-104">KB number: 4614109</span></span>

## <a name="symptoms"></a><span data-ttu-id="02bcd-105">現象</span><span class="sxs-lookup"><span data-stu-id="02bcd-105">Symptoms</span></span>

<span data-ttu-id="02bcd-106">データ エンティティを使用して需要予測レコードをインポートする場合、既存のレコードの **予測単価** の値はインポートされたデータに一致するようには更新されません。</span><span class="sxs-lookup"><span data-stu-id="02bcd-106">When you use data entities to import demand forecast records, the **Forecasted unit cost** value for existing records isn't updated so that it matches the imported data.</span></span>

## <a name="cause"></a><span data-ttu-id="02bcd-107">原因</span><span class="sxs-lookup"><span data-stu-id="02bcd-107">Cause</span></span>

<span data-ttu-id="02bcd-108">**予測単位原価** は読み取り専用フィールドです。</span><span class="sxs-lookup"><span data-stu-id="02bcd-108">**Forecasted unit cost** is a read-only field.</span></span> <span data-ttu-id="02bcd-109">この値は製品の単位原価に基づいており、インポートによって直接設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="02bcd-109">The value is based on the product unit cost and can't be set directly through import.</span></span>

## <a name="resolution"></a><span data-ttu-id="02bcd-110">解像度</span><span class="sxs-lookup"><span data-stu-id="02bcd-110">Resolution</span></span>

<span data-ttu-id="02bcd-111">このフィールドは読み取り専用であるため、値をインポートできません。</span><span class="sxs-lookup"><span data-stu-id="02bcd-111">Because the field is read only, you can't import values for it.</span></span> <span data-ttu-id="02bcd-112">この値は、既存のビジネス ロジックに従って計算されます。</span><span class="sxs-lookup"><span data-stu-id="02bcd-112">The value will be calculated according to the existing business logic.</span></span>
