---
title: 仕入先要求コンフィギュレーション
description: このトピックでは、新しい仕入先要求で設定する必要があるフィールドについて説明します。
author: kamaybac
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: a78ec681ff9bfe9f7792da04553e4b543bf4a183
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809305"
---
# <a name="vendor-request-configurations"></a><span data-ttu-id="bfd5f-103">仕入先要求コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="bfd5f-103">Vendor request configurations</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="bfd5f-104">仕入先要求を完了するには、仕入先連絡担当者は、見込み仕入先の登録ウィザードを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfd5f-104">To complete a vendor request, a vendor contact person must complete the prospective vendor registration wizard.</span></span>

<span data-ttu-id="bfd5f-105">**仕入先要求コンフィギュレーション** フォームで、必須フィールドおよび見込み仕入先の登録ウィザードで表示されるフィールドを指定するプロファイルを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="bfd5f-105">In the **Vendor request configurations** form, you can create profiles that specify required fields and visible fields in the prospective vendor registration wizard.</span></span>

<span data-ttu-id="bfd5f-106">仕入先登録ウィザードは、仕入先がどの国/地域で取引を行っているかを見込み仕入先ユーザーに質問をすることで開始します。</span><span class="sxs-lookup"><span data-stu-id="bfd5f-106">The vendor registration wizard will start out by asking the prospective vendor user which country/region the vendor is doing business in.</span></span> <span data-ttu-id="bfd5f-107">この情報は、該当するコンフィギュレーションを決定します。</span><span class="sxs-lookup"><span data-stu-id="bfd5f-107">This information determines the applicable configuration.</span></span> <span data-ttu-id="bfd5f-108">国/地域の特定のコンフィギュレーションが定義されていない場合は、既定のコンフィギュレーションが使用されます。</span><span class="sxs-lookup"><span data-stu-id="bfd5f-108">If no specific configuration is defined for a country/region, a default configuration will be used.</span></span>

### <a name="set-up-a-vendor-request-configuration"></a><span data-ttu-id="bfd5f-109">仕入先要求コンフィギュレーションを設定する</span><span class="sxs-lookup"><span data-stu-id="bfd5f-109">Set up a vendor request configuration</span></span>

<span data-ttu-id="bfd5f-110">既定では、仕入先要求コンフィギュレーション フォームで使用可能な仕入先コンフィギュレーションがあります。</span><span class="sxs-lookup"><span data-stu-id="bfd5f-110">By default, there is a vendor configuration available in the Vendor request configurations form.</span></span>

<span data-ttu-id="bfd5f-111">既定のコンフィギュレーションでは国/地域を選択できないため、**国/地域** セクションを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="bfd5f-111">It is not possible to select country/regions for the default configuration, so the **Countries/regions** section cannot be changed.</span></span>

1. <span data-ttu-id="bfd5f-112">**調達** > **設定** > **仕入先** をクリックし、次に **仕入先要求コンフィギュレーション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfd5f-112">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2. <span data-ttu-id="bfd5f-113">**フィールド** タブをクリックして、一覧のフィールドのステータスを設定します。</span><span class="sxs-lookup"><span data-stu-id="bfd5f-113">Click the **Fields** tab to set the status of the listed fields.</span></span>
3. <span data-ttu-id="bfd5f-114">非表示 (表示されません)</span><span class="sxs-lookup"><span data-stu-id="bfd5f-114">Hidden (Not visible)</span></span>
4. <span data-ttu-id="bfd5f-115">表示 (表示されるが必須ではない)</span><span class="sxs-lookup"><span data-stu-id="bfd5f-115">Displayed (Visible but not mandatory)</span></span>
5. <span data-ttu-id="bfd5f-116">必須 (表示および必須である)</span><span class="sxs-lookup"><span data-stu-id="bfd5f-116">Required (Visible and mandatory)</span></span>
6. <span data-ttu-id="bfd5f-117">**コンテンツ** タブをクリックして、テキストがウィザードに表示される場合、および見込み仕入先ユーザーがウィザードの次のステップに移動する前にこれを受け入れる必要があるという確認がある場合を指定します。</span><span class="sxs-lookup"><span data-stu-id="bfd5f-117">Click the **Content** tab to specify if text is going to be shown on the wizard and if there should be an acknowledgement that the prospective vendor user must accept this before moving to the next step in the wizard.</span></span> <span data-ttu-id="bfd5f-118">その確認は、続行するためにユーザーが受け入れるべき契約条件に対して必要です。</span><span class="sxs-lookup"><span data-stu-id="bfd5f-118">The acknowledgement will be requested for any terms and conditions that the user must accept to continue.</span></span>

<span data-ttu-id="bfd5f-119">ウィザードを確定するときに表示される確認メッセージを入力することもでき、1 つまたは複数のアンケートを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="bfd5f-119">You can also enter a confirmation message that will be displayed when the wizard is finalized, and you can add one or more questionnaires.</span></span>

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a><span data-ttu-id="bfd5f-120">特定の国/地域に対する仕入先のコンフィギュレーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="bfd5f-120">Create a vendor configuration for a specific country/region</span></span>
1.  <span data-ttu-id="bfd5f-121">**調達** > **設定** > **仕入先** をクリックし、次に **仕入先要求コンフィギュレーション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfd5f-121">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="bfd5f-122">**新規** をクリックして新しいコンフィギュレーションを作成し、コンフィギュレーションの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="bfd5f-122">Click **New** to create a new configuration, and provide a name for the configuration.</span></span>
3.  <span data-ttu-id="bfd5f-123">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfd5f-123">Click **Save**.</span></span>
4.  <span data-ttu-id="bfd5f-124">**国/地域** タブを開き、コンフィギュレーションを使用すべき国/地域を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfd5f-124">Open the **Country/regions** tab to select the country/region that the configuration should be used for.</span></span>
5.  <span data-ttu-id="bfd5f-125">既定のコンフィギュレーションに対する以下のガイドラインに従って、コンフィギュレーションを完了します。</span><span class="sxs-lookup"><span data-stu-id="bfd5f-125">Complete the configuration by following the guidelines for the default configuration.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]