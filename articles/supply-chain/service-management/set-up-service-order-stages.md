---
title: サービス注文ステージを設定します
description: サービス注文ステージを設定します。
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30f6a6afa6ab91bed41bb19b8312dc7e25bd2478
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "366768"
---
# <a name="set-up-service-order-stages"></a><span data-ttu-id="b2e68-103">サービス注文ステージを設定します</span><span class="sxs-lookup"><span data-stu-id="b2e68-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="b2e68-104">**サービス管理** \> **設定** \> **サービス注文** \> **サービス ステージ**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2e68-104">Click **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="b2e68-105">Ctrl + N キーを押して、新しいレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="b2e68-105">Press CTRL+N to create a new record.</span></span>

3.  <span data-ttu-id="b2e68-106">**サービス ステージ**および**説明**フィールドで、サービス ステージ ID と説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="b2e68-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="b2e68-107">ステージの適切なパラメータを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2e68-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="b2e68-108">現在のステージの親ステージを選択するか、ステージ設定でステージが初期ステージである場合は**親**フィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="b2e68-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b2e68-109">ステージを保存した後で<STRONG>親</STRONG>フィールドを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="b2e68-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="b2e68-110">代わりに、レコードを削除し、<STRONG>親</STRONG>フィールドで別の選択を行ってレコードをもう一度作成できます。</span><span class="sxs-lookup"><span data-stu-id="b2e68-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="b2e68-111">また、空の<STRONG>親</STRONG>フィールドに対して、ステージは 1 つしか作成できません。</span><span class="sxs-lookup"><span data-stu-id="b2e68-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="b2e68-112">つまり、初期ステージは 1 つしか許可されません。</span><span class="sxs-lookup"><span data-stu-id="b2e68-112">That is, only one initial stage is permitted.</span></span></P>


  


