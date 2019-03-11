---
title: スライダーとメッセージ ボックス ダイアログ
description: 既存のダイアログ ボックスである Slider と Dynamics AX 2012 の MessageBox の代わりに、2 つのダイアログがあります。
author: robinarh
manager: AnnBe
ms.date: 11/09/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 64253
ms.assetid: ef0924d0-ee42-4b0d-8602-4dfe15454350
ms.search.region: Global
ms.author: aorth
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65823eae3ff1ca30eee6d057a9426dd9520318f5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369758"
---
# <a name="slider-and-messagebox-dialogs"></a><span data-ttu-id="703d2-103">スライダー ダイアログとメッセージ ボックス ダイアログ</span><span class="sxs-lookup"><span data-stu-id="703d2-103">Slider and MessageBox dialogs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="703d2-104">ダイアログ</span><span class="sxs-lookup"><span data-stu-id="703d2-104">Dialogs</span></span>

<span data-ttu-id="703d2-105">既存のダイアログ ボックスである Slider と Dynamics AX 2012 の MessageBox の代わりに、2 つのダイアログがあります。</span><span class="sxs-lookup"><span data-stu-id="703d2-105">There are two dialogs that replace the existing dialog box, the Slider and the MessageBox from Dynamics AX 2012:</span></span>

-   <span data-ttu-id="703d2-106">スライダー</span><span class="sxs-lookup"><span data-stu-id="703d2-106">Slider</span></span>
-   <span data-ttu-id="703d2-107">MessageBox</span><span class="sxs-lookup"><span data-stu-id="703d2-107">MessageBox</span></span>

<span data-ttu-id="703d2-108">次のセクションでは、各概念の具体的な目標について説明します。</span><span class="sxs-lookup"><span data-stu-id="703d2-108">The following sections discuss the specific goals for each concept.</span></span>

## <a name="slider"></a><span data-ttu-id="703d2-109">スライダー</span><span class="sxs-lookup"><span data-stu-id="703d2-109">Slider</span></span>
<span data-ttu-id="703d2-110">スライダーまたはスライダーダイアログは、画面の右端からアクティブなページのコンテンツの上に「スライド」するダイアログ ボックスです。</span><span class="sxs-lookup"><span data-stu-id="703d2-110">The slider, or slider dialog, is a dialog box that "slides" in on top of the active page's content from the right edge of the screen.</span></span> <span data-ttu-id="703d2-111">次のスクリーン ショットでは、スライダーはウィンドウの右側の**レンタル開始**というキャプションがある白い領域です。</span><span class="sxs-lookup"><span data-stu-id="703d2-111">In the following screen shot, the slider is the white region that has the caption **Start rental** on the right side of the window.</span></span> <span data-ttu-id="703d2-112">ユーザーがスライダーの下にあるページは操作できないことを理解できるように、スライダーの左側の領域がグレー表示になっていることに注意します。</span><span class="sxs-lookup"><span data-stu-id="703d2-112">Notice that the area to the left of the slider is shaded to help the user understand that the page beneath the slider isn't currently available for interaction.</span></span> 

<span data-ttu-id="703d2-113">[![slidermessagebox](./media/slidermessagebox.png)](./media/slidermessagebox.png)</span><span class="sxs-lookup"><span data-stu-id="703d2-113">[![slidermessagebox](./media/slidermessagebox.png)](./media/slidermessagebox.png)</span></span> 

<span data-ttu-id="703d2-114">スライダーを開いた後、ユーザーは 2 つの方法で閉じることができます。</span><span class="sxs-lookup"><span data-stu-id="703d2-114">After a slider opens, the user can dismiss it in two ways:</span></span>

-   <span data-ttu-id="703d2-115">基になるフォーム自体が閉じるアクションをスライダー内で実行します。</span><span class="sxs-lookup"><span data-stu-id="703d2-115">Perform an action within the slider that causes the underlying form to dismiss itself.</span></span> <span data-ttu-id="703d2-116">たとえば、**キャンセル**をクリックして、または必要な情報を入力してから **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="703d2-116">For example, click **Cancel**, or enter required information and then click **OK**.</span></span>
-   <span data-ttu-id="703d2-117">斜線領域のスライダの外側をクリックして、左に移動します。</span><span class="sxs-lookup"><span data-stu-id="703d2-117">Click outside the slider in the shaded area to the left.</span></span> <span data-ttu-id="703d2-118">これにより、スライダが取り消され、それ以上のアクションは実行されません。</span><span class="sxs-lookup"><span data-stu-id="703d2-118">This cancels the slider, and no further actions are performed.</span></span>

