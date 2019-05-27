---
title: PowerApps ホスト コントロール
description: PowerApps ホスト コントロールを使用することにより、作成した PowerApps アプリまたは共有 PowerApps アプリを埋め込むことができます。
author: TLeforMicrosoft
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 16061
ms.assetid: 80c93e91-1952-44ce-af93-a17965ee476a
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2017-04-26
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 606cb9564c4a9236033bf74b445297ffa30cd5fb
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1506193"
---
# <a name="powerapps-host-control"></a><span data-ttu-id="9f1c9-103">PowerApps ホスト コントロール</span><span class="sxs-lookup"><span data-stu-id="9f1c9-103">PowerApps Host control</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f1c9-104">Microsoft PowerApps では、作成したアプリや他のユーザーが作成および共有しているアプリを実行することで組織のデータを管理できます。</span><span class="sxs-lookup"><span data-stu-id="9f1c9-104">In Microsoft PowerApps, you can manage organizational data by running an app that you created, or an app that someone else created and shared with you.</span></span> <span data-ttu-id="9f1c9-105">アプリは[電話などのモバイル デバイスで実行する](https://powerapps.microsoft.com/en-us/tutorials/run-app-client/)か、またはそれらを[ブラウザーで](https://powerapps.microsoft.com/en-us/tutorials/run-app-browser/) Microsoft Dynamics 365 for Finance and Operations を起動することによって実行します。</span><span class="sxs-lookup"><span data-stu-id="9f1c9-105">Apps run on [mobile devices such as phones](https://powerapps.microsoft.com/en-us/tutorials/run-app-client/), or you can run them [in a browser](https://powerapps.microsoft.com/en-us/tutorials/run-app-browser/) by starting Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="9f1c9-106">C\# 等のプログラミング言語を学習せずに、多くの種類のアプリを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="9f1c9-106">You can create many types of apps without having to learn a programming language such as C\#.</span></span> <span data-ttu-id="9f1c9-107">Microsoft Visual Studio を使用する開発者が利用できる PowerApps ホスト コントロールを使用することにより、作成した PowerApps アプリまたは共有 PowerApps アプリを埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="9f1c9-107">By using the PowerApps Host control that is available to developers who use Microsoft Visual Studio, you can embed a PowerApps app that you’ve created or a shared PowerApps app.</span></span> <span data-ttu-id="9f1c9-108">PowerApps の詳細については、[[https://powerapps.microsoft.com](https://powerapps.microsoft.com/)] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f1c9-108">To learn more about PowerApps, see [https://powerapps.microsoft.com](https://powerapps.microsoft.com/).</span></span>

## <a name="host-a-powerapps-app-on-a-page"></a><span data-ttu-id="9f1c9-109">ページの PowerApps アプリをホストする</span><span class="sxs-lookup"><span data-stu-id="9f1c9-109">Host a PowerApps app on a page</span></span>

1.  <span data-ttu-id="9f1c9-110">PowerApps で、ホストする Web ベースの PowerApps アプリを検索し、**アプリ ID** の値を記録またはコピーします。</span><span class="sxs-lookup"><span data-stu-id="9f1c9-110">In PowerApps, find the web-based PowerApps app that you want to host, and record or copy the **App ID** value.</span></span>
  
    ![PowerApps アプリ ID](media/powerapps-appid.png)
  
2.  <span data-ttu-id="9f1c9-112">Visual Studio で、プロジェクトを開いてから、フォーム デザイナーでページに PowerApps ホスト コントロールのインスタンスを追加します。</span><span class="sxs-lookup"><span data-stu-id="9f1c9-112">In Visual Studio, open your project, and then, in the form designer, add an instance of a PowerApps Host control to your page.</span></span>
3.  <span data-ttu-id="9f1c9-113">**プロパティ** ウィンドウに**アプリ ID** の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9f1c9-113">In the **Properties** pane, enter the **App ID** value.</span></span>
4.  <span data-ttu-id="9f1c9-114">ページで PowerApps アプリが現在のデータ ソースを共有、またはそこにリンクされている場合、PowerApps アプリで表示するデータのプライマリまたはリンクされたキー フィールドの ID を渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f1c9-114">If your PowerApps app shares or is linked to the current data source on your page, you should pass the ID of the primary or linked key field for the data that you want your PowerApps app to show.</span></span> <span data-ttu-id="9f1c9-115">この場合、ID を**エンティティ ID**、**エンティティ ID データ ソース/フィールド**、または **DataMethod** プロパティの値で指定します。</span><span class="sxs-lookup"><span data-stu-id="9f1c9-115">In this case, provide the ID as the value of the **Entity ID**, **Entity ID Data Source/Field**, or **DataMethod** property.</span></span> <span data-ttu-id="9f1c9-116">この値は、PowerApps アプリに parm 値として渡され、PowerApps アプリはその値を使用して、リンクされているデータを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f1c9-116">This value will then be passed to your PowerApps app as a parm value, and your PowerApps app must use that value to obtain the linked data.</span></span> 
    
    ![PowerApps ホスト コントロールのプロパティ ウィンドウ](media/powerapps-properties.png)
    
5.  <span data-ttu-id="9f1c9-118">場合によっては、Microsoft によって提供される開発またはサンドボックス PowerApps 環境で PowerApps アプリをホストする場合があります。</span><span class="sxs-lookup"><span data-stu-id="9f1c9-118">In some cases, your PowerApps app might be hosted in a development or sandbox PowerApps environment that is provided by Microsoft.</span></span> <span data-ttu-id="9f1c9-119">この場合、**PowerApps 環境のオーバーライド** プロパティの値としてそのオーバーライド URL を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f1c9-119">In this case, you must supply that override URL as the value of the **PowerApps Environment Override** property.</span></span>

<span data-ttu-id="9f1c9-120">サイズは、コントロールを配置したコンテナーによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="9f1c9-120">Sizing is determined by the container that you put your control in.</span></span> <span data-ttu-id="9f1c9-121">使用可能なスペースが限られているフォーム パターンでコントロールを配置し、PowerApps アプリケーションが使用可能領域よりも大きく設計されている場合、PowerApps アプリケーションにスクロール バーが表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="9f1c9-121">If you put your control in a form pattern that has limited available space, and your PowerApps app has been designed to be larger than the available space, your PowerApps app will have scroll bars.</span></span>
