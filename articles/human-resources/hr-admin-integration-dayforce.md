---
title: Dayforce との統合を構成する
description: Microsoft Dynamics 365 Human Resources および Ceridian Dayforce 間での統合は、この記事で説明するいくつかの構成手順に依存します。 支払の実行を処理する前に、Human Resources および Dayforce の両方で、統合を構成する必要があります。
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 044a2d2f632b2c98ce94b6d61c2582a861640b68
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113252"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="be3b9-104">Dayforce との統合を構成する</span><span class="sxs-lookup"><span data-stu-id="be3b9-104">Configure integration with Dayforce</span></span>

<span data-ttu-id="be3b9-105">Microsoft Dynamics 365 Human Resources および Ceridian Dayforce 間での統合は、この記事で説明するいくつかの構成手順に依存します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="be3b9-106">支払の実行を処理する前に、Human Resources および Dayforce の両方で、統合を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="be3b9-107">支払の実行を完了するため Dayforce などのサービスを使用する場合、Human Resources 内の統合を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="be3b9-108">統合には Human Resources からの固有のデータが必要です。</span><span class="sxs-lookup"><span data-stu-id="be3b9-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="be3b9-109">したがって、Dayforce にマップされているデータが、統合をサポートする方法で Human Resources 内で構成されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="be3b9-110">統合は次の広範なデータ カテゴリを使用します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="be3b9-111">人事管理データ</span><span class="sxs-lookup"><span data-stu-id="be3b9-111">Human resources data</span></span>
- <span data-ttu-id="be3b9-112">報酬データ</span><span class="sxs-lookup"><span data-stu-id="be3b9-112">Compensation data</span></span>
- <span data-ttu-id="be3b9-113">支払サイクル、支払期間、および所得コードなどの給与データ</span><span class="sxs-lookup"><span data-stu-id="be3b9-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="be3b9-114">作業者データ</span><span class="sxs-lookup"><span data-stu-id="be3b9-114">Worker data</span></span>

<span data-ttu-id="be3b9-115">この記事では、統合を有効にするために従う必要がある手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="be3b9-116">統合に必要なデータの種類およびコンフィギュレーションの詳細についても説明します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="be3b9-117">統合の有効化</span><span class="sxs-lookup"><span data-stu-id="be3b9-117">Enable the integration</span></span>

<span data-ttu-id="be3b9-118">Human Resources 内で統合を有効にし、Dayforce に接続する構成情報を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="be3b9-119">生成される一般会計トランザクションを Microsoft Dynamics 365 Finance にインポートしたい場合、Microsoft Azure ストレージ アカウントを設定し、Finance 内で、Azure Storage の接続文字列を入力する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="be3b9-120">Human Resources 内で統合を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="be3b9-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="be3b9-121">**システム管理** ページで、**統合コンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="be3b9-122">セキュリティで保護された FTP (File Transfer Protocol) のエンドポイント、およびセキュリティで保護された FTP フォルダー パスを入力します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="be3b9-123">セキュリティで保護された FTP エンドポイントおよびフォルダー パスにアクセスするユーザーのユーザー名とパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="be3b9-124">必要に応じて接続をテストし、**給与統合の有効化** のオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="be3b9-125">統合が有効な場合、データのエクスポート パッケージおよびファイルが作成され、頻度が設定されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="be3b9-126">必要に応じて、この頻度を変更できます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="be3b9-127">Azure Storage アカウント および Azure Storage の接続文字列の詳細については、次の Azure の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be3b9-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="be3b9-128">Azure ストレージ アカウントについて</span><span class="sxs-lookup"><span data-stu-id="be3b9-128">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="be3b9-129">Azure ストレージの接続文字列のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="be3b9-129">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="be3b9-130">給与統合が有効になっている場合の技術詳細</span><span class="sxs-lookup"><span data-stu-id="be3b9-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="be3b9-131">給与統合を有効にすることには、次の 2 つの主な効果があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="be3b9-132">「給与統合エクスポート」という名前のデータ エクスポート プロジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="be3b9-133">このプロジェクトには、給与統合に必要なエンティティとフィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="be3b9-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="be3b9-134">プロジェクトを確認するには、**システム管理** に移動し、**データ管理** タイルを選択して、プロジェクトの一覧からデータ プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="be3b9-135">このバッチ ジョブは、データ エクスポート プロジェクトを実行し、結果のデータ パッケージを暗号化し、**統合コンフィギュレーション** 画面でコンフィギュレーションされた SFTP エンドポイントにデータ パッケージ ファイルを転送します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="be3b9-136">SFTP エンドポイントに転送されるデータ パッケージは、そのパッケージに固有のキーを使用して暗号化されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="be3b9-137">キーは、Ceridian によってのみアクセス可能な Azure Key Vault にあります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="be3b9-138">データ パッケージの内容を復号化して確認することはできません。</span><span class="sxs-lookup"><span data-stu-id="be3b9-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="be3b9-139">データ パッケージの内容を確認する必要がある場合は、"給与統合エクスポート" データ プロジェクトを手動でエクスポートし、ダウンロードしてから、それを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="be3b9-140">手動エクスポートでは、暗号化が適用されないか、またはパッケージが転送されません。</span><span class="sxs-lookup"><span data-stu-id="be3b9-140">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="be3b9-141">データのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="be3b9-141">Configure your data</span></span> 

<span data-ttu-id="be3b9-142">給与を処理するには、Human Resources で人事管理のデータを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-142">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="be3b9-143">職務と職位などの組織データを、給付金および報酬情報と共に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-143">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="be3b9-144">この情報は、雇用、支払、および従業員の給与を生成するために必要な控除情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-144">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="be3b9-145">人事管理データ</span><span class="sxs-lookup"><span data-stu-id="be3b9-145">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="be3b9-146">福利厚生</span><span class="sxs-lookup"><span data-stu-id="be3b9-146">Benefits</span></span> 

<span data-ttu-id="be3b9-147">人事管理は、給付金、控除、および組織が作業者に対して提供または処理する作業者の報酬プランを設定および管理するツールを提供します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-147">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="be3b9-148">給付金を作成する場合、Dayforce で使用される次のデータとコンフィギュレーションに留意してください。</span><span class="sxs-lookup"><span data-stu-id="be3b9-148">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="be3b9-149">福利厚生計画</span><span class="sxs-lookup"><span data-stu-id="be3b9-149">Benefit plans</span></span>

- <span data-ttu-id="be3b9-150">計画 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-150">Plan (required)</span></span>
- <span data-ttu-id="be3b9-151">種類 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-151">Type (required)</span></span>
- <span data-ttu-id="be3b9-152">給与の影響 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-152">Payroll impact (required)</span></span>
- <span data-ttu-id="be3b9-153">未払金の回収</span><span class="sxs-lookup"><span data-stu-id="be3b9-153">Recover arrears</span></span>
- <span data-ttu-id="be3b9-154">控除方式</span><span class="sxs-lookup"><span data-stu-id="be3b9-154">Deduction method</span></span>
- <span data-ttu-id="be3b9-155">控除の優先順位</span><span class="sxs-lookup"><span data-stu-id="be3b9-155">Deduction priority</span></span>
- <span data-ttu-id="be3b9-156">制限の期間</span><span class="sxs-lookup"><span data-stu-id="be3b9-156">Limit period</span></span>
- <span data-ttu-id="be3b9-157">限度金額</span><span class="sxs-lookup"><span data-stu-id="be3b9-157">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="be3b9-158">福利厚生</span><span class="sxs-lookup"><span data-stu-id="be3b9-158">Benefits</span></span>

