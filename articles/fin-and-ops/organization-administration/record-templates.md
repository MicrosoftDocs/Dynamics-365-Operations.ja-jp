---
title: "レコード テンプレート"
description: "この記事は、レコード テンプレートの概念を紹介し、情報を共有するレコードを作成して使用する方法を説明します。"
author: pvillads
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 298f34871265dbf5c437dcdc6c05270b4e2a9a9d
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="record-templates"></a><span data-ttu-id="01147-103">レコード テンプレート</span><span class="sxs-lookup"><span data-stu-id="01147-103">Record templates</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="01147-104">この記事は、レコード テンプレートの概念を紹介し、情報を共有するレコードを作成して使用する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="01147-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="01147-105">レコード テンプレートを使用すると、Microsoft Dynamics 365 for Finance and Operations でレコードをもっと迅速に作成することができます。</span><span class="sxs-lookup"><span data-stu-id="01147-105">Record templates can help you to create records more quickly in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="01147-106">Microsoft Dynamics 365 for Finance and Operations のレコード タイプの一部のみを対象としたレコード テンプレートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="01147-106">You can create record templates for only some of the record types in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="01147-107">たとえば、 サンフランシスコにあるレンタカー事業のレンタル情報を入力するとします。</span><span class="sxs-lookup"><span data-stu-id="01147-107">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="01147-108">顧客のほとんどは、サンフランシスコ周辺から来ますから、レンタル フォームの [**州**]、[**国**]、[**市町村**] フィールドに値を自動的に記入できれば、良いでしょう。</span><span class="sxs-lookup"><span data-stu-id="01147-108">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span> 

> [!Note]
> <span data-ttu-id="01147-109">テンプレートを適用できるのは、アクセス権のある Finance and Operations の領域だけです。</span><span class="sxs-lookup"><span data-stu-id="01147-109">You can apply templates only for the areas of Finance and Operations that you have access to.</span></span> <span data-ttu-id="01147-110">ただし、すべてのユーザーが使用できるテンプレートを作成している場合、新しいレコードを作成すると、すべてのテンプレートのタイトルが、本人と他のユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="01147-110">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="01147-111">テンプレートを命名する場合には、これを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="01147-111">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="01147-112">たとえば、法人の一部の従業員に歩合給が支払われていることが機密事項の場合、「コミッション」などの、用語が含まれる名前の使用を避けてください。</span><span class="sxs-lookup"><span data-stu-id="01147-112">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span> 

<span data-ttu-id="01147-113">アクセス許可がある 1 つ以上のテンプレートが特定のフォームに存在し、そのフォームで新しいレコードを作成するときには、[**目的のテンプレートの選択**] ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="01147-113">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="01147-114">一覧からテンプレートを選択すると、新しいレコードが作成されて、選択したテンプレートに基づく既定の情報が設定されます。</span><span class="sxs-lookup"><span data-stu-id="01147-114">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="01147-115">新しいレコードを作成するときにテンプレートを使用しない場合は、[**テンプレートの選択**] ページの [**今後このメッセージを表示しない**] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="01147-115">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="01147-116">テンプレート選択ダイアログ ボックスを再び表示するには、レコードを右クリックし、[**レコード情報**] をクリックして、[**テンプレート選択の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="01147-116">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>




