---
title: レコード テンプレートの概要
description: この記事は、レコード テンプレートの概念を紹介し、情報を共有するレコードを作成して使用する方法を説明します。
author: pvillads
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0b55046e6c523398b4a30e674dc9f77bb6fedf3
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693211"
---
# <a name="record-templates-overview"></a><span data-ttu-id="677c9-103">レコード テンプレートの概要</span><span class="sxs-lookup"><span data-stu-id="677c9-103">Record templates overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="677c9-104">この記事は、レコード テンプレートの概念を紹介し、情報を共有するレコードを作成して使用する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="677c9-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="677c9-105">レコード テンプレートによりレコードを迅速に作成することができますが、一部のレコード タイプに対するレコード テンプレートのみ作成することができます。</span><span class="sxs-lookup"><span data-stu-id="677c9-105">Record templates can help you to create records more quickly, however you can only create record templates for some record types.</span></span>

<span data-ttu-id="677c9-106">たとえば、 サンフランシスコにあるレンタカー事業のレンタル情報を入力するとします。</span><span class="sxs-lookup"><span data-stu-id="677c9-106">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="677c9-107">顧客のほとんどは、サンフランシスコ周辺から来ますから、レンタル フォームの **州**、**国**、**市町村** フィールドに値を自動的に記入できれば、良いでしょう。</span><span class="sxs-lookup"><span data-stu-id="677c9-107">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span>

> [!NOTE]
> <span data-ttu-id="677c9-108">テンプレートを適用できるのは、アクセスできる領域だけです。</span><span class="sxs-lookup"><span data-stu-id="677c9-108">You can apply templates only in areas that you have access to.</span></span> <span data-ttu-id="677c9-109">ただし、すべてのユーザーが使用できるテンプレートを作成している場合、新しいレコードを作成すると、すべてのテンプレートのタイトルが、本人と他のユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="677c9-109">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="677c9-110">テンプレートを命名する場合には、これを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="677c9-110">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="677c9-111">たとえば、法人の一部の従業員に歩合給が支払われていることが機密事項の場合、「コミッション」などの、用語が含まれる名前の使用を避けてください。</span><span class="sxs-lookup"><span data-stu-id="677c9-111">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span>

<span data-ttu-id="677c9-112">アクセス許可がある 1 つ以上のテンプレートが特定のフォームに存在し、そのフォームで新しいレコードを作成するときには、**目的のテンプレートの選択** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="677c9-112">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="677c9-113">一覧からテンプレートを選択すると、新しいレコードが作成されて、選択したテンプレートに基づく既定の情報が設定されます。</span><span class="sxs-lookup"><span data-stu-id="677c9-113">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="677c9-114">新しいレコードを作成するときにテンプレートを使用しない場合は、**テンプレートの選択** ページの **今後このメッセージを表示しない** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="677c9-114">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="677c9-115">テンプレート選択ダイアログ ボックスを再び表示するには、レコードを右クリックし、**レコード情報** をクリックして、**テンプレート選択の表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="677c9-115">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>
