---
title: BOM 明細行の部品消費ルールの設定が念入りではない
description: 部品表 (BOM) 明細行の部品消費ルールの設定が念入りではない。
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026679"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a><span data-ttu-id="6591d-103">BOM 明細行の部品消費ルールの設定が念入りではない</span><span class="sxs-lookup"><span data-stu-id="6591d-103">Flushing principle settings on BOM lines aren't respected</span></span>

<span data-ttu-id="6591d-104">KB 番号: 4612725</span><span class="sxs-lookup"><span data-stu-id="6591d-104">KB number: 4612725</span></span>

## <a name="symptoms"></a><span data-ttu-id="6591d-105">現象</span><span class="sxs-lookup"><span data-stu-id="6591d-105">Symptoms</span></span>

<span data-ttu-id="6591d-106">この問題は、**生産管理パラメータ** ページの **自動更新** タブの **自動 BOM 消費** フィールドが *部品消費ルール* に設定 されている場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="6591d-106">This issue occurs when the **Automatic BOM consumption** field on the **Automatic update** tab of the **Production control parameters** page is set to *Flushing principle*.</span></span> <span data-ttu-id="6591d-107">この設定は、発注書を受け取った時点で、すべての部品表 (BOM) 明細行が自動的に消費されます。</span><span class="sxs-lookup"><span data-stu-id="6591d-107">This setting indicates that all bill of materials (BOM) lines should automatically be consumed when a purchase order is received.</span></span> <span data-ttu-id="6591d-108">BOM 明細行の **部品消費ルール** フィールドが明示的に *手動* に設定されている場合は、BOM 明細行が自動的に消費される可能性が 生じない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6591d-108">If the **Flushing principle** field on BOM lines is explicitly set to *Manual*, you might expect that the BOM lines won't automatically be consumed.</span></span> <span data-ttu-id="6591d-109">ただし、この問題が発生すると、**部品消費ルール** フィールドが *手動* に設定されている BOM 明細行が自動的に消費されます。</span><span class="sxs-lookup"><span data-stu-id="6591d-109">However, when this issue occurs, BOM lines where the **Flushing principle** field is set to *Manual* are automatically consumed anyway.</span></span>

## <a name="resolution"></a><span data-ttu-id="6591d-110">解像度</span><span class="sxs-lookup"><span data-stu-id="6591d-110">Resolution</span></span>

<span data-ttu-id="6591d-111">この問題が発生した場合は、BOM 明細行の **部品消費ルール** の設定を上書きするために生産管理パラメータが設定されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6591d-111">If you're experiencing this issue, your production control parameters might be set up to override the **Flushing principle** setting on BOM lines.</span></span> <span data-ttu-id="6591d-112">**生産管理パラメータ** ページの **自動更新** タブで、**自動 BOM 消費** フィールドの値を確認 します。</span><span class="sxs-lookup"><span data-stu-id="6591d-112">On the **Production control parameters** page, on the **Automatic update** tab, check the value of the **Automatic BOM consumption** field.</span></span> <span data-ttu-id="6591d-113">*常時* に設定されている場合、システムは、すべての BOM 明細行の **部品消費ルール** 設定を無視し、常に明細行をフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="6591d-113">If it's set to *Always*, the system will disregard the **Flushing principle** setting on all BOM lines and will always flush the lines.</span></span> <span data-ttu-id="6591d-114">BOM 明細行の **部品消費ルール** 設定をシステムで適用するには、**自動 BOM 消費** フィールドの値を *部品消費原則* に変更します 。</span><span class="sxs-lookup"><span data-stu-id="6591d-114">To make the system respect the **Flushing principle** setting on BOM lines, change the value of the **Automatic BOM consumption** field to *Flushing principle*.</span></span>
