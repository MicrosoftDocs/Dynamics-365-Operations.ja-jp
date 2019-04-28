---
title: Talent と Dayforce 間での給与統合のコンフィギュレーション
description: このトピックでは、Microsoft Dynamics 365 for Talent と Ceridian Dayforce 間での統合をコンフィギュレーションして、支払実行を処理する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9a88bf61dbb12520b555ceb7363b1c646d95386e
ms.sourcegitcommit: 204e4554e409c39fbbf7b273ad138ce2809931a8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2019
ms.locfileid: "898447"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="26d8a-103">Talent と Dayforce 間の給与統合のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="26d8a-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="26d8a-104">Microsoft Dynamics 365 for Talent および Ceridian Dayforce 間での統合は、このトピックで説明するいくつかのコンフィギュレーション手順に依存します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="26d8a-105">支払の実行を処理する前に、Talent および Dayforce の両方で、統合をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="26d8a-106">支払の実行を完了するため Dayforce などのサービスを使用する場合、Talent 内の統合を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="26d8a-107">統合には Talent からの固有データが必要です。</span><span class="sxs-lookup"><span data-stu-id="26d8a-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="26d8a-108">したがって、Dayforce にマップされているデータが、統合をサポートする方法で Talent 内でコンフィギュレーションされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="26d8a-109">統合は次の広範なデータ カテゴリを使用します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="26d8a-110">人事管理データ</span><span class="sxs-lookup"><span data-stu-id="26d8a-110">Human resources data</span></span>
- <span data-ttu-id="26d8a-111">報酬データ</span><span class="sxs-lookup"><span data-stu-id="26d8a-111">Compensation data</span></span>
- <span data-ttu-id="26d8a-112">支払サイクル、支払期間、および所得コードなどの給与データ</span><span class="sxs-lookup"><span data-stu-id="26d8a-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="26d8a-113">作業者データ</span><span class="sxs-lookup"><span data-stu-id="26d8a-113">Worker data</span></span>

<span data-ttu-id="26d8a-114">このトピックでは、統合を有効にするために従う必要がある手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="26d8a-115">統合に必要なデータの種類およびコンフィギュレーションの詳細についても説明します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="26d8a-116">統合の有効化</span><span class="sxs-lookup"><span data-stu-id="26d8a-116">Enable the integration</span></span>

<span data-ttu-id="26d8a-117">Talent 内で統合を有効にし、Dayforce に接続するコンフィギュレーション情報を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="26d8a-118">生成される一般会計トランザクションを Microsoft Dynamics 365 for Finance and Operations にインポートしたい場合、Microsoft Azure ストレージ アカウントを設定し、Finance and Operations 内で、Azure Storage の接続文字列を入力する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="26d8a-119">Talent 内で統合を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="26d8a-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="26d8a-120">**システム管理**ページで、**統合コンフィギュレーション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="26d8a-121">セキュリティで保護された FTP (File Transfer Protocol) のエンドポイント、およびセキュリティで保護された FTP フォルダー パスを入力します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="26d8a-122">セキュリティで保護された FTP エンドポイントおよびフォルダー パスにアクセスするユーザーのユーザー名とパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="26d8a-123">必要に応じて接続をテストし、**給与統合の有効化**のオプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="26d8a-124">統合が有効な場合、データのエクスポート パッケージおよびファイルが作成され、頻度が設定されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="26d8a-125">必要に応じて、この頻度を変更できます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="26d8a-126">Azure ストレージ アカウント および Azure ストレージの接続文字列の詳細については、次の Azure のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="26d8a-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="26d8a-127">Azure ストレージ アカウントについて</span><span class="sxs-lookup"><span data-stu-id="26d8a-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="26d8a-128">Azure ストレージの接続文字列のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="26d8a-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="26d8a-129">データのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="26d8a-129">Configure your data</span></span> 

<span data-ttu-id="26d8a-130">給与を処理するには、Talent で人事管理のデータをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="26d8a-131">職務と職位などの組織データを、給付金および報酬情報と共に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="26d8a-132">この情報は、雇用、支払、および従業員の給与を生成するために必要な控除情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="26d8a-133">人事管理データ</span><span class="sxs-lookup"><span data-stu-id="26d8a-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="26d8a-134">福利厚生</span><span class="sxs-lookup"><span data-stu-id="26d8a-134">Benefits</span></span> 

<span data-ttu-id="26d8a-135">人事管理は、給付金、控除、および組織が作業者に対して提供または処理する作業者の報酬プランを設定および管理するツールを提供します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="26d8a-136">給付金を作成する場合、Dayforce で使用される次のデータとコンフィギュレーションに留意してください。</span><span class="sxs-lookup"><span data-stu-id="26d8a-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="26d8a-137">福利厚生計画</span><span class="sxs-lookup"><span data-stu-id="26d8a-137">Benefit plans</span></span>

- <span data-ttu-id="26d8a-138">計画 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-138">Plan (required)</span></span>
- <span data-ttu-id="26d8a-139">種類 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-139">Type (required)</span></span>
- <span data-ttu-id="26d8a-140">給与の影響 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-140">Payroll impact (required)</span></span>
- <span data-ttu-id="26d8a-141">未払金の回収</span><span class="sxs-lookup"><span data-stu-id="26d8a-141">Recover arrears</span></span>
- <span data-ttu-id="26d8a-142">控除方式</span><span class="sxs-lookup"><span data-stu-id="26d8a-142">Deduction method</span></span>
- <span data-ttu-id="26d8a-143">控除の優先順位</span><span class="sxs-lookup"><span data-stu-id="26d8a-143">Deduction priority</span></span>
- <span data-ttu-id="26d8a-144">制限の期間</span><span class="sxs-lookup"><span data-stu-id="26d8a-144">Limit period</span></span>
- <span data-ttu-id="26d8a-145">限度金額</span><span class="sxs-lookup"><span data-stu-id="26d8a-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="26d8a-146">福利厚生</span><span class="sxs-lookup"><span data-stu-id="26d8a-146">Benefits</span></span>

