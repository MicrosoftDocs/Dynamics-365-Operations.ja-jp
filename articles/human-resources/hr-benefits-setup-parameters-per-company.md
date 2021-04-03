---
title: 会社ごとに給付金管理パラメータを構成する
description: Microsoft Dynamics 365 Human Resources で会社ごとの給付金管理に対するパラメーターを構成します。
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 31f30c3d268132327074e931b714b5b2ee3ec5ac
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466643"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="8f448-103">会社ごとに給付金管理パラメータを構成する</span><span class="sxs-lookup"><span data-stu-id="8f448-103">Configure Benefits management parameters per company</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8f448-104">給付金を提供する組織ごとに、給付金確認メールの設定を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f448-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="8f448-105">確認メール設定の設定</span><span class="sxs-lookup"><span data-stu-id="8f448-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="8f448-106">**福利厚生管理** ワークスペースの **設定** で、**人事管理パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f448-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="8f448-107">**福利厚生の管理** タブで、次のフィールドの値を指定します:</span><span class="sxs-lookup"><span data-stu-id="8f448-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="8f448-108">フィールド</span><span class="sxs-lookup"><span data-stu-id="8f448-108">Field</span></span> | <span data-ttu-id="8f448-109">説明</span><span class="sxs-lookup"><span data-stu-id="8f448-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="8f448-110">**確認メールを送信する**</span><span class="sxs-lookup"><span data-stu-id="8f448-110">**Send confirmation email**</span></span> | <span data-ttu-id="8f448-111">この機能がオンになっている場合は、従業員セルフサービスの給付金登録エクスペリエンスから確認メールが従業員に送信されます。</span><span class="sxs-lookup"><span data-stu-id="8f448-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="8f448-112">**確認メール テンプレート**</span><span class="sxs-lookup"><span data-stu-id="8f448-112">**Confirmation email template**</span></span> | <span data-ttu-id="8f448-113">登録の確認を送信するときに使用する組織のメール テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="8f448-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="8f448-114">テンプレートを選択しない場合は、次の一般的なメールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="8f448-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="8f448-115">%EmployeeFirstName%、</span><span class="sxs-lookup"><span data-stu-id="8f448-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="8f448-116">おめでとうございます。</span><span class="sxs-lookup"><span data-stu-id="8f448-116">Congratulations!</span></span> <span data-ttu-id="8f448-117">給付金の登録が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="8f448-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="8f448-118">よろしくお願いいたします。</span><span class="sxs-lookup"><span data-stu-id="8f448-118">Thank you,</span></span><br><span data-ttu-id="8f448-119"><会社/組織名> 給付金。</span><span class="sxs-lookup"><span data-stu-id="8f448-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="8f448-120">**既定のメール送信者アドレス**</span><span class="sxs-lookup"><span data-stu-id="8f448-120">**Default email sender address**</span></span> | <span data-ttu-id="8f448-121">確認メールを送信するときに使用するメール アドレス。</span><span class="sxs-lookup"><span data-stu-id="8f448-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="8f448-122">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f448-122">Select **Save**.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]