---
title: AX 2009 の移行 － マップの生成
description: このトピックは、データ マップを生成し、Microsoft Dynamics AX 2009 から Finance and Operations へデータを移行する方法を説明します。
author: kfend
manager: AnnBe
ms.date: 06/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2018-06-21
ms.dyn365.ops.version: Platform update 17
ms.openlocfilehash: a58a05160f9102f3b2e0cdb1b8f86239a65923ce
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183165"
---
# <a name="ax-2009-migration--generate-maps"></a><span data-ttu-id="16468-103">AX 2009 の移行 － マップの生成</span><span class="sxs-lookup"><span data-stu-id="16468-103">AX 2009 migration – Generate maps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16468-104">Microsoft Dynamics AX 2009 から Finance and Operations へデータを移行する前に、ターゲット環境で、ソース データを配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16468-104">Before you can migrate your data from Microsoft Dynamics AX 2009 to Finance and Operations, you must align your source data with your target environment.</span></span> <span data-ttu-id="16468-105">このトピックでは、ソースとターゲットのマッピングを生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="16468-105">This topic explains how to generate source-to-target mappings.</span></span>

<span data-ttu-id="16468-106">マップを生成するには、接続を検証するための対象の URL、テナント URL、およびサービス アプリケーション ID を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16468-106">Before you can generate maps, you must provide the target URL, tenant URL, and service app ID to validate the connection.</span></span>

> [!NOTE]
> <span data-ttu-id="16468-107">Azure ポータルの Microsoft Azure Active Directory (Azure AD) で新しいアプリケーションを作成するとき、2 つのオプション **Web API** と **ネイティブ** があります。</span><span class="sxs-lookup"><span data-stu-id="16468-107">When you create a new app under Microsoft Azure Active Directory (Azure AD) in the Azure portal, you have two options, **Web API** and **Native**.</span></span> <span data-ttu-id="16468-108">**ネイティブ**を選択し、ネイティブ Azure AD アプリケーションへのアクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="16468-108">Select **Native**, and grant permissions to the native Azure AD app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="16468-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="16468-109">Prerequisites</span></span>
<span data-ttu-id="16468-110">ソース環境とターゲット環境間でデータ マップを生成する前に、データ移行ツール (DMT) をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="16468-110">Before you generate the data maps between the source and target environments, you must install the Data migration tool (DMT).</span></span> <span data-ttu-id="16468-111">詳細については、[データ移行ツールーのインストール](install-dmt.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16468-111">For more information, see [Install the Data migration tool](install-dmt.md).</span></span>

## <a name="generate-maps"></a><span data-ttu-id="16468-112">マップの生成</span><span class="sxs-lookup"><span data-stu-id="16468-112">Generate maps</span></span>
<span data-ttu-id="16468-113">データ移行のためのマップを生成するには、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="16468-113">Follow these steps to generate maps for data migration.</span></span>

1. <span data-ttu-id="16468-114">AX 2009 のナビゲーション ウィンドウで、**データ移行**\>**設定** \>**接続の構成**に移動します。</span><span class="sxs-lookup"><span data-stu-id="16468-114">In AX 2009, in the navigation pane, go to **Data migration** \> **Setup** \> **Configure connections**.</span></span>
2. <span data-ttu-id="16468-115">フィールドの情報を確認して正しいことを確認し、**検証** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16468-115">Review the field information to verify that it's correct, and then click **Validate**.</span></span>
3. <span data-ttu-id="16468-116">検証の完了後、フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="16468-116">After the validation is completed, close the form.</span></span>
4. <span data-ttu-id="16468-117">**設定**で、**マップを構成および生成** ををクリックします。</span><span class="sxs-lookup"><span data-stu-id="16468-117">Under **Setup**, click **Configure and generate maps**.</span></span>
5. <span data-ttu-id="16468-118">フォームの情報が正しいことを確認してから、**パスの検証** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16468-118">Verify that the information in the form is correct, and then click **Validate path**.</span></span>
6. <span data-ttu-id="16468-119">検証が完了したら、**マップを生成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16468-119">After validation is completed, click **Generate maps**.</span></span>