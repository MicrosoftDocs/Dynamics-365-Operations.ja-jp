---
title: 組織の法律条項およびプライバシーに関する声明へのリンクの追加
description: このトピックでは、管理者が Microsoft Dynamics 365 Finance 、Supply Chain Management、および小売のバージョン情報ウィンドウで、組織の法律条項およびプライバシーに関する声明にリンクを追加する方法について説明します。
author: aneesmsft
manager: AnnBe
ms.date: 10/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SystemParameters, SysAbout
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, Retail
ms.custom: 267894
ms.assetid: b74f8d8b-e20b-4ffd-8fd6-c64c2fe31c8a
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Application update 4
ms.openlocfilehash: 2b8540b68783fb7581e55f9051c6c91cc4fa9949
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183075"
---
# <a name="add-links-to-your-organizations-legal-terms-and-privacy-statement"></a><span data-ttu-id="1e780-103">組織の法律条項およびプライバシーに関する声明へのリンクの追加</span><span class="sxs-lookup"><span data-stu-id="1e780-103">Add links to your organization's legal terms and privacy statement</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e780-104">このトピックでは、管理者が Microsoft Dynamics 365 Finance、Supply Chain Management、および小売の<strong>バージョン情報</strong>ウィンドウで、組織の法律条項およびプライバシーに関する声明にリンクを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1e780-104">This topic explains how administrators can add links to their organization's legal terms and privacy statement in the <strong>About</strong> pane of Microsoft Dynamics 365 Finance, Supply Chain Management, and Retail.</span></span>

<span data-ttu-id="1e780-105">組織は、多くの場合、法的およびコンプライアンス要件を満たすため、その法的な条件およびプライバシーに関する声明へのリンクをユーザーがすぐに入手して表示できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e780-105">Organizations often need to ensure that the links to their legal terms and privacy statement are readily available and visible to users in order to meet legal and compliance requirements.</span></span> <span data-ttu-id="1e780-106">組織の管理者は、以下の手順に従って、**バージョン情報**ウィンドウ (**設定** &gt; **バージョン情報**) で利用可能である法律条項とプライバシーに関する声明へのリンクを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="1e780-106">Administrators of an organization can follow these steps to have the links to their legal terms and privacy statement be available in the **About** pane (**Settings** &gt; **About**).</span></span>

## <a name="add-links"></a><span data-ttu-id="1e780-107">リンクの追加</span><span class="sxs-lookup"><span data-stu-id="1e780-107">Add links</span></span>
1.  <span data-ttu-id="1e780-108">**システム パラメーター**ページに移動し、**法的情報およびプライバシー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1e780-108">Go to the **System parameters** page and click **Legal and Privacy.**</span></span> <span data-ttu-id="1e780-109">このページでは:</span><span class="sxs-lookup"><span data-stu-id="1e780-109">On this page:</span></span>

    1.  <span data-ttu-id="1e780-110">組織の法的条件を説明するページへのリンクを入力します。</span><span class="sxs-lookup"><span data-stu-id="1e780-110">Enter the link to a page that outlines the legal terms for your organization.</span></span>

    2.  <span data-ttu-id="1e780-111">組織のプライバシーに関する声明を説明するページへのリンクを入力します。</span><span class="sxs-lookup"><span data-stu-id="1e780-111">Enter the link to a page that outlines the privacy statement for your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="1e780-112">*https* または *http* のいずれかで始まる完全な URL を入力していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1e780-112">Make sure that you enter the full URL, starting with either *https* or *http*.</span></span>

2.  <span data-ttu-id="1e780-113">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1e780-113">Click **Save**.</span></span>

3.  <span data-ttu-id="1e780-114">小売を使用している場合は、**配送スケジュール**ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="1e780-114">If you are using Retail, go to the **Distribution schedules** page.</span></span> <span data-ttu-id="1e780-115">このページでは:</span><span class="sxs-lookup"><span data-stu-id="1e780-115">On this page:</span></span>

    1.  <span data-ttu-id="1e780-116">**1110 – グローバル構成** ジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="1e780-116">Select the **1110 – Global configuration** job.</span></span>

    2.  <span data-ttu-id="1e780-117">**今すぐ実行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1e780-117">Click **Run now**.</span></span>

>   <span data-ttu-id="1e780-118">ジョブが完了したことを確認するには、**ダウンロード セッション** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="1e780-118">To verify that the job completed, go to the **Download sessions** page.</span></span>

## <a name="validate-links"></a><span data-ttu-id="1e780-119">リンクの検証</span><span class="sxs-lookup"><span data-stu-id="1e780-119">Validate links</span></span>

### <a name="validate-the-links-in-finance-supply-chain-management-and-retail"></a><span data-ttu-id="1e780-120">財務、Supply Chain Management、および小売のリンクを検証</span><span class="sxs-lookup"><span data-stu-id="1e780-120">Validate the links in Finance, Supply Chain Management, and Retail</span></span>

<span data-ttu-id="1e780-121">リンクが追加されたことを確認するには、ページ上部のツールバーで **設定** アイコンをクリックし、**詳細** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1e780-121">To validate that the links have been added, on the toolbar at the top of the page, click the **Settings** icon, and then click **About**.</span></span> <span data-ttu-id="1e780-122">ウィンドウの**リンク** セクションに 2 つの新しいリンクが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1e780-122">In the **Links** section of the pane, you should see two new links:</span></span>

-   <span data-ttu-id="1e780-123">**お客様の組織の法律条項**</span><span class="sxs-lookup"><span data-stu-id="1e780-123">**Your organization’s Legal terms**</span></span>
-   <span data-ttu-id="1e780-124">**お客様の組織のプライバシーと Cookie**</span><span class="sxs-lookup"><span data-stu-id="1e780-124">**Your organization’s Privacy and Cookies**</span></span>

<span data-ttu-id="1e780-125">これらのリンクをクリックして、適切なページが開いていることを検証します。</span><span class="sxs-lookup"><span data-stu-id="1e780-125">Click these links to validate that the appropriate pages open.</span></span> 

> [!NOTE]
> <span data-ttu-id="1e780-126">リンクが新しいウィンドウで開きますので、ポップアップ ブロッカーが有効になっている場合は、ポップアップ ブロック設定に例外を追加して新しいウィンドウを起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e780-126">The links open in a new window, so if you have a pop-up blocker enabled, you will need to add an exception to your pop-up blocker settings to launch a new window.</span></span>

### <a name="validate-the-links-in-modern-point-of-sale-mpos-and-cloud-point-of-sale-cpos"></a><span data-ttu-id="1e780-127">Modern POS (MPOS) およびクラウド POS (CPOS) のリンクの検証</span><span class="sxs-lookup"><span data-stu-id="1e780-127">Validate the links in Modern Point of Sale (MPOS) and Cloud Point of Sale (CPOS)</span></span>
<span data-ttu-id="1e780-128">リンクが追加されたことを検証するには、**設定** ページにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="1e780-128">To validate that the links have been added, go to the **Settings** page.</span></span> <span data-ttu-id="1e780-129">**情報**セクションで、適切なページが開くことを検証するためにリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1e780-129">In the **About** section, click the links to validate that the appropriate pages open.</span></span>