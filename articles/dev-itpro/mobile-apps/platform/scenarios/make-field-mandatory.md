---
title: "ワークスペース クラスを使用して必須フィールドを設定する"
description: "このトピックでは、ワークスペース クラスを使用して、フィールドを必須にする方法について説明します。"
author: makhabaz
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 255544
ms.assetid: 
ms.search.region: Global
ms.author: makhabaz
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: Platform update 3
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 15a493decdf690bc4bd00b6f0a8c8e87eaccef4c
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-mandatory-fields-through-workspace-classes"></a><span data-ttu-id="33d9a-103">ワークスペース クラスを使用して必須フィールドを設定する</span><span class="sxs-lookup"><span data-stu-id="33d9a-103">Set up mandatory fields through workspace classes</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="33d9a-104">モバイル アプリ デザイナーを使用してアクション用のフィールドを選択するとき、一部のプロパティは推定できます。</span><span class="sxs-lookup"><span data-stu-id="33d9a-104">When you use the mobile app designer to select fields for actions, some properties can be inferred.</span></span> <span data-ttu-id="33d9a-105">これらのプロパティには、フィールドの長さ、タイプ、フィールドが必須かどうかが含まれます。</span><span class="sxs-lookup"><span data-stu-id="33d9a-105">These properties include the field length, the type, and whether the field is mandatory.</span></span> <span data-ttu-id="33d9a-106">これらのプロパティを更新するには、ワークスペース クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="33d9a-106">The workspace classes can be used to update these properties.</span></span> <span data-ttu-id="33d9a-107">たとえば、次の図に示すように、顧客レコードが作成されると**名前**フィールドが必須になるよう指定する場合があります。</span><span class="sxs-lookup"><span data-stu-id="33d9a-107">For example, you might want to specify that the **Name** field is mandatory when a customer record is created, as shown in the following images.</span></span>

![アクションおよびフィールド](media/workspace-api/MarkFieldAsMandatoryDesigner.png)

![必須フィールドがマークされているアクション](media/workspace-api/MarkFieldAsMandatoryAction.png)

<span data-ttu-id="33d9a-110">ワークスペース クラスを使用して**配送条件**フィールドを必須にするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="33d9a-110">Follow these steps to make the **Delivery terms** field mandatory by using the workspace class.</span></span>

1. <span data-ttu-id="33d9a-111">アプリ デザイナーを使用して、コントロール名を取得します。</span><span class="sxs-lookup"><span data-stu-id="33d9a-111">Get the control name by using the app designer.</span></span> <span data-ttu-id="33d9a-112">この例では、コントロール名は **DynamicDetail_DlvTerm** です。</span><span class="sxs-lookup"><span data-stu-id="33d9a-112">In this example, the control name is **DynamicDetail_DlvTerm**.</span></span>
2. <span data-ttu-id="33d9a-113">次のコードを追加して、コントロールの**必須**プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="33d9a-113">Add the following code to set the **Mandatory** property for the control.</span></span> <span data-ttu-id="33d9a-114">このコードでは、リフレクションベースの **setProperty** メソッドを使用して**必須**プロパティを設定しています。</span><span class="sxs-lookup"><span data-stu-id="33d9a-114">This code uses the reflection-based **setProperty** method to set the **Mandatory** property.</span></span>

    ```javascript
    public SysAppWorkspaceMetadata getWorkspaceMetadata()
    {
        SysAppWorkspaceMetadata appMetadata;
        appMetadata = super();
        var createCustAction = appMetadata.getAction("createCust");
        this.setCustAccountMandatory(createCustAction);
        return appMetadata;
    }
    private void setCustAccountMandatory(SysAPpActionMetadata _createCustAction)
    {
        var custAccount = +createCustAction.getControl("DynamicDetail_DlvTerm");
        custAccount.setProperty("Mandatory", true);
    }
    ```

3. <span data-ttu-id="33d9a-115">ソリューションをビルドし、モバイル アプリでアプリのメタデータを更新します。</span><span class="sxs-lookup"><span data-stu-id="33d9a-115">Build the solution, and then update the app metadata on the mobile app.</span></span>

<span data-ttu-id="33d9a-116">**配送条件** フィールドは、次の図に示すように **必須** としてマークされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="33d9a-116">The **Delivery terms** field is now marked as **Mandatory**, as shown in the following illustration.</span></span>

![配信条件フィールドは必須とマークされています](media/workspace-api/MarkFieldAsMandatoryFinal.png)