- <span data-ttu-id="be3b9-159">計画 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-159">Plan (required)</span></span>
- <span data-ttu-id="be3b9-160">種類 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-160">Type (required)</span></span>
- <span data-ttu-id="be3b9-161">オプション (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-161">Option (required)</span></span>
- <span data-ttu-id="be3b9-162">給付金 ID (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-162">Benefit ID (required)</span></span>
- <span data-ttu-id="be3b9-163">頻度</span><span class="sxs-lookup"><span data-stu-id="be3b9-163">Frequency</span></span>
- <span data-ttu-id="be3b9-164">基準</span><span class="sxs-lookup"><span data-stu-id="be3b9-164">Basis</span></span>
- <span data-ttu-id="be3b9-165">金額またはレート</span><span class="sxs-lookup"><span data-stu-id="be3b9-165">Amount or rate</span></span>
- <span data-ttu-id="be3b9-166">所得コード</span><span class="sxs-lookup"><span data-stu-id="be3b9-166">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="be3b9-167">サポートされる頻度</span><span class="sxs-lookup"><span data-stu-id="be3b9-167">Supported frequencies</span></span> 

- <span data-ttu-id="be3b9-168">毎週</span><span class="sxs-lookup"><span data-stu-id="be3b9-168">Weekly</span></span>
- <span data-ttu-id="be3b9-169">隔週</span><span class="sxs-lookup"><span data-stu-id="be3b9-169">Bi-weekly</span></span>
- <span data-ttu-id="be3b9-170">半月ごと</span><span class="sxs-lookup"><span data-stu-id="be3b9-170">Semi-monthly</span></span>
- <span data-ttu-id="be3b9-171">月 1 回</span><span class="sxs-lookup"><span data-stu-id="be3b9-171">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="be3b9-172">サポートされる基準</span><span class="sxs-lookup"><span data-stu-id="be3b9-172">Supported bases</span></span> 

- <span data-ttu-id="be3b9-173">固定金額</span><span class="sxs-lookup"><span data-stu-id="be3b9-173">Fixed amount</span></span>
- <span data-ttu-id="be3b9-174">所得の割合</span><span class="sxs-lookup"><span data-stu-id="be3b9-174">Percent of earnings</span></span>
- <span data-ttu-id="be3b9-175">生産時間</span><span class="sxs-lookup"><span data-stu-id="be3b9-175">Productive hours</span></span>

<span data-ttu-id="be3b9-176">Dayforce は、給付金の計画で定義される給与影響に基づいて次の控除を作成します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-176">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="be3b9-177">Human Resources における選択</span><span class="sxs-lookup"><span data-stu-id="be3b9-177">Selection in Human Resources</span></span>        | <span data-ttu-id="be3b9-178">Dayforce での結果</span><span class="sxs-lookup"><span data-stu-id="be3b9-178">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="be3b9-179">なし</span><span class="sxs-lookup"><span data-stu-id="be3b9-179">None</span></span>                       | <span data-ttu-id="be3b9-180">控除は作成されません。</span><span class="sxs-lookup"><span data-stu-id="be3b9-180">No deduction is created.</span></span>                      |
| <span data-ttu-id="be3b9-181">控除のみ</span><span class="sxs-lookup"><span data-stu-id="be3b9-181">Deduction only</span></span>             | <span data-ttu-id="be3b9-182">従業員控除が作成されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-182">An employee deduction is created.</span></span>             |
| <span data-ttu-id="be3b9-183">貢献度のみ</span><span class="sxs-lookup"><span data-stu-id="be3b9-183">Contribution only</span></span>          | <span data-ttu-id="be3b9-184">雇用主控除が作成されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-184">An employer deduction is created.</span></span>             |
| <span data-ttu-id="be3b9-185">控除と貢献度</span><span class="sxs-lookup"><span data-stu-id="be3b9-185">Deduction and contribution</span></span> | <span data-ttu-id="be3b9-186">従業員および雇用主の控除が作成されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-186">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="be3b9-187">給付金プログラムを定義し、管理する方法の詳細については、次の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be3b9-187">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="be3b9-188">従業員手当プログラムの提供</span><span class="sxs-lookup"><span data-stu-id="be3b9-188">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="be3b9-189">新しい給付金の作成</span><span class="sxs-lookup"><span data-stu-id="be3b9-189">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="be3b9-190">給付金の適格性ルールおよびポリシーの定義</span><span class="sxs-lookup"><span data-stu-id="be3b9-190">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="be3b9-191">作業者の福利厚生の登録および削除</span><span class="sxs-lookup"><span data-stu-id="be3b9-191">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="be3b9-192">報酬</span><span class="sxs-lookup"><span data-stu-id="be3b9-192">Compensation</span></span> 

<span data-ttu-id="be3b9-193">基準賃金と報奨を管理するには、報酬管理を使用します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-193">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="be3b9-194">従業員の固定基準賃金および昇給は固定報酬プランで管理されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-194">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="be3b9-195">インセンティブ支払 (賞与の支払、業績報奨、ストック オプション、付与など) の支払および一時報奨は変動報酬プランで管理します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-195">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="be3b9-196">Dayforce は、報酬情報を使用して、従業員の時間または年間レートを計算します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-196">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="be3b9-197">固定報酬プランと支払レートの換算が必要です。</span><span class="sxs-lookup"><span data-stu-id="be3b9-197">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="be3b9-198">従業員は固定報酬プランに関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-198">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="be3b9-199">報酬プランの詳細については、次の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be3b9-199">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="be3b9-200">固定報酬プランの作成</span><span class="sxs-lookup"><span data-stu-id="be3b9-200">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="be3b9-201">変動報酬プランの作成</span><span class="sxs-lookup"><span data-stu-id="be3b9-201">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="be3b9-202">給与/報酬構造および計画の作成</span><span class="sxs-lookup"><span data-stu-id="be3b9-202">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="be3b9-203">報酬の処理</span><span class="sxs-lookup"><span data-stu-id="be3b9-203">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="be3b9-204">報酬プロセスの定義と結果の計算</span><span class="sxs-lookup"><span data-stu-id="be3b9-204">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="be3b9-205">固定報酬プランへの従業員の登録</span><span class="sxs-lookup"><span data-stu-id="be3b9-205">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="be3b9-206">変動報酬プランへの従業員の登録</span><span class="sxs-lookup"><span data-stu-id="be3b9-206">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="be3b9-207">職務</span><span class="sxs-lookup"><span data-stu-id="be3b9-207">Jobs</span></span> 

<span data-ttu-id="be3b9-208">職務とは、職務を遂行する担当者に必要なタスクと職責の集合です。</span><span class="sxs-lookup"><span data-stu-id="be3b9-208">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="be3b9-209">詳細については、次の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be3b9-209">For more information, see the following articles:</span></span>

- [<span data-ttu-id="be3b9-210">職務のコンポーネントの設定</span><span class="sxs-lookup"><span data-stu-id="be3b9-210">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="be3b9-211">新しい職務の定義</span><span class="sxs-lookup"><span data-stu-id="be3b9-211">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="be3b9-212">職位</span><span class="sxs-lookup"><span data-stu-id="be3b9-212">Positions</span></span>

<span data-ttu-id="be3b9-213">職位は、職務の個々のインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="be3b9-213">A position is an individual instance of a job.</span></span> <span data-ttu-id="be3b9-214">たとえば、「販売マネージャー (東部)」という職位は、「販売マネージャー」という職務に関連付けられている職位の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="be3b9-214">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="be3b9-215">職位は、部門内に存在します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-215">A position exists in a department.</span></span> <span data-ttu-id="be3b9-216">1 人の作業者は 1 つの職位にのみ関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-216">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="be3b9-217">職位を設定する場合、次のデータとコンフィギュレーションに注意してください。</span><span class="sxs-lookup"><span data-stu-id="be3b9-217">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="be3b9-218">職位 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-218">Position (required)</span></span>
- <span data-ttu-id="be3b9-219">説明 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-219">Description (required)</span></span>
- <span data-ttu-id="be3b9-220">職務 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-220">Job (required)</span></span>
- <span data-ttu-id="be3b9-221">部門 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-221">Department (required)</span></span>
- <span data-ttu-id="be3b9-222">職位タイプ (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-222">Position type (required)</span></span>
- <span data-ttu-id="be3b9-223">フルタイム相当</span><span class="sxs-lookup"><span data-stu-id="be3b9-223">Full-time equivalent</span></span>
- <span data-ttu-id="be3b9-224">年間基本勤務時間 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-224">Annual regular hours (required)</span></span>
- <span data-ttu-id="be3b9-225">法人による支払 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-225">Paid by legal entity (required)</span></span>
- <span data-ttu-id="be3b9-226">支払サイクル (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-226">Pay cycle (required)</span></span>
- <span data-ttu-id="be3b9-227">既定の財務分析コード – 原価部門 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-227">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="be3b9-228">作業者割り当て – 作業者、割り当ての開始、割り当ての終了、理由コード</span><span class="sxs-lookup"><span data-stu-id="be3b9-228">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="be3b9-229">同じ部門の複数の職位が同じジョブに関連付けられている場合、Dayforce で 1 つの職位に連結します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-229">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="be3b9-230">詳細については、次の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be3b9-230">For more information, see the following articles:</span></span>

- [<span data-ttu-id="be3b9-231">部門、職務、職位を使用した従業員の編成</span><span class="sxs-lookup"><span data-stu-id="be3b9-231">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="be3b9-232">職位の設定</span><span class="sxs-lookup"><span data-stu-id="be3b9-232">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="be3b9-233">部門</span><span class="sxs-lookup"><span data-stu-id="be3b9-233">Departments</span></span>

<span data-ttu-id="be3b9-234">部門は、組織のカテゴリまたは機能領域を表す作業単位です。</span><span class="sxs-lookup"><span data-stu-id="be3b9-234">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="be3b9-235">部門は、販売、会計、または人事管理など、組織内の特定の領域を担当します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-235">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="be3b9-236">機能領域の報告に部門を使用できます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-236">You can use departments to report on functional areas.</span></span> <span data-ttu-id="be3b9-237">部門は損益の職責を持つ場合があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-237">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="be3b9-238">詳細については、次の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be3b9-238">For more information, see the following articles:</span></span>

- [<span data-ttu-id="be3b9-239">部門の作成と部門階層への関連付け</span><span class="sxs-lookup"><span data-stu-id="be3b9-239">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="be3b9-240">新しい部門の定義</span><span class="sxs-lookup"><span data-stu-id="be3b9-240">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="be3b9-241">支払サイクルと支払期間</span><span class="sxs-lookup"><span data-stu-id="be3b9-241">Pay cycles and pay periods</span></span>

<span data-ttu-id="be3b9-242">給与計算頻度および作業者が支払を受ける特定の日は、支払サイクルによって決まります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-242">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="be3b9-243">たとえば、支払サイクルが月単位で、その月の最後の日に従業員に支払われる場合があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-243">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="be3b9-244">または、支払サイクルが週単位で、支払期間終了日の次の火曜日に支払われる場合もあります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-244">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="be3b9-245">支払サイクルは、それらの職位にある作業者にいつ支払われるかを制御するために、職位に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-245">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="be3b9-246">支払サイクルを作成した後、各サイクルごとに支払期間を生成できます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-246">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="be3b9-247">各支払期間には、入力した情報に基づく既定の支払期日が含まれます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-247">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="be3b9-248">ただし、支払期日が休日になる場合などの例外を許可するため、支払期間の既定の支払期日を変更できます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-248">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="be3b9-249">次の情報は、Dayforce で使用されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-249">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="be3b9-250">支払サイクル (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-250">Pay cycle (required)</span></span>
- <span data-ttu-id="be3b9-251">支払サイクル頻度 (頻度)</span><span class="sxs-lookup"><span data-stu-id="be3b9-251">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="be3b9-252">期間開始日 (最初の支払期間は必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-252">Period start date (first pay period required)</span></span>
- <span data-ttu-id="be3b9-253">既定の支払期日 (最初の支払期間は必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-253">Default payment date (first pay period required)</span></span>

<span data-ttu-id="be3b9-254">この情報は、支払グループとして Dayforce に統合され、各支払サイクルごとに国または地域で区切られます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-254">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="be3b9-255">統合の前に、少なくとも 1 つの支払期間を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-255">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="be3b9-256">Dayforce は、最初の支払期日の開始日および Human Resources で設定された既定の支払期日に基づいて、支払グループのカレンダーと支払期日を生成します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-256">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="be3b9-257">所得コード</span><span class="sxs-lookup"><span data-stu-id="be3b9-257">Earning codes</span></span>

<span data-ttu-id="be3b9-258">所得コードは、作業者が受け取るすべての収益のタイプを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-258">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="be3b9-259">コードには、会計ルール、税法、レポート要件、およびグロスアップ能力など、所得に関連付けられているさまざまなパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-259">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="be3b9-260">次の情報は、Dayforce で使用されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-260">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="be3b9-261">所得コード (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-261">Earning Code (required)</span></span>
- <span data-ttu-id="be3b9-262">説明</span><span class="sxs-lookup"><span data-stu-id="be3b9-262">Description</span></span>
- <span data-ttu-id="be3b9-263">計量単位</span><span class="sxs-lookup"><span data-stu-id="be3b9-263">Unit of measure</span></span>
- <span data-ttu-id="be3b9-264">生産</span><span class="sxs-lookup"><span data-stu-id="be3b9-264">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="be3b9-265">作業者データ</span><span class="sxs-lookup"><span data-stu-id="be3b9-265">Worker data</span></span>

<span data-ttu-id="be3b9-266">人事管理と給与システムにとって、所有しているさまざまなタイプの作業者のレコードは重要です。</span><span class="sxs-lookup"><span data-stu-id="be3b9-266">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="be3b9-267">入力された情報を使用して、作業者と個人情報を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-267">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="be3b9-268">作業者には次の情報を管理できます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-268">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="be3b9-269">**基本** – 連絡先情報、人口学的情報、識別情報、家族情報、兵役の状態、海外在住情報、自宅、緊急連絡先など、作業者に関する基本的な情報を管理します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-269">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="be3b9-270">**雇用** – 法人や組織への所属、職位割り当て、開始日と終了日、業務適性、雇用条件、年金、休暇、再配置情報など、作業者の雇用に関する情報を管理します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-270">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="be3b9-271">**休暇** – 作業カレンダー、休暇トランザクション、休暇設定など、作業者の休暇に関する情報を管理します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-271">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="be3b9-272">**報酬と給与** – プラン登録、報奨、実績、手数料、税金情報、退職、給与控除など、作業者の報酬プランと給与情報に関する情報を管理します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-272">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="be3b9-273">作業者情報を入力する場合、Dayforce で使用される次のデータとコンフィギュレーションに留意してください。</span><span class="sxs-lookup"><span data-stu-id="be3b9-273">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="be3b9-274">一般情報</span><span class="sxs-lookup"><span data-stu-id="be3b9-274">General information</span></span>

- <span data-ttu-id="be3b9-275">個人番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-275">Personnel number (required)</span></span>
- <span data-ttu-id="be3b9-276">名 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-276">First name (required)</span></span>
- <span data-ttu-id="be3b9-277">姓 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-277">Last name (required)</span></span>
- <span data-ttu-id="be3b9-278">ミドル ネーム</span><span class="sxs-lookup"><span data-stu-id="be3b9-278">Middle name</span></span>
- <span data-ttu-id="be3b9-279">勤続日数</span><span class="sxs-lookup"><span data-stu-id="be3b9-279">Seniority date</span></span>
- <span data-ttu-id="be3b9-280">呼称</span><span class="sxs-lookup"><span data-stu-id="be3b9-280">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="be3b9-281">個人情報</span><span class="sxs-lookup"><span data-stu-id="be3b9-281">Personal information</span></span>

- <span data-ttu-id="be3b9-282">配偶者の有無 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-282">Marital status (required)</span></span>
- <span data-ttu-id="be3b9-283">生年月日 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-283">Birth date (required)</span></span>
- <span data-ttu-id="be3b9-284">性別 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-284">Gender (required)</span></span>
- <span data-ttu-id="be3b9-285">障碍のあるユーザー</span><span class="sxs-lookup"><span data-stu-id="be3b9-285">Person with disabilities</span></span>
- <span data-ttu-id="be3b9-286">国籍 国 地域 (メキシコの場合のみ)</span><span class="sxs-lookup"><span data-stu-id="be3b9-286">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="be3b9-287">住所情報</span><span class="sxs-lookup"><span data-stu-id="be3b9-287">Address information</span></span>

- <span data-ttu-id="be3b9-288">基本 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-288">Primary (required)</span></span>
- <span data-ttu-id="be3b9-289">国/地域 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-289">Country/region (required)</span></span>
- <span data-ttu-id="be3b9-290">郵便番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-290">Postal code (required)</span></span>
- <span data-ttu-id="be3b9-291">番地 (必須) (メキシコの場合のみ)</span><span class="sxs-lookup"><span data-stu-id="be3b9-291">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="be3b9-292">建物名 (メキシコの場合のみ)</span><span class="sxs-lookup"><span data-stu-id="be3b9-292">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="be3b9-293">市町村 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-293">City (required)</span></span>
- <span data-ttu-id="be3b9-294">都道府県 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-294">State (required)</span></span>
- <span data-ttu-id="be3b9-295">国 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-295">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="be3b9-296">連絡先情報</span><span class="sxs-lookup"><span data-stu-id="be3b9-296">Contact information</span></span> 

- <span data-ttu-id="be3b9-297">基本 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-297">Primary (required)</span></span>
- <span data-ttu-id="be3b9-298">連絡先の電話番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-298">Contact number (required)</span></span>
- <span data-ttu-id="be3b9-299">内線</span><span class="sxs-lookup"><span data-stu-id="be3b9-299">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="be3b9-300">給与情報および所得コード</span><span class="sxs-lookup"><span data-stu-id="be3b9-300">Payroll information and earning codes</span></span>

<span data-ttu-id="be3b9-301">従業員は、指定された支払頻度で特定の所得が割り当てられ、希望の支払方法を有する場合があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-301">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="be3b9-302">次のフィールドは、それらの基本設定と設定が使用されることを保証するために Dayforce で使用されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-302">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="be3b9-303">所得コード</span><span class="sxs-lookup"><span data-stu-id="be3b9-303">Earning codes</span></span>

- <span data-ttu-id="be3b9-304">職位 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-304">Position (required)</span></span>
- <span data-ttu-id="be3b9-305">所得コード (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-305">Earning Code (required)</span></span>
- <span data-ttu-id="be3b9-306">頻度 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-306">Frequency (required)</span></span>
- <span data-ttu-id="be3b9-307">金額 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-307">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="be3b9-308">給与情報</span><span class="sxs-lookup"><span data-stu-id="be3b9-308">Payroll information</span></span>

- <span data-ttu-id="be3b9-309">支払方法</span><span class="sxs-lookup"><span data-stu-id="be3b9-309">Payment Method</span></span>
- <span data-ttu-id="be3b9-310">経済地域 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-310">Economic Region (required)</span></span>
- <span data-ttu-id="be3b9-311">従業員手当 ID</span><span class="sxs-lookup"><span data-stu-id="be3b9-311">Employee Benefits ID</span></span>
- <span data-ttu-id="be3b9-312">国民 ID 番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-312">National ID Number (required)</span></span>
- <span data-ttu-id="be3b9-313">兵役番号</span><span class="sxs-lookup"><span data-stu-id="be3b9-313">Military Service Number</span></span>
- <span data-ttu-id="be3b9-314">シフト ID (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-314">Shift ID (required)</span></span>
- <span data-ttu-id="be3b9-315">税番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-315">Tax Number (required)</span></span>
- <span data-ttu-id="be3b9-316">労働組合 ID (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-316">Union ID (required)</span></span>
- <span data-ttu-id="be3b9-317">作業日 ID (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-317">Work Day ID (required)</span></span>
- <span data-ttu-id="be3b9-318">労働許可番号</span><span class="sxs-lookup"><span data-stu-id="be3b9-318">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="be3b9-319">支払方法について、メキシコでは **現金**、**小切手** (会社の現物小切手)、および **電子支払** がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-319">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="be3b9-320">NP 支払方法が指定されている場合、既定で **小切手** が使用されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-320">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="be3b9-321">従業員の詳細</span><span class="sxs-lookup"><span data-stu-id="be3b9-321">Employment details</span></span>

<span data-ttu-id="be3b9-322">雇用の詳細履歴は、Dayforce で従業員の採用、退職、および再雇用のステータスを派生させるため、重要な情報として使用されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-322">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="be3b9-323">Dayforce は、一度に 1 つだけ有効な雇用レコードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="be3b9-323">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="be3b9-324">雇用開始日 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-324">Employment start date (required)</span></span>
- <span data-ttu-id="be3b9-325">雇用終了日</span><span class="sxs-lookup"><span data-stu-id="be3b9-325">Employment end date</span></span>
- <span data-ttu-id="be3b9-326">入社日</span><span class="sxs-lookup"><span data-stu-id="be3b9-326">Start date</span></span>
- <span data-ttu-id="be3b9-327">調整済開始日</span><span class="sxs-lookup"><span data-stu-id="be3b9-327">Adjusted start date</span></span>
- <span data-ttu-id="be3b9-328">退職日 (退職時は必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-328">Termination date (required upon termination)</span></span>
- <span data-ttu-id="be3b9-329">退職理由 (退職時は必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-329">Termination reason (required upon termination)</span></span>

<span data-ttu-id="be3b9-330">従業員の重要な日付は、次の情報を使用して派生されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-330">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="be3b9-331">人事管理</span><span class="sxs-lookup"><span data-stu-id="be3b9-331">Human Resources</span></span>                | <span data-ttu-id="be3b9-332">Dayforce</span><span class="sxs-lookup"><span data-stu-id="be3b9-332">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be3b9-333">最新の採用日付</span><span class="sxs-lookup"><span data-stu-id="be3b9-333">Most recent hire date</span></span> | <span data-ttu-id="be3b9-334">現在の非退職雇用履歴レコードの雇用開始</span><span class="sxs-lookup"><span data-stu-id="be3b9-334">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="be3b9-335">退職日</span><span class="sxs-lookup"><span data-stu-id="be3b9-335">Termination date</span></span>      | <span data-ttu-id="be3b9-336">現在の非退職雇用履歴レコードの退職日</span><span class="sxs-lookup"><span data-stu-id="be3b9-336">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="be3b9-337">入社日</span><span class="sxs-lookup"><span data-stu-id="be3b9-337">Start date</span></span>            | <span data-ttu-id="be3b9-338">現在の非アクティブ雇用履歴レコードの調整済開始日、開始日、または雇用開始</span><span class="sxs-lookup"><span data-stu-id="be3b9-338">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="be3b9-339">元の採用日付</span><span class="sxs-lookup"><span data-stu-id="be3b9-339">Original hire date</span></span>    | <span data-ttu-id="be3b9-340">最も早い雇用履歴レコードの雇用開始</span><span class="sxs-lookup"><span data-stu-id="be3b9-340">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="be3b9-341">報酬</span><span class="sxs-lookup"><span data-stu-id="be3b9-341">Compensation</span></span>

<span data-ttu-id="be3b9-342">固定報酬計画は、雇用期間全体ですべての従業員の基本職位に関連付けられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-342">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="be3b9-343">この期間は、従業員が採用された日付 (または雇用の開始日) に開始し、退職するまで継続します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-343">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="be3b9-344">有効日 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-344">Effective Date (required)</span></span>
- <span data-ttu-id="be3b9-345">有効期限</span><span class="sxs-lookup"><span data-stu-id="be3b9-345">Expiration date</span></span>
- <span data-ttu-id="be3b9-346">支払レート (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-346">Pay Rate (required)</span></span>
- <span data-ttu-id="be3b9-347">支払レートの変換 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-347">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="be3b9-348">年間相当額 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-348">Annual equivalent (required)</span></span>
- <span data-ttu-id="be3b9-349">時間相当額 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-349">Hourly equivalent (required)</span></span>

<span data-ttu-id="be3b9-350">時給払いの従業員に複数の職位がある場合、基本職位の固定報酬が作業者レベルの基準レートまたは給与として Dayforce にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-350">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="be3b9-351">基本以外の職位については、時給のレートが Dayforce の対応する職位に保存されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-351">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="be3b9-352">月給払いの従業員に複数の職位がある場合、累計時間率およびすべての有効な職位全体での年間給与が派生され、従業員レベルの基準レートまたは給与として使用されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-352">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="be3b9-353">ID 番号</span><span class="sxs-lookup"><span data-stu-id="be3b9-353">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="be3b9-354">社会保障 ID</span><span class="sxs-lookup"><span data-stu-id="be3b9-354">Social Security identifier</span></span> 

<span data-ttu-id="be3b9-355">すべての従業員は、1 つの基本 ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="be3b9-355">Every employee must have one primary identifier.</span></span> <span data-ttu-id="be3b9-356">この ID は **SSN** ID タイプにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-356">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="be3b9-357">Dayforce では、採用に必要な従業員の社会保障 ID として自動的に派生されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-357">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="be3b9-358">基本 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-358">Primary (required)</span></span>
- <span data-ttu-id="be3b9-359">ID タイプ = "SSN"</span><span class="sxs-lookup"><span data-stu-id="be3b9-359">Identification Type = "SSN"</span></span>
- <span data-ttu-id="be3b9-360">発行日付</span><span class="sxs-lookup"><span data-stu-id="be3b9-360">Issued Date</span></span>
- <span data-ttu-id="be3b9-361">有効期限</span><span class="sxs-lookup"><span data-stu-id="be3b9-361">Expiration Date</span></span>

<span data-ttu-id="be3b9-362">従業員は、**SSN** ID タイプの複数の ID 番号を申告できます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-362">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="be3b9-363">ただし、その番号が有効かまたは期限切れかに関係なく、**基本** としてマークされているレコードのみ Dayforce に統合されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-363">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="be3b9-364">銀行口座および出金</span><span class="sxs-lookup"><span data-stu-id="be3b9-364">Bank accounts and disbursements</span></span>

<span data-ttu-id="be3b9-365">銀行口座振替による支払を選択した従業員すべてのために、有効な銀行口座情報を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-365">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="be3b9-366">人事管理</span><span class="sxs-lookup"><span data-stu-id="be3b9-366">Human Resources</span></span>                         | <span data-ttu-id="be3b9-367">Dayforce</span><span class="sxs-lookup"><span data-stu-id="be3b9-367">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be3b9-368">銀行口座番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-368">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="be3b9-369">SWIFT コード (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-369">SWIFT code (required)</span></span>          | <span data-ttu-id="be3b9-370">メキシコの給与処理に使用される **銀行 ID** フィールド。</span><span class="sxs-lookup"><span data-stu-id="be3b9-370">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="be3b9-371">支店番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-371">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="be3b9-372">銀行口座の種類 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-372">Bank account type (required)</span></span>   | <span data-ttu-id="be3b9-373">メキシコの給与処理に使用される **口座の種類** フィールド。</span><span class="sxs-lookup"><span data-stu-id="be3b9-373">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="be3b9-374">サポートされている値には、**当座預金** および **給与** が含まれます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-374">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="be3b9-375">銀行口座振替による支払を選択した従業員は、メキシコに基本住所を持つ法人の下にあり、メキシコの銀行から有効な銀行口座に関連付けられている残余口座のリンクを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-375">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="be3b9-376">その他のすべての非残余口座は無視されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-376">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="be3b9-377">住所情報</span><span class="sxs-lookup"><span data-stu-id="be3b9-377">Address information</span></span>

<span data-ttu-id="be3b9-378">すべての従業員は、1 つの基本場所が必要です。</span><span class="sxs-lookup"><span data-stu-id="be3b9-378">Every employee must have one primary location.</span></span> <span data-ttu-id="be3b9-379">Dayforce において、この場所は課税額算出のために従業員の基本居住地を特定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-379">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="be3b9-380">基本 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-380">Primary (required)</span></span>
- <span data-ttu-id="be3b9-381">国/地域 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-381">Country/region (required)</span></span>
- <span data-ttu-id="be3b9-382">郵便番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-382">Zip/postal code (required)</span></span>
- <span data-ttu-id="be3b9-383">住所 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-383">Street (required)</span></span>
- <span data-ttu-id="be3b9-384">番地 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-384">Street Number (required)</span></span>
- <span data-ttu-id="be3b9-385">建物名</span><span class="sxs-lookup"><span data-stu-id="be3b9-385">Building Complement</span></span>
- <span data-ttu-id="be3b9-386">市町村 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-386">City (required)</span></span>
- <span data-ttu-id="be3b9-387">都道府県 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-387">State (required)</span></span>
- <span data-ttu-id="be3b9-388">国 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-388">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="be3b9-389">米国およびカナダでの給与を生成するために、データをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="be3b9-389">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="be3b9-390">米国およびカナダの従業員のために支払を生成している場合、次の要素をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-390">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="be3b9-391">職位に部門が必要です。</span><span class="sxs-lookup"><span data-stu-id="be3b9-391">Departments are required on positions.</span></span>
- <span data-ttu-id="be3b9-392">原価部門を財務分析コードとして設定し、既定の財務分析コード文字列の最初の要素とする必要があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-392">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="be3b9-393">職位が部門を指定するように Human Resources を構成することができます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-393">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="be3b9-394">この作業を実行するには、**人事管理共有職位 > 職位 > 職位の部門を要求** に移動します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-394">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="be3b9-395">この設定は、システムの統合に適用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="be3b9-395">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="be3b9-396">職務タイプ</span><span class="sxs-lookup"><span data-stu-id="be3b9-396">Job types</span></span>

<span data-ttu-id="be3b9-397">職務タイプは、類似した職務をカテゴリにグループ化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-397">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="be3b9-398">職務タイプは、米国およびカナダでの給与を処理するために必要です。</span><span class="sxs-lookup"><span data-stu-id="be3b9-398">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="be3b9-399">職務タイプの例には、フルタイムおよびパートタイム、または給与払いおよび時給払いが含まれます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-399">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="be3b9-400">職務タイプは、従業員が時給払いかあるいは給与払いなのかを示す支払タイプとして Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-400">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="be3b9-401">次の職務タイプと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="be3b9-401">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="be3b9-402">ジョブ タイプ</span><span class="sxs-lookup"><span data-stu-id="be3b9-402">Job type</span></span>   | <span data-ttu-id="be3b9-403">説明</span><span class="sxs-lookup"><span data-stu-id="be3b9-403">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="be3b9-404">時間</span><span class="sxs-lookup"><span data-stu-id="be3b9-404">Hourly</span></span>     | <span data-ttu-id="be3b9-405">時間</span><span class="sxs-lookup"><span data-stu-id="be3b9-405">Hourly</span></span>      |
| <span data-ttu-id="be3b9-406">給与払い</span><span class="sxs-lookup"><span data-stu-id="be3b9-406">Salaried</span></span>   | <span data-ttu-id="be3b9-407">給与払い</span><span class="sxs-lookup"><span data-stu-id="be3b9-407">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="be3b9-408">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="be3b9-408">Position types</span></span> 

<span data-ttu-id="be3b9-409">職位がフルタイム、パートタイム、またはその他のタイプかどうかを説明するために職位タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-409">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="be3b9-410">職位タイプは、従業員がフルタイムかあるいはパートタイムなのかを示す支払クラスとして Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-410">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="be3b9-411">次の職位タイプと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="be3b9-411">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="be3b9-412">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="be3b9-412">Position type</span></span>   | <span data-ttu-id="be3b9-413">説明</span><span class="sxs-lookup"><span data-stu-id="be3b9-413">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="be3b9-414">フルタイム</span><span class="sxs-lookup"><span data-stu-id="be3b9-414">Full-time</span></span>       | <span data-ttu-id="be3b9-415">フルタイム従業員</span><span class="sxs-lookup"><span data-stu-id="be3b9-415">Full time employee</span></span> |
| <span data-ttu-id="be3b9-416">パートタイム</span><span class="sxs-lookup"><span data-stu-id="be3b9-416">Part-time</span></span>       | <span data-ttu-id="be3b9-417">パートタイム従業員</span><span class="sxs-lookup"><span data-stu-id="be3b9-417">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="be3b9-418">理由コード</span><span class="sxs-lookup"><span data-stu-id="be3b9-418">Reason codes</span></span>

<span data-ttu-id="be3b9-419">理由コードは、従業員のステータスに関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-419">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="be3b9-420">理由コードは、従業員の職位または雇用ステータスへの変更の理由を示すステータス理由として Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-420">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="be3b9-421">次の理由コードと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="be3b9-421">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="be3b9-422">理由コード</span><span class="sxs-lookup"><span data-stu-id="be3b9-422">Reason code</span></span>    | <span data-ttu-id="be3b9-423">説明</span><span class="sxs-lookup"><span data-stu-id="be3b9-423">Description</span></span>      | <span data-ttu-id="be3b9-424">適用可能なシナリオ</span><span class="sxs-lookup"><span data-stu-id="be3b9-424">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="be3b9-425">辞職</span><span class="sxs-lookup"><span data-stu-id="be3b9-425">RESIGNATION</span></span>    | <span data-ttu-id="be3b9-426">辞職</span><span class="sxs-lookup"><span data-stu-id="be3b9-426">Resignation</span></span>      | <span data-ttu-id="be3b9-427">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="be3b9-427">Terminate worker</span></span>     |
| <span data-ttu-id="be3b9-428">終了</span><span class="sxs-lookup"><span data-stu-id="be3b9-428">TERMINATION</span></span>    | <span data-ttu-id="be3b9-429">終了</span><span class="sxs-lookup"><span data-stu-id="be3b9-429">Termination</span></span>      | <span data-ttu-id="be3b9-430">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="be3b9-430">Terminate worker</span></span>     |
| <span data-ttu-id="be3b9-431">定年退職</span><span class="sxs-lookup"><span data-stu-id="be3b9-431">RETIREMENT</span></span>     | <span data-ttu-id="be3b9-432">償却</span><span class="sxs-lookup"><span data-stu-id="be3b9-432">Retirement</span></span>       | <span data-ttu-id="be3b9-433">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="be3b9-433">Terminate worker</span></span>     |
| <span data-ttu-id="be3b9-434">その他</span><span class="sxs-lookup"><span data-stu-id="be3b9-434">OTHER</span></span>          | <span data-ttu-id="be3b9-435">その他の理由</span><span class="sxs-lookup"><span data-stu-id="be3b9-435">Other Reasons</span></span>    | <span data-ttu-id="be3b9-436">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="be3b9-436">Terminate worker</span></span>     |
| <span data-ttu-id="be3b9-437">死亡</span><span class="sxs-lookup"><span data-stu-id="be3b9-437">DEATH</span></span>          | <span data-ttu-id="be3b9-438">死亡</span><span class="sxs-lookup"><span data-stu-id="be3b9-438">Death</span></span>            | <span data-ttu-id="be3b9-439">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="be3b9-439">Terminate worker</span></span>     |
| <span data-ttu-id="be3b9-440">休暇</span><span class="sxs-lookup"><span data-stu-id="be3b9-440">LEAVEOFABSENCE</span></span> | <span data-ttu-id="be3b9-441">休暇</span><span class="sxs-lookup"><span data-stu-id="be3b9-441">Leave of Absence</span></span> | <span data-ttu-id="be3b9-442">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="be3b9-442">Terminate worker</span></span>     |
| <span data-ttu-id="be3b9-443">契約の終了</span><span class="sxs-lookup"><span data-stu-id="be3b9-443">CONTRACTEND</span></span>    | <span data-ttu-id="be3b9-444">契約の終了</span><span class="sxs-lookup"><span data-stu-id="be3b9-444">End of Contract</span></span>  | <span data-ttu-id="be3b9-445">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="be3b9-445">Terminate worker</span></span>     |
| <span data-ttu-id="be3b9-446">給与の変更</span><span class="sxs-lookup"><span data-stu-id="be3b9-446">SALARYCHANGE</span></span>   | <span data-ttu-id="be3b9-447">給与の変更</span><span class="sxs-lookup"><span data-stu-id="be3b9-447">Change of Salary</span></span> | <span data-ttu-id="be3b9-448">報酬</span><span class="sxs-lookup"><span data-stu-id="be3b9-448">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="be3b9-449">配偶者の有無</span><span class="sxs-lookup"><span data-stu-id="be3b9-449">Marital status</span></span>

<span data-ttu-id="be3b9-450">配偶者有無の値は、Dayforce にマップされ、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-450">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="be3b9-451">次の表に、配偶者有無の値がどのように Dayforce にマップされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-451">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="be3b9-452">人事管理</span><span class="sxs-lookup"><span data-stu-id="be3b9-452">Human Resources</span></span>                 | <span data-ttu-id="be3b9-453">Dayforce</span><span class="sxs-lookup"><span data-stu-id="be3b9-453">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="be3b9-454">既婚</span><span class="sxs-lookup"><span data-stu-id="be3b9-454">Married</span></span>                | <span data-ttu-id="be3b9-455">既婚</span><span class="sxs-lookup"><span data-stu-id="be3b9-455">Married</span></span>              |
| <span data-ttu-id="be3b9-456">未婚</span><span class="sxs-lookup"><span data-stu-id="be3b9-456">Single</span></span>                 | <span data-ttu-id="be3b9-457">未婚</span><span class="sxs-lookup"><span data-stu-id="be3b9-457">Single</span></span>               |
| <span data-ttu-id="be3b9-458">死別</span><span class="sxs-lookup"><span data-stu-id="be3b9-458">Widowed</span></span>                | <span data-ttu-id="be3b9-459">死別</span><span class="sxs-lookup"><span data-stu-id="be3b9-459">Widowed</span></span>              |
| <span data-ttu-id="be3b9-460">離婚</span><span class="sxs-lookup"><span data-stu-id="be3b9-460">Divorced</span></span>               | <span data-ttu-id="be3b9-461">離婚</span><span class="sxs-lookup"><span data-stu-id="be3b9-461">Divorced</span></span>             |
| <span data-ttu-id="be3b9-462">登録済パートナーシップ</span><span class="sxs-lookup"><span data-stu-id="be3b9-462">Registered Partnership</span></span> | <span data-ttu-id="be3b9-463">ドメスティック パートナーシップ</span><span class="sxs-lookup"><span data-stu-id="be3b9-463">Domestic Partnership</span></span> |
| <span data-ttu-id="be3b9-464">None</span><span class="sxs-lookup"><span data-stu-id="be3b9-464">None</span></span>                   | <span data-ttu-id="be3b9-465">None</span><span class="sxs-lookup"><span data-stu-id="be3b9-465">None</span></span>                 |
| <span data-ttu-id="be3b9-466">同棲中</span><span class="sxs-lookup"><span data-stu-id="be3b9-466">Cohabiting</span></span>             | <span data-ttu-id="be3b9-467">同棲中</span><span class="sxs-lookup"><span data-stu-id="be3b9-467">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="be3b9-468">種類</span><span class="sxs-lookup"><span data-stu-id="be3b9-468">Gender</span></span>

<span data-ttu-id="be3b9-469">性別の指定は、Dayforce にマップされ、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-469">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="be3b9-470">次の表に、性別の指定がどのように Dayforce にマップされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-470">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="be3b9-471">人事管理</span><span class="sxs-lookup"><span data-stu-id="be3b9-471">Human Resources</span></span>       | <span data-ttu-id="be3b9-472">Dayforce</span><span class="sxs-lookup"><span data-stu-id="be3b9-472">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="be3b9-473">男性</span><span class="sxs-lookup"><span data-stu-id="be3b9-473">Male</span></span>         | <span data-ttu-id="be3b9-474">男性</span><span class="sxs-lookup"><span data-stu-id="be3b9-474">Male</span></span>            |
| <span data-ttu-id="be3b9-475">女性</span><span class="sxs-lookup"><span data-stu-id="be3b9-475">Female</span></span>       | <span data-ttu-id="be3b9-476">女性</span><span class="sxs-lookup"><span data-stu-id="be3b9-476">Female</span></span>          |
| <span data-ttu-id="be3b9-477">不特定</span><span class="sxs-lookup"><span data-stu-id="be3b9-477">Non-specific</span></span> | <span data-ttu-id="be3b9-478">*サポートされていません*</span><span class="sxs-lookup"><span data-stu-id="be3b9-478">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="be3b9-479">所得コード</span><span class="sxs-lookup"><span data-stu-id="be3b9-479">Earning codes</span></span>

<span data-ttu-id="be3b9-480">所得コードは、作業者が受け取るすべての収益のタイプを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-480">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="be3b9-481">コードには、会計ルール、税法、レポート要件、およびグロスアップ能力など、所得に関連付けられている複数のパラメーターが含まれます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-481">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="be3b9-482">サポートされていない頻度を使用する場合、既定で **すべての支払** 頻度が計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-482">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="be3b9-483">サポートされる頻度</span><span class="sxs-lookup"><span data-stu-id="be3b9-483">Supported frequencies</span></span>

- <span data-ttu-id="be3b9-484">All</span><span class="sxs-lookup"><span data-stu-id="be3b9-484">All</span></span>
- <span data-ttu-id="be3b9-485">すべての支払</span><span class="sxs-lookup"><span data-stu-id="be3b9-485">EVERYPAY</span></span>
- <span data-ttu-id="be3b9-486">各支払期間</span><span class="sxs-lookup"><span data-stu-id="be3b9-486">EACHPAYPERIOD</span></span>
- <span data-ttu-id="be3b9-487">他のすべての奇数支払</span><span class="sxs-lookup"><span data-stu-id="be3b9-487">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="be3b9-488">他のすべての偶数支払</span><span class="sxs-lookup"><span data-stu-id="be3b9-488">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="be3b9-489">1 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-489">1OFMTH</span></span>
- <span data-ttu-id="be3b9-490">月の最終日</span><span class="sxs-lookup"><span data-stu-id="be3b9-490">LASTOFMTH</span></span>
- <span data-ttu-id="be3b9-491">2 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-491">2OFMTH</span></span>
- <span data-ttu-id="be3b9-492">3 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-492">3OFMTH</span></span>
- <span data-ttu-id="be3b9-493">4 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-493">4OFMTH</span></span>
- <span data-ttu-id="be3b9-494">5 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-494">5OFMTH</span></span>
- <span data-ttu-id="be3b9-495">1 か月および 2 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-495">1N2OFMTH</span></span>
- <span data-ttu-id="be3b9-496">3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-496">3N4OFMTH</span></span>
- <span data-ttu-id="be3b9-497">1 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-497">1N3OFMTH</span></span>
- <span data-ttu-id="be3b9-498">1 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-498">1N4OFMTH</span></span>
- <span data-ttu-id="be3b9-499">2 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-499">2N3OFMTH</span></span>
- <span data-ttu-id="be3b9-500">2 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-500">2N4OFMTH</span></span>
- <span data-ttu-id="be3b9-501">1 か月、2 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-501">1N2N3OFMTH</span></span>
- <span data-ttu-id="be3b9-502">1 か月、2 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-502">1N2N4OFMTH</span></span>
- <span data-ttu-id="be3b9-503">1 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-503">1N3N4OFMTH</span></span>
- <span data-ttu-id="be3b9-504">2 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-504">2N3N4OFMTH</span></span>
- <span data-ttu-id="be3b9-505">1 か月、2 か月、3 か月および 4 か月 - 1 か月、2 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="be3b9-506">2 か月、3 か月、4 か月および 5 か月 - 2 か月、3 か月、4 か月および 5 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-506">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="be3b9-507">四半期の 1 - 四半期の 1</span><span class="sxs-lookup"><span data-stu-id="be3b9-507">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="be3b9-508">四半期の最終日 – 四半期の最終日</span><span class="sxs-lookup"><span data-stu-id="be3b9-508">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="be3b9-509">四半期の最後の月 – 四半期の最後の月</span><span class="sxs-lookup"><span data-stu-id="be3b9-509">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="be3b9-510">1 年 - 1 年</span><span class="sxs-lookup"><span data-stu-id="be3b9-510">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="be3b9-511">年の最終日 – 年の最終日</span><span class="sxs-lookup"><span data-stu-id="be3b9-511">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="be3b9-512">年の 11 月および 12 月 - 年の 11 月および 12 月</span><span class="sxs-lookup"><span data-stu-id="be3b9-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="be3b9-513">住所</span><span class="sxs-lookup"><span data-stu-id="be3b9-513">Addresses</span></span>

<span data-ttu-id="be3b9-514">特定の国または地域、都道府県、および市区郡 (自治体) の ID には、Dayforce および国内または地域内のプロバイダーが認識できる特定の形式が必要です。</span><span class="sxs-lookup"><span data-stu-id="be3b9-514">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="be3b9-515">市町村の形式は柔軟ですが、すべての市町村が都道府県と関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-515">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="be3b9-516">人事管理</span><span class="sxs-lookup"><span data-stu-id="be3b9-516">Human Resources</span></span>          | <span data-ttu-id="be3b9-517">Dayforce</span><span class="sxs-lookup"><span data-stu-id="be3b9-517">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="be3b9-518">国/地域</span><span class="sxs-lookup"><span data-stu-id="be3b9-518">Country/Region</span></span>  | <span data-ttu-id="be3b9-519">国コード</span><span class="sxs-lookup"><span data-stu-id="be3b9-519">Country Code</span></span>          |
| <span data-ttu-id="be3b9-520">郵便番号</span><span class="sxs-lookup"><span data-stu-id="be3b9-520">Zip/Postal Code</span></span> | <span data-ttu-id="be3b9-521">郵便番号</span><span class="sxs-lookup"><span data-stu-id="be3b9-521">Postal Code</span></span>           |
| <span data-ttu-id="be3b9-522">行政単位 (区画)</span><span class="sxs-lookup"><span data-stu-id="be3b9-522">State</span></span>           | <span data-ttu-id="be3b9-523">都道府県コード</span><span class="sxs-lookup"><span data-stu-id="be3b9-523">State Code</span></span>            |
| <span data-ttu-id="be3b9-524">市町村</span><span class="sxs-lookup"><span data-stu-id="be3b9-524">City</span></span>            | <span data-ttu-id="be3b9-525">市町村</span><span class="sxs-lookup"><span data-stu-id="be3b9-525">City</span></span>                  |
| <span data-ttu-id="be3b9-526">郡</span><span class="sxs-lookup"><span data-stu-id="be3b9-526">County</span></span>          | <span data-ttu-id="be3b9-527">市区郡 (自治体)</span><span class="sxs-lookup"><span data-stu-id="be3b9-527">County (Municipality)</span></span> |
| <span data-ttu-id="be3b9-528">住所</span><span class="sxs-lookup"><span data-stu-id="be3b9-528">Street</span></span>          | <span data-ttu-id="be3b9-529">住所行 1</span><span class="sxs-lookup"><span data-stu-id="be3b9-529">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="be3b9-530">税地域</span><span class="sxs-lookup"><span data-stu-id="be3b9-530">Tax regions</span></span>

<span data-ttu-id="be3b9-531">税地域は、給与の生成時に適用する適切な税を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-531">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="be3b9-532">税地域は、場所の住所として Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-532">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="be3b9-533">既定の税地域は、作業者の有効な職位に関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-533">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="be3b9-534">税地域 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-534">Tax region (required)</span></span>
- <span data-ttu-id="be3b9-535">国/地域 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-535">Country/Region (required)</span></span>
- <span data-ttu-id="be3b9-536">都道府県 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-536">State (required)</span></span>
- <span data-ttu-id="be3b9-537">郡</span><span class="sxs-lookup"><span data-stu-id="be3b9-537">County</span></span> 
- <span data-ttu-id="be3b9-538">市町村 (必須)</span><span class="sxs-lookup"><span data-stu-id="be3b9-538">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="be3b9-539">メキシコの給与を生成するためのデータ コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="be3b9-539">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="be3b9-540">メキシコの従業員のために支払を生成している場合、次の要素をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-540">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="be3b9-541">職位に部門が必要です。</span><span class="sxs-lookup"><span data-stu-id="be3b9-541">Departments are required on positions.</span></span>
- <span data-ttu-id="be3b9-542">原価部門を財務分析コードとして設定し、既定の財務分析コード文字列の最初の要素とする必要があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-542">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="be3b9-543">ジョブ タイプ</span><span class="sxs-lookup"><span data-stu-id="be3b9-543">Job types</span></span>

<span data-ttu-id="be3b9-544">職務タイプは、類似した職務をカテゴリにグループ化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-544">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="be3b9-545">職務タイプは、メキシコでの給与を処理するために必要です。</span><span class="sxs-lookup"><span data-stu-id="be3b9-545">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="be3b9-546">職務タイプの例には、フルタイムおよびパートタイム、または給与払いおよび時給払いが含まれます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-546">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="be3b9-547">職務タイプは、従業員が時給払いかあるいは給与払いなのかを示す支払タイプとして Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-547">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="be3b9-548">次の職務タイプと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="be3b9-548">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="be3b9-549">ジョブ タイプ</span><span class="sxs-lookup"><span data-stu-id="be3b9-549">Job type</span></span>   | <span data-ttu-id="be3b9-550">説明</span><span class="sxs-lookup"><span data-stu-id="be3b9-550">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="be3b9-551">時間</span><span class="sxs-lookup"><span data-stu-id="be3b9-551">Hourly</span></span>     | <span data-ttu-id="be3b9-552">MX 時給払い</span><span class="sxs-lookup"><span data-stu-id="be3b9-552">MX Hourly</span></span>   |
| <span data-ttu-id="be3b9-553">給与払い</span><span class="sxs-lookup"><span data-stu-id="be3b9-553">Salaried</span></span>   | <span data-ttu-id="be3b9-554">MX 給与払い</span><span class="sxs-lookup"><span data-stu-id="be3b9-554">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="be3b9-555">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="be3b9-555">Position types</span></span> 

<span data-ttu-id="be3b9-556">職位がフルタイム、パートタイム、またはその他のタイプかどうかを説明するために職位タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-556">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="be3b9-557">職位タイプは、従業員がフルタイムかあるいはパートタイムなのかを示す支払クラスとして Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-557">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="be3b9-558">次の職位タイプと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="be3b9-558">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="be3b9-559">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="be3b9-559">Position type</span></span>   | <span data-ttu-id="be3b9-560">説明</span><span class="sxs-lookup"><span data-stu-id="be3b9-560">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="be3b9-561">フルタイム</span><span class="sxs-lookup"><span data-stu-id="be3b9-561">Full-time</span></span>       | <span data-ttu-id="be3b9-562">フルタイム従業員</span><span class="sxs-lookup"><span data-stu-id="be3b9-562">Full time employee</span></span> |
| <span data-ttu-id="be3b9-563">パートタイム</span><span class="sxs-lookup"><span data-stu-id="be3b9-563">Part-time</span></span>       | <span data-ttu-id="be3b9-564">パートタイム従業員</span><span class="sxs-lookup"><span data-stu-id="be3b9-564">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="be3b9-565">理由コード</span><span class="sxs-lookup"><span data-stu-id="be3b9-565">Reason codes</span></span>

<span data-ttu-id="be3b9-566">理由コードは、従業員のステータスに関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-566">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="be3b9-567">理由コードは、従業員の職位または雇用ステータスへの変更の理由を示すステータス理由として Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-567">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="be3b9-568">次の理由コードと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="be3b9-568">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="be3b9-569">理由コード</span><span class="sxs-lookup"><span data-stu-id="be3b9-569">Reason code</span></span>            | <span data-ttu-id="be3b9-570">説明</span><span class="sxs-lookup"><span data-stu-id="be3b9-570">Description</span></span>                    | <span data-ttu-id="be3b9-571">適用可能なシナリオ</span><span class="sxs-lookup"><span data-stu-id="be3b9-571">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="be3b9-572">支払前の除籍</span><span class="sxs-lookup"><span data-stu-id="be3b9-572">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="be3b9-573">最初の給与の前の除籍</span><span class="sxs-lookup"><span data-stu-id="be3b9-573">Departure before first payroll</span></span> | <span data-ttu-id="be3b9-574">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="be3b9-574">Terminate worker</span></span>     |
| <span data-ttu-id="be3b9-575">辞職</span><span class="sxs-lookup"><span data-stu-id="be3b9-575">RESIGNATION</span></span>            | <span data-ttu-id="be3b9-576">辞職</span><span class="sxs-lookup"><span data-stu-id="be3b9-576">Resignation</span></span>                    | <span data-ttu-id="be3b9-577">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="be3b9-577">Terminate worker</span></span>     |
| <span data-ttu-id="be3b9-578">年金</span><span class="sxs-lookup"><span data-stu-id="be3b9-578">PENSION</span></span>                | <span data-ttu-id="be3b9-579">年金</span><span class="sxs-lookup"><span data-stu-id="be3b9-579">Pension</span></span>                        | <span data-ttu-id="be3b9-580">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="be3b9-580">Terminate worker</span></span>     |
| <span data-ttu-id="be3b9-581">終了</span><span class="sxs-lookup"><span data-stu-id="be3b9-581">TERMINATION</span></span>            | <span data-ttu-id="be3b9-582">終了</span><span class="sxs-lookup"><span data-stu-id="be3b9-582">Termination</span></span>                    | <span data-ttu-id="be3b9-583">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="be3b9-583">Terminate worker</span></span>     |
| <span data-ttu-id="be3b9-584">定年退職</span><span class="sxs-lookup"><span data-stu-id="be3b9-584">RETIREMENT</span></span>             | <span data-ttu-id="be3b9-585">償却</span><span class="sxs-lookup"><span data-stu-id="be3b9-585">Retirement</span></span>                     | <span data-ttu-id="be3b9-586">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="be3b9-586">Terminate worker</span></span>     |
| <span data-ttu-id="be3b9-587">休暇者</span><span class="sxs-lookup"><span data-stu-id="be3b9-587">ABSENTEE</span></span>               | <span data-ttu-id="be3b9-588">休暇者</span><span class="sxs-lookup"><span data-stu-id="be3b9-588">Absentee</span></span>                       | <span data-ttu-id="be3b9-589">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="be3b9-589">Terminate worker</span></span>     |
| <span data-ttu-id="be3b9-590">その他</span><span class="sxs-lookup"><span data-stu-id="be3b9-590">OTHER</span></span>                  | <span data-ttu-id="be3b9-591">その他の理由</span><span class="sxs-lookup"><span data-stu-id="be3b9-591">Other Reasons</span></span>                  | <span data-ttu-id="be3b9-592">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="be3b9-592">Terminate worker</span></span>     |
| <span data-ttu-id="be3b9-593">休業</span><span class="sxs-lookup"><span data-stu-id="be3b9-593">CLOSURE</span></span>                | <span data-ttu-id="be3b9-594">業務休業</span><span class="sxs-lookup"><span data-stu-id="be3b9-594">Business Closure</span></span>               | <span data-ttu-id="be3b9-595">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="be3b9-595">Terminate worker</span></span>     |
| <span data-ttu-id="be3b9-596">死亡</span><span class="sxs-lookup"><span data-stu-id="be3b9-596">DEATH</span></span>                  | <span data-ttu-id="be3b9-597">死亡</span><span class="sxs-lookup"><span data-stu-id="be3b9-597">Death</span></span>                          | <span data-ttu-id="be3b9-598">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="be3b9-598">Terminate worker</span></span>     |
| <span data-ttu-id="be3b9-599">休暇</span><span class="sxs-lookup"><span data-stu-id="be3b9-599">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="be3b9-600">休暇</span><span class="sxs-lookup"><span data-stu-id="be3b9-600">Leave of Absence</span></span>               | <span data-ttu-id="be3b9-601">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="be3b9-601">Terminate worker</span></span>     |
| <span data-ttu-id="be3b9-602">契約の終了</span><span class="sxs-lookup"><span data-stu-id="be3b9-602">CONTRACTEND</span></span>            | <span data-ttu-id="be3b9-603">契約の終了</span><span class="sxs-lookup"><span data-stu-id="be3b9-603">End of Contract</span></span>                | <span data-ttu-id="be3b9-604">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="be3b9-604">Terminate worker</span></span>     |
| <span data-ttu-id="be3b9-605">給与の変更</span><span class="sxs-lookup"><span data-stu-id="be3b9-605">SALARYCHANGE</span></span>           | <span data-ttu-id="be3b9-606">給与の変更</span><span class="sxs-lookup"><span data-stu-id="be3b9-606">Change of Salary</span></span>               | <span data-ttu-id="be3b9-607">報酬</span><span class="sxs-lookup"><span data-stu-id="be3b9-607">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="be3b9-608">雇用条件</span><span class="sxs-lookup"><span data-stu-id="be3b9-608">Terms of employment</span></span>

<span data-ttu-id="be3b9-609">雇用条件は、雇用条件のカテゴリを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-609">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="be3b9-610">条件は、雇用インジケーターの値として Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-610">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="be3b9-611">次の雇用条件および説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="be3b9-611">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="be3b9-612">雇用条件</span><span class="sxs-lookup"><span data-stu-id="be3b9-612">Terms of employment</span></span>   | <span data-ttu-id="be3b9-613">説明</span><span class="sxs-lookup"><span data-stu-id="be3b9-613">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="be3b9-614">通常</span><span class="sxs-lookup"><span data-stu-id="be3b9-614">Regular</span></span>               | <span data-ttu-id="be3b9-615">通常</span><span class="sxs-lookup"><span data-stu-id="be3b9-615">Regular</span></span>     |
| <span data-ttu-id="be3b9-616">直接</span><span class="sxs-lookup"><span data-stu-id="be3b9-616">Direct</span></span>                | <span data-ttu-id="be3b9-617">直接</span><span class="sxs-lookup"><span data-stu-id="be3b9-617">Direct</span></span>      |
| <span data-ttu-id="be3b9-618">インターンシップ</span><span class="sxs-lookup"><span data-stu-id="be3b9-618">Internship</span></span>            | <span data-ttu-id="be3b9-619">インターンシップ</span><span class="sxs-lookup"><span data-stu-id="be3b9-619">Internship</span></span>  |
| <span data-ttu-id="be3b9-620">永続的</span><span class="sxs-lookup"><span data-stu-id="be3b9-620">Permanent</span></span>             | <span data-ttu-id="be3b9-621">永続的</span><span class="sxs-lookup"><span data-stu-id="be3b9-621">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="be3b9-622">配偶者の有無</span><span class="sxs-lookup"><span data-stu-id="be3b9-622">Marital status</span></span>

<span data-ttu-id="be3b9-623">配偶者有無の値は、Dayforce にマップされ、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-623">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="be3b9-624">次の表に、配偶者有無の値がどのように Dayforce にマップされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-624">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="be3b9-625">人事管理</span><span class="sxs-lookup"><span data-stu-id="be3b9-625">Human Resources</span></span>                 | <span data-ttu-id="be3b9-626">Dayforce</span><span class="sxs-lookup"><span data-stu-id="be3b9-626">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="be3b9-627">既婚</span><span class="sxs-lookup"><span data-stu-id="be3b9-627">Married</span></span>                | <span data-ttu-id="be3b9-628">既婚</span><span class="sxs-lookup"><span data-stu-id="be3b9-628">Married</span></span>                   |
| <span data-ttu-id="be3b9-629">未婚</span><span class="sxs-lookup"><span data-stu-id="be3b9-629">Single</span></span>                 | <span data-ttu-id="be3b9-630">未婚</span><span class="sxs-lookup"><span data-stu-id="be3b9-630">Single</span></span>                    |
| <span data-ttu-id="be3b9-631">死別</span><span class="sxs-lookup"><span data-stu-id="be3b9-631">Widowed</span></span>                | <span data-ttu-id="be3b9-632">死別</span><span class="sxs-lookup"><span data-stu-id="be3b9-632">Widowed</span></span>                   |
| <span data-ttu-id="be3b9-633">離婚</span><span class="sxs-lookup"><span data-stu-id="be3b9-633">Divorced</span></span>               | <span data-ttu-id="be3b9-634">離婚</span><span class="sxs-lookup"><span data-stu-id="be3b9-634">Divorced</span></span>                  |
| <span data-ttu-id="be3b9-635">登録済パートナーシップ</span><span class="sxs-lookup"><span data-stu-id="be3b9-635">Registered Partnership</span></span> | <span data-ttu-id="be3b9-636">ドメスティック パートナーシップ</span><span class="sxs-lookup"><span data-stu-id="be3b9-636">Domestic Partnership</span></span>      |
| <span data-ttu-id="be3b9-637">None</span><span class="sxs-lookup"><span data-stu-id="be3b9-637">None</span></span>                   | <span data-ttu-id="be3b9-638">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="be3b9-638">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="be3b9-639">同棲中</span><span class="sxs-lookup"><span data-stu-id="be3b9-639">Cohabiting</span></span>             | <span data-ttu-id="be3b9-640">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="be3b9-640">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="be3b9-641">種類</span><span class="sxs-lookup"><span data-stu-id="be3b9-641">Gender</span></span>

<span data-ttu-id="be3b9-642">性別の指定は、Dayforce にマップされ、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-642">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="be3b9-643">次の表に、性別の指定がどのように Dayforce にマップされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-643">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="be3b9-644">人事管理</span><span class="sxs-lookup"><span data-stu-id="be3b9-644">Human Resources</span></span>       | <span data-ttu-id="be3b9-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="be3b9-645">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="be3b9-646">男性</span><span class="sxs-lookup"><span data-stu-id="be3b9-646">Male</span></span>         | <span data-ttu-id="be3b9-647">男性</span><span class="sxs-lookup"><span data-stu-id="be3b9-647">Male</span></span>                      |
| <span data-ttu-id="be3b9-648">女性</span><span class="sxs-lookup"><span data-stu-id="be3b9-648">Female</span></span>       | <span data-ttu-id="be3b9-649">女性</span><span class="sxs-lookup"><span data-stu-id="be3b9-649">Female</span></span>                    |
| <span data-ttu-id="be3b9-650">不特定</span><span class="sxs-lookup"><span data-stu-id="be3b9-650">Non-specific</span></span> | <span data-ttu-id="be3b9-651">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="be3b9-651">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="be3b9-652">支払方法</span><span class="sxs-lookup"><span data-stu-id="be3b9-652">Payment method</span></span>

<span data-ttu-id="be3b9-653">支払方法は、従業員に支払が行われる方法を従業員および会社に説明します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-653">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="be3b9-654">支払方法は、Dayforce にマップされ、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-654">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="be3b9-655">次の表に、支払方法がどのように Dayforce にマップされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-655">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="be3b9-656">人事管理</span><span class="sxs-lookup"><span data-stu-id="be3b9-656">Human Resources</span></span>             | <span data-ttu-id="be3b9-657">Dayforce</span><span class="sxs-lookup"><span data-stu-id="be3b9-657">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="be3b9-658">現金</span><span class="sxs-lookup"><span data-stu-id="be3b9-658">Cash</span></span>               | <span data-ttu-id="be3b9-659">現金</span><span class="sxs-lookup"><span data-stu-id="be3b9-659">Cash</span></span>                      |
| <span data-ttu-id="be3b9-660">電子支払</span><span class="sxs-lookup"><span data-stu-id="be3b9-660">Electronic Payment</span></span> | <span data-ttu-id="be3b9-661">転送</span><span class="sxs-lookup"><span data-stu-id="be3b9-661">Transfer</span></span>                  |
| <span data-ttu-id="be3b9-662">チェック</span><span class="sxs-lookup"><span data-stu-id="be3b9-662">Check</span></span>              | <span data-ttu-id="be3b9-663">小切手</span><span class="sxs-lookup"><span data-stu-id="be3b9-663">Cheque</span></span>                    |
| <span data-ttu-id="be3b9-664">銀行為替手形</span><span class="sxs-lookup"><span data-stu-id="be3b9-664">Bank Draft</span></span>         | <span data-ttu-id="be3b9-665">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="be3b9-665">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="be3b9-666">外</span><span class="sxs-lookup"><span data-stu-id="be3b9-666">Other</span></span>              | <span data-ttu-id="be3b9-667">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="be3b9-667">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="be3b9-668">銀行口座の種類</span><span class="sxs-lookup"><span data-stu-id="be3b9-668">Bank account type</span></span>

<span data-ttu-id="be3b9-669">銀行口座の種類は、従業員への電子支払のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-669">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="be3b9-670">銀行口座の種類は、振替口座情報として Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-670">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="be3b9-671">銀行口座の種類は、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-671">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="be3b9-672">人事管理</span><span class="sxs-lookup"><span data-stu-id="be3b9-672">Human Resources</span></span>            | <span data-ttu-id="be3b9-673">Dayforce</span><span class="sxs-lookup"><span data-stu-id="be3b9-673">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="be3b9-674">当座預金口座</span><span class="sxs-lookup"><span data-stu-id="be3b9-674">Checking Account</span></span>  | <span data-ttu-id="be3b9-675">当座預金口座</span><span class="sxs-lookup"><span data-stu-id="be3b9-675">CheckingAccount</span></span>           |
| <span data-ttu-id="be3b9-676">給与口座</span><span class="sxs-lookup"><span data-stu-id="be3b9-676">Payroll Account</span></span>   | <span data-ttu-id="be3b9-677">給与口座</span><span class="sxs-lookup"><span data-stu-id="be3b9-677">PayrollAccount</span></span>            |
| <span data-ttu-id="be3b9-678">普通預金口座</span><span class="sxs-lookup"><span data-stu-id="be3b9-678">Savings Account</span></span>   | <span data-ttu-id="be3b9-679">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="be3b9-679">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="be3b9-680">BankGirot 口座</span><span class="sxs-lookup"><span data-stu-id="be3b9-680">BankGirot account</span></span> | <span data-ttu-id="be3b9-681">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="be3b9-681">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="be3b9-682">PlusGirot 口座</span><span class="sxs-lookup"><span data-stu-id="be3b9-682">PlusGirot account</span></span> | <span data-ttu-id="be3b9-683">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="be3b9-683">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="be3b9-684">所得コード</span><span class="sxs-lookup"><span data-stu-id="be3b9-684">Earning codes</span></span>

<span data-ttu-id="be3b9-685">所得コードは、作業者が受け取るすべての収益のタイプを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="be3b9-685">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="be3b9-686">コードには、会計ルール、税法、レポート要件、およびグロスアップ能力など、所得に関連付けられている複数のパラメーターが含まれます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-686">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="be3b9-687">サポートされていない頻度を使用する場合、既定で **すべての支払** 頻度が計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-687">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="be3b9-688">サポートされる頻度</span><span class="sxs-lookup"><span data-stu-id="be3b9-688">Supported frequencies</span></span>

- <span data-ttu-id="be3b9-689">All</span><span class="sxs-lookup"><span data-stu-id="be3b9-689">All</span></span>
- <span data-ttu-id="be3b9-690">すべての支払</span><span class="sxs-lookup"><span data-stu-id="be3b9-690">EVERYPAY</span></span>
- <span data-ttu-id="be3b9-691">各支払期間</span><span class="sxs-lookup"><span data-stu-id="be3b9-691">EACHPAYPERIOD</span></span>
- <span data-ttu-id="be3b9-692">他のすべての奇数支払</span><span class="sxs-lookup"><span data-stu-id="be3b9-692">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="be3b9-693">他のすべての偶数支払</span><span class="sxs-lookup"><span data-stu-id="be3b9-693">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="be3b9-694">1 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-694">1OFMTH</span></span>
- <span data-ttu-id="be3b9-695">月の最終日</span><span class="sxs-lookup"><span data-stu-id="be3b9-695">LASTOFMTH</span></span>
- <span data-ttu-id="be3b9-696">2 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-696">2OFMTH</span></span>
- <span data-ttu-id="be3b9-697">3 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-697">3OFMTH</span></span>
- <span data-ttu-id="be3b9-698">4 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-698">4OFMTH</span></span>
- <span data-ttu-id="be3b9-699">5 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-699">5OFMTH</span></span>
- <span data-ttu-id="be3b9-700">1 か月および 2 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-700">1N2OFMTH</span></span>
- <span data-ttu-id="be3b9-701">3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-701">3N4OFMTH</span></span>
- <span data-ttu-id="be3b9-702">1 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-702">1N3OFMTH</span></span>
- <span data-ttu-id="be3b9-703">1 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-703">1N4OFMTH</span></span>
- <span data-ttu-id="be3b9-704">2 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-704">2N3OFMTH</span></span>
- <span data-ttu-id="be3b9-705">2 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-705">2N4OFMTH</span></span>
- <span data-ttu-id="be3b9-706">1 か月、2 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-706">1N2N3OFMTH</span></span>
- <span data-ttu-id="be3b9-707">1 か月、2 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-707">1N2N4OFMTH</span></span>
- <span data-ttu-id="be3b9-708">1 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-708">1N3N4OFMTH</span></span>
- <span data-ttu-id="be3b9-709">2 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-709">2N3N4OFMTH</span></span>
- <span data-ttu-id="be3b9-710">1 か月、2 か月、3 か月および 4 か月 - 1 か月、2 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="be3b9-711">2 か月、3 か月、4 か月および 5 か月 - 2 か月、3 か月、4 か月および 5 か月</span><span class="sxs-lookup"><span data-stu-id="be3b9-711">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="be3b9-712">四半期の 1 - 四半期の 1</span><span class="sxs-lookup"><span data-stu-id="be3b9-712">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="be3b9-713">四半期の最終日 – 四半期の最終日</span><span class="sxs-lookup"><span data-stu-id="be3b9-713">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="be3b9-714">四半期の最後の月 – 四半期の最後の月</span><span class="sxs-lookup"><span data-stu-id="be3b9-714">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="be3b9-715">1 年 - 1 年</span><span class="sxs-lookup"><span data-stu-id="be3b9-715">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="be3b9-716">年の最終日 – 年の最終日</span><span class="sxs-lookup"><span data-stu-id="be3b9-716">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="be3b9-717">年の 11 月および 12 月 - 年の 11 月および 12 月</span><span class="sxs-lookup"><span data-stu-id="be3b9-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="be3b9-718">住所</span><span class="sxs-lookup"><span data-stu-id="be3b9-718">Addresses</span></span>

<span data-ttu-id="be3b9-719">特定の国または地域、都道府県、および市区郡 (自治体) の ID には、Dayforce および国内または地域内のプロバイダーが認識できる特定の形式が必要です。</span><span class="sxs-lookup"><span data-stu-id="be3b9-719">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="be3b9-720">市町村の形式は柔軟ですが、すべての市町村が都道府県と関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="be3b9-720">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="be3b9-721">人事管理</span><span class="sxs-lookup"><span data-stu-id="be3b9-721">Human Resources</span></span>              | <span data-ttu-id="be3b9-722">Dayforce</span><span class="sxs-lookup"><span data-stu-id="be3b9-722">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="be3b9-723">国/地域</span><span class="sxs-lookup"><span data-stu-id="be3b9-723">Country/Region</span></span>      | <span data-ttu-id="be3b9-724">国コード</span><span class="sxs-lookup"><span data-stu-id="be3b9-724">Country Code</span></span>          |
| <span data-ttu-id="be3b9-725">郵便番号</span><span class="sxs-lookup"><span data-stu-id="be3b9-725">Zip/Postal Code</span></span>     | <span data-ttu-id="be3b9-726">郵便番号</span><span class="sxs-lookup"><span data-stu-id="be3b9-726">Postal Code</span></span>           |
| <span data-ttu-id="be3b9-727">行政単位 (区画)</span><span class="sxs-lookup"><span data-stu-id="be3b9-727">State</span></span>               | <span data-ttu-id="be3b9-728">都道府県コード</span><span class="sxs-lookup"><span data-stu-id="be3b9-728">State Code</span></span>            |
| <span data-ttu-id="be3b9-729">市町村</span><span class="sxs-lookup"><span data-stu-id="be3b9-729">City</span></span>                | <span data-ttu-id="be3b9-730">市町村</span><span class="sxs-lookup"><span data-stu-id="be3b9-730">City</span></span>                  |
| <span data-ttu-id="be3b9-731">郡</span><span class="sxs-lookup"><span data-stu-id="be3b9-731">County</span></span>              | <span data-ttu-id="be3b9-732">市区郡 (自治体)</span><span class="sxs-lookup"><span data-stu-id="be3b9-732">County (Municipality)</span></span> |
| <span data-ttu-id="be3b9-733">住所</span><span class="sxs-lookup"><span data-stu-id="be3b9-733">Street</span></span>              | <span data-ttu-id="be3b9-734">住所行 1</span><span class="sxs-lookup"><span data-stu-id="be3b9-734">Address Line 1</span></span>        |
| <span data-ttu-id="be3b9-735">番地</span><span class="sxs-lookup"><span data-stu-id="be3b9-735">Street Number</span></span>       | <span data-ttu-id="be3b9-736">住所行 2</span><span class="sxs-lookup"><span data-stu-id="be3b9-736">Address Line 2</span></span>        |
| <span data-ttu-id="be3b9-737">建物名</span><span class="sxs-lookup"><span data-stu-id="be3b9-737">Building Complement</span></span> | <span data-ttu-id="be3b9-738">住所行 5</span><span class="sxs-lookup"><span data-stu-id="be3b9-738">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="be3b9-739">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="be3b9-739">Passport number</span></span>

<span data-ttu-id="be3b9-740">従業員は、パスポート情報を申告できます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-740">Employees can declare passport information.</span></span> <span data-ttu-id="be3b9-741">この情報は、**パスポート** ID タイプになり、従業員のメキシコ固有の情報の一部として Dayforce に統合されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-741">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="be3b9-742">ID タイプ = "Passport"</span><span class="sxs-lookup"><span data-stu-id="be3b9-742">Identification Type = "Passport"</span></span>
- <span data-ttu-id="be3b9-743">発行日付</span><span class="sxs-lookup"><span data-stu-id="be3b9-743">Issued Date</span></span>
- <span data-ttu-id="be3b9-744">有効期限</span><span class="sxs-lookup"><span data-stu-id="be3b9-744">Expiration Date</span></span>

<span data-ttu-id="be3b9-745">従業員は、**パスポート** ID タイプの複数の ID 番号を申告できます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-745">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="be3b9-746">ただし、現在の有効なパスポート入力のみが Dayforce に統合されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-746">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="be3b9-747">すべてのパスポート入力が期限切れの場合、最後に発行されたパスポートが Dayforce に統合されます。</span><span class="sxs-lookup"><span data-stu-id="be3b9-747">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

