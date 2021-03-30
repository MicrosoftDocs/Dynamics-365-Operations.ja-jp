---
title: 資産グループの減損損失の提案と転記
description: 日本では、減損金額の計算後に、その金額を固定資産仕訳帳に提案し転記することができます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf3e153adfb4fc65e2d4eabad02765a2cf45a5c2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239609"
---
# <a name="propose-and-post-the-impairment-amount-on-a-cash-generating-unit"></a><span data-ttu-id="141a7-103">資産グループの減損損失の提案と転記</span><span class="sxs-lookup"><span data-stu-id="141a7-103">Propose and post the impairment amount on a cash generating unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="141a7-104">日本では、減損金額の計算後に、その金額を固定資産仕訳帳に提案し転記することができます。</span><span class="sxs-lookup"><span data-stu-id="141a7-104">For Japan, after the calculation of the impairment amount, you can propose and post it in a fixed asset journal.</span></span>



<span data-ttu-id="141a7-105">この手順では、資産グループで認識および計算された減損金額の提案と転記について説明します。</span><span class="sxs-lookup"><span data-stu-id="141a7-105">This procedure walks you through proposing and posting impairment amounts that are recognized and calculated on cash generating unit.</span></span> 



<span data-ttu-id="141a7-106">このタスクを完了するには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="141a7-106">In order to complete this task, the  Fixed Asset configuration key must be selected.</span></span>

<span data-ttu-id="141a7-107">また、このタスクを実行する前に認識テストを作成し確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="141a7-107">Also, you will need to create and confirm a recognition test before running this task.</span></span> 



<span data-ttu-id="141a7-108">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="141a7-108">This procedure was created using the demo data company JPMF.</span></span>

1. <span data-ttu-id="141a7-109">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="141a7-109">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="141a7-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="141a7-110">Click New.</span></span>
3. <span data-ttu-id="141a7-111">[名前] フィールドに値を入力するか選択します。</span><span class="sxs-lookup"><span data-stu-id="141a7-111">In the Name field, type or select a value.</span></span>
4. <span data-ttu-id="141a7-112">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="141a7-112">Click Lines.</span></span>
5. <span data-ttu-id="141a7-113">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="141a7-113">Click Proposals.</span></span>
6. <span data-ttu-id="141a7-114">[減損提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="141a7-114">Click Impairment proposal.</span></span>
7. <span data-ttu-id="141a7-115">[減損テスト ID] フィールドに、転記する認識テストの ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="141a7-115">In the Impairment test ID field, enter the ID of the recognition test that you want to post.</span></span>
8. <span data-ttu-id="141a7-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="141a7-116">Click OK.</span></span>
9. <span data-ttu-id="141a7-117">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="141a7-117">Click Post.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]