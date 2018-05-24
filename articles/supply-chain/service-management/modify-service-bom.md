---
title: "サービス BOM の変更"
description: "サービス BOM を変更します。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
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
ms.openlocfilehash: 5ebbcf3865d176c713d96bf90b819b8252e8087f
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---


# <a name="modify-a-service-bom"></a><span data-ttu-id="9963e-103">サービス BOM の変更</span><span class="sxs-lookup"><span data-stu-id="9963e-103">Modify a Service BOM</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="9963e-104">サービス BOM 内の要素の履歴を記録できます。</span><span class="sxs-lookup"><span data-stu-id="9963e-104">You can record the history of an element in a service BOM.</span></span> <span data-ttu-id="9963e-105">BOM 明細行を更新するたびに、履歴行が**履歴**ウィンドウ内に作成されます。</span><span class="sxs-lookup"><span data-stu-id="9963e-105">Every time that you update a BOM line, a history line is created in the **History** pane.</span></span> <span data-ttu-id="9963e-106">履歴行には、BOM 明細行の現在のステータスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9963e-106">The history line shows the current state of the BOM line.</span></span>

## <a name="update-a-service-bom-element"></a><span data-ttu-id="9963e-107">サービス BOM 要素の更新</span><span class="sxs-lookup"><span data-stu-id="9963e-107">Update a service BOM element</span></span>

1.  <span data-ttu-id="9963e-108">**サービス管理** \> **共通** \> **サービス契約** \> **サービス契約**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="9963e-108">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="9963e-109">**編集**をクリックして**サービス合意**詳細フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="9963e-109">Click **Edit** to open the **Service agreements** details form.</span></span>

3.  <span data-ttu-id="9963e-110">**アクション ウィンドウ**で、**サービス対象**をクリックして**サービス対象**フォームを開くきます。</span><span class="sxs-lookup"><span data-stu-id="9963e-110">On the **Action Pane**, click **Service objects** to open the **Service objects** form.</span></span>

4.  <span data-ttu-id="9963e-111">BOM 明細行を更新する対象を選択し、**デザイナ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9963e-111">Select the object to update a BOM line for, and then click **Designer**.</span></span>

5.  <span data-ttu-id="9963e-112">**デザイナ**フォームで、更新する BOM 明細行を選択し、**BOM 明細行の編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9963e-112">In the **Designer** form, select the BOM line to update, and then click **Edit BOM line**.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="9963e-113">明細行をサービス BOM にドラッグする際に<STRONG>BOM 明細行の編集</STRONG>フォームを開く場合、<STRONG>設定</STRONG>タブで、<STRONG>追加時に編集</STRONG>チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="9963e-113">On the <STRONG>Setup</STRONG> tab, select the <STRONG>Edit when adding</STRONG> check box if you want the <STRONG>Edit BOM line</STRONG> form to open when you drag a line into the service BOM.</span></span></P>

6.  <span data-ttu-id="9963e-114">**数量** フィールドで、数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="9963e-114">In the **Quantity** field, enter the quantity.</span></span>

7.  <span data-ttu-id="9963e-115">請求できる交換品目のサービス注文明細行を作成する場合は、**サービス注文明細行の作成**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="9963e-115">If you want to create a service order line for the replacement item, which can then be invoiced, select the **Create service order line** check box.</span></span>

8.  <span data-ttu-id="9963e-116">**OK** をクリックしてフォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9963e-116">Click **OK** to close the form.</span></span>

## <a name="delete-a-service-bom-line"></a><span data-ttu-id="9963e-117">サービス BOM 明細行の削除</span><span class="sxs-lookup"><span data-stu-id="9963e-117">Delete a service BOM line</span></span>

1.  <span data-ttu-id="9963e-118">**サービス管理** \> **共通** \> **サービス契約** \> **サービス契約**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="9963e-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="9963e-119">**編集**をクリックして**サービス合意**詳細フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="9963e-119">Click **Edit** to open the **Service agreements** details form.</span></span>

3.  <span data-ttu-id="9963e-120">**アクション ウィンドウ**で、**サービス対象**をクリックして**サービス対象**フォームを開くきます。</span><span class="sxs-lookup"><span data-stu-id="9963e-120">On the **Action Pane**, click **Service objects** to open the **Service objects** form.</span></span>

4.  <span data-ttu-id="9963e-121">サービス BOM 明細行を削除する対象を選択し、**デザイナ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9963e-121">Select the object to delete a service BOM line from, and then click **Designer**.</span></span>

5.  <span data-ttu-id="9963e-122">**デザイナ**フォームで、削除する BOM 明細行を選択し、**BOM 明細行の削除**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9963e-122">In the **Designer** form, select the BOM line to delete, and then click **Delete BOM line**.</span></span>

## <a name="see-also"></a><span data-ttu-id="9963e-123">参照</span><span class="sxs-lookup"><span data-stu-id="9963e-123">See also</span></span>

[<span data-ttu-id="9963e-124">テンプレート BOM</span><span class="sxs-lookup"><span data-stu-id="9963e-124">Template BOMs</span></span>](template-boms.md)

  