<span data-ttu-id="703d2-119">スライダーは、モデル化されたフォームを含み、ユーザーから情報を収集するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="703d2-119">A slider contains a modeled form and is used to gather information from the user.</span></span> <span data-ttu-id="703d2-120">したがって、過去にダイアログ ボックスが使用されているほとんどの状況で、スライダーを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="703d2-120">Therefore, a slider should be used in most situations where a dialog box has been used in the past.</span></span> <span data-ttu-id="703d2-121">たとえば、上記のスクリーン ショットに示すように、スライダーは通常ユーザーが新しいレコードを作成するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="703d2-121">For example, a slider is typically used when the user creates a new record, as in the preceding screen shot.</span></span> <span data-ttu-id="703d2-122">ただし、単純な通知またはユーザーへのメッセージ用に、スライダーを使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="703d2-122">However, a slider should not be used for simple notifications or messages to the user.</span></span> <span data-ttu-id="703d2-123">このような状況のため、次のセクションで説明するように、メッセージ ボックスが使用される必要があります。</span><span class="sxs-lookup"><span data-stu-id="703d2-123">For these situations, a MessageBox should be used, as described in the next section.</span></span> <span data-ttu-id="703d2-124">スライダーをモデル化するには、フォームを作成し、**Form.Design** ノードで**スタイル**プロパティを**ダイアログ**に設定します。</span><span class="sxs-lookup"><span data-stu-id="703d2-124">To model a slider, you create a form, and then set the **Style** property to **Dialog** on the **Form.Design** node.</span></span> <span data-ttu-id="703d2-125">次に、必要なフォームの要素 (フィールドやボタンなど) をモデル化します。</span><span class="sxs-lookup"><span data-stu-id="703d2-125">You then model the form elements that you require (for example, fields and buttons).</span></span> <span data-ttu-id="703d2-126">キャプションは **Form.Design.Caption** によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="703d2-126">The caption is defined by **Form.Design.Caption**.</span></span> <span data-ttu-id="703d2-127">スライダーの作成プロセスを簡略化するために、スライダー ダイアログのモデリングのテンプレートとして **SysBPStyle\_ダイアログ** フォームを用意しました。</span><span class="sxs-lookup"><span data-stu-id="703d2-127">To simplify the process for creating sliders, we have provided the **SysBPStyle\_Dialog** form as a template for modeling slider dialogs.</span></span> <span data-ttu-id="703d2-128">このテンプレートを使用するには、新しいフォームにコピーし、必要に応じて拡張します。</span><span class="sxs-lookup"><span data-stu-id="703d2-128">To use this template, copy it into a new form, and then extend it as you require.</span></span>

## <a name="messagebox"></a><span data-ttu-id="703d2-129">MessageBox</span><span class="sxs-lookup"><span data-stu-id="703d2-129">MessageBox</span></span>
<span data-ttu-id="703d2-130">MessageBox は、既存のページ上に「ライト ボックス」として表示されるダイアログのタイプです。</span><span class="sxs-lookup"><span data-stu-id="703d2-130">A MessageBox is a type of dialog that is rendered as a "lightbox" on top of an existing page.</span></span> <span data-ttu-id="703d2-131">MessageBox は全幅モーダル ポップアップとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="703d2-131">A MessageBox appears as a full-width modal pop-up.</span></span> <span data-ttu-id="703d2-132">次のスクリーン ショットは、メッセージ ボックスの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="703d2-132">The following screen shot shows an example of a MessageBox.</span></span> 

<span data-ttu-id="703d2-133">[![2\_ダイアログ](./media/2_dialog.png)](./media/2_dialog.png)</span><span class="sxs-lookup"><span data-stu-id="703d2-133">[![2\_Dialog](./media/2_dialog.png)](./media/2_dialog.png)</span></span> 

<span data-ttu-id="703d2-134">MessageBox は、重要な状況について通知するためユーザーを中断させる必要がある場合に使用する正しいメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="703d2-134">A MessageBox is the correct mechanism to use when you must interrupt the user to notify him or her about a critical situation.</span></span> <span data-ttu-id="703d2-135">たとえば、ユーザーにメッセージ センターのエラー メッセージを表示するため、メッセージ ボックスが使用されます。</span><span class="sxs-lookup"><span data-stu-id="703d2-135">For example, a MessageBox is used to display a Message center error message to the user.</span></span> <span data-ttu-id="703d2-136">MessageBox はモーダルなので、ユーザーはその MessageBox が処理されるか、または却下されるまで MessageBox の下のページとやりとりができません。</span><span class="sxs-lookup"><span data-stu-id="703d2-136">Because a MessageBox is modal, the user can't interact with the page beneath the MessageBox until that MessageBox has been dealt with or dismissed.</span></span> <span data-ttu-id="703d2-137">前のスクリーン ショットで、ページが MessageBox によって見えづらくなっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="703d2-137">In the preceding screen shot, notice that the page is obscured by the MessageBox.</span></span> <span data-ttu-id="703d2-138">また、メッセージ ボックスの上下にある領域は、ページが現在インタラクションのために使用可能でないことをユーザーが理解するのを助けるために影付きで表示されます。</span><span class="sxs-lookup"><span data-stu-id="703d2-138">Additionally, the areas above and below the MessageBox are shaded to help the user understand that the page isn't currently available for interaction.</span></span> <span data-ttu-id="703d2-139">スライダーとは異なり、ユーザーは斜線領域の外側をクリックして MessageBox を閉じることはできません。</span><span class="sxs-lookup"><span data-stu-id="703d2-139">Be aware that, unlike a slider, the user can't dismiss a MessageBox by clicking outside it, in the shaded areas.</span></span> <span data-ttu-id="703d2-140">MessageBox は、Box アプリケーション プログラミング インターフェイス (API)、またはエラーの表示をトリガーするために前述したメソッドのいずれかを使用してトリガーできます。</span><span class="sxs-lookup"><span data-stu-id="703d2-140">A MessageBox can be triggered by using either the Box application programming interface (API) or any of the methods that are described earlier for triggering the display of an error.</span></span> <span data-ttu-id="703d2-141">詳細については、[メッセージ API: メッセージ センター、メッセージ バー、メッセージの詳細](messaging-api-center-bar-details.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="703d2-141">For more information, see the [Message API: Message center, message bar, message details](messaging-api-center-bar-details.md).</span></span>



