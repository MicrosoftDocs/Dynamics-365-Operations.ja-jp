---
title: 月次締め請求書の対象にする仕入先マスターおよび発注書の設定
description: 日本では通常、仕入先はトランザクションに月次締め請求書を使用します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, PurchTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2364ee80cae1c32fbfcd88ee4cb7e2b01bbb84c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252119"
---
# <a name="setup-vendor-master-and-purchase-order-to-be-target-of-consolidated-invoice"></a><span data-ttu-id="7485f-103">月次締め請求書の対象にする仕入先マスターおよび発注書の設定</span><span class="sxs-lookup"><span data-stu-id="7485f-103">Setup vendor master and purchase order to be target of consolidated invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7485f-104">日本では通常、仕入先はトランザクションに月次締め請求書を使用します。</span><span class="sxs-lookup"><span data-stu-id="7485f-104">In Japan, the vendors usually use consolidated invoice for transactions.</span></span> 



<span data-ttu-id="7485f-105">このタスクは、仕入先マスターおよび発注書を構成して月次締め請求書を使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7485f-105">This task walks you through configuring a vendor master and purchase order to use the consolidated invoice.</span></span> 



<span data-ttu-id="7485f-106">このタスクは デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="7485f-106">This task was created using the demo data company JPMF.</span></span>


## <a name="set-up-vendor-master"></a><span data-ttu-id="7485f-107">仕入先マスターの設定</span><span class="sxs-lookup"><span data-stu-id="7485f-107">Set up vendor master</span></span>
1. <span data-ttu-id="7485f-108">[買掛金勘定] > [仕入先] > [すべての仕入先] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7485f-108">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="7485f-109">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7485f-109">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="7485f-110">[支払] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="7485f-110">Expand or collapse the Payment section.</span></span>
    * <span data-ttu-id="7485f-111">支払条件 で [締日] が使用されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7485f-111">Verify that the terms of payment uses the Cutoff day.</span></span>  
    * <span data-ttu-id="7485f-112">仕入先の [月次締め日] を指定します。</span><span class="sxs-lookup"><span data-stu-id="7485f-112">Specify a Consolidation day for the vendor.</span></span>  
    * <span data-ttu-id="7485f-113">このフィールドの更新には [編集] をクリックする必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="7485f-113">You might need to click Edit first, before you can update this field.</span></span>  

## <a name="set-a-purchase-order-to-be-target-of-consolidated-invoice"></a><span data-ttu-id="7485f-114">月次締め請求書の対象とする発注書の設定</span><span class="sxs-lookup"><span data-stu-id="7485f-114">Set a purchase order to be target of consolidated invoice</span></span>
1. <span data-ttu-id="7485f-115">[買掛金勘定] > [発注書] > [すべての発注書] に移動します。</span><span class="sxs-lookup"><span data-stu-id="7485f-115">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="7485f-116">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7485f-116">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="7485f-117">[アクション] ウィンドウで、[オプション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7485f-117">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="7485f-118">[ビューの変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7485f-118">Click Change view.</span></span>
5. <span data-ttu-id="7485f-119">[ヘッダーの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7485f-119">Click Header view.</span></span>
    * <span data-ttu-id="7485f-120">[締めの対象] スライダーが「はい」に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7485f-120">Verify that the Target of consolidation slider is set to 'Yes'.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]