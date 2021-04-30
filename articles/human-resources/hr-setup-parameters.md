---
title: Human Resources パラメーターのコンフィギュレーション
description: このトピックでは、Dynamics 365 Human Resources で会社固有のパラメーターを設定する方法を説明します。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cd66cb4f5ac02407250e15ae134b36f5ccd4d290
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889935"
---
# <a name="configure-human-resources-parameters"></a><span data-ttu-id="63463-103">Human Resources パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="63463-103">Configure Human resources parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="63463-104">他のパラメーター設定は会社固有ですが、人事管理のパラメーター設定は会社間で共有されます。</span><span class="sxs-lookup"><span data-stu-id="63463-104">The settings of some Human resources parameters are shared across companies, while the settings of other parameters are company-specific.</span></span> <span data-ttu-id="63463-105">このトピックでは、会社固有の人事管理のパラメーターを設定する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="63463-105">This topic explains how to set up company-specific Human resources parameters.</span></span>

<span data-ttu-id="63463-106">2 つのページが人事管理のパラメータの設定に使用されます。</span><span class="sxs-lookup"><span data-stu-id="63463-106">Two pages are used to set Human resources parameters.</span></span> <span data-ttu-id="63463-107">会社間で共有されるパラメータに、**人事管理の共有パラメーター** ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="63463-107">For parameters that are shared across companies, you use the **Human resources shared parameters** page.</span></span> <span data-ttu-id="63463-108">会社固有のパラメータ (つまり、設定を単一の会社に適用する場合) に、**人事管理パラメータ** ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="63463-108">For parameters that are company-specific (in other words, the settings apply to a single company), you use the **Human resource parameters** page.</span></span>

![人事管理パラメーターに移動する](./media/hr-employee-self-service-human-resources-parameters.png)

<span data-ttu-id="63463-110">**人事管理パラメーター** ページで、設定は 6 つのタブに分割されます:</span><span class="sxs-lookup"><span data-stu-id="63463-110">On the **Human resources parameters** page, the settings are divided among six tabs:</span></span>

