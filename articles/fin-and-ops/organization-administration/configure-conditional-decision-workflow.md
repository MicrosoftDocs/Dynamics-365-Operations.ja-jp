---
title: "ワークフローでの条件付き意思決定のコンフィギュレーション"
description: "条件判断のプロパティをコンフィギュレーションするには、次の手順に従います。"
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e9d5c8add546cad0446e863f64cac8f9cb603cbb
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="configure-a-conditional-decision-in-a-workflow"></a><span data-ttu-id="ae502-103">ワークフローでの条件付き意思決定のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="ae502-103">Configure a conditional decision in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ae502-104">条件判断のプロパティをコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ae502-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="ae502-105">条件判断は、ワークフローが 2 つの分岐に分かれるポイントです。</span><span class="sxs-lookup"><span data-stu-id="ae502-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="ae502-106">条件判断をコンフィギュレーションするには、ワークフロー エディターで条件判断を右クリックし、[**プロパティ**] をクリックして、[**プロパティ**] フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="ae502-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="ae502-107">名前の設定</span><span class="sxs-lookup"><span data-stu-id="ae502-107">Name a decision</span></span>
<span data-ttu-id="ae502-108">条件判断の名前を入力するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ae502-108">Follow these steps to enter a name for a conditional decision.</span></span>
1.  <span data-ttu-id="ae502-109">左ウィンドウで [**基本設定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae502-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="ae502-110">[**名前**] フィールドに、条件判断の固有の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae502-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="ae502-111">条件の設定</span><span class="sxs-lookup"><span data-stu-id="ae502-111">Set conditions</span></span>
<span data-ttu-id="ae502-112">使用される分岐は、提出されたドキュメントが特定の条件を満たすかどうかをシステムが評価して決定します。</span><span class="sxs-lookup"><span data-stu-id="ae502-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>
1.  <span data-ttu-id="ae502-113">左ウィンドウで [**基本設定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae502-113">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="ae502-114">[**条件の追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae502-114">Click **Add condition**.</span></span>
3.  <span data-ttu-id="ae502-115">条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae502-115">Enter a condition.</span></span>
4.  <span data-ttu-id="ae502-116">必要に応じて、追加条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae502-116">Enter additional conditions, if they are required.</span></span>
5.  <span data-ttu-id="ae502-117">入力した条件が正しくコンフィギュレーションされていることを確認するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ae502-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>
    1.  <span data-ttu-id="ae502-118">[**テスト**] をクリックして、[**ワークフロー条件のテスト**] フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="ae502-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2.  <span data-ttu-id="ae502-119">フォームの [**条件の検証**] 領域でレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="ae502-119">Select a record in the **Validate condition** area of the form.</span></span>
    3.  <span data-ttu-id="ae502-120">[**テスト**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae502-120">Click **Test**.</span></span> <span data-ttu-id="ae502-121">システムによってレコードが評価され、定義した条件を満たすかどうかが判定されます。</span><span class="sxs-lookup"><span data-stu-id="ae502-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="ae502-122">[**OK**] または [**キャンセル**] をクリックして、[**プロパティ**] フォームに戻ります。</span><span class="sxs-lookup"><span data-stu-id="ae502-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>






