---
title: 独立系ソフトウェア ベンダーのライセンス ステータスの表示
description: このトピックでは、Finance and Operations アプリで独立系ソフトウェア ベンダーのステータスを表示する方法について説明します。
author: Peakerbl
ms.date: 01/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: toskaue
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 031bcafa9b3117f49f0fb5bdb3cf1da766f24f71
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745727"
---
# <a name="view-independent-software-vendor-license-status"></a><span data-ttu-id="bebfa-103">独立系ソフトウェア ベンダーのライセンス ステータスの表示</span><span class="sxs-lookup"><span data-stu-id="bebfa-103">View independent software vendor license status</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="bebfa-104">このトピックでは、Dynamics 365 Finance、Dynamics 365 Supply Chain Management、および Dynamics 365 Commerce などの Finance and Operations アプリの独立系ソフトウェア ベンダー (ISV) ライセンスのステータスを表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="bebfa-104">This topic explains how you can view the status of independent software vendor (ISV) licenses for Finance and Operations apps, such as Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Commerce.</span></span>

<span data-ttu-id="bebfa-105">ライセンス コードとコンフィギュレーション キーは、Finance and Operations アプリの ISV ライセンス　モデルの一部です。</span><span class="sxs-lookup"><span data-stu-id="bebfa-105">License codes and configuration keys are part of the ISV licensing model for Finance and Operations apps.</span></span>

> [!NOTE]
> <span data-ttu-id="bebfa-106">Microsoft が提供するコンフィギュレーション キーは、Finance and Operations アプリのライセンス モデルの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="bebfa-106">Configuration keys that are provided by Microsoft aren't part of the licensing model for Finance and Operations apps.</span></span> <span data-ttu-id="bebfa-107">キーは、機能を有効または無効にするためにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="bebfa-107">The keys are only used to enable and disable functionality.</span></span>

<span data-ttu-id="bebfa-108">ISV のライセンス キーとコードがインストールされると、対応するコンフィギュレーション キーは、**ライセンス コンフィギュレーション** ページで使用可能になり、有効になります。</span><span class="sxs-lookup"><span data-stu-id="bebfa-108">When an ISV license key and code are installed, the corresponding configuration key will be available and enabled on the **License configuration** page.</span></span>

## <a name="view-isv-license-status"></a><span data-ttu-id="bebfa-109">ISV ライセンス ステータスの表示</span><span class="sxs-lookup"><span data-stu-id="bebfa-109">View ISV license status</span></span>
<span data-ttu-id="bebfa-110">ライセンスに関連付けられた各 ISV ソリューションは、有効なライセンス コードが顧客の環境に存在する場合にのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="bebfa-110">Each ISV solution that is tied to a license runs only when a valid license code exists in the customer's environment.</span></span> <span data-ttu-id="bebfa-111">したがって、ISV がソリューションをライセンスに結び付けても、顧客に有効なライセンス コードがない場合、ソリューションは実行されません。</span><span class="sxs-lookup"><span data-stu-id="bebfa-111">Therefore, if an ISV ties their solution to a license, but the customer doesn't have a valid license code, the solution doesn't run.</span></span> <span data-ttu-id="bebfa-112">機能が失われるのを防ぐには、ライセンス コードの有効期限 (該当する場合) を追跡することが重要です。</span><span class="sxs-lookup"><span data-stu-id="bebfa-112">To prevent the loss of functionality, it's important to track the expiration dates, if applicable, for license codes.</span></span> <span data-ttu-id="bebfa-113">有効期限を表示するには、**システム管理** > **設定** > **ライセンス コンフィギュレーション** に移動し、**ライセンス コード** のタブを選択します。</span><span class="sxs-lookup"><span data-stu-id="bebfa-113">To view the expiration dates, go to **System administration** > **Setup** > **License configuration**, and select the **License codes** tab.</span></span>

<span data-ttu-id="bebfa-114">ダウンタイムを回避するには、ライセンス キーの有効期限を確認し、該当する場合は、新しいバージョンに移行する前に新しいライセンス キーを取得してインポートします。</span><span class="sxs-lookup"><span data-stu-id="bebfa-114">To avoid downtime, review the expiration dates of the license keys, and if applicable, obtain and import new license keys before moving to a new version.</span></span>
<span data-ttu-id="bebfa-115">**ライセンス コード** のタブには、期限切れのライセンス コードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bebfa-115">The **License codes** tab shows the expired license codes.</span></span> <span data-ttu-id="bebfa-116">対応するコンフィギュレーション キーは、**コンフィギュレーション キー** のタブには表示されません。</span><span class="sxs-lookup"><span data-stu-id="bebfa-116">The corresponding configuration key won't appear in the **Configuration keys** tab.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="bebfa-117">追加リソース</span><span class="sxs-lookup"><span data-stu-id="bebfa-117">Additional resources</span></span>
<span data-ttu-id="bebfa-118">ISV ライセンス機能の詳細については、[独立系ソフトウェア ベンダー (ISV) ライセンス](../dev-tools/isv-licensing.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bebfa-118">For more information about the ISV licensing feature, see [Independent software vendor (ISV) licensing](../dev-tools/isv-licensing.md).</span></span>

<span data-ttu-id="bebfa-119">ISV ライセンスを環境内の配置にインポートする方法の詳細については、[独立系ソフトウェア ベンダー (ISV) ライセンス (オンプレミス)](../dev-tools/isv-licensing-on-prem.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bebfa-119">For more information about how to import ISV licenses into an on-premises deployment, see [Independent software vendor (ISV) licensing (on-premises)](../dev-tools/isv-licensing-on-prem.md).</span></span>

<span data-ttu-id="bebfa-120">コンフィギュレーション キーレポートの詳細については、[ライセンス コードとコンフィギュレーション キーのレポート](license-codes-configuration-keys-report.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bebfa-120">For more information about the configuration keys report, see [License codes and configuration keys report](license-codes-configuration-keys-report.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