- <span data-ttu-id="63463-111">**全般**</span><span class="sxs-lookup"><span data-stu-id="63463-111">**General**</span></span>
- <span data-ttu-id="63463-112">**採用** (これは Dynamics 365 Human Resources には含まれていません)</span><span class="sxs-lookup"><span data-stu-id="63463-112">**Recruitment** (this tab isn't included in Dynamics 365 Human Resources)</span></span>
- <span data-ttu-id="63463-113">**報酬**</span><span class="sxs-lookup"><span data-stu-id="63463-113">**Compensation**</span></span>
- <span data-ttu-id="63463-114">**番号順序**</span><span class="sxs-lookup"><span data-stu-id="63463-114">**Number sequences**</span></span>
- <span data-ttu-id="63463-115">**FMLA**</span><span class="sxs-lookup"><span data-stu-id="63463-115">**FMLA**</span></span>
- <span data-ttu-id="63463-116">**従業員セルフ サービス**</span><span class="sxs-lookup"><span data-stu-id="63463-116">**Employee self service**</span></span>
- <span data-ttu-id="63463-117">**マネージャー セルフ サービス**</span><span class="sxs-lookup"><span data-stu-id="63463-117">**Manager self service**</span></span>
- <span data-ttu-id="63463-118">**給付金管理**</span><span class="sxs-lookup"><span data-stu-id="63463-118">**Benefits management**</span></span>
- <span data-ttu-id="63463-119">**休暇**</span><span class="sxs-lookup"><span data-stu-id="63463-119">**Leave and absence**</span></span>
- <span data-ttu-id="63463-120">**支払方法**</span><span class="sxs-lookup"><span data-stu-id="63463-120">**Payment methods**</span></span>

<span data-ttu-id="63463-121">各タブには単一の会社に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="63463-121">Each tab contains information that pertains to a single company.</span></span>

## <a name="general"></a><span data-ttu-id="63463-122">全般</span><span class="sxs-lookup"><span data-stu-id="63463-122">General</span></span>

<span data-ttu-id="63463-123">**概要** タブの設定は、休暇、傷害と疾病、新規採用に関する情報の外観を定義します。</span><span class="sxs-lookup"><span data-stu-id="63463-123">The settings on the **General** tab define the appearance of information about absence, injury and illness, and new hires.</span></span> <span data-ttu-id="63463-124">このタブの設定は、作業中と表示される既定のエントリも定義します。</span><span class="sxs-lookup"><span data-stu-id="63463-124">The settings on this tab also define some default entries that appear as you work.</span></span> <span data-ttu-id="63463-125">特に、このタブでは次のことができます。</span><span class="sxs-lookup"><span data-stu-id="63463-125">Specifically, this tab lets you:</span></span>

- <span data-ttu-id="63463-126">未処理の休暇トランザクションに適用する色を選択します</span><span class="sxs-lookup"><span data-stu-id="63463-126">Select a color to apply to open absence transactions</span></span>
- <span data-ttu-id="63463-127">レポートに使用するスタイル シートを指定します</span><span class="sxs-lookup"><span data-stu-id="63463-127">Specify the style sheet to use for reports</span></span>
- <span data-ttu-id="63463-128">トレーニング コースと休暇登録間の統合を有効にします</span><span class="sxs-lookup"><span data-stu-id="63463-128">Enable the integration between training courses and absence registration</span></span>
- <span data-ttu-id="63463-129">この統合を制御するために使用する休暇コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="63463-129">Select the absence code that is used to control this integration.</span></span>
- <span data-ttu-id="63463-130">けが/病気のケース インシデントを保持する期間を示します。</span><span class="sxs-lookup"><span data-stu-id="63463-130">Indicate how long to keep injury and illness case incidents.</span></span>
- <span data-ttu-id="63463-131">新しい従業員の雇用時に表示される既定の ID 番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="63463-131">Specify the default identification number shown when a new worker is hired.</span></span>

![[全般] タブ](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a><span data-ttu-id="63463-133">採用</span><span class="sxs-lookup"><span data-stu-id="63463-133">Recruitment</span></span>

<span data-ttu-id="63463-134">**採用** タブの設定では、申請者に自動的に送信される通信文書に使用するドキュメント タイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="63463-134">The settings on the **Recruitment** tab define the document types used for correspondence automatically sent to applicants.</span></span> <span data-ttu-id="63463-135">未承諾の申請に使用される採用プロジェクトを示すこともできます。</span><span class="sxs-lookup"><span data-stu-id="63463-135">You can also indicate the recruitment project used for unsolicited applications.</span></span>

<span data-ttu-id="63463-136">採用プロジェクトのエイジングとして定義されている期間によって、**採用管理** ワークスペースの、**エイジング プロジェクト** タイルに含まれている採用プロジェクトが決まります。</span><span class="sxs-lookup"><span data-stu-id="63463-136">The period defined for recruitment project aging determines the recruitment projects included on the **Aging projects** tile in the **Recruitment management** workspace.</span></span> <span data-ttu-id="63463-137">**採用** ワークスペースの、**申請の期限が近づいています** タイルで申込期限が近づいている採用プロジェクトを表示するために、申請の期限の警告に定義されている期間が使用されます。</span><span class="sxs-lookup"><span data-stu-id="63463-137">The period defined for the application deadline warning is used to display recruitment projects that are approaching their application deadline on the **Application deadline approaching** tile in the **Recruitment** workspace.</span></span>

<span data-ttu-id="63463-138">採用の詳細については、[職務候補者の採用](hr-personnel-recruit.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63463-138">For more information about recruiting, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="compensation"></a><span data-ttu-id="63463-139">報酬</span><span class="sxs-lookup"><span data-stu-id="63463-139">Compensation</span></span>

<span data-ttu-id="63463-140">Dynamics 365 Finance では、**報酬** タブの設定は、ユーザーが固定または変動報酬プランの情報を保存するかどうかの確認を定義します。</span><span class="sxs-lookup"><span data-stu-id="63463-140">In Dynamics 365 Finance, the settings on the **Compensation** tab define whether users must confirm that they want to save information for a fixed or variable compensation plan.</span></span> <span data-ttu-id="63463-141">**保存の検証を有効にします** をオンにすると、そのユーザーが報酬に関連付けられたページを閉じるときに、レコードを保存するかどうか確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="63463-141">If you select **Enable save validation**, when users close a compensation-related page, they receive a message that asks whether they want to save the record.</span></span> <span data-ttu-id="63463-142">報酬管理の一部のページでは、ユーザーが情報を削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="63463-142">Some pages in Compensation management don't let users delete information.</span></span> <span data-ttu-id="63463-143">ユーザーに情報を保存するかどうかを確認するよう促すことにより、後で削除できない保存される情報の量を限定できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="63463-143">By prompting users to verify that they want to save information, you might be able to limit the amount of information that is saved but can't be deleted later.</span></span> <span data-ttu-id="63463-144">**保存の検証を有効にします** をオフにすると、場合によってはユーザーの準備が整う前に、レコードはすぐに保存されます。</span><span class="sxs-lookup"><span data-stu-id="63463-144">If you clear **Enable save validation**, records save immediately, possibly before the user is ready.</span></span> <span data-ttu-id="63463-145">パフォーマンス管理を使用している場合は、**報酬** タブでも、パフォーマンスを評価するときに報酬プランに割り当てられているモデルの代わりに使用する評価モデルを選択できます。</span><span class="sxs-lookup"><span data-stu-id="63463-145">If you're using Performance management, the **Compensation** tab also lets you select a rating model to use instead of the model assigned to compensation plans when rating performance.</span></span>

<span data-ttu-id="63463-146">人事管理では、**報酬** タブを使用して、報酬プランへのアクセスの制限や、既定の通貨の設定を選択できます。</span><span class="sxs-lookup"><span data-stu-id="63463-146">In Human Resources, you can use the **Compensation** tab to choose to restrict access to compensation plans and to set a default currency.</span></span>

<span data-ttu-id="63463-147">報酬の詳細については、[報酬プランの概要](hr-compensation-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63463-147">For more information about compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![報酬タブ](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a><span data-ttu-id="63463-149">番号順序</span><span class="sxs-lookup"><span data-stu-id="63463-149">Number sequences</span></span>

<span data-ttu-id="63463-150">**番号順序** タブの設定により、次のような人事管理の品目に対して自動的に ID を割り当てるために使用する順序が決定されます。</span><span class="sxs-lookup"><span data-stu-id="63463-150">The settings on the **Number sequence** tab determine the sequences used to automatically assign IDs to items in Human Resources, such as:</span></span>

- <span data-ttu-id="63463-151">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="63463-151">Applications</span></span>
- <span data-ttu-id="63463-152">休暇登録</span><span class="sxs-lookup"><span data-stu-id="63463-152">Absence registrations</span></span>
- <span data-ttu-id="63463-153">報酬プロセスの結果</span><span class="sxs-lookup"><span data-stu-id="63463-153">Compensation process results</span></span>
- <span data-ttu-id="63463-154">ケース番号</span><span class="sxs-lookup"><span data-stu-id="63463-154">Case numbers</span></span>
- <span data-ttu-id="63463-155">コース</span><span class="sxs-lookup"><span data-stu-id="63463-155">Courses</span></span>
- <span data-ttu-id="63463-156">コースの議題</span><span class="sxs-lookup"><span data-stu-id="63463-156">Course agendas</span></span>

<span data-ttu-id="63463-157">番号順序およびコードを管理するには、**番号順序** リスト ページを使用します (**組織管理 > 番号順序 > 番号順序** の順に選択します)。</span><span class="sxs-lookup"><span data-stu-id="63463-157">To maintain number sequence references and codes, use the **Number sequences** list page (select **Organization administration > Number sequences > Number sequences**).</span></span>

<span data-ttu-id="63463-158">詳細については、[番号順序の概要](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63463-158">For more information, see [Number sequences overview](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

> [!NOTE]
> <span data-ttu-id="63463-159">作業時間数は 1,250 を超えることはできず、雇用期間は 12 か月を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="63463-159">The number of hours that are worked can't exceed 1,250, and the length of employment can't exceed 12 months.</span></span> <span data-ttu-id="63463-160">これらの最大値は米国の連邦法に従います。</span><span class="sxs-lookup"><span data-stu-id="63463-160">These maximum values are in accordance with federal law in the United States.</span></span>

![番号順序タブ](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a><span data-ttu-id="63463-162">FMLA</span><span class="sxs-lookup"><span data-stu-id="63463-162">FMLA</span></span>

<span data-ttu-id="63463-163">FMLA タブでは、FMLA 資格条件と、FMLA 資格付与時間を設定します。</span><span class="sxs-lookup"><span data-stu-id="63463-163">On the FMLA tab, you set FMLA eligibility requirements and FMLA entitlement hours.</span></span> <span data-ttu-id="63463-164">詳細については、[休暇および欠勤パラメーターのコンフィギュレーション](hr-leave-and-absence-parameters.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63463-164">For more information, see [Configure leave and absence parameters](hr-leave-and-absence-parameters.md).</span></span>

![FMLA タブ ](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a><span data-ttu-id="63463-166">従業員セルフ サービス</span><span class="sxs-lookup"><span data-stu-id="63463-166">Employee self service</span></span>

<span data-ttu-id="63463-167">**従業員セルフ サービス** タブの設定は、従業員セルフ サービスが従業員にどのように表示されるかに影響します。</span><span class="sxs-lookup"><span data-stu-id="63463-167">The settings on the **Employee self service** tab affect how Employee self service appears to employees.</span></span> <span data-ttu-id="63463-168">このタブで次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="63463-168">On this tab, you can:</span></span>

- <span data-ttu-id="63463-169">従業員セルフサービス ワークスペースの名前を入力します</span><span class="sxs-lookup"><span data-stu-id="63463-169">Enter a name for the Employee self service workspace</span></span>
- <span data-ttu-id="63463-170">従業員に対してマネージャが入力できる情報を選択します</span><span class="sxs-lookup"><span data-stu-id="63463-170">Select which information a manager can enter for employees</span></span>
- <span data-ttu-id="63463-171">従業員向けに役立つリンクを追加します</span><span class="sxs-lookup"><span data-stu-id="63463-171">Add useful links for employees</span></span>
- <span data-ttu-id="63463-172">従業員がビジネスの連絡先情報を追加または編集するのを制限します。</span><span class="sxs-lookup"><span data-stu-id="63463-172">Restrict employees from adding or editing business contact details.</span></span> <span data-ttu-id="63463-173">詳細については、[個人情報の編集の制限](hr-employee-self-service-restrict-editing.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63463-173">For more information, see [Restrict editing of personal information](hr-employee-self-service-restrict-editing.md).</span></span>

<span data-ttu-id="63463-174">従業員セルフ サービスの設定の詳細については、[従業員およびマネージャー セルフ サービスの概要](hr-employee-manager-self-service-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63463-174">For more information about setting up Employee self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![従業員セルフ サービス タブ](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a><span data-ttu-id="63463-176">マネージャー セルフ サービス</span><span class="sxs-lookup"><span data-stu-id="63463-176">Manager self service</span></span>

<span data-ttu-id="63463-177">**マネージャー セルフ サービス** の設定は、マネージャーがマネージャー セルフ サービスに表示する内容に影響します。</span><span class="sxs-lookup"><span data-stu-id="63463-177">The settings on the **Manager self service** tab affect what managers see in Manager self service.</span></span> <span data-ttu-id="63463-178">このタブでは、次のオプションを構成できます。</span><span class="sxs-lookup"><span data-stu-id="63463-178">On this tab, you can configure the following options:</span></span>

- <span data-ttu-id="63463-179">期限が切れるレコードの範囲</span><span class="sxs-lookup"><span data-stu-id="63463-179">The range for expiring records</span></span>
- <span data-ttu-id="63463-180">マネージャーが期限が切れるレコードで表示できる情報</span><span class="sxs-lookup"><span data-stu-id="63463-180">Information managers can view in expiring records</span></span>
- <span data-ttu-id="63463-181">マネージャーが拡張レポートの空いている職位を表示できるかどうか</span><span class="sxs-lookup"><span data-stu-id="63463-181">Whether managers can view open positions for extended reports</span></span>
- <span data-ttu-id="63463-182">既存の作業者の表示</span><span class="sxs-lookup"><span data-stu-id="63463-182">Views of exiting workers</span></span>
- <span data-ttu-id="63463-183">マネージャー向けに役立つリンク</span><span class="sxs-lookup"><span data-stu-id="63463-183">Useful links for managers</span></span>

<span data-ttu-id="63463-184">マネージャー セルフ サービスの設定の詳細については、[従業員およびマネージャー セルフ サービスの概要](hr-employee-manager-self-service-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63463-184">For more information about setting up Manager self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![マネージャー セルフ サービス タブ](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a><span data-ttu-id="63463-186">給付金管理</span><span class="sxs-lookup"><span data-stu-id="63463-186">Benefits management</span></span>

<span data-ttu-id="63463-187">給付金管理タブで、給付金管理の電子メール オプションを構成できます。</span><span class="sxs-lookup"><span data-stu-id="63463-187">On the Benefits management tab, you can configure email options for Benefits management.</span></span> <span data-ttu-id="63463-188">給付金管理の設定および使用の詳細については、[給付金管理の概要](hr-benefits-management-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63463-188">For information about setting up and using Benefits management, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

![給付金管理タブ](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a><span data-ttu-id="63463-190">休暇</span><span class="sxs-lookup"><span data-stu-id="63463-190">Leave and absence</span></span>

<span data-ttu-id="63463-191">休暇と欠勤の設定および使用の詳細については、[休暇と欠勤の概要](hr-leave-and-absence-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63463-191">For information about setting up and using Leave and absence, see [Leave and absence overview](hr-leave-and-absence-overview.md).</span></span>

## <a name="payment-methods"></a><span data-ttu-id="63463-192">支払方法</span><span class="sxs-lookup"><span data-stu-id="63463-192">Payment methods</span></span>

<span data-ttu-id="63463-193">**支払方法** タブで、組織でサポートされている支払方法を選択できます。</span><span class="sxs-lookup"><span data-stu-id="63463-193">On the **Payment methods** tab, you can select the payment methods supported by your organization.</span></span> <span data-ttu-id="63463-194">報酬の構成の詳細については、[報酬プランの概要](hr-compensation-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63463-194">For more information about configuring compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![支払方法タブ](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]