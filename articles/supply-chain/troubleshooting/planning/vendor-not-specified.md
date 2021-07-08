---
title: 計画オーダーの確定時に仕入先が指定されていない場合
description: 計画オーダーを確定しようとすると、仕入先が指定されていないというエラー メッセージが表示されます。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cf41295045211f8a714194494028922d573c9e9e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294116"
---
# <a name="vendor-isnt-specified-when-planned-orders-are-firmed"></a><span data-ttu-id="23a9e-103">計画オーダーの確定時に仕入先が指定されていない場合</span><span class="sxs-lookup"><span data-stu-id="23a9e-103">Vendor isn't specified when planned orders are firmed</span></span>

<span data-ttu-id="23a9e-104">エラーコード: SYS23532</span><span class="sxs-lookup"><span data-stu-id="23a9e-104">Error code: SYS23532</span></span>

## <a name="symptoms"></a><span data-ttu-id="23a9e-105">現象</span><span class="sxs-lookup"><span data-stu-id="23a9e-105">Symptoms</span></span>

<span data-ttu-id="23a9e-106">計画オーダーを確定しようとする際に、次のエラー メッセージが表示されます:</span><span class="sxs-lookup"><span data-stu-id="23a9e-106">When you try to firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="23a9e-107">仕入先が指定されていません</span><span class="sxs-lookup"><span data-stu-id="23a9e-107">Vendor is not specified</span></span>

## <a name="resolution"></a><span data-ttu-id="23a9e-108">解決策</span><span class="sxs-lookup"><span data-stu-id="23a9e-108">Resolution</span></span>

<span data-ttu-id="23a9e-109">仕入先を指定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="23a9e-109">To specify a vendor, follow these steps.</span></span>

1. <span data-ttu-id="23a9e-110">仕入先が欠落している計画オーダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="23a9e-110">Open the planned order that is missing a vendor.</span></span>
1. <span data-ttu-id="23a9e-111">**計画済供給** クイックタブの、**仕入先** フィールドで、仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="23a9e-111">On the **Planned supply** FastTab, in the **Vendor** field, select a vendor.</span></span>
