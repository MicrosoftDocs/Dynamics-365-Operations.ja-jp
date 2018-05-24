---
title: "廃棄コードを設定します"
description: "顧客が返品した品目のプロセス方法を指定する廃棄コードを設定できます。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReturnDispositionCode
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 35358850776a6e27b55cc1dfe69704508e31ac54
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---


# <a name="set-up-disposition-codes"></a><span data-ttu-id="a0d97-103">廃棄コードを設定します</span><span class="sxs-lookup"><span data-stu-id="a0d97-103">Set up disposition codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a0d97-104">顧客が返品した品目のプロセス方法を指定する廃棄コードを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a0d97-104">You can set up disposition codes to specify how to process an item that is returned by a customer.</span></span> <span data-ttu-id="a0d97-105">たとえば、返品品目が修理されてから顧客に返送されることを示す **Repair and return** という名前の廃棄コードを作成します。</span><span class="sxs-lookup"><span data-stu-id="a0d97-105">For example, create a disposition code named **Repair and return** to indicate that the returned item will be repaired and then returned to the customer.</span></span> <span data-ttu-id="a0d97-106">顧客が返品した品目に通常使用される廃棄コードの例については、[返品品目の廃棄方法の指定](specify-how-to-dispose-of-returned-items.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0d97-106">For more examples of disposition codes that are typically used for items that are returned by customers, see [Specify how to dispose of returned items](specify-how-to-dispose-of-returned-items.md).</span></span>

<span data-ttu-id="a0d97-107">品目が返品された理由を説明するのに役立つ理由コードも設定できます。</span><span class="sxs-lookup"><span data-stu-id="a0d97-107">You can also set up a reason code to help explain why an item was returned.</span></span> <span data-ttu-id="a0d97-108">理由コードの詳細については、[返品理由コードの設定](set-up-return-reason-code.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0d97-108">For more information about reason codes, see [Set up return reason code](set-up-return-reason-code.md).</span></span>

1.  <span data-ttu-id="a0d97-109">**販売とマーケティング** \> **設定** \> **販売注文** \> **返品** \> **廃棄コード**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d97-109">Click **Sales and marketing** \> **Setup** \> **Sales orders** \> **Returns** \> **Disposition codes**.</span></span>

2.  <span data-ttu-id="a0d97-110">**新規** をクリックするか、CTRL+N キーを押して、新しい廃棄コードを作成します。</span><span class="sxs-lookup"><span data-stu-id="a0d97-110">Click **New** or press CTRL+N to create a new disposition code.</span></span>

3.  <span data-ttu-id="a0d97-111">廃棄コードの内容を示す一意の名前を入力し、アクションを選択して、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="a0d97-111">Enter a unique, descriptive name, select an action, and enter a description for the disposition code.</span></span>

4.  <span data-ttu-id="a0d97-112">この廃棄コードに顧客請求金額を関連付ける場合は、**雑費**ボタンをクリックして**雑費の設定**フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="a0d97-112">If you want to associate any customer charges with this disposition code, click the **Charges** button to open the **Set up charges** form.</span></span>

5.  <span data-ttu-id="a0d97-113">会社独自の廃棄コードに対応する外部コードを定義する場合は、**外部コード**ボタンをクリックして**外部コード**フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="a0d97-113">If you want to define any external codes to match with the company's own disposition codes, click the **External codes** button to open the **External codes** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0d97-114">参照</span><span class="sxs-lookup"><span data-stu-id="a0d97-114">See also</span></span>

[<span data-ttu-id="a0d97-115">廃棄コードおよび返品理由コード</span><span class="sxs-lookup"><span data-stu-id="a0d97-115">Disposition codes and return reason codes</span></span>](disposition-and-return-reason-codes.md)

<span data-ttu-id="a0d97-116">[廃棄コード (フォーム)](https://technet.microsoft.com/en-us/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="a0d97-116">[Disposition codes (form)](https://technet.microsoft.com/en-us/library/hh597113\(v=ax.60\))</span></span>

<span data-ttu-id="a0d97-117">[自動請求 (フォーム)](https://technet.microsoft.com/en-us/library/aa582856\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="a0d97-117">[Auto charges (form)](https://technet.microsoft.com/en-us/library/aa582856\(v=ax.60\))</span></span>

<span data-ttu-id="a0d97-118">[外部コード (フォーム)](https://technet.microsoft.com/en-us/library/aa583814\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="a0d97-118">[External codes (form)](https://technet.microsoft.com/en-us/library/aa583814\(v=ax.60\))</span></span>

  



