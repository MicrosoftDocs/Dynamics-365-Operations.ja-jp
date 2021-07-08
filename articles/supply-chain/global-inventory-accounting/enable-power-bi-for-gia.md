---
title: グローバル在庫会計の Power BI を有効にする
description: このトピックでは、グローバル在庫会計の Microsoft Power BI を有効にする方法について説明します。
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d7979ed18b98ee6133774cd91bc866d6fca92d5f
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273185"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a><span data-ttu-id="f3ccb-103">グローバル在庫会計の Power BI を有効にする</span><span class="sxs-lookup"><span data-stu-id="f3ccb-103">Enable Power BI for Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="f3ccb-104">[PowerBI.com](https://powerbi.com/) アカウントから Microsoft Dynamics 365 アプリケーション ワークスペースにタイル、ダッシュ ボード、およびレポートをピン留めすることができます。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-104">You can pin tiles, dashboards, and reports from your [PowerBI.com](https://powerbi.com/) account to your Microsoft Dynamics 365 application workspace.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f3ccb-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="f3ccb-105">Prerequisites</span></span>

<span data-ttu-id="f3ccb-106">Power BI レポートを有効にするには、次の前提条件が満たされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-106">The following prerequisites must be in place before you can enable Power BI reporting:</span></span>

- <span data-ttu-id="f3ccb-107">Dynamics 365 アプリケーションのシステム管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-107">You must be a system administrator in the Dynamics 365 application.</span></span>
- <span data-ttu-id="f3ccb-108">[PowerBI.com](https://powerbi.com/) アカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-108">You must have a [PowerBI.com](https://powerbi.com/) account.</span></span>
- <span data-ttu-id="f3ccb-109">自分の Power BI アカウントに、少なくとも 1 つのダッシュボードと 1 つのレポートがあることが必要です。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-109">You must have at least one dashboard and one report in your Power BI account.</span></span>
- <span data-ttu-id="f3ccb-110">Azure Active Directory (Azure AD) アカウントの管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-110">You must be an administrator for your Azure Active Directory (Azure AD) account.</span></span>
- <span data-ttu-id="f3ccb-111">Azure AD ドメインは、自分の [PowerBI.com](https://powerbi.com/) アカウントに使用したドメインと同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-111">The Azure AD domain must be the same domain that you used for your [PowerBI.com](https://powerbi.com/) account.</span></span>

## <a name="setup"></a><span data-ttu-id="f3ccb-112">段取り</span><span class="sxs-lookup"><span data-stu-id="f3ccb-112">Setup</span></span>

<span data-ttu-id="f3ccb-113">Power BI 統合を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-113">To set up the Power BI integration, follow these steps.</span></span>

1. <span data-ttu-id="f3ccb-114">[Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) にログインします。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-114">Sign in to [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="f3ccb-115">**共用資産ライブラリ** に移動し、資産タイプとして **Power BI レポート モデル** を選択し、**グローバル在庫会計** パッケージをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-115">Go to **Shared asset library**, select **Power BI report model** as the asset type, and download the **Global Inventory Accounting** package.</span></span> 
1. <span data-ttu-id="f3ccb-116">[PowerBI.com](https://app.powerbi.com/) にログインして、次の手順に従って **グローバル在庫会計** Power BI レポート ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-116">Sign in to [PowerBI.com](https://app.powerbi.com/), and upload the **Global Inventory Accounting** Power BI report file by following these steps:</span></span>

    1. <span data-ttu-id="f3ccb-117">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-117">Select **New**.</span></span>
    1. <span data-ttu-id="f3ccb-118">**ファイルをアップロードする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-118">Select **Upload a file**.</span></span>
    1. <span data-ttu-id="f3ccb-119">**グローバル在庫会計** Power BI レポート ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-119">Select the **Global Inventory Accounting** Power BI report file.</span></span>

1. <span data-ttu-id="f3ccb-120">次の手順に従って **グローバル在庫会計** Power BI レポートを構成します。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-120">Configure the **Global Inventory Accounting** Power BI report by following these steps:</span></span>

    1. <span data-ttu-id="f3ccb-121">**マイ ワークスペース** に移動し、グローバル在庫会計のデータセットを検索してから **オプション** メニューで **設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-121">Go to **My workspace**, find the dataset for Global Inventory Accounting, and then, on the **Options** menu, select **Settings**.</span></span>
    1. <span data-ttu-id="f3ccb-122">**グローバル在庫会計の設定** で、**パラメーター** を展開し、必要に応じてすべてのパラメーターを更新します。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-122">In **Settings for Global inventory accounting**, expand **Parameters**, and update all parameters as required.</span></span>

1. <span data-ttu-id="f3ccb-123">[PowerBI.com 統合のコンフィギュレーション](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process) で説明されているようにアプリケーションを登録します。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-123">Register the application as described in [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span></span>
1. <span data-ttu-id="f3ccb-124">次の手順に従って、**グローバル在庫会計** Power BI レポート ファイルを Dynamics 365 Supply Chain Management に統合します。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-124">Integrate the **Global Inventory Accounting** Power BI report file into Dynamics 365 Supply Chain Management by following these steps:</span></span>

    1. <span data-ttu-id="f3ccb-125">**システム管理 \> 設定 \> PowerBI.com コンフィギュレーション** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-125">Go to **System administration \> Setup \> PowerBI.com configuration**.</span></span>
    1. <span data-ttu-id="f3ccb-126">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-126">Select **Edit**.</span></span>
    1. <span data-ttu-id="f3ccb-127">**PowerBI.com 統合を有効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-127">Select **Enable PowerBI.Com integration**.</span></span>
    1. <span data-ttu-id="f3ccb-128">**アプリケーション ID** フィールドに、アプリケーション ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-128">In the **Application ID** field, enter the application ID.</span></span>
    1. <span data-ttu-id="f3ccb-129">**アプリケーション キー** フィールドに、アプリケーション キーを入力します。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-129">In the **Application key** field, enter the application key.</span></span>
    1. <span data-ttu-id="f3ccb-130">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-130">Select **Save**.</span></span>

1. <span data-ttu-id="f3ccb-131">ページを更新すると、Power BI サインイン ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-131">Refresh the page so that the Power BI sign-in dialog box appears.</span></span>
1. <span data-ttu-id="f3ccb-132">**オプション** タブで、**レポート カタログを開く** を選択し、先ほどアップロードした **グローバル在庫会計** Power BI レポート ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-132">On the **Options** tab, select **Open report catalog**, and then select the **Global Inventory Accounting** Power BI report file that you uploaded earlier.</span></span>
1. <span data-ttu-id="f3ccb-133">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-133">Refresh the page.</span></span> <span data-ttu-id="f3ccb-134">追加されたレポートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-134">You should see that your report has been added.</span></span>
1. <span data-ttu-id="f3ccb-135">**Power BI レポート** の下で、**グローバル在庫会計** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-135">Under **Power BI reports**, select the **Global Inventory Accounting** link.</span></span>

<span data-ttu-id="f3ccb-136">詳細については、[PowerBI.com 統合のコンフィギュレーション](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f3ccb-136">For more information, see [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span></span>
