---
title: "Microsoft Dynamics 365 for Talent の機能を拡張します。"
description: "任意の Microsoft PowerApps を作成した場合は、Microsoft Dynamics 365 for Talent 内のリンクからそれらのアプリケーションを開始できます。"
author: rschloma
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: fbd5335f64865dfe6122d88b3bc45ec614fc0677
ms.openlocfilehash: c01a8f0106ee1181e973da50d428b8fc5e6e5a06
ms.contentlocale: ja-jp
ms.lasthandoff: 04/19/2018

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a><span data-ttu-id="b9773-103">Microsoft Dynamics 365 for Talent の機能を拡張します。</span><span class="sxs-lookup"><span data-stu-id="b9773-103">Extend the functionality of Microsoft Dynamics 365 for Talent</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="b9773-104">任意の Microsoft PowerApps を作成した場合は、Microsoft Dynamics 365 for Talent 内のリンクからそれらのアプリケーションを開始できます。</span><span class="sxs-lookup"><span data-stu-id="b9773-104">If you’ve created any Microsoft PowerApps, you can start those applications from links within Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="b9773-105">アプリケーションへのアクセスを設定するには、**システム管理** ワークスペースから開けるコンフィギュレーション ページの Talent で、一部の情報を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9773-105">To set up access to your applications, you’ll need to set up some information in Talent on a configuration page that you can open from the **System administration** workspace.</span></span>

## <a name="configuring-embedded-powerapps-within-talent"></a><span data-ttu-id="b9773-106">Talent 内の埋め込み型 PowerApps のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b9773-106">Configuring embedded PowerApps within Talent</span></span>
<span data-ttu-id="b9773-107">**埋め込み型 Microsoft PowerApps の設定** ページを使用して PowerApps アプリケーションを起動する Talent ページを構成します。</span><span class="sxs-lookup"><span data-stu-id="b9773-107">Use the **Set embedded Microsoft PowerApps** page to configure Talent pages to start PowerApps applications.</span></span> <span data-ttu-id="b9773-108">**埋め込み型 Microsoft PowerApps の設定** ページを開くには、**システム管理** ワークスペースを開き、**リンク** タブを開きます。**設定** グループから **Microsoft PowerApps** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9773-108">To open the **Set embedded Microsoft PowerApps** page, open the **System administration** workspace and then open the **Links** tab. Select **Microsoft PowerApps** from the **Setup** group.</span></span> 

