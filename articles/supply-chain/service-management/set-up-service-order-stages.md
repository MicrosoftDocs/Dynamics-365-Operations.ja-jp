---
title: サービス注文ステージを設定します
description: サービス注文ステージを設定します。
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b6e245b351b66724eedf8e0d1a0ebf0202df857
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824417"
---
# <a name="set-up-service-order-stages"></a><span data-ttu-id="11b63-103">サービス注文ステージを設定します</span><span class="sxs-lookup"><span data-stu-id="11b63-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="11b63-104">**サービス管理** \> **設定** \> **サービス注文** \> **サービス ステージ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="11b63-104">Go to **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="11b63-105">**新規作成** を選択して、新しいレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="11b63-105">Select **New** to create a new record.</span></span>

3.  <span data-ttu-id="11b63-106">**サービス ステージ** および **説明** フィールドで、サービス ステージ ID と説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="11b63-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="11b63-107">ステージの適切なパラメータを選択します。</span><span class="sxs-lookup"><span data-stu-id="11b63-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="11b63-108">現在のステージの親ステージを選択するか、ステージ設定でステージが初期ステージである場合は **親** フィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="11b63-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="11b63-109">ステージを保存した後で<STRONG>親</STRONG>フィールドを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="11b63-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="11b63-110">代わりに、レコードを削除し、<STRONG>親</STRONG>フィールドで別の選択を行ってレコードをもう一度作成できます。</span><span class="sxs-lookup"><span data-stu-id="11b63-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="11b63-111">また、空の<STRONG>親</STRONG>フィールドに対して、ステージは 1 つしか作成できません。</span><span class="sxs-lookup"><span data-stu-id="11b63-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="11b63-112">つまり、初期ステージは 1 つしか許可されません。</span><span class="sxs-lookup"><span data-stu-id="11b63-112">That is, only one initial stage is permitted.</span></span></P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]