- <span data-ttu-id="26d8a-147">計画 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-147">Plan (required)</span></span>
- <span data-ttu-id="26d8a-148">種類 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-148">Type (required)</span></span>
- <span data-ttu-id="26d8a-149">オプション (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-149">Option (required)</span></span>
- <span data-ttu-id="26d8a-150">給付金 ID (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-150">Benefit ID (required)</span></span>
- <span data-ttu-id="26d8a-151">頻度</span><span class="sxs-lookup"><span data-stu-id="26d8a-151">Frequency</span></span>
- <span data-ttu-id="26d8a-152">基準</span><span class="sxs-lookup"><span data-stu-id="26d8a-152">Basis</span></span>
- <span data-ttu-id="26d8a-153">金額またはレート</span><span class="sxs-lookup"><span data-stu-id="26d8a-153">Amount or rate</span></span>
- <span data-ttu-id="26d8a-154">所得コード</span><span class="sxs-lookup"><span data-stu-id="26d8a-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="26d8a-155">サポートされる頻度</span><span class="sxs-lookup"><span data-stu-id="26d8a-155">Supported frequencies</span></span> 

- <span data-ttu-id="26d8a-156">毎週</span><span class="sxs-lookup"><span data-stu-id="26d8a-156">Weekly</span></span>
- <span data-ttu-id="26d8a-157">隔週</span><span class="sxs-lookup"><span data-stu-id="26d8a-157">Bi-weekly</span></span>
- <span data-ttu-id="26d8a-158">半月ごと</span><span class="sxs-lookup"><span data-stu-id="26d8a-158">Semi-monthly</span></span>
- <span data-ttu-id="26d8a-159">月 1 回</span><span class="sxs-lookup"><span data-stu-id="26d8a-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="26d8a-160">サポートされる基準</span><span class="sxs-lookup"><span data-stu-id="26d8a-160">Supported bases</span></span> 

- <span data-ttu-id="26d8a-161">固定金額</span><span class="sxs-lookup"><span data-stu-id="26d8a-161">Fixed amount</span></span>
- <span data-ttu-id="26d8a-162">所得の割合</span><span class="sxs-lookup"><span data-stu-id="26d8a-162">Percent of earnings</span></span>
- <span data-ttu-id="26d8a-163">生産時間</span><span class="sxs-lookup"><span data-stu-id="26d8a-163">Productive hours</span></span>

<span data-ttu-id="26d8a-164">Dayforce は、給付金の計画で定義される給与影響に基づいて次の控除を作成します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="26d8a-165">Talent での選択</span><span class="sxs-lookup"><span data-stu-id="26d8a-165">Selection in Talent</span></span>        | <span data-ttu-id="26d8a-166">Dayforce での結果</span><span class="sxs-lookup"><span data-stu-id="26d8a-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="26d8a-167">None</span><span class="sxs-lookup"><span data-stu-id="26d8a-167">None</span></span>                       | <span data-ttu-id="26d8a-168">控除は作成されません。</span><span class="sxs-lookup"><span data-stu-id="26d8a-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="26d8a-169">控除のみ</span><span class="sxs-lookup"><span data-stu-id="26d8a-169">Deduction only</span></span>             | <span data-ttu-id="26d8a-170">従業員控除が作成されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="26d8a-171">貢献度のみ</span><span class="sxs-lookup"><span data-stu-id="26d8a-171">Contribution only</span></span>          | <span data-ttu-id="26d8a-172">雇用主控除が作成されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="26d8a-173">控除と貢献度</span><span class="sxs-lookup"><span data-stu-id="26d8a-173">Deduction and contribution</span></span> | <span data-ttu-id="26d8a-174">従業員および雇用主の控除が作成されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="26d8a-175">給付金プログラムを定義し、管理する方法の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="26d8a-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="26d8a-176">従業員手当プログラムの提供</span><span class="sxs-lookup"><span data-stu-id="26d8a-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="26d8a-177">新しい給付金の作成</span><span class="sxs-lookup"><span data-stu-id="26d8a-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="26d8a-178">給付金の適格性ルールおよびポリシーの定義</span><span class="sxs-lookup"><span data-stu-id="26d8a-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="26d8a-179">作業者の福利厚生の登録および削除</span><span class="sxs-lookup"><span data-stu-id="26d8a-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="26d8a-180">報酬</span><span class="sxs-lookup"><span data-stu-id="26d8a-180">Compensation</span></span> 

<span data-ttu-id="26d8a-181">基準賃金と報奨を管理するには、報酬管理を使用します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="26d8a-182">従業員の固定基準賃金および昇給は固定報酬プランで管理されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="26d8a-183">インセンティブ支払 (賞与の支払、業績報奨、ストック オプション、付与など) の支払および一時報奨は変動報酬プランで管理します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="26d8a-184">Dayforce は、報酬情報を使用して、従業員の時間または年間レートを計算します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="26d8a-185">固定報酬プランと支払レートの換算が必要です。</span><span class="sxs-lookup"><span data-stu-id="26d8a-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="26d8a-186">従業員は固定報酬プランに関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="26d8a-187">報酬プランの詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="26d8a-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="26d8a-188">固定報酬プランの作成</span><span class="sxs-lookup"><span data-stu-id="26d8a-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="26d8a-189">変動報酬プランの作成</span><span class="sxs-lookup"><span data-stu-id="26d8a-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="26d8a-190">給与/報酬構造および計画の作成</span><span class="sxs-lookup"><span data-stu-id="26d8a-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="26d8a-191">報酬の処理</span><span class="sxs-lookup"><span data-stu-id="26d8a-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="26d8a-192">報酬プロセスの定義と結果の計算</span><span class="sxs-lookup"><span data-stu-id="26d8a-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="26d8a-193">固定報酬プランへの従業員の登録</span><span class="sxs-lookup"><span data-stu-id="26d8a-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="26d8a-194">変動報酬プランへの従業員の登録</span><span class="sxs-lookup"><span data-stu-id="26d8a-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="26d8a-195">職務</span><span class="sxs-lookup"><span data-stu-id="26d8a-195">Jobs</span></span> 

<span data-ttu-id="26d8a-196">職務とは、職務を遂行する担当者に必要なタスクと職責の集合です。</span><span class="sxs-lookup"><span data-stu-id="26d8a-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="26d8a-197">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="26d8a-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="26d8a-198">職務のコンポーネントの設定</span><span class="sxs-lookup"><span data-stu-id="26d8a-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="26d8a-199">新しいジョブの定義</span><span class="sxs-lookup"><span data-stu-id="26d8a-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="26d8a-200">職位</span><span class="sxs-lookup"><span data-stu-id="26d8a-200">Positions</span></span>

<span data-ttu-id="26d8a-201">職位は、職務の個々のインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="26d8a-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="26d8a-202">たとえば、「販売マネージャー (東部)」という職位は、「販売マネージャー」という職務に関連付けられている職位の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="26d8a-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="26d8a-203">職位は、部門内に存在します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-203">A position exists in a department.</span></span> <span data-ttu-id="26d8a-204">1 人の作業者は 1 つの職位にのみ関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="26d8a-205">職位を設定する場合、次のデータとコンフィギュレーションに注意してください。</span><span class="sxs-lookup"><span data-stu-id="26d8a-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="26d8a-206">職位 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-206">Position (required)</span></span>
- <span data-ttu-id="26d8a-207">説明 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-207">Description (required)</span></span>
- <span data-ttu-id="26d8a-208">職務 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-208">Job (required)</span></span>
- <span data-ttu-id="26d8a-209">部門 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-209">Department (required)</span></span>
- <span data-ttu-id="26d8a-210">職位タイプ (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-210">Position type (required)</span></span>
- <span data-ttu-id="26d8a-211">フルタイム相当</span><span class="sxs-lookup"><span data-stu-id="26d8a-211">Full-time equivalent</span></span>
- <span data-ttu-id="26d8a-212">年間基本勤務時間 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="26d8a-213">法人による支払 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="26d8a-214">支払サイクル (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-214">Pay cycle (required)</span></span>
- <span data-ttu-id="26d8a-215">既定の財務分析コード – 原価部門 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="26d8a-216">作業者割り当て – 作業者、割り当ての開始、割り当ての終了、理由コード</span><span class="sxs-lookup"><span data-stu-id="26d8a-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="26d8a-217">同じ部門の複数の職位が同じジョブに関連付けられている場合、Dayforce で 1 つの職位に連結します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="26d8a-218">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="26d8a-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="26d8a-219">部門、職務、職位を使用した従業員の編成</span><span class="sxs-lookup"><span data-stu-id="26d8a-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="26d8a-220">職位の設定</span><span class="sxs-lookup"><span data-stu-id="26d8a-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="26d8a-221">部門</span><span class="sxs-lookup"><span data-stu-id="26d8a-221">Departments</span></span>

<span data-ttu-id="26d8a-222">部門は、組織のカテゴリまたは機能領域を表す作業単位です。</span><span class="sxs-lookup"><span data-stu-id="26d8a-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="26d8a-223">部門は、販売、会計、または人事管理など、組織内の特定の領域を担当します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="26d8a-224">機能領域の報告に部門を使用できます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="26d8a-225">部門は損益の職責を持つ場合があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="26d8a-226">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="26d8a-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="26d8a-227">部門の作成と部門階層への関連付け</span><span class="sxs-lookup"><span data-stu-id="26d8a-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="26d8a-228">新しい部門の定義</span><span class="sxs-lookup"><span data-stu-id="26d8a-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="26d8a-229">支払サイクルと支払期間</span><span class="sxs-lookup"><span data-stu-id="26d8a-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="26d8a-230">給与計算頻度および作業者が支払を受ける特定の日は、支払サイクルによって決まります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="26d8a-231">たとえば、支払サイクルが月単位で、その月の最後の日に従業員に支払われる場合があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="26d8a-232">または、支払サイクルが週単位で、支払期間終了日の次の火曜日に支払われる場合もあります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="26d8a-233">支払サイクルは、それらの職位にある作業者にいつ支払われるかを制御するために、職位に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="26d8a-234">支払サイクルを作成した後、各サイクルごとに支払期間を生成できます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="26d8a-235">各支払期間には、入力した情報に基づく既定の支払期日が含まれます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="26d8a-236">ただし、支払期日が休日になる場合などの例外を許可するため、支払期間の既定の支払期日を変更できます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="26d8a-237">次の情報は、Dayforce で使用されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="26d8a-238">支払サイクル (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-238">Pay cycle (required)</span></span>
- <span data-ttu-id="26d8a-239">支払サイクル頻度 (頻度)</span><span class="sxs-lookup"><span data-stu-id="26d8a-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="26d8a-240">期間開始日 (最初の支払期間は必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="26d8a-241">既定の支払期日 (最初の支払期間は必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="26d8a-242">この情報は、支払グループとして Dayforce に統合され、各支払サイクルごとに国または地域で区切られます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="26d8a-243">統合の前に、少なくとも 1 つの支払期間を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="26d8a-244">Dayforce は、最初の支払期日の開始日および Talent で設定された既定の支払期日に基づいて、支払グループのカレンダーと支払期日を生成します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="26d8a-245">所得コード</span><span class="sxs-lookup"><span data-stu-id="26d8a-245">Earning codes</span></span>

<span data-ttu-id="26d8a-246">所得コードは、作業者が受け取るすべての収益のタイプを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="26d8a-247">コードには、会計ルール、税法、レポート要件、およびグロスアップ能力など、所得に関連付けられているさまざまなパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="26d8a-248">次の情報は、Dayforce で使用されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="26d8a-249">所得コード (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-249">Earning Code (required)</span></span>
- <span data-ttu-id="26d8a-250">説明</span><span class="sxs-lookup"><span data-stu-id="26d8a-250">Description</span></span>
- <span data-ttu-id="26d8a-251">計量単位</span><span class="sxs-lookup"><span data-stu-id="26d8a-251">Unit of measure</span></span>
- <span data-ttu-id="26d8a-252">生産</span><span class="sxs-lookup"><span data-stu-id="26d8a-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="26d8a-253">作業者データ</span><span class="sxs-lookup"><span data-stu-id="26d8a-253">Worker data</span></span>

<span data-ttu-id="26d8a-254">人事管理と給与システムにとって、所有しているさまざまなタイプの作業者のレコードは重要です。</span><span class="sxs-lookup"><span data-stu-id="26d8a-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="26d8a-255">入力された情報を使用して、作業者と個人情報を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="26d8a-256">作業者には次の情報を管理できます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="26d8a-257">**基本** – 連絡先情報、人口学的情報、識別情報、家族情報、兵役の状態、海外在住情報、自宅、緊急連絡先など、作業者に関する基本的な情報を管理します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="26d8a-258">**雇用** – 法人や組織への所属、職位割り当て、開始日と終了日、業務適性、雇用条件、年金、休暇、再配置情報など、作業者の雇用に関する情報を管理します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="26d8a-259">**休暇** – 作業カレンダー、休暇トランザクション、休暇設定など、作業者の休暇に関する情報を管理します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="26d8a-260">**報酬と給与** – プラン登録、報奨、実績、手数料、税金情報、退職、給与控除など、作業者の報酬プランと給与情報に関する情報を管理します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="26d8a-261">作業者情報を入力する場合、Dayforce で使用される次のデータとコンフィギュレーションに留意してください。</span><span class="sxs-lookup"><span data-stu-id="26d8a-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="26d8a-262">一般情報</span><span class="sxs-lookup"><span data-stu-id="26d8a-262">General information</span></span>

- <span data-ttu-id="26d8a-263">個人番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-263">Personnel number (required)</span></span>
- <span data-ttu-id="26d8a-264">名 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-264">First name (required)</span></span>
- <span data-ttu-id="26d8a-265">姓 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-265">Last name (required)</span></span>
- <span data-ttu-id="26d8a-266">ミドル ネーム</span><span class="sxs-lookup"><span data-stu-id="26d8a-266">Middle name</span></span>
- <span data-ttu-id="26d8a-267">勤続日数</span><span class="sxs-lookup"><span data-stu-id="26d8a-267">Seniority date</span></span>
- <span data-ttu-id="26d8a-268">呼称</span><span class="sxs-lookup"><span data-stu-id="26d8a-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="26d8a-269">個人情報</span><span class="sxs-lookup"><span data-stu-id="26d8a-269">Personal information</span></span>

- <span data-ttu-id="26d8a-270">配偶者の有無 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-270">Marital status (required)</span></span>
- <span data-ttu-id="26d8a-271">生年月日 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-271">Birth date (required)</span></span>
- <span data-ttu-id="26d8a-272">性別 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-272">Gender (required)</span></span>
- <span data-ttu-id="26d8a-273">障碍のあるユーザー</span><span class="sxs-lookup"><span data-stu-id="26d8a-273">Person with disabilities</span></span>
- <span data-ttu-id="26d8a-274">国籍 国 地域 (メキシコの場合のみ)</span><span class="sxs-lookup"><span data-stu-id="26d8a-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="26d8a-275">住所情報</span><span class="sxs-lookup"><span data-stu-id="26d8a-275">Address information</span></span>

- <span data-ttu-id="26d8a-276">基本 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-276">Primary (required)</span></span>
- <span data-ttu-id="26d8a-277">国/地域 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-277">Country/region (required)</span></span>
- <span data-ttu-id="26d8a-278">郵便番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-278">Postal code (required)</span></span>
- <span data-ttu-id="26d8a-279">番地 (必須) (メキシコの場合のみ)</span><span class="sxs-lookup"><span data-stu-id="26d8a-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="26d8a-280">建物名 (メキシコの場合のみ)</span><span class="sxs-lookup"><span data-stu-id="26d8a-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="26d8a-281">市町村 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-281">City (required)</span></span>
- <span data-ttu-id="26d8a-282">都道府県 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-282">State (required)</span></span>
- <span data-ttu-id="26d8a-283">国 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="26d8a-284">連絡先情報</span><span class="sxs-lookup"><span data-stu-id="26d8a-284">Contact information</span></span> 

- <span data-ttu-id="26d8a-285">基本 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-285">Primary (required)</span></span>
- <span data-ttu-id="26d8a-286">連絡先の電話番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-286">Contact number (required)</span></span>
- <span data-ttu-id="26d8a-287">内線</span><span class="sxs-lookup"><span data-stu-id="26d8a-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="26d8a-288">給与情報および所得コード</span><span class="sxs-lookup"><span data-stu-id="26d8a-288">Payroll information and earning codes</span></span>

<span data-ttu-id="26d8a-289">従業員は、指定された支払頻度で特定の所得が割り当てられ、希望の支払方法を有する場合があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="26d8a-290">次のフィールドは、それらの基本設定と設定が使用されることを保証するために Dayforce で使用されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="26d8a-291">所得コード</span><span class="sxs-lookup"><span data-stu-id="26d8a-291">Earning codes</span></span>

- <span data-ttu-id="26d8a-292">職位 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-292">Position (required)</span></span>
- <span data-ttu-id="26d8a-293">所得コード (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-293">Earning Code (required)</span></span>
- <span data-ttu-id="26d8a-294">頻度 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-294">Frequency (required)</span></span>
- <span data-ttu-id="26d8a-295">金額 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="26d8a-296">給与情報</span><span class="sxs-lookup"><span data-stu-id="26d8a-296">Payroll information</span></span>

- <span data-ttu-id="26d8a-297">支払方法</span><span class="sxs-lookup"><span data-stu-id="26d8a-297">Payment Method</span></span>
- <span data-ttu-id="26d8a-298">経済地域 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-298">Economic Region (required)</span></span>
- <span data-ttu-id="26d8a-299">従業員手当 ID</span><span class="sxs-lookup"><span data-stu-id="26d8a-299">Employee Benefits ID</span></span>
- <span data-ttu-id="26d8a-300">国民 ID 番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-300">National ID Number (required)</span></span>
- <span data-ttu-id="26d8a-301">兵役番号</span><span class="sxs-lookup"><span data-stu-id="26d8a-301">Military Service Number</span></span>
- <span data-ttu-id="26d8a-302">シフト ID (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-302">Shift ID (required)</span></span>
- <span data-ttu-id="26d8a-303">税番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-303">Tax Number (required)</span></span>
- <span data-ttu-id="26d8a-304">労働組合 ID (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-304">Union ID (required)</span></span>
- <span data-ttu-id="26d8a-305">作業日 ID (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-305">Work Day ID (required)</span></span>
- <span data-ttu-id="26d8a-306">労働許可番号</span><span class="sxs-lookup"><span data-stu-id="26d8a-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="26d8a-307">支払方法について、メキシコでは**現金**、**小切手** (会社の現物小切手)、および**電子支払**がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="26d8a-308">NP 支払方法が指定されている場合、既定で**小切手**が使用されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="26d8a-309">従業員の詳細</span><span class="sxs-lookup"><span data-stu-id="26d8a-309">Employment details</span></span>

<span data-ttu-id="26d8a-310">雇用の詳細履歴は、Dayforce で従業員の採用、退職、および再雇用のステータスを派生させるため、重要な情報として使用されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="26d8a-311">Dayforce は、一度に 1 つだけ有効な雇用レコードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="26d8a-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="26d8a-312">雇用開始日 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-312">Employment start date (required)</span></span>
- <span data-ttu-id="26d8a-313">雇用終了日</span><span class="sxs-lookup"><span data-stu-id="26d8a-313">Employment end date</span></span>
- <span data-ttu-id="26d8a-314">入社日</span><span class="sxs-lookup"><span data-stu-id="26d8a-314">Start date</span></span>
- <span data-ttu-id="26d8a-315">調整済開始日</span><span class="sxs-lookup"><span data-stu-id="26d8a-315">Adjusted start date</span></span>
- <span data-ttu-id="26d8a-316">退職日 (退職時は必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="26d8a-317">退職理由 (退職時は必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="26d8a-318">従業員の重要な日付は、次の情報を使用して派生されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="26d8a-319">Talent</span><span class="sxs-lookup"><span data-stu-id="26d8a-319">Talent</span></span>                | <span data-ttu-id="26d8a-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="26d8a-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26d8a-321">最新の採用日付</span><span class="sxs-lookup"><span data-stu-id="26d8a-321">Most recent hire date</span></span> | <span data-ttu-id="26d8a-322">現在の非退職雇用履歴レコードの雇用開始</span><span class="sxs-lookup"><span data-stu-id="26d8a-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="26d8a-323">退職日</span><span class="sxs-lookup"><span data-stu-id="26d8a-323">Termination date</span></span>      | <span data-ttu-id="26d8a-324">現在の非退職雇用履歴レコードの退職日</span><span class="sxs-lookup"><span data-stu-id="26d8a-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="26d8a-325">入社日</span><span class="sxs-lookup"><span data-stu-id="26d8a-325">Start date</span></span>            | <span data-ttu-id="26d8a-326">現在の非アクティブ雇用履歴レコードの調整済開始日、開始日、または雇用開始</span><span class="sxs-lookup"><span data-stu-id="26d8a-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="26d8a-327">元の採用日付</span><span class="sxs-lookup"><span data-stu-id="26d8a-327">Original hire date</span></span>    | <span data-ttu-id="26d8a-328">最も早い雇用履歴レコードの雇用開始</span><span class="sxs-lookup"><span data-stu-id="26d8a-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="26d8a-329">報酬</span><span class="sxs-lookup"><span data-stu-id="26d8a-329">Compensation</span></span>

<span data-ttu-id="26d8a-330">固定報酬計画は、雇用期間全体ですべての従業員の基本職位に関連付けられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="26d8a-331">この期間は、従業員が採用された日付 (または雇用の開始日) に開始し、退職するまで継続します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="26d8a-332">有効日 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-332">Effective Date (required)</span></span>
- <span data-ttu-id="26d8a-333">有効期限</span><span class="sxs-lookup"><span data-stu-id="26d8a-333">Expiration date</span></span>
- <span data-ttu-id="26d8a-334">支払レート (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-334">Pay Rate (required)</span></span>
- <span data-ttu-id="26d8a-335">支払レートの変換 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="26d8a-336">年間相当額 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="26d8a-337">時間相当額 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="26d8a-338">時給払いの従業員に複数の職位がある場合、基本職位の固定報酬が作業者レベルの基準レートまたは給与として Dayforce にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="26d8a-339">基本以外の職位については、時給のレートが Dayforce の対応する職位に保存されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="26d8a-340">月給払いの従業員に複数の職位がある場合、累計時間率およびすべての有効な職位全体での年間給与が派生され、従業員レベルの基準レートまたは給与として使用されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="26d8a-341">ID 番号</span><span class="sxs-lookup"><span data-stu-id="26d8a-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="26d8a-342">社会保障 ID</span><span class="sxs-lookup"><span data-stu-id="26d8a-342">Social Security identifier</span></span> 

<span data-ttu-id="26d8a-343">すべての従業員は、1 つの基本 ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="26d8a-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="26d8a-344">この ID は **SSN** ID タイプにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="26d8a-345">Dayforce では、採用に必要な従業員の社会保障 ID として自動的に派生されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="26d8a-346">基本 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-346">Primary (required)</span></span>
- <span data-ttu-id="26d8a-347">ID タイプ = "SSN"</span><span class="sxs-lookup"><span data-stu-id="26d8a-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="26d8a-348">発行日付</span><span class="sxs-lookup"><span data-stu-id="26d8a-348">Issued Date</span></span>
- <span data-ttu-id="26d8a-349">有効期限</span><span class="sxs-lookup"><span data-stu-id="26d8a-349">Expiration Date</span></span>

<span data-ttu-id="26d8a-350">従業員は、**SSN** ID タイプの複数の ID 番号を申告できます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="26d8a-351">ただし、その番号が有効かまたは期限切れかに関係なく、**基本**としてマークされているレコードのみ Dayforce に統合されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="26d8a-352">銀行口座および出金</span><span class="sxs-lookup"><span data-stu-id="26d8a-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="26d8a-353">銀行口座振替による支払を選択した従業員すべてのために、有効な銀行口座情報を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="26d8a-354">Talent</span><span class="sxs-lookup"><span data-stu-id="26d8a-354">Talent</span></span>                         | <span data-ttu-id="26d8a-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="26d8a-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26d8a-356">銀行口座番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="26d8a-357">SWIFT コード (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-357">SWIFT code (required)</span></span>          | <span data-ttu-id="26d8a-358">メキシコの給与処理に使用される**銀行 ID** フィールド。</span><span class="sxs-lookup"><span data-stu-id="26d8a-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="26d8a-359">支店番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="26d8a-360">銀行口座の種類 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-360">Bank account type (required)</span></span>   | <span data-ttu-id="26d8a-361">メキシコの給与処理に使用される**口座の種類**フィールド。</span><span class="sxs-lookup"><span data-stu-id="26d8a-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="26d8a-362">サポートされている値には、**当座預金**および**給与**が含まれます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="26d8a-363">銀行口座振替による支払を選択した従業員は、メキシコに基本住所を持つ法人の下にあり、メキシコの銀行から有効な銀行口座に関連付けられている残余口座のリンクを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="26d8a-364">その他のすべての非残余口座は無視されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="26d8a-365">住所情報</span><span class="sxs-lookup"><span data-stu-id="26d8a-365">Address information</span></span>

<span data-ttu-id="26d8a-366">すべての従業員は、1 つの基本場所が必要です。</span><span class="sxs-lookup"><span data-stu-id="26d8a-366">Every employee must have one primary location.</span></span> <span data-ttu-id="26d8a-367">Dayforce において、この場所は課税額算出のために従業員の基本居住地を特定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="26d8a-368">基本 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-368">Primary (required)</span></span>
- <span data-ttu-id="26d8a-369">国/地域 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-369">Country/region (required)</span></span>
- <span data-ttu-id="26d8a-370">郵便番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="26d8a-371">住所 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-371">Street (required)</span></span>
- <span data-ttu-id="26d8a-372">番地 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-372">Street Number (required)</span></span>
- <span data-ttu-id="26d8a-373">建物名</span><span class="sxs-lookup"><span data-stu-id="26d8a-373">Building Complement</span></span>
- <span data-ttu-id="26d8a-374">市町村 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-374">City (required)</span></span>
- <span data-ttu-id="26d8a-375">都道府県 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-375">State (required)</span></span>
- <span data-ttu-id="26d8a-376">国 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="26d8a-377">米国およびカナダでの給与を生成するために、データをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="26d8a-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="26d8a-378">米国およびカナダの従業員のために支払を生成している場合、次の要素をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="26d8a-379">職位に部門が必要です。</span><span class="sxs-lookup"><span data-stu-id="26d8a-379">Departments are required on positions.</span></span>
- <span data-ttu-id="26d8a-380">原価部門を財務分析コードとして設定し、既定の財務分析コード文字列の最初の要素とする必要があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="26d8a-381">職位が部門を指定するように人材を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-381">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="26d8a-382">この作業を実行するには、**人事管理共有職位 > 職位 > 職位の部門を要求**に移動します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-382">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="26d8a-383">この設定は、システムの統合に適用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="26d8a-383">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="26d8a-384">職務タイプ</span><span class="sxs-lookup"><span data-stu-id="26d8a-384">Job types</span></span>

<span data-ttu-id="26d8a-385">職務タイプは、類似した職務をカテゴリにグループ化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-385">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="26d8a-386">職務タイプは、米国およびカナダでの給与を処理するために必要です。</span><span class="sxs-lookup"><span data-stu-id="26d8a-386">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="26d8a-387">職務タイプの例には、フルタイムおよびパートタイム、または給与払いおよび時給払いが含まれます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-387">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="26d8a-388">職務タイプは、従業員が時給払いかあるいは給与払いなのかを示す支払タイプとして Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-388">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="26d8a-389">次の職務タイプと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="26d8a-389">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="26d8a-390">ジョブ タイプ</span><span class="sxs-lookup"><span data-stu-id="26d8a-390">Job type</span></span>   | <span data-ttu-id="26d8a-391">説明</span><span class="sxs-lookup"><span data-stu-id="26d8a-391">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="26d8a-392">時間</span><span class="sxs-lookup"><span data-stu-id="26d8a-392">Hourly</span></span>     | <span data-ttu-id="26d8a-393">時間</span><span class="sxs-lookup"><span data-stu-id="26d8a-393">Hourly</span></span>      |
| <span data-ttu-id="26d8a-394">給与払い</span><span class="sxs-lookup"><span data-stu-id="26d8a-394">Salaried</span></span>   | <span data-ttu-id="26d8a-395">給与払い</span><span class="sxs-lookup"><span data-stu-id="26d8a-395">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="26d8a-396">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="26d8a-396">Position types</span></span> 

<span data-ttu-id="26d8a-397">職位がフルタイム、パートタイム、またはその他のタイプかどうかを説明するために職位タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-397">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="26d8a-398">職位タイプは、従業員がフルタイムかあるいはパートタイムなのかを示す支払クラスとして Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-398">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="26d8a-399">次の職位タイプと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="26d8a-399">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="26d8a-400">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="26d8a-400">Position type</span></span>   | <span data-ttu-id="26d8a-401">説明</span><span class="sxs-lookup"><span data-stu-id="26d8a-401">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="26d8a-402">フルタイム</span><span class="sxs-lookup"><span data-stu-id="26d8a-402">Full-time</span></span>       | <span data-ttu-id="26d8a-403">フルタイム従業員</span><span class="sxs-lookup"><span data-stu-id="26d8a-403">Full time employee</span></span> |
| <span data-ttu-id="26d8a-404">パートタイム</span><span class="sxs-lookup"><span data-stu-id="26d8a-404">Part-time</span></span>       | <span data-ttu-id="26d8a-405">パートタイム従業員</span><span class="sxs-lookup"><span data-stu-id="26d8a-405">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="26d8a-406">理由コード</span><span class="sxs-lookup"><span data-stu-id="26d8a-406">Reason codes</span></span>

<span data-ttu-id="26d8a-407">理由コードは、従業員のステータスに関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-407">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="26d8a-408">理由コードは、従業員の職位または雇用ステータスへの変更の理由を示すステータス理由として Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-408">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="26d8a-409">次の理由コードと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="26d8a-409">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="26d8a-410">理由コード</span><span class="sxs-lookup"><span data-stu-id="26d8a-410">Reason code</span></span>    | <span data-ttu-id="26d8a-411">説明</span><span class="sxs-lookup"><span data-stu-id="26d8a-411">Description</span></span>      | <span data-ttu-id="26d8a-412">適用可能なシナリオ</span><span class="sxs-lookup"><span data-stu-id="26d8a-412">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="26d8a-413">辞職</span><span class="sxs-lookup"><span data-stu-id="26d8a-413">RESIGNATION</span></span>    | <span data-ttu-id="26d8a-414">辞職</span><span class="sxs-lookup"><span data-stu-id="26d8a-414">Resignation</span></span>      | <span data-ttu-id="26d8a-415">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="26d8a-415">Terminate worker</span></span>     |
| <span data-ttu-id="26d8a-416">終了</span><span class="sxs-lookup"><span data-stu-id="26d8a-416">TERMINATION</span></span>    | <span data-ttu-id="26d8a-417">終了</span><span class="sxs-lookup"><span data-stu-id="26d8a-417">Termination</span></span>      | <span data-ttu-id="26d8a-418">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="26d8a-418">Terminate worker</span></span>     |
| <span data-ttu-id="26d8a-419">定年退職</span><span class="sxs-lookup"><span data-stu-id="26d8a-419">RETIREMENT</span></span>     | <span data-ttu-id="26d8a-420">償却</span><span class="sxs-lookup"><span data-stu-id="26d8a-420">Retirement</span></span>       | <span data-ttu-id="26d8a-421">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="26d8a-421">Terminate worker</span></span>     |
| <span data-ttu-id="26d8a-422">その他</span><span class="sxs-lookup"><span data-stu-id="26d8a-422">OTHER</span></span>          | <span data-ttu-id="26d8a-423">その他の理由</span><span class="sxs-lookup"><span data-stu-id="26d8a-423">Other Reasons</span></span>    | <span data-ttu-id="26d8a-424">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="26d8a-424">Terminate worker</span></span>     |
| <span data-ttu-id="26d8a-425">死亡</span><span class="sxs-lookup"><span data-stu-id="26d8a-425">DEATH</span></span>          | <span data-ttu-id="26d8a-426">死亡</span><span class="sxs-lookup"><span data-stu-id="26d8a-426">Death</span></span>            | <span data-ttu-id="26d8a-427">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="26d8a-427">Terminate worker</span></span>     |
| <span data-ttu-id="26d8a-428">休暇</span><span class="sxs-lookup"><span data-stu-id="26d8a-428">LEAVEOFABSENCE</span></span> | <span data-ttu-id="26d8a-429">休暇</span><span class="sxs-lookup"><span data-stu-id="26d8a-429">Leave of Absence</span></span> | <span data-ttu-id="26d8a-430">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="26d8a-430">Terminate worker</span></span>     |
| <span data-ttu-id="26d8a-431">契約の終了</span><span class="sxs-lookup"><span data-stu-id="26d8a-431">CONTRACTEND</span></span>    | <span data-ttu-id="26d8a-432">契約の終了</span><span class="sxs-lookup"><span data-stu-id="26d8a-432">End of Contract</span></span>  | <span data-ttu-id="26d8a-433">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="26d8a-433">Terminate worker</span></span>     |
| <span data-ttu-id="26d8a-434">給与の変更</span><span class="sxs-lookup"><span data-stu-id="26d8a-434">SALARYCHANGE</span></span>   | <span data-ttu-id="26d8a-435">給与の変更</span><span class="sxs-lookup"><span data-stu-id="26d8a-435">Change of Salary</span></span> | <span data-ttu-id="26d8a-436">報酬</span><span class="sxs-lookup"><span data-stu-id="26d8a-436">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="26d8a-437">配偶者の有無</span><span class="sxs-lookup"><span data-stu-id="26d8a-437">Marital status</span></span>

<span data-ttu-id="26d8a-438">配偶者有無の値は、Dayforce にマップされ、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-438">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="26d8a-439">次の表に、配偶者有無の値がどのように Dayforce にマップされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-439">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="26d8a-440">Talent</span><span class="sxs-lookup"><span data-stu-id="26d8a-440">Talent</span></span>                 | <span data-ttu-id="26d8a-441">Dayforce</span><span class="sxs-lookup"><span data-stu-id="26d8a-441">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="26d8a-442">既婚</span><span class="sxs-lookup"><span data-stu-id="26d8a-442">Married</span></span>                | <span data-ttu-id="26d8a-443">既婚</span><span class="sxs-lookup"><span data-stu-id="26d8a-443">Married</span></span>              |
| <span data-ttu-id="26d8a-444">未婚</span><span class="sxs-lookup"><span data-stu-id="26d8a-444">Single</span></span>                 | <span data-ttu-id="26d8a-445">未婚</span><span class="sxs-lookup"><span data-stu-id="26d8a-445">Single</span></span>               |
| <span data-ttu-id="26d8a-446">死別</span><span class="sxs-lookup"><span data-stu-id="26d8a-446">Widowed</span></span>                | <span data-ttu-id="26d8a-447">死別</span><span class="sxs-lookup"><span data-stu-id="26d8a-447">Widowed</span></span>              |
| <span data-ttu-id="26d8a-448">離婚</span><span class="sxs-lookup"><span data-stu-id="26d8a-448">Divorced</span></span>               | <span data-ttu-id="26d8a-449">離婚</span><span class="sxs-lookup"><span data-stu-id="26d8a-449">Divorced</span></span>             |
| <span data-ttu-id="26d8a-450">登録済パートナーシップ</span><span class="sxs-lookup"><span data-stu-id="26d8a-450">Registered Partnership</span></span> | <span data-ttu-id="26d8a-451">ドメスティック パートナーシップ</span><span class="sxs-lookup"><span data-stu-id="26d8a-451">Domestic Partnership</span></span> |
| <span data-ttu-id="26d8a-452">None</span><span class="sxs-lookup"><span data-stu-id="26d8a-452">None</span></span>                   | <span data-ttu-id="26d8a-453">None</span><span class="sxs-lookup"><span data-stu-id="26d8a-453">None</span></span>                 |
| <span data-ttu-id="26d8a-454">同棲中</span><span class="sxs-lookup"><span data-stu-id="26d8a-454">Cohabiting</span></span>             | <span data-ttu-id="26d8a-455">同棲中</span><span class="sxs-lookup"><span data-stu-id="26d8a-455">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="26d8a-456">種類</span><span class="sxs-lookup"><span data-stu-id="26d8a-456">Gender</span></span>

<span data-ttu-id="26d8a-457">性別の指定は、Dayforce にマップされ、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-457">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="26d8a-458">次の表に、性別の指定がどのように Dayforce にマップされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-458">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="26d8a-459">Talent</span><span class="sxs-lookup"><span data-stu-id="26d8a-459">Talent</span></span>       | <span data-ttu-id="26d8a-460">Dayforce</span><span class="sxs-lookup"><span data-stu-id="26d8a-460">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="26d8a-461">男性</span><span class="sxs-lookup"><span data-stu-id="26d8a-461">Male</span></span>         | <span data-ttu-id="26d8a-462">男性</span><span class="sxs-lookup"><span data-stu-id="26d8a-462">Male</span></span>            |
| <span data-ttu-id="26d8a-463">女性</span><span class="sxs-lookup"><span data-stu-id="26d8a-463">Female</span></span>       | <span data-ttu-id="26d8a-464">女性</span><span class="sxs-lookup"><span data-stu-id="26d8a-464">Female</span></span>          |
| <span data-ttu-id="26d8a-465">不特定</span><span class="sxs-lookup"><span data-stu-id="26d8a-465">Non-specific</span></span> | <span data-ttu-id="26d8a-466">*サポートされていません*</span><span class="sxs-lookup"><span data-stu-id="26d8a-466">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="26d8a-467">所得コード</span><span class="sxs-lookup"><span data-stu-id="26d8a-467">Earning codes</span></span>

<span data-ttu-id="26d8a-468">所得コードは、作業者が受け取るすべての収益のタイプを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-468">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="26d8a-469">コードには、会計ルール、税法、レポート要件、およびグロスアップ能力など、所得に関連付けられている複数のパラメーターが含まれます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-469">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="26d8a-470">サポートされていない頻度を使用する場合、既定で**すべての支払**頻度が計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-470">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="26d8a-471">サポートされる頻度</span><span class="sxs-lookup"><span data-stu-id="26d8a-471">Supported frequencies</span></span>

- <span data-ttu-id="26d8a-472">All</span><span class="sxs-lookup"><span data-stu-id="26d8a-472">All</span></span>
- <span data-ttu-id="26d8a-473">すべての支払</span><span class="sxs-lookup"><span data-stu-id="26d8a-473">EVERYPAY</span></span>
- <span data-ttu-id="26d8a-474">各支払期間</span><span class="sxs-lookup"><span data-stu-id="26d8a-474">EACHPAYPERIOD</span></span>
- <span data-ttu-id="26d8a-475">他のすべての奇数支払</span><span class="sxs-lookup"><span data-stu-id="26d8a-475">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="26d8a-476">他のすべての偶数支払</span><span class="sxs-lookup"><span data-stu-id="26d8a-476">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="26d8a-477">1 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-477">1OFMTH</span></span>
- <span data-ttu-id="26d8a-478">月の最終日</span><span class="sxs-lookup"><span data-stu-id="26d8a-478">LASTOFMTH</span></span>
- <span data-ttu-id="26d8a-479">2 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-479">2OFMTH</span></span>
- <span data-ttu-id="26d8a-480">3 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-480">3OFMTH</span></span>
- <span data-ttu-id="26d8a-481">4 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-481">4OFMTH</span></span>
- <span data-ttu-id="26d8a-482">5 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-482">5OFMTH</span></span>
- <span data-ttu-id="26d8a-483">1 か月および 2 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-483">1N2OFMTH</span></span>
- <span data-ttu-id="26d8a-484">3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-484">3N4OFMTH</span></span>
- <span data-ttu-id="26d8a-485">1 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-485">1N3OFMTH</span></span>
- <span data-ttu-id="26d8a-486">1 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-486">1N4OFMTH</span></span>
- <span data-ttu-id="26d8a-487">2 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-487">2N3OFMTH</span></span>
- <span data-ttu-id="26d8a-488">2 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-488">2N4OFMTH</span></span>
- <span data-ttu-id="26d8a-489">1 か月、2 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-489">1N2N3OFMTH</span></span>
- <span data-ttu-id="26d8a-490">1 か月、2 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-490">1N2N4OFMTH</span></span>
- <span data-ttu-id="26d8a-491">1 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-491">1N3N4OFMTH</span></span>
- <span data-ttu-id="26d8a-492">2 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-492">2N3N4OFMTH</span></span>
- <span data-ttu-id="26d8a-493">1 か月、2 か月、3 か月および 4 か月 - 1 か月、2 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="26d8a-494">2 か月、3 か月、4 か月および 5 か月 - 2 か月、3 か月、4 か月および 5 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-494">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="26d8a-495">四半期の 1 - 四半期の 1</span><span class="sxs-lookup"><span data-stu-id="26d8a-495">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="26d8a-496">四半期の最終日 – 四半期の最終日</span><span class="sxs-lookup"><span data-stu-id="26d8a-496">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="26d8a-497">四半期の最後の月 – 四半期の最後の月</span><span class="sxs-lookup"><span data-stu-id="26d8a-497">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="26d8a-498">1 年 - 1 年</span><span class="sxs-lookup"><span data-stu-id="26d8a-498">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="26d8a-499">年の最終日 – 年の最終日</span><span class="sxs-lookup"><span data-stu-id="26d8a-499">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="26d8a-500">年の 11 月および 12 月 - 年の 11 月および 12 月</span><span class="sxs-lookup"><span data-stu-id="26d8a-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="26d8a-501">住所</span><span class="sxs-lookup"><span data-stu-id="26d8a-501">Addresses</span></span>

<span data-ttu-id="26d8a-502">特定の国または地域、都道府県、および市区郡 (自治体) の ID には、Dayforce および国内または地域内のプロバイダーが認識できる特定の形式が必要です。</span><span class="sxs-lookup"><span data-stu-id="26d8a-502">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="26d8a-503">市町村の形式は柔軟ですが、すべての市町村が都道府県と関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-503">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="26d8a-504">Talent</span><span class="sxs-lookup"><span data-stu-id="26d8a-504">Talent</span></span>          | <span data-ttu-id="26d8a-505">Dayforce</span><span class="sxs-lookup"><span data-stu-id="26d8a-505">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="26d8a-506">国/地域</span><span class="sxs-lookup"><span data-stu-id="26d8a-506">Country/Region</span></span>  | <span data-ttu-id="26d8a-507">国コード</span><span class="sxs-lookup"><span data-stu-id="26d8a-507">Country Code</span></span>          |
| <span data-ttu-id="26d8a-508">郵便番号</span><span class="sxs-lookup"><span data-stu-id="26d8a-508">Zip/Postal Code</span></span> | <span data-ttu-id="26d8a-509">郵便番号</span><span class="sxs-lookup"><span data-stu-id="26d8a-509">Postal Code</span></span>           |
| <span data-ttu-id="26d8a-510">行政単位 (区画)</span><span class="sxs-lookup"><span data-stu-id="26d8a-510">State</span></span>           | <span data-ttu-id="26d8a-511">都道府県コード</span><span class="sxs-lookup"><span data-stu-id="26d8a-511">State Code</span></span>            |
| <span data-ttu-id="26d8a-512">市町村</span><span class="sxs-lookup"><span data-stu-id="26d8a-512">City</span></span>            | <span data-ttu-id="26d8a-513">市町村</span><span class="sxs-lookup"><span data-stu-id="26d8a-513">City</span></span>                  |
| <span data-ttu-id="26d8a-514">郡</span><span class="sxs-lookup"><span data-stu-id="26d8a-514">County</span></span>          | <span data-ttu-id="26d8a-515">市区郡 (自治体)</span><span class="sxs-lookup"><span data-stu-id="26d8a-515">County (Municipality)</span></span> |
| <span data-ttu-id="26d8a-516">住所</span><span class="sxs-lookup"><span data-stu-id="26d8a-516">Street</span></span>          | <span data-ttu-id="26d8a-517">住所行 1</span><span class="sxs-lookup"><span data-stu-id="26d8a-517">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="26d8a-518">税地域</span><span class="sxs-lookup"><span data-stu-id="26d8a-518">Tax regions</span></span>

<span data-ttu-id="26d8a-519">税地域は、給与の生成時に適用する適切な税を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-519">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="26d8a-520">税地域は、場所の住所として Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-520">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="26d8a-521">既定の税地域は、作業者の有効な職位に関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-521">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="26d8a-522">税地域 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-522">Tax region (required)</span></span>
- <span data-ttu-id="26d8a-523">国/地域 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-523">Country/Region (required)</span></span>
- <span data-ttu-id="26d8a-524">都道府県 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-524">State (required)</span></span>
- <span data-ttu-id="26d8a-525">郡</span><span class="sxs-lookup"><span data-stu-id="26d8a-525">County</span></span> 
- <span data-ttu-id="26d8a-526">市町村 (必須)</span><span class="sxs-lookup"><span data-stu-id="26d8a-526">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="26d8a-527">メキシコの給与を生成するためのデータ コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="26d8a-527">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="26d8a-528">メキシコの従業員のために支払を生成している場合、次の要素をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-528">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="26d8a-529">職位に部門が必要です。</span><span class="sxs-lookup"><span data-stu-id="26d8a-529">Departments are required on positions.</span></span>
- <span data-ttu-id="26d8a-530">原価部門を財務分析コードとして設定し、既定の財務分析コード文字列の最初の要素とする必要があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-530">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="26d8a-531">ジョブ タイプ</span><span class="sxs-lookup"><span data-stu-id="26d8a-531">Job types</span></span>

<span data-ttu-id="26d8a-532">職務タイプは、類似した職務をカテゴリにグループ化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-532">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="26d8a-533">職務タイプは、メキシコでの給与を処理するために必要です。</span><span class="sxs-lookup"><span data-stu-id="26d8a-533">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="26d8a-534">職務タイプの例には、フルタイムおよびパートタイム、または給与払いおよび時給払いが含まれます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-534">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="26d8a-535">職務タイプは、従業員が時給払いかあるいは給与払いなのかを示す支払タイプとして Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-535">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="26d8a-536">次の職務タイプと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="26d8a-536">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="26d8a-537">ジョブ タイプ</span><span class="sxs-lookup"><span data-stu-id="26d8a-537">Job type</span></span>   | <span data-ttu-id="26d8a-538">説明</span><span class="sxs-lookup"><span data-stu-id="26d8a-538">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="26d8a-539">時間</span><span class="sxs-lookup"><span data-stu-id="26d8a-539">Hourly</span></span>     | <span data-ttu-id="26d8a-540">MX 時給払い</span><span class="sxs-lookup"><span data-stu-id="26d8a-540">MX Hourly</span></span>   |
| <span data-ttu-id="26d8a-541">給与払い</span><span class="sxs-lookup"><span data-stu-id="26d8a-541">Salaried</span></span>   | <span data-ttu-id="26d8a-542">MX 給与払い</span><span class="sxs-lookup"><span data-stu-id="26d8a-542">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="26d8a-543">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="26d8a-543">Position types</span></span> 

<span data-ttu-id="26d8a-544">職位がフルタイム、パートタイム、またはその他のタイプかどうかを説明するために職位タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-544">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="26d8a-545">職位タイプは、従業員がフルタイムかあるいはパートタイムなのかを示す支払クラスとして Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-545">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="26d8a-546">次の職位タイプと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="26d8a-546">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="26d8a-547">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="26d8a-547">Position type</span></span>   | <span data-ttu-id="26d8a-548">説明</span><span class="sxs-lookup"><span data-stu-id="26d8a-548">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="26d8a-549">フルタイム</span><span class="sxs-lookup"><span data-stu-id="26d8a-549">Full-time</span></span>       | <span data-ttu-id="26d8a-550">フルタイム従業員</span><span class="sxs-lookup"><span data-stu-id="26d8a-550">Full time employee</span></span> |
| <span data-ttu-id="26d8a-551">パートタイム</span><span class="sxs-lookup"><span data-stu-id="26d8a-551">Part-time</span></span>       | <span data-ttu-id="26d8a-552">パートタイム従業員</span><span class="sxs-lookup"><span data-stu-id="26d8a-552">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="26d8a-553">理由コード</span><span class="sxs-lookup"><span data-stu-id="26d8a-553">Reason codes</span></span>

<span data-ttu-id="26d8a-554">理由コードは、従業員のステータスに関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-554">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="26d8a-555">理由コードは、従業員の職位または雇用ステータスへの変更の理由を示すステータス理由として Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-555">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="26d8a-556">次の理由コードと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="26d8a-556">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="26d8a-557">理由コード</span><span class="sxs-lookup"><span data-stu-id="26d8a-557">Reason code</span></span>            | <span data-ttu-id="26d8a-558">説明</span><span class="sxs-lookup"><span data-stu-id="26d8a-558">Description</span></span>                    | <span data-ttu-id="26d8a-559">適用可能なシナリオ</span><span class="sxs-lookup"><span data-stu-id="26d8a-559">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="26d8a-560">支払前の除籍</span><span class="sxs-lookup"><span data-stu-id="26d8a-560">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="26d8a-561">最初の給与の前の除籍</span><span class="sxs-lookup"><span data-stu-id="26d8a-561">Departure before first payroll</span></span> | <span data-ttu-id="26d8a-562">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="26d8a-562">Terminate worker</span></span>     |
| <span data-ttu-id="26d8a-563">辞職</span><span class="sxs-lookup"><span data-stu-id="26d8a-563">RESIGNATION</span></span>            | <span data-ttu-id="26d8a-564">辞職</span><span class="sxs-lookup"><span data-stu-id="26d8a-564">Resignation</span></span>                    | <span data-ttu-id="26d8a-565">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="26d8a-565">Terminate worker</span></span>     |
| <span data-ttu-id="26d8a-566">年金</span><span class="sxs-lookup"><span data-stu-id="26d8a-566">PENSION</span></span>                | <span data-ttu-id="26d8a-567">年金</span><span class="sxs-lookup"><span data-stu-id="26d8a-567">Pension</span></span>                        | <span data-ttu-id="26d8a-568">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="26d8a-568">Terminate worker</span></span>     |
| <span data-ttu-id="26d8a-569">終了</span><span class="sxs-lookup"><span data-stu-id="26d8a-569">TERMINATION</span></span>            | <span data-ttu-id="26d8a-570">終了</span><span class="sxs-lookup"><span data-stu-id="26d8a-570">Termination</span></span>                    | <span data-ttu-id="26d8a-571">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="26d8a-571">Terminate worker</span></span>     |
| <span data-ttu-id="26d8a-572">定年退職</span><span class="sxs-lookup"><span data-stu-id="26d8a-572">RETIREMENT</span></span>             | <span data-ttu-id="26d8a-573">償却</span><span class="sxs-lookup"><span data-stu-id="26d8a-573">Retirement</span></span>                     | <span data-ttu-id="26d8a-574">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="26d8a-574">Terminate worker</span></span>     |
| <span data-ttu-id="26d8a-575">休暇者</span><span class="sxs-lookup"><span data-stu-id="26d8a-575">ABSENTEE</span></span>               | <span data-ttu-id="26d8a-576">休暇者</span><span class="sxs-lookup"><span data-stu-id="26d8a-576">Absentee</span></span>                       | <span data-ttu-id="26d8a-577">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="26d8a-577">Terminate worker</span></span>     |
| <span data-ttu-id="26d8a-578">その他</span><span class="sxs-lookup"><span data-stu-id="26d8a-578">OTHER</span></span>                  | <span data-ttu-id="26d8a-579">その他の理由</span><span class="sxs-lookup"><span data-stu-id="26d8a-579">Other Reasons</span></span>                  | <span data-ttu-id="26d8a-580">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="26d8a-580">Terminate worker</span></span>     |
| <span data-ttu-id="26d8a-581">休業</span><span class="sxs-lookup"><span data-stu-id="26d8a-581">CLOSURE</span></span>                | <span data-ttu-id="26d8a-582">業務休業</span><span class="sxs-lookup"><span data-stu-id="26d8a-582">Business Closure</span></span>               | <span data-ttu-id="26d8a-583">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="26d8a-583">Terminate worker</span></span>     |
| <span data-ttu-id="26d8a-584">死亡</span><span class="sxs-lookup"><span data-stu-id="26d8a-584">DEATH</span></span>                  | <span data-ttu-id="26d8a-585">死亡</span><span class="sxs-lookup"><span data-stu-id="26d8a-585">Death</span></span>                          | <span data-ttu-id="26d8a-586">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="26d8a-586">Terminate worker</span></span>     |
| <span data-ttu-id="26d8a-587">休暇</span><span class="sxs-lookup"><span data-stu-id="26d8a-587">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="26d8a-588">休暇</span><span class="sxs-lookup"><span data-stu-id="26d8a-588">Leave of Absence</span></span>               | <span data-ttu-id="26d8a-589">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="26d8a-589">Terminate worker</span></span>     |
| <span data-ttu-id="26d8a-590">契約の終了</span><span class="sxs-lookup"><span data-stu-id="26d8a-590">CONTRACTEND</span></span>            | <span data-ttu-id="26d8a-591">契約の終了</span><span class="sxs-lookup"><span data-stu-id="26d8a-591">End of Contract</span></span>                | <span data-ttu-id="26d8a-592">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="26d8a-592">Terminate worker</span></span>     |
| <span data-ttu-id="26d8a-593">給与の変更</span><span class="sxs-lookup"><span data-stu-id="26d8a-593">SALARYCHANGE</span></span>           | <span data-ttu-id="26d8a-594">給与の変更</span><span class="sxs-lookup"><span data-stu-id="26d8a-594">Change of Salary</span></span>               | <span data-ttu-id="26d8a-595">報酬</span><span class="sxs-lookup"><span data-stu-id="26d8a-595">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="26d8a-596">雇用条件</span><span class="sxs-lookup"><span data-stu-id="26d8a-596">Terms of employment</span></span>

<span data-ttu-id="26d8a-597">雇用条件は、雇用条件のカテゴリを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-597">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="26d8a-598">条件は、雇用インジケーターの値として Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-598">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="26d8a-599">次の雇用条件および説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="26d8a-599">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="26d8a-600">雇用条件</span><span class="sxs-lookup"><span data-stu-id="26d8a-600">Terms of employment</span></span>   | <span data-ttu-id="26d8a-601">説明</span><span class="sxs-lookup"><span data-stu-id="26d8a-601">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="26d8a-602">通常</span><span class="sxs-lookup"><span data-stu-id="26d8a-602">Regular</span></span>               | <span data-ttu-id="26d8a-603">通常</span><span class="sxs-lookup"><span data-stu-id="26d8a-603">Regular</span></span>     |
| <span data-ttu-id="26d8a-604">直接</span><span class="sxs-lookup"><span data-stu-id="26d8a-604">Direct</span></span>                | <span data-ttu-id="26d8a-605">直接</span><span class="sxs-lookup"><span data-stu-id="26d8a-605">Direct</span></span>      |
| <span data-ttu-id="26d8a-606">インターンシップ</span><span class="sxs-lookup"><span data-stu-id="26d8a-606">Internship</span></span>            | <span data-ttu-id="26d8a-607">インターンシップ</span><span class="sxs-lookup"><span data-stu-id="26d8a-607">Internship</span></span>  |
| <span data-ttu-id="26d8a-608">永続的</span><span class="sxs-lookup"><span data-stu-id="26d8a-608">Permanent</span></span>             | <span data-ttu-id="26d8a-609">永続的</span><span class="sxs-lookup"><span data-stu-id="26d8a-609">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="26d8a-610">配偶者の有無</span><span class="sxs-lookup"><span data-stu-id="26d8a-610">Marital status</span></span>

<span data-ttu-id="26d8a-611">配偶者有無の値は、Dayforce にマップされ、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-611">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="26d8a-612">次の表に、配偶者有無の値がどのように Dayforce にマップされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-612">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="26d8a-613">Talent</span><span class="sxs-lookup"><span data-stu-id="26d8a-613">Talent</span></span>                 | <span data-ttu-id="26d8a-614">Dayforce</span><span class="sxs-lookup"><span data-stu-id="26d8a-614">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="26d8a-615">既婚</span><span class="sxs-lookup"><span data-stu-id="26d8a-615">Married</span></span>                | <span data-ttu-id="26d8a-616">既婚</span><span class="sxs-lookup"><span data-stu-id="26d8a-616">Married</span></span>                   |
| <span data-ttu-id="26d8a-617">未婚</span><span class="sxs-lookup"><span data-stu-id="26d8a-617">Single</span></span>                 | <span data-ttu-id="26d8a-618">未婚</span><span class="sxs-lookup"><span data-stu-id="26d8a-618">Single</span></span>                    |
| <span data-ttu-id="26d8a-619">死別</span><span class="sxs-lookup"><span data-stu-id="26d8a-619">Widowed</span></span>                | <span data-ttu-id="26d8a-620">死別</span><span class="sxs-lookup"><span data-stu-id="26d8a-620">Widowed</span></span>                   |
| <span data-ttu-id="26d8a-621">離婚</span><span class="sxs-lookup"><span data-stu-id="26d8a-621">Divorced</span></span>               | <span data-ttu-id="26d8a-622">離婚</span><span class="sxs-lookup"><span data-stu-id="26d8a-622">Divorced</span></span>                  |
| <span data-ttu-id="26d8a-623">登録済パートナーシップ</span><span class="sxs-lookup"><span data-stu-id="26d8a-623">Registered Partnership</span></span> | <span data-ttu-id="26d8a-624">ドメスティック パートナーシップ</span><span class="sxs-lookup"><span data-stu-id="26d8a-624">Domestic Partnership</span></span>      |
| <span data-ttu-id="26d8a-625">None</span><span class="sxs-lookup"><span data-stu-id="26d8a-625">None</span></span>                   | <span data-ttu-id="26d8a-626">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="26d8a-626">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="26d8a-627">同棲中</span><span class="sxs-lookup"><span data-stu-id="26d8a-627">Cohabiting</span></span>             | <span data-ttu-id="26d8a-628">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="26d8a-628">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="26d8a-629">種類</span><span class="sxs-lookup"><span data-stu-id="26d8a-629">Gender</span></span>

<span data-ttu-id="26d8a-630">性別の指定は、Dayforce にマップされ、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-630">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="26d8a-631">次の表に、性別の指定がどのように Dayforce にマップされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-631">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="26d8a-632">Talent</span><span class="sxs-lookup"><span data-stu-id="26d8a-632">Talent</span></span>       | <span data-ttu-id="26d8a-633">Dayforce</span><span class="sxs-lookup"><span data-stu-id="26d8a-633">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="26d8a-634">男性</span><span class="sxs-lookup"><span data-stu-id="26d8a-634">Male</span></span>         | <span data-ttu-id="26d8a-635">男性</span><span class="sxs-lookup"><span data-stu-id="26d8a-635">Male</span></span>                      |
| <span data-ttu-id="26d8a-636">女性</span><span class="sxs-lookup"><span data-stu-id="26d8a-636">Female</span></span>       | <span data-ttu-id="26d8a-637">女性</span><span class="sxs-lookup"><span data-stu-id="26d8a-637">Female</span></span>                    |
| <span data-ttu-id="26d8a-638">不特定</span><span class="sxs-lookup"><span data-stu-id="26d8a-638">Non-specific</span></span> | <span data-ttu-id="26d8a-639">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="26d8a-639">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="26d8a-640">支払方法</span><span class="sxs-lookup"><span data-stu-id="26d8a-640">Payment method</span></span>

<span data-ttu-id="26d8a-641">支払方法は、従業員に支払が行われる方法を従業員および会社に説明します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-641">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="26d8a-642">支払方法は、Dayforce にマップされ、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-642">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="26d8a-643">次の表に、支払方法がどのように Dayforce にマップされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-643">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="26d8a-644">Talent</span><span class="sxs-lookup"><span data-stu-id="26d8a-644">Talent</span></span>             | <span data-ttu-id="26d8a-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="26d8a-645">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="26d8a-646">現金</span><span class="sxs-lookup"><span data-stu-id="26d8a-646">Cash</span></span>               | <span data-ttu-id="26d8a-647">現金</span><span class="sxs-lookup"><span data-stu-id="26d8a-647">Cash</span></span>                      |
| <span data-ttu-id="26d8a-648">電子支払</span><span class="sxs-lookup"><span data-stu-id="26d8a-648">Electronic Payment</span></span> | <span data-ttu-id="26d8a-649">転送</span><span class="sxs-lookup"><span data-stu-id="26d8a-649">Transfer</span></span>                  |
| <span data-ttu-id="26d8a-650">確認</span><span class="sxs-lookup"><span data-stu-id="26d8a-650">Check</span></span>              | <span data-ttu-id="26d8a-651">小切手</span><span class="sxs-lookup"><span data-stu-id="26d8a-651">Cheque</span></span>                    |
| <span data-ttu-id="26d8a-652">銀行為替手形</span><span class="sxs-lookup"><span data-stu-id="26d8a-652">Bank Draft</span></span>         | <span data-ttu-id="26d8a-653">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="26d8a-653">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="26d8a-654">外</span><span class="sxs-lookup"><span data-stu-id="26d8a-654">Other</span></span>              | <span data-ttu-id="26d8a-655">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="26d8a-655">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="26d8a-656">銀行口座の種類</span><span class="sxs-lookup"><span data-stu-id="26d8a-656">Bank account type</span></span>

<span data-ttu-id="26d8a-657">銀行口座の種類は、従業員への電子支払のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-657">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="26d8a-658">銀行口座の種類は、振替口座情報として Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-658">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="26d8a-659">銀行口座の種類は、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-659">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="26d8a-660">Talent</span><span class="sxs-lookup"><span data-stu-id="26d8a-660">Talent</span></span>            | <span data-ttu-id="26d8a-661">Dayforce</span><span class="sxs-lookup"><span data-stu-id="26d8a-661">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="26d8a-662">当座預金口座</span><span class="sxs-lookup"><span data-stu-id="26d8a-662">Checking Account</span></span>  | <span data-ttu-id="26d8a-663">当座預金口座</span><span class="sxs-lookup"><span data-stu-id="26d8a-663">CheckingAccount</span></span>           |
| <span data-ttu-id="26d8a-664">給与口座</span><span class="sxs-lookup"><span data-stu-id="26d8a-664">Payroll Account</span></span>   | <span data-ttu-id="26d8a-665">給与口座</span><span class="sxs-lookup"><span data-stu-id="26d8a-665">PayrollAccount</span></span>            |
| <span data-ttu-id="26d8a-666">普通預金口座</span><span class="sxs-lookup"><span data-stu-id="26d8a-666">Savings Account</span></span>   | <span data-ttu-id="26d8a-667">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="26d8a-667">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="26d8a-668">BankGirot 口座</span><span class="sxs-lookup"><span data-stu-id="26d8a-668">BankGirot account</span></span> | <span data-ttu-id="26d8a-669">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="26d8a-669">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="26d8a-670">PlusGirot 口座</span><span class="sxs-lookup"><span data-stu-id="26d8a-670">PlusGirot account</span></span> | <span data-ttu-id="26d8a-671">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="26d8a-671">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="26d8a-672">所得コード</span><span class="sxs-lookup"><span data-stu-id="26d8a-672">Earning codes</span></span>

<span data-ttu-id="26d8a-673">所得コードは、作業者が受け取るすべての収益のタイプを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="26d8a-673">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="26d8a-674">コードには、会計ルール、税法、レポート要件、およびグロスアップ能力など、所得に関連付けられている複数のパラメーターが含まれます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-674">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="26d8a-675">サポートされていない頻度を使用する場合、既定で**すべての支払**頻度が計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-675">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="26d8a-676">サポートされる頻度</span><span class="sxs-lookup"><span data-stu-id="26d8a-676">Supported frequencies</span></span>

- <span data-ttu-id="26d8a-677">All</span><span class="sxs-lookup"><span data-stu-id="26d8a-677">All</span></span>
- <span data-ttu-id="26d8a-678">すべての支払</span><span class="sxs-lookup"><span data-stu-id="26d8a-678">EVERYPAY</span></span>
- <span data-ttu-id="26d8a-679">各支払期間</span><span class="sxs-lookup"><span data-stu-id="26d8a-679">EACHPAYPERIOD</span></span>
- <span data-ttu-id="26d8a-680">他のすべての奇数支払</span><span class="sxs-lookup"><span data-stu-id="26d8a-680">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="26d8a-681">他のすべての偶数支払</span><span class="sxs-lookup"><span data-stu-id="26d8a-681">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="26d8a-682">1 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-682">1OFMTH</span></span>
- <span data-ttu-id="26d8a-683">月の最終日</span><span class="sxs-lookup"><span data-stu-id="26d8a-683">LASTOFMTH</span></span>
- <span data-ttu-id="26d8a-684">2 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-684">2OFMTH</span></span>
- <span data-ttu-id="26d8a-685">3 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-685">3OFMTH</span></span>
- <span data-ttu-id="26d8a-686">4 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-686">4OFMTH</span></span>
- <span data-ttu-id="26d8a-687">5 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-687">5OFMTH</span></span>
- <span data-ttu-id="26d8a-688">1 か月および 2 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-688">1N2OFMTH</span></span>
- <span data-ttu-id="26d8a-689">3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-689">3N4OFMTH</span></span>
- <span data-ttu-id="26d8a-690">1 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-690">1N3OFMTH</span></span>
- <span data-ttu-id="26d8a-691">1 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-691">1N4OFMTH</span></span>
- <span data-ttu-id="26d8a-692">2 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-692">2N3OFMTH</span></span>
- <span data-ttu-id="26d8a-693">2 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-693">2N4OFMTH</span></span>
- <span data-ttu-id="26d8a-694">1 か月、2 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-694">1N2N3OFMTH</span></span>
- <span data-ttu-id="26d8a-695">1 か月、2 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-695">1N2N4OFMTH</span></span>
- <span data-ttu-id="26d8a-696">1 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-696">1N3N4OFMTH</span></span>
- <span data-ttu-id="26d8a-697">2 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-697">2N3N4OFMTH</span></span>
- <span data-ttu-id="26d8a-698">1 か月、2 か月、3 か月および 4 か月 - 1 か月、2 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="26d8a-699">2 か月、3 か月、4 か月および 5 か月 - 2 か月、3 か月、4 か月および 5 か月</span><span class="sxs-lookup"><span data-stu-id="26d8a-699">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="26d8a-700">四半期の 1 - 四半期の 1</span><span class="sxs-lookup"><span data-stu-id="26d8a-700">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="26d8a-701">四半期の最終日 – 四半期の最終日</span><span class="sxs-lookup"><span data-stu-id="26d8a-701">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="26d8a-702">四半期の最後の月 – 四半期の最後の月</span><span class="sxs-lookup"><span data-stu-id="26d8a-702">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="26d8a-703">1 年 - 1 年</span><span class="sxs-lookup"><span data-stu-id="26d8a-703">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="26d8a-704">年の最終日 – 年の最終日</span><span class="sxs-lookup"><span data-stu-id="26d8a-704">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="26d8a-705">年の 11 月および 12 月 - 年の 11 月および 12 月</span><span class="sxs-lookup"><span data-stu-id="26d8a-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="26d8a-706">住所</span><span class="sxs-lookup"><span data-stu-id="26d8a-706">Addresses</span></span>

<span data-ttu-id="26d8a-707">特定の国または地域、都道府県、および市区郡 (自治体) の ID には、Dayforce および国内または地域内のプロバイダーが認識できる特定の形式が必要です。</span><span class="sxs-lookup"><span data-stu-id="26d8a-707">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="26d8a-708">市町村の形式は柔軟ですが、すべての市町村が都道府県と関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="26d8a-708">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="26d8a-709">Talent</span><span class="sxs-lookup"><span data-stu-id="26d8a-709">Talent</span></span>              | <span data-ttu-id="26d8a-710">Dayforce</span><span class="sxs-lookup"><span data-stu-id="26d8a-710">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="26d8a-711">国/地域</span><span class="sxs-lookup"><span data-stu-id="26d8a-711">Country/Region</span></span>      | <span data-ttu-id="26d8a-712">国コード</span><span class="sxs-lookup"><span data-stu-id="26d8a-712">Country Code</span></span>          |
| <span data-ttu-id="26d8a-713">郵便番号</span><span class="sxs-lookup"><span data-stu-id="26d8a-713">Zip/Postal Code</span></span>     | <span data-ttu-id="26d8a-714">郵便番号</span><span class="sxs-lookup"><span data-stu-id="26d8a-714">Postal Code</span></span>           |
| <span data-ttu-id="26d8a-715">行政単位 (区画)</span><span class="sxs-lookup"><span data-stu-id="26d8a-715">State</span></span>               | <span data-ttu-id="26d8a-716">都道府県コード</span><span class="sxs-lookup"><span data-stu-id="26d8a-716">State Code</span></span>            |
| <span data-ttu-id="26d8a-717">市町村</span><span class="sxs-lookup"><span data-stu-id="26d8a-717">City</span></span>                | <span data-ttu-id="26d8a-718">市町村</span><span class="sxs-lookup"><span data-stu-id="26d8a-718">City</span></span>                  |
| <span data-ttu-id="26d8a-719">郡</span><span class="sxs-lookup"><span data-stu-id="26d8a-719">County</span></span>              | <span data-ttu-id="26d8a-720">市区郡 (自治体)</span><span class="sxs-lookup"><span data-stu-id="26d8a-720">County (Municipality)</span></span> |
| <span data-ttu-id="26d8a-721">住所</span><span class="sxs-lookup"><span data-stu-id="26d8a-721">Street</span></span>              | <span data-ttu-id="26d8a-722">住所行 1</span><span class="sxs-lookup"><span data-stu-id="26d8a-722">Address Line 1</span></span>        |
| <span data-ttu-id="26d8a-723">番地</span><span class="sxs-lookup"><span data-stu-id="26d8a-723">Street Number</span></span>       | <span data-ttu-id="26d8a-724">住所行 2</span><span class="sxs-lookup"><span data-stu-id="26d8a-724">Address Line 2</span></span>        |
| <span data-ttu-id="26d8a-725">建物名</span><span class="sxs-lookup"><span data-stu-id="26d8a-725">Building Complement</span></span> | <span data-ttu-id="26d8a-726">住所行 5</span><span class="sxs-lookup"><span data-stu-id="26d8a-726">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="26d8a-727">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="26d8a-727">Passport number</span></span>

<span data-ttu-id="26d8a-728">従業員は、パスポート情報を申告できます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-728">Employees can declare passport information.</span></span> <span data-ttu-id="26d8a-729">この情報は、**パスポート** ID タイプになり、従業員のメキシコ固有の情報の一部として Dayforce に統合されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-729">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="26d8a-730">ID タイプ = "Passport"</span><span class="sxs-lookup"><span data-stu-id="26d8a-730">Identification Type = "Passport"</span></span>
- <span data-ttu-id="26d8a-731">発行日付</span><span class="sxs-lookup"><span data-stu-id="26d8a-731">Issued Date</span></span>
- <span data-ttu-id="26d8a-732">有効期限</span><span class="sxs-lookup"><span data-stu-id="26d8a-732">Expiration Date</span></span>

<span data-ttu-id="26d8a-733">従業員は、**パスポート** ID タイプの複数の ID 番号を申告できます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-733">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="26d8a-734">ただし、現在の有効なパスポート入力のみが Dayforce に統合されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-734">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="26d8a-735">すべてのパスポート入力が期限切れの場合、最後に発行されたパスポートが Dayforce に統合されます。</span><span class="sxs-lookup"><span data-stu-id="26d8a-735">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
