---
title: Power Apps ホスト コントロール
description: Power Apps ホスト コントロールを使用すると、アプリを Power Apps から Finance and Operations アプリの 1 つに埋め込むことができます。
author: TLeforMicrosoft
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 16061
ms.assetid: 80c93e91-1952-44ce-af93-a17965ee476a
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2017-04-26
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7ac28419315d03c2935ba318c032882365ea9d8
ms.sourcegitcommit: 17fe0218e8e3f2f4c57c73c0c438a6ebf1ef32a6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/01/2020
ms.locfileid: "3329872"
---
# <a name="power-apps-host-control"></a><span data-ttu-id="07fda-103">Power Apps ホスト コントロール</span><span class="sxs-lookup"><span data-stu-id="07fda-103">Power Apps Host control</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07fda-104">Microsoft Power Apps では、作成したアプリ、または別の人が作成してユーザーと共有したアプリを使用して組織データを管理できます。</span><span class="sxs-lookup"><span data-stu-id="07fda-104">In Microsoft Power Apps, you can manage organizational data through apps that you created, or apps that someone else created and shared with you.</span></span> <span data-ttu-id="07fda-105">[電話などのモバイル デバイス](https://powerapps.microsoft.com/tutorials/run-app-client/) または [ブラウザー](https://powerapps.microsoft.com/tutorials/run-app-browser/) で実行するアプリ。</span><span class="sxs-lookup"><span data-stu-id="07fda-105">Apps run on [mobile devices such as phones](https://powerapps.microsoft.com/tutorials/run-app-client/) or [in a browser](https://powerapps.microsoft.com/tutorials/run-app-browser/).</span></span> <span data-ttu-id="07fda-106">Microsoft Visual Studio 開発者エクスペリエンスを使用する開発者は、アプリを Finance and Operations アプリに組み込むこともできます。</span><span class="sxs-lookup"><span data-stu-id="07fda-106">Apps can also be embedded in Finance and Operations apps by developers using the Microsoft Visual Studio developer experience.</span></span> <span data-ttu-id="07fda-107">Power Apps の詳細については、[https://powerapps.microsoft.com](https://powerapps.microsoft.com/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07fda-107">To learn more about Power Apps, see [https://powerapps.microsoft.com](https://powerapps.microsoft.com/).</span></span>

## <a name="host-an-app-from-power-apps-on-a-page"></a><span data-ttu-id="07fda-108">ページの Power Apps からアプリをホストする</span><span class="sxs-lookup"><span data-stu-id="07fda-108">Host an app from Power Apps on a page</span></span>

1.  <span data-ttu-id="07fda-109">Power Apps で、ホストする Web ベースのアプリを検索し、**アプリ ID** 値を記録またはコピーします。</span><span class="sxs-lookup"><span data-stu-id="07fda-109">In Power Apps, find the web-based app that you want to host, and record or copy the **App ID** value.</span></span>
  
    ![アプリ ID](media/powerapps-appid.png)
  
2.  <span data-ttu-id="07fda-111">Visual Studio でプロジェクトを開き、フォーム デザイナーで、Power Apps ホスト コントロールのインスタンスをページに追加します。</span><span class="sxs-lookup"><span data-stu-id="07fda-111">In Visual Studio, open your project, and then, in the form designer, add an instance of a Power Apps Host control to your page.</span></span>
3.  <span data-ttu-id="07fda-112">**プロパティ** ウィンドウに**アプリ ID** の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="07fda-112">In the **Properties** pane, enter the **App ID** value.</span></span>
4.  <span data-ttu-id="07fda-113">ページでアプリが現在のデータ ソースを共有、またはそこにリンクされている場合、アプリで表示するデータのプライマリまたはリンクされたキー フィールドの ID を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="07fda-113">If your app shares or is linked to the current data source on your page, you can pass the ID of the primary or linked key field for the data that you want your app to show.</span></span> <span data-ttu-id="07fda-114">この場合、ID を**エンティティ ID**、**エンティティ ID データ ソース/フィールド**、または **DataMethod** プロパティの値で指定します。</span><span class="sxs-lookup"><span data-stu-id="07fda-114">In this case, provide the ID as the value of the **Entity ID**, **Entity ID Data Source/Field**, or **DataMethod** property.</span></span> <span data-ttu-id="07fda-115">この値は、アプリにパラメーター値として渡され、アプリはその値を使用して、リンクされているデータを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="07fda-115">This value will then be passed to your app as a parmeter value, and your app must use that value to obtain the linked data.</span></span> 
    
    ![Power Apps ホスト コントロールのプロパティ ウィンドウ](media/powerapps-properties.png)
    
5.  <span data-ttu-id="07fda-117">場合によっては、Microsoft によって提供される開発またはサンドボックス Power Apps 環境でアプリをホストする場合があります。</span><span class="sxs-lookup"><span data-stu-id="07fda-117">In some cases, your app might be hosted in a development or sandbox Power Apps environment that is provided by Microsoft.</span></span> <span data-ttu-id="07fda-118">この場合、**Power Apps 環境のオーバーライド** プロパティの値としてそのオーバーライド URL を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="07fda-118">In this case, you must supply that override URL as the value of the **Power Apps Environment Override** property.</span></span>

<span data-ttu-id="07fda-119">サイズは、コントロールを配置したコンテナーによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="07fda-119">Sizing is determined by the container that you put your control in.</span></span> <span data-ttu-id="07fda-120">使用可能なスペースが限られているフォーム パターンでコントロールを配置し、アプリが使用可能領域よりも大きく設計されている場合、埋め込みアプリにスクロール バーが表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="07fda-120">If you put your control in a form pattern that has limited available space, and your app has been designed to be larger than the available space, your embedded app will have scroll bars.</span></span>
