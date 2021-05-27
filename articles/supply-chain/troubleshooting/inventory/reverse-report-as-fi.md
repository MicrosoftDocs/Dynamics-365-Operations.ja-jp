---
title: 完了報告の取消によって、予期しないオープン トランザクションが作成される
description: マーキングが設定されている完了報告を取り消すと、取り消された数量の在庫分析コードが取り消されたトランザクションと同じオープン トランザクションが作成されます。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026689"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a><span data-ttu-id="20339-103">完了報告の取消によって、予期しないオープン トランザクションが作成される</span><span class="sxs-lookup"><span data-stu-id="20339-103">Reversal of reporting as finished creates an unexpected open transaction</span></span>

<span data-ttu-id="20339-104">KB 番号: 4612469</span><span class="sxs-lookup"><span data-stu-id="20339-104">KB number: 4612469</span></span>

## <a name="symptoms"></a><span data-ttu-id="20339-105">現象</span><span class="sxs-lookup"><span data-stu-id="20339-105">Symptoms</span></span>

<span data-ttu-id="20339-106">マーキングが設定されている完了報告を取り消すと、システムが、取り消された数量の在庫分析コードが取り消されたトランザクションと同じオープン トランザクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="20339-106">If you reverse reporting as finished that has marking, the system creates an open transaction where the reversed quantity has the same inventory dimensions as the transaction that was reversed.</span></span>

## <a name="resolution"></a><span data-ttu-id="20339-107">解像度</span><span class="sxs-lookup"><span data-stu-id="20339-107">Resolution</span></span>

<span data-ttu-id="20339-108">完了レポートの操作を取り消す場合、在庫分析コードは生産仕訳帳から初期化されます。</span><span class="sxs-lookup"><span data-stu-id="20339-108">When you reverse a report-as-finished operation, the inventory dimension is initialized from the production journal.</span></span> <span data-ttu-id="20339-109">したがって、バッチ番号が取得されます。</span><span class="sxs-lookup"><span data-stu-id="20339-109">Therefore, it gets the batch number.</span></span> <span data-ttu-id="20339-110">マーキングのため、販売注文トランザクションはバッチ番号を継承します。</span><span class="sxs-lookup"><span data-stu-id="20339-110">Because of marking, the sales order transactions will inherit the batch number.</span></span>

<span data-ttu-id="20339-111">完了レポートが転記される際に分析コードをリセットできます。</span><span class="sxs-lookup"><span data-stu-id="20339-111">The dimension can be reset when the reporting as finished is posted.</span></span>
