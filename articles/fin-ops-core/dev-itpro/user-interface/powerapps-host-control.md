---
title: Power Apps ホスト コントロール
description: Power Apps ホスト コントロールを使用することにより、作成した PowerApps アプリまたは共有  Power Apps アプリを埋め込むことができます。
author: TLeforMicrosoft
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 16061
ms.assetid: 80c93e91-1952-44ce-af93-a17965ee476a
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2017-04-26
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 96165ef62181219110172603caf83617a15c11c9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769566"
---
# <a name="power-apps-host-control"></a><span data-ttu-id="1d35a-103">Power Apps ホスト コントロール</span><span class="sxs-lookup"><span data-stu-id="1d35a-103">Power Apps Host control</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d35a-104">Microsoft Power Apps では、作成したアプリや他のユーザーが作成および共有しているアプリを実行することで組織のデータを管理できます。</span><span class="sxs-lookup"><span data-stu-id="1d35a-104">In Microsoft Power Apps, you can manage organizational data by running an app that you created, or an app that someone else created and shared with you.</span></span> <span data-ttu-id="1d35a-105">アプリは[電話などのモバイルデバイスで実行](https://powerapps.microsoft.com/tutorials/run-app-client/)されます。または、Finance and Operations を起動して、[ブラウザー](https://powerapps.microsoft.com/tutorials/run-app-browser/)で実行できます。</span><span class="sxs-lookup"><span data-stu-id="1d35a-105">Apps run on [mobile devices such as phones](https://powerapps.microsoft.com/tutorials/run-app-client/), or you can run them [in a browser](https://powerapps.microsoft.com/tutorials/run-app-browser/) by starting Finance and Operations apps.</span></span> <span data-ttu-id="1d35a-106">C\# 等のプログラミング言語を学習せずに、多くの種類のアプリを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="1d35a-106">You can create many types of apps without having to learn a programming language such as C\#.</span></span> <span data-ttu-id="1d35a-107">Microsoft Visual Studio を使用する開発者が利用できる Power Apps ホスト コントロールを使用すると、作成した Power Apps アプリまたは共有 Power Apps アプリを埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="1d35a-107">By using the Power Apps Host control that is available to developers who use Microsoft Visual Studio, you can embed a Power Apps app that you’ve created or a shared Power Apps app.</span></span> <span data-ttu-id="1d35a-108">Power Apps の詳細については、[https://powerapps.microsoft.com](https://powerapps.microsoft.com/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1d35a-108">To learn more about Power Apps, see [https://powerapps.microsoft.com](https://powerapps.microsoft.com/).</span></span>

## <a name="host-a-power-apps-app-on-a-page"></a><span data-ttu-id="1d35a-109">ページの Power Apps アプリをホストする</span><span class="sxs-lookup"><span data-stu-id="1d35a-109">Host a Power Apps app on a page</span></span>

1.  <span data-ttu-id="1d35a-110">Power Apps で、ホストする Web ベースの Power Apps アプリを見つけ、**アプリ ID** 値を記録またはコピーします。</span><span class="sxs-lookup"><span data-stu-id="1d35a-110">In Power Apps, find the web-based Power Apps app that you want to host, and record or copy the **App ID** value.</span></span>
  
    ![Power Apps アプリ ID](media/powerapps-appid.png)
  
2.  <span data-ttu-id="1d35a-112">Visual Studio でプロジェクトを開き、フォーム デザイナーで、Power Apps ホスト コントロールのインスタンスをページに追加します。</span><span class="sxs-lookup"><span data-stu-id="1d35a-112">In Visual Studio, open your project, and then, in the form designer, add an instance of a Power Apps Host control to your page.</span></span>
3.  <span data-ttu-id="1d35a-113">**プロパティ** ウィンドウに**アプリ ID** の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1d35a-113">In the **Properties** pane, enter the **App ID** value.</span></span>
4.  <span data-ttu-id="1d35a-114">ページで  Power Apps アプリが現在のデータ ソースを共有、またはそこにリンクされている場合、Power Apps アプリで表示するデータのプライマリまたはリンクされたキー フィールドの ID を渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d35a-114">If your Power Apps app shares or is linked to the current data source on your page, you should pass the ID of the primary or linked key field for the data that you want your Power Apps app to show.</span></span> <span data-ttu-id="1d35a-115">この場合、ID を**エンティティ ID**、**エンティティ ID データ ソース/フィールド**、または **DataMethod** プロパティの値で指定します。</span><span class="sxs-lookup"><span data-stu-id="1d35a-115">In this case, provide the ID as the value of the **Entity ID**, **Entity ID Data Source/Field**, or **DataMethod** property.</span></span> <span data-ttu-id="1d35a-116">この値は、 Power Apps アプリに parm 値として渡され、Power Apps アプリはその値を使用して、リンクされているデータを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d35a-116">This value will then be passed to your Power Apps app as a parm value, and your Power Apps app must use that value to obtain the linked data.</span></span> 
    
    ![Power Apps ホスト コントロールのプロパティ ウィンドウ](media/powerapps-properties.png)
    
5.  <span data-ttu-id="1d35a-118">場合によっては、Microsoft によって提供される開発またはサンドボックス Power Apps 環境で Power Apps アプリをホストする場合があります。</span><span class="sxs-lookup"><span data-stu-id="1d35a-118">In some cases, your Power Apps app might be hosted in a development or sandbox Power Apps environment that is provided by Microsoft.</span></span> <span data-ttu-id="1d35a-119">この場合、**Power Apps 環境のオーバーライド** プロパティの値としてそのオーバーライド URL を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d35a-119">In this case, you must supply that override URL as the value of the **Power Apps Environment Override** property.</span></span>

<span data-ttu-id="1d35a-120">サイズは、コントロールを配置したコンテナーによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="1d35a-120">Sizing is determined by the container that you put your control in.</span></span> <span data-ttu-id="1d35a-121">使用可能なスペースが限られているフォーム パターンでコントロールを配置し、Power Apps アプリケーションが使用可能領域よりも大きく設計されている場合、Power Apps アプリケーションにスクロール バーが表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="1d35a-121">If you put your control in a form pattern that has limited available space, and your Power Apps app has been designed to be larger than the available space, your Power Apps app will have scroll bars.</span></span>