<span data-ttu-id="b9773-109">以下の情報を入力するか、またはこのページで設定します。</span><span class="sxs-lookup"><span data-stu-id="b9773-109">The following information is entered or set on this page:</span></span> 

 -  <span data-ttu-id="b9773-110">各 PowerApps アプリケーションの内容を説明する名前または識別子。</span><span class="sxs-lookup"><span data-stu-id="b9773-110">A descriptive name or identifier for each PowerApps application.</span></span>
 -  <span data-ttu-id="b9773-111">Talent ページに追加する各アプリケーションの固有識別子 (GUID)。</span><span class="sxs-lookup"><span data-stu-id="b9773-111">A unique identifier (GUID) for each application that you add to a Talent page.</span></span> <span data-ttu-id="b9773-112">アプリ IDは、PowerApps サイト [powerapps.com](http://powerapps.com/)で使用できます。</span><span class="sxs-lookup"><span data-stu-id="b9773-112">The app ID is available on the PowerApps site, [powerapps.com](http://powerapps.com/).</span></span> 
 -  <span data-ttu-id="b9773-113">ユーザーがアプリケーションまたはレポートを開くことができるページ。</span><span class="sxs-lookup"><span data-stu-id="b9773-113">The page from which users can open an application or report.</span></span> <span data-ttu-id="b9773-114">すべての Talent ページが、埋め込み型 PowerApps および Power BI レポートをサポートするわけではありません。</span><span class="sxs-lookup"><span data-stu-id="b9773-114">Not all Talent pages support embedded PowerApps and Power BI reports.</span></span> 

 > [!NOTE]
 >  <span data-ttu-id="b9773-115">ページの上部に表示される表示名ではなく、ページの内部名称を入力します。</span><span class="sxs-lookup"><span data-stu-id="b9773-115">Enter the internal name of the page, rather than the display name that appears at the top of the page.</span></span> <span data-ttu-id="b9773-116">内部名称を検索するには、内部名称が必要なページを開き、ページ上の任意の場所で右クリックします。</span><span class="sxs-lookup"><span data-stu-id="b9773-116">To find the internal name, open the page that you need the internal name of, and right-click anywhere on the page.</span></span> <span data-ttu-id="b9773-117">メニューを開いたら、**フォーム情報** 項目をポイントします。</span><span class="sxs-lookup"><span data-stu-id="b9773-117">When the menu opens, hover over the **Form information** item.</span></span> <span data-ttu-id="b9773-118">内部フォーム名が、メニューの **フォーム情報** 項目の横に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9773-118">The internal form name is displayed next to the **Form information** item in the menu.</span></span>
 
-   <span data-ttu-id="b9773-119">アプリケーションがコンテキスト データを取得するフォーム コントロールを指定します。</span><span class="sxs-lookup"><span data-stu-id="b9773-119">Specify the form control from which the application can retrieve context data.</span></span> <span data-ttu-id="b9773-120">たとえば、アプリケーションは、作業者に関するデータを使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="b9773-120">For example, an application might use data about a worker.</span></span> <span data-ttu-id="b9773-121">**コンテキスト** フィールドで **作業者** ページを入力する場合、アプリケーションを起動すると **作業者** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="b9773-121">If you enter the **Worker** page in the **Context** field, the **Worker** page will open when you start the application.</span></span> <span data-ttu-id="b9773-122">**コンテキスト フィールド** の入力はオプションです。</span><span class="sxs-lookup"><span data-stu-id="b9773-122">An entry in the **Context field** is optional.</span></span> 
-   <span data-ttu-id="b9773-123">PowerApps アプリケーションを実行するダイアログ ボックスのサイズを設定します。</span><span class="sxs-lookup"><span data-stu-id="b9773-123">Set the size of the dialog box on which the PowerApps application will run.</span></span> <span data-ttu-id="b9773-124">アプリケーションが電話や大きなデバイスで実行している場合、ユーザー インターフェイスを最適化するため、ダイアログ ボックスがそれぞれ “小“ または “大“ に指定されます。</span><span class="sxs-lookup"><span data-stu-id="b9773-124">The dialog boxes are designated as “small” or “large” to optimize the user interface when your application for running on a phone or a larger device, respectively.</span></span> 


<span data-ttu-id="b9773-125">どの法人に対してアプリケーションが利用できるか、またはすべての法人に対してアプリケーションを利用できるように指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="b9773-125">You can also specify which legal entities an application will be available for, or you can make it available to all your legal entities.</span></span> <span data-ttu-id="b9773-126">既定では、PowerApps アプリケーションはすべての法人に対して利用できます。</span><span class="sxs-lookup"><span data-stu-id="b9773-126">By default, your PowerApps applications are available to all legal entities.</span></span>

## <a name="opening-an-application"></a><span data-ttu-id="b9773-127">申請の開始</span><span class="sxs-lookup"><span data-stu-id="b9773-127">Opening an application</span></span>
<span data-ttu-id="b9773-128">埋め込み型 PowerApps アプリケーションを構成した場合、指定したアプリケーションへのリンクが Talent 内のページに追加されます。</span><span class="sxs-lookup"><span data-stu-id="b9773-128">When you’ve configured embedded PowerApps applications, links to the applications that you specified will be added to the pages within Talent.</span></span> <span data-ttu-id="b9773-129">申請書を開くためのリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9773-129">Click a link to open an application.</span></span> 



