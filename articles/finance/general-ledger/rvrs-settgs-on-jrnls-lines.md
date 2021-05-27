---
title: 仕訳帳と明細行の逆仕訳設定
description: このトピックでは、一般仕訳帳に入力された逆仕訳入力が、転記済トランザクションに含まれない可能性がある理由を説明します。
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 74020f6fc9b0fa8e05a1e2a09fd13dcd60490dc0
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028572"
---
# <a name="reverse-settings-on-journals-and-lines"></a><span data-ttu-id="f60fd-103">仕訳帳と明細行の逆仕訳設定</span><span class="sxs-lookup"><span data-stu-id="f60fd-103">Reverse settings on journals and lines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f60fd-104">このトピックでは、一般仕訳帳に入力された逆仕訳入力が、転記済トランザクションに含まれない可能性がある理由を説明します。</span><span class="sxs-lookup"><span data-stu-id="f60fd-104">This topic addresses why a reversing entry that was entered on a general journal might not be included on the posted transaction.</span></span>  

## <a name="symptom"></a><span data-ttu-id="f60fd-105">現象</span><span class="sxs-lookup"><span data-stu-id="f60fd-105">Symptom</span></span>

<span data-ttu-id="f60fd-106">一般仕訳帳には、仕訳帳の逆仕訳入力と逆仕訳日が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f60fd-106">A general journal includes a reversing entry and reversing date on the journal.</span></span> <span data-ttu-id="f60fd-107">仕訳帳を転記しても、いずれの伝票も逆仕訳されません。</span><span class="sxs-lookup"><span data-stu-id="f60fd-107">When you post the journal, none of the vouchers are reversed.</span></span> <span data-ttu-id="f60fd-108">なぜこのようなことが起こるのでしょうか?</span><span class="sxs-lookup"><span data-stu-id="f60fd-108">Why does this happen?</span></span>

## <a name="resolution"></a><span data-ttu-id="f60fd-109">解決策</span><span class="sxs-lookup"><span data-stu-id="f60fd-109">Resolution</span></span>

<span data-ttu-id="f60fd-110">仕訳帳を転記すると、逆仕訳プロセスでは、伝票の **明細行** セクションの **逆仕訳入力** 設定と **逆仕訳日** 設定のみ確認されます。</span><span class="sxs-lookup"><span data-stu-id="f60fd-110">When the journal is posted, the reversing process looks only at the **Revering entry** and **Reversing date** settings on the **Lines** section of the voucher.</span></span> <span data-ttu-id="f60fd-111">この方法では、仕訳帳に、逆仕訳するようにマークされた一部の伝票を含めることができ、マークされていない伝票は含まれません。</span><span class="sxs-lookup"><span data-stu-id="f60fd-111">This approach allows a journal to include some vouchers that are marked for reversing, and others that are not.</span></span>

<span data-ttu-id="f60fd-112">仕訳帳の値は、*新しい* 明細行を追加する場合の既定値としてのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="f60fd-112">The values from the journal are only used as defaults when adding *new* lines.</span></span> <span data-ttu-id="f60fd-113">仕訳帳の値を変更しても、既存の明細行には影響しません。</span><span class="sxs-lookup"><span data-stu-id="f60fd-113">Changing the values on the journal doesn’t affect existing lines.</span></span> <span data-ttu-id="f60fd-114">この例では、伝票の明細行が最初に入力されました。</span><span class="sxs-lookup"><span data-stu-id="f60fd-114">In this example, the voucher lines were entered first.</span></span> <span data-ttu-id="f60fd-115">仕訳帳を逆仕訳として指定する前に明細行の詳細を入力すると、逆仕訳入力および日付としての指定は既存の明細行には適用されません。</span><span class="sxs-lookup"><span data-stu-id="f60fd-115">When you enter the line detail before designating the journal as reversing, the designation as a reversing entry and date won't be applied to any existing lines.</span></span>

<span data-ttu-id="f60fd-116">既存の明細行の逆仕訳入力または逆仕訳日付を変更すると、その変更が同じ伝票の他の明細行にも反映されます。</span><span class="sxs-lookup"><span data-stu-id="f60fd-116">Changing the reversing entry or reversing date on an existing line propagates that change to other lines in the same voucher.</span></span> <span data-ttu-id="f60fd-117">パフォーマンスを最適化するために、他の明細行に変更が反映された後にグリッドは更新されません。</span><span class="sxs-lookup"><span data-stu-id="f60fd-117">To optimize performance, the grid is not refreshed after propagating changes to other Lines.</span></span> <span data-ttu-id="f60fd-118">グリッドを更新すると、更新後の値を表示できます。</span><span class="sxs-lookup"><span data-stu-id="f60fd-118">You can display the updated values by refreshing the grid.</span></span>


