---
title: Dayforce との統合を構成する
description: Microsoft Dynamics 365 Human Resources および Ceridian Dayforce 間での統合は、この記事で説明するいくつかの構成手順に依存します。 支払の実行を処理する前に、Human Resources および Dayforce の両方で、統合を構成する必要があります。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d150daa92fe79cf6620ce5ddf1a01f369c64053
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051500"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="d53ed-104">Dayforce との統合を構成する</span><span class="sxs-lookup"><span data-stu-id="d53ed-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d53ed-105">Microsoft Dynamics 365 Human Resources および Ceridian Dayforce 間での統合は、この記事で説明するいくつかの構成手順に依存します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="d53ed-106">支払の実行を処理する前に、Human Resources および Dayforce の両方で、統合を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="d53ed-107">支払の実行を完了するため Dayforce などのサービスを使用する場合、Human Resources 内の統合を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="d53ed-108">統合には Human Resources からの固有のデータが必要です。</span><span class="sxs-lookup"><span data-stu-id="d53ed-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="d53ed-109">したがって、Dayforce にマップされているデータが、統合をサポートする方法で Human Resources 内で構成されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="d53ed-110">統合は次の広範なデータ カテゴリを使用します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="d53ed-111">人事管理データ</span><span class="sxs-lookup"><span data-stu-id="d53ed-111">Human resources data</span></span>
- <span data-ttu-id="d53ed-112">報酬データ</span><span class="sxs-lookup"><span data-stu-id="d53ed-112">Compensation data</span></span>
- <span data-ttu-id="d53ed-113">支払サイクル、支払期間、および所得コードなどの給与データ</span><span class="sxs-lookup"><span data-stu-id="d53ed-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="d53ed-114">作業者データ</span><span class="sxs-lookup"><span data-stu-id="d53ed-114">Worker data</span></span>

<span data-ttu-id="d53ed-115">この記事では、統合を有効にするために従う必要がある手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="d53ed-116">統合に必要なデータの種類およびコンフィギュレーションの詳細についても説明します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="d53ed-117">統合の有効化</span><span class="sxs-lookup"><span data-stu-id="d53ed-117">Enable the integration</span></span>

<span data-ttu-id="d53ed-118">Human Resources 内で統合を有効にし、Dayforce に接続する構成情報を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="d53ed-119">生成される一般会計トランザクションを Microsoft Dynamics 365 Finance にインポートしたい場合、Microsoft Azure ストレージ アカウントを設定し、Finance 内で、Azure Storage の接続文字列を入力する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="d53ed-120">Human Resources 内で統合を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d53ed-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="d53ed-121">**システム管理** ページで、**統合コンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="d53ed-122">セキュリティで保護された FTP (File Transfer Protocol) のエンドポイント、およびセキュリティで保護された FTP フォルダー パスを入力します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="d53ed-123">セキュリティで保護された FTP エンドポイントおよびフォルダー パスにアクセスするユーザーのユーザー名とパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="d53ed-124">必要に応じて接続をテストし、**給与統合の有効化** のオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="d53ed-125">統合が有効な場合、データのエクスポート パッケージおよびファイルが作成され、頻度が設定されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="d53ed-126">必要に応じて、この頻度を変更できます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="d53ed-127">Azure Storage アカウント および Azure Storage の接続文字列の詳細については、次の Azure の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d53ed-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="d53ed-128">Azure ストレージ アカウントについて</span><span class="sxs-lookup"><span data-stu-id="d53ed-128">About Azure storage accounts</span></span>](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="d53ed-129">Azure ストレージの接続文字列のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d53ed-129">Configure Azure Storage connection strings</span></span>](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="d53ed-130">給与統合が有効になっている場合の技術詳細</span><span class="sxs-lookup"><span data-stu-id="d53ed-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="d53ed-131">給与統合を有効にすることには、次の 2 つの主な効果があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="d53ed-132">「給与統合エクスポート」という名前のデータ エクスポート プロジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="d53ed-133">このプロジェクトには、給与統合に必要なエンティティとフィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d53ed-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="d53ed-134">プロジェクトを確認するには、**システム管理** に移動し、**データ管理** タイルを選択して、プロジェクトの一覧からデータ プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="d53ed-135">このバッチ ジョブは、データ エクスポート プロジェクトを実行し、結果のデータ パッケージを暗号化し、**統合コンフィギュレーション** 画面でコンフィギュレーションされた SFTP エンドポイントにデータ パッケージ ファイルを転送します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="d53ed-136">SFTP エンドポイントに転送されるデータ パッケージは、そのパッケージに固有のキーを使用して暗号化されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="d53ed-137">キーは、Ceridian によってのみアクセス可能な Azure Key Vault にあります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="d53ed-138">データ パッケージの内容を復号化して確認することはできません。</span><span class="sxs-lookup"><span data-stu-id="d53ed-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="d53ed-139">データ パッケージの内容を確認する必要がある場合は、"給与統合エクスポート" データ プロジェクトを手動でエクスポートし、ダウンロードしてから、それを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="d53ed-140">手動エクスポートでは、暗号化が適用されないか、またはパッケージが転送されません。</span><span class="sxs-lookup"><span data-stu-id="d53ed-140">Manual export will not apply encryption or transfer the package.</span></span>
> <span data-ttu-id="d53ed-141">統合ファイルが Dynamics 365 Human Resources UAT またはサンドボックス環境から Ceridian Dayforce Test 環境に送信される場合は、次のキー コンテナー URL を使用できます: https://payrollintegrationprod.vault.azure.net。</span><span class="sxs-lookup"><span data-stu-id="d53ed-141">For instances where the integration files are sent from a Dynamics 365 Human Resources UAT or Sandbox environment to a Ceridian Dayforce Test environment, you can use the following key vault URL: https://payrollintegrationprod.vault.azure.net.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="d53ed-142">データのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d53ed-142">Configure your data</span></span> 

<span data-ttu-id="d53ed-143">給与を処理するには、Human Resources で人事管理のデータを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-143">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="d53ed-144">職務と職位などの組織データを、給付金および報酬情報と共に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-144">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="d53ed-145">この情報は、雇用、支払、および従業員の給与を生成するために必要な控除情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-145">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="d53ed-146">人事管理データ</span><span class="sxs-lookup"><span data-stu-id="d53ed-146">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="d53ed-147">福利厚生</span><span class="sxs-lookup"><span data-stu-id="d53ed-147">Benefits</span></span> 

<span data-ttu-id="d53ed-148">人事管理は、給付金、控除、および組織が作業者に対して提供または処理する作業者の報酬プランを設定および管理するツールを提供します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-148">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="d53ed-149">給付金を作成する場合、Dayforce で使用される次のデータとコンフィギュレーションに留意してください。</span><span class="sxs-lookup"><span data-stu-id="d53ed-149">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="d53ed-150">福利厚生計画</span><span class="sxs-lookup"><span data-stu-id="d53ed-150">Benefit plans</span></span>

- <span data-ttu-id="d53ed-151">計画 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-151">Plan (required)</span></span>
- <span data-ttu-id="d53ed-152">種類 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-152">Type (required)</span></span>
- <span data-ttu-id="d53ed-153">給与の影響 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-153">Payroll impact (required)</span></span>
- <span data-ttu-id="d53ed-154">未払金の回収</span><span class="sxs-lookup"><span data-stu-id="d53ed-154">Recover arrears</span></span>
- <span data-ttu-id="d53ed-155">控除方式</span><span class="sxs-lookup"><span data-stu-id="d53ed-155">Deduction method</span></span>
- <span data-ttu-id="d53ed-156">控除の優先順位</span><span class="sxs-lookup"><span data-stu-id="d53ed-156">Deduction priority</span></span>
- <span data-ttu-id="d53ed-157">制限の期間</span><span class="sxs-lookup"><span data-stu-id="d53ed-157">Limit period</span></span>
- <span data-ttu-id="d53ed-158">限度金額</span><span class="sxs-lookup"><span data-stu-id="d53ed-158">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="d53ed-159">福利厚生</span><span class="sxs-lookup"><span data-stu-id="d53ed-159">Benefits</span></span>

- <span data-ttu-id="d53ed-160">計画 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-160">Plan (required)</span></span>
- <span data-ttu-id="d53ed-161">種類 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-161">Type (required)</span></span>
- <span data-ttu-id="d53ed-162">オプション (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-162">Option (required)</span></span>
- <span data-ttu-id="d53ed-163">給付金 ID (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-163">Benefit ID (required)</span></span>
- <span data-ttu-id="d53ed-164">頻度</span><span class="sxs-lookup"><span data-stu-id="d53ed-164">Frequency</span></span>
- <span data-ttu-id="d53ed-165">基準</span><span class="sxs-lookup"><span data-stu-id="d53ed-165">Basis</span></span>
- <span data-ttu-id="d53ed-166">金額またはレート</span><span class="sxs-lookup"><span data-stu-id="d53ed-166">Amount or rate</span></span>
- <span data-ttu-id="d53ed-167">所得コード</span><span class="sxs-lookup"><span data-stu-id="d53ed-167">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="d53ed-168">サポートされる頻度</span><span class="sxs-lookup"><span data-stu-id="d53ed-168">Supported frequencies</span></span> 

- <span data-ttu-id="d53ed-169">毎週</span><span class="sxs-lookup"><span data-stu-id="d53ed-169">Weekly</span></span>
- <span data-ttu-id="d53ed-170">隔週</span><span class="sxs-lookup"><span data-stu-id="d53ed-170">Bi-weekly</span></span>
- <span data-ttu-id="d53ed-171">半月ごと</span><span class="sxs-lookup"><span data-stu-id="d53ed-171">Semi-monthly</span></span>
- <span data-ttu-id="d53ed-172">月 1 回</span><span class="sxs-lookup"><span data-stu-id="d53ed-172">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="d53ed-173">サポートされる基準</span><span class="sxs-lookup"><span data-stu-id="d53ed-173">Supported bases</span></span> 

- <span data-ttu-id="d53ed-174">固定金額</span><span class="sxs-lookup"><span data-stu-id="d53ed-174">Fixed amount</span></span>
- <span data-ttu-id="d53ed-175">所得の割合</span><span class="sxs-lookup"><span data-stu-id="d53ed-175">Percent of earnings</span></span>
- <span data-ttu-id="d53ed-176">生産時間</span><span class="sxs-lookup"><span data-stu-id="d53ed-176">Productive hours</span></span>

<span data-ttu-id="d53ed-177">Dayforce は、給付金の計画で定義される給与影響に基づいて次の控除を作成します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-177">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="d53ed-178">Human Resources における選択</span><span class="sxs-lookup"><span data-stu-id="d53ed-178">Selection in Human Resources</span></span>        | <span data-ttu-id="d53ed-179">Dayforce での結果</span><span class="sxs-lookup"><span data-stu-id="d53ed-179">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="d53ed-180">なし</span><span class="sxs-lookup"><span data-stu-id="d53ed-180">None</span></span>                       | <span data-ttu-id="d53ed-181">控除は作成されません。</span><span class="sxs-lookup"><span data-stu-id="d53ed-181">No deduction is created.</span></span>                      |
| <span data-ttu-id="d53ed-182">控除のみ</span><span class="sxs-lookup"><span data-stu-id="d53ed-182">Deduction only</span></span>             | <span data-ttu-id="d53ed-183">従業員控除が作成されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-183">An employee deduction is created.</span></span>             |
| <span data-ttu-id="d53ed-184">貢献度のみ</span><span class="sxs-lookup"><span data-stu-id="d53ed-184">Contribution only</span></span>          | <span data-ttu-id="d53ed-185">雇用主控除が作成されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-185">An employer deduction is created.</span></span>             |
| <span data-ttu-id="d53ed-186">控除と貢献度</span><span class="sxs-lookup"><span data-stu-id="d53ed-186">Deduction and contribution</span></span> | <span data-ttu-id="d53ed-187">従業員および雇用主の控除が作成されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-187">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="d53ed-188">給付金プログラムを定義し、管理する方法の詳細については、次の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d53ed-188">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="d53ed-189">従業員手当プログラムの提供</span><span class="sxs-lookup"><span data-stu-id="d53ed-189">Deliver an employee benefits program</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="d53ed-190">新しい給付金の作成</span><span class="sxs-lookup"><span data-stu-id="d53ed-190">Create a new benefit</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="d53ed-191">給付金の適格性ルールおよびポリシーの定義</span><span class="sxs-lookup"><span data-stu-id="d53ed-191">Define benefit eligibility rules and policies</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="d53ed-192">作業者の福利厚生の登録および削除</span><span class="sxs-lookup"><span data-stu-id="d53ed-192">Enroll and remove benefits from workers</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="d53ed-193">報酬</span><span class="sxs-lookup"><span data-stu-id="d53ed-193">Compensation</span></span> 

<span data-ttu-id="d53ed-194">基準賃金と報奨を管理するには、報酬管理を使用します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-194">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="d53ed-195">従業員の固定基準賃金および昇給は固定報酬プランで管理されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-195">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="d53ed-196">インセンティブ支払 (賞与の支払、業績報奨、ストック オプション、付与など) の支払および一時報奨は変動報酬プランで管理します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-196">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="d53ed-197">Dayforce は、報酬情報を使用して、従業員の時間または年間レートを計算します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-197">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="d53ed-198">固定報酬プランと支払レートの換算が必要です。</span><span class="sxs-lookup"><span data-stu-id="d53ed-198">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="d53ed-199">従業員は固定報酬プランに関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-199">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="d53ed-200">報酬プランの詳細については、次の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d53ed-200">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="d53ed-201">固定報酬プランの作成</span><span class="sxs-lookup"><span data-stu-id="d53ed-201">Create fixed compensation plans</span></span>](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="d53ed-202">変動報酬プランの作成</span><span class="sxs-lookup"><span data-stu-id="d53ed-202">Create variable compensation plans</span></span>](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="d53ed-203">給与/報酬構造および計画の作成</span><span class="sxs-lookup"><span data-stu-id="d53ed-203">Develop salary/compensation structure and plans</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="d53ed-204">報酬の処理</span><span class="sxs-lookup"><span data-stu-id="d53ed-204">Process compensation</span></span>](/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="d53ed-205">報酬プロセスの定義と結果の計算</span><span class="sxs-lookup"><span data-stu-id="d53ed-205">Define compensation process and calculate results</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="d53ed-206">固定報酬プランへの従業員の登録</span><span class="sxs-lookup"><span data-stu-id="d53ed-206">Enroll an employee in a fixed compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="d53ed-207">変動報酬プランへの従業員の登録</span><span class="sxs-lookup"><span data-stu-id="d53ed-207">Enroll an employee in a variable compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="d53ed-208">職務</span><span class="sxs-lookup"><span data-stu-id="d53ed-208">Jobs</span></span> 

<span data-ttu-id="d53ed-209">職務とは、職務を遂行する担当者に必要なタスクと職責の集合です。</span><span class="sxs-lookup"><span data-stu-id="d53ed-209">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="d53ed-210">詳細については、次の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d53ed-210">For more information, see the following articles:</span></span>

- [<span data-ttu-id="d53ed-211">職務のコンポーネントの設定</span><span class="sxs-lookup"><span data-stu-id="d53ed-211">Setting up the components of a job</span></span>](/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="d53ed-212">新しい職務の定義</span><span class="sxs-lookup"><span data-stu-id="d53ed-212">Define new jobs</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="d53ed-213">職位</span><span class="sxs-lookup"><span data-stu-id="d53ed-213">Positions</span></span>

<span data-ttu-id="d53ed-214">職位は、職務の個々のインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="d53ed-214">A position is an individual instance of a job.</span></span> <span data-ttu-id="d53ed-215">たとえば、「販売マネージャー (東部)」という職位は、「販売マネージャー」という職務に関連付けられている職位の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="d53ed-215">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="d53ed-216">職位は、部門内に存在します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-216">A position exists in a department.</span></span> <span data-ttu-id="d53ed-217">1 人の作業者は 1 つの職位にのみ関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-217">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="d53ed-218">職位を設定する場合、次のデータとコンフィギュレーションに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d53ed-218">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="d53ed-219">職位 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-219">Position (required)</span></span>
- <span data-ttu-id="d53ed-220">説明 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-220">Description (required)</span></span>
- <span data-ttu-id="d53ed-221">職務 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-221">Job (required)</span></span>
- <span data-ttu-id="d53ed-222">部門 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-222">Department (required)</span></span>
- <span data-ttu-id="d53ed-223">職位タイプ (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-223">Position type (required)</span></span>
- <span data-ttu-id="d53ed-224">フルタイム相当</span><span class="sxs-lookup"><span data-stu-id="d53ed-224">Full-time equivalent</span></span>
- <span data-ttu-id="d53ed-225">年間基本勤務時間 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-225">Annual regular hours (required)</span></span>
- <span data-ttu-id="d53ed-226">法人による支払 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-226">Paid by legal entity (required)</span></span>
- <span data-ttu-id="d53ed-227">支払サイクル (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-227">Pay cycle (required)</span></span>
- <span data-ttu-id="d53ed-228">既定の財務分析コード – 原価部門 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-228">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="d53ed-229">作業者割り当て – 作業者、割り当ての開始、割り当ての終了、理由コード</span><span class="sxs-lookup"><span data-stu-id="d53ed-229">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="d53ed-230">同じ部門の複数の職位が同じジョブに関連付けられている場合、Dayforce で 1 つの職位に連結します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-230">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="d53ed-231">詳細については、次の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d53ed-231">For more information, see the following articles:</span></span>

- [<span data-ttu-id="d53ed-232">部門、職務、職位を使用した従業員の編成</span><span class="sxs-lookup"><span data-stu-id="d53ed-232">Organize your workforce using departments, jobs, and positions</span></span>](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="d53ed-233">職位の設定</span><span class="sxs-lookup"><span data-stu-id="d53ed-233">Set up positions</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="d53ed-234">部門</span><span class="sxs-lookup"><span data-stu-id="d53ed-234">Departments</span></span>

<span data-ttu-id="d53ed-235">部門は、組織のカテゴリまたは機能領域を表す作業単位です。</span><span class="sxs-lookup"><span data-stu-id="d53ed-235">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="d53ed-236">部門は、販売、会計、または人事管理など、組織内の特定の領域を担当します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-236">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="d53ed-237">機能領域の報告に部門を使用できます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-237">You can use departments to report on functional areas.</span></span> <span data-ttu-id="d53ed-238">部門は損益の職責を持つ場合があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-238">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="d53ed-239">詳細については、次の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d53ed-239">For more information, see the following articles:</span></span>

- [<span data-ttu-id="d53ed-240">部門の作成と部門階層への関連付け</span><span class="sxs-lookup"><span data-stu-id="d53ed-240">Create a department and associate it with the department hierarchy</span></span>](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="d53ed-241">新しい部門の定義</span><span class="sxs-lookup"><span data-stu-id="d53ed-241">Define new departments</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="d53ed-242">支払サイクルと支払期間</span><span class="sxs-lookup"><span data-stu-id="d53ed-242">Pay cycles and pay periods</span></span>

<span data-ttu-id="d53ed-243">給与計算頻度および作業者が支払を受ける特定の日は、支払サイクルによって決まります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-243">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="d53ed-244">たとえば、支払サイクルが月単位で、その月の最後の日に従業員に支払われる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-244">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="d53ed-245">または、支払サイクルが週単位で、支払期間終了日の次の火曜日に支払われる場合もあります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-245">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="d53ed-246">支払サイクルは、それらの職位にある作業者にいつ支払われるかを制御するために、職位に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-246">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="d53ed-247">支払サイクルを作成した後、各サイクルごとに支払期間を生成できます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-247">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="d53ed-248">各支払期間には、入力した情報に基づく既定の支払期日が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-248">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="d53ed-249">ただし、支払期日が休日になる場合などの例外を許可するため、支払期間の既定の支払期日を変更できます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-249">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="d53ed-250">次の情報は、Dayforce で使用されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-250">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="d53ed-251">支払サイクル (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-251">Pay cycle (required)</span></span>
- <span data-ttu-id="d53ed-252">支払サイクル頻度 (頻度)</span><span class="sxs-lookup"><span data-stu-id="d53ed-252">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="d53ed-253">期間開始日 (最初の支払期間は必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-253">Period start date (first pay period required)</span></span>
- <span data-ttu-id="d53ed-254">既定の支払期日 (最初の支払期間は必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-254">Default payment date (first pay period required)</span></span>

<span data-ttu-id="d53ed-255">この情報は、支払グループとして Dayforce に統合され、各支払サイクルごとに国または地域で区切られます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-255">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="d53ed-256">統合の前に、少なくとも 1 つの支払期間を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-256">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="d53ed-257">Dayforce は、最初の支払期日の開始日および Human Resources で設定された既定の支払期日に基づいて、支払グループのカレンダーと支払期日を生成します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-257">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="d53ed-258">所得コード</span><span class="sxs-lookup"><span data-stu-id="d53ed-258">Earning codes</span></span>

<span data-ttu-id="d53ed-259">所得コードは、作業者が受け取るすべての収益のタイプを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-259">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d53ed-260">コードには、会計ルール、税法、レポート要件、およびグロスアップ能力など、所得に関連付けられているさまざまなパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-260">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="d53ed-261">次の情報は、Dayforce で使用されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-261">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="d53ed-262">所得コード (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-262">Earning Code (required)</span></span>
- <span data-ttu-id="d53ed-263">説明</span><span class="sxs-lookup"><span data-stu-id="d53ed-263">Description</span></span>
- <span data-ttu-id="d53ed-264">計量単位</span><span class="sxs-lookup"><span data-stu-id="d53ed-264">Unit of measure</span></span>
- <span data-ttu-id="d53ed-265">生産</span><span class="sxs-lookup"><span data-stu-id="d53ed-265">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="d53ed-266">作業者データ</span><span class="sxs-lookup"><span data-stu-id="d53ed-266">Worker data</span></span>

<span data-ttu-id="d53ed-267">人事管理と給与システムにとって、所有しているさまざまなタイプの作業者のレコードは重要です。</span><span class="sxs-lookup"><span data-stu-id="d53ed-267">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="d53ed-268">入力された情報を使用して、作業者と個人情報を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-268">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="d53ed-269">作業者には次の情報を管理できます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-269">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="d53ed-270">**基本** – 連絡先情報、人口学的情報、識別情報、家族情報、兵役の状態、海外在住情報、自宅、緊急連絡先など、作業者に関する基本的な情報を管理します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-270">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="d53ed-271">**雇用** – 法人や組織への所属、職位割り当て、開始日と終了日、業務適性、雇用条件、年金、休暇、再配置情報など、作業者の雇用に関する情報を管理します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-271">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="d53ed-272">**休暇** – 作業カレンダー、休暇トランザクション、休暇設定など、作業者の休暇に関する情報を管理します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-272">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="d53ed-273">**報酬と給与** – プラン登録、報奨、実績、手数料、税金情報、退職、給与控除など、作業者の報酬プランと給与情報に関する情報を管理します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-273">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="d53ed-274">作業者情報を入力する場合、Dayforce で使用される次のデータとコンフィギュレーションに留意してください。</span><span class="sxs-lookup"><span data-stu-id="d53ed-274">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="d53ed-275">一般情報</span><span class="sxs-lookup"><span data-stu-id="d53ed-275">General information</span></span>

- <span data-ttu-id="d53ed-276">個人番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-276">Personnel number (required)</span></span>
- <span data-ttu-id="d53ed-277">名 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-277">First name (required)</span></span>
- <span data-ttu-id="d53ed-278">姓 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-278">Last name (required)</span></span>
- <span data-ttu-id="d53ed-279">ミドル ネーム</span><span class="sxs-lookup"><span data-stu-id="d53ed-279">Middle name</span></span>
- <span data-ttu-id="d53ed-280">勤続日数</span><span class="sxs-lookup"><span data-stu-id="d53ed-280">Seniority date</span></span>
- <span data-ttu-id="d53ed-281">呼称</span><span class="sxs-lookup"><span data-stu-id="d53ed-281">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="d53ed-282">個人情報</span><span class="sxs-lookup"><span data-stu-id="d53ed-282">Personal information</span></span>

- <span data-ttu-id="d53ed-283">配偶者の有無 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-283">Marital status (required)</span></span>
- <span data-ttu-id="d53ed-284">生年月日 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-284">Birth date (required)</span></span>
- <span data-ttu-id="d53ed-285">性別 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-285">Gender (required)</span></span>
- <span data-ttu-id="d53ed-286">障碍のあるユーザー</span><span class="sxs-lookup"><span data-stu-id="d53ed-286">Person with disabilities</span></span>
- <span data-ttu-id="d53ed-287">国籍 国 地域 (メキシコの場合のみ)</span><span class="sxs-lookup"><span data-stu-id="d53ed-287">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="d53ed-288">住所情報</span><span class="sxs-lookup"><span data-stu-id="d53ed-288">Address information</span></span>

- <span data-ttu-id="d53ed-289">基本 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-289">Primary (required)</span></span>
- <span data-ttu-id="d53ed-290">国/地域 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-290">Country/region (required)</span></span>
- <span data-ttu-id="d53ed-291">郵便番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-291">Postal code (required)</span></span>
- <span data-ttu-id="d53ed-292">番地 (必須) (メキシコの場合のみ)</span><span class="sxs-lookup"><span data-stu-id="d53ed-292">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="d53ed-293">建物名 (メキシコの場合のみ)</span><span class="sxs-lookup"><span data-stu-id="d53ed-293">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="d53ed-294">市町村 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-294">City (required)</span></span>
- <span data-ttu-id="d53ed-295">都道府県 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-295">State (required)</span></span>
- <span data-ttu-id="d53ed-296">国 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-296">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="d53ed-297">連絡先情報</span><span class="sxs-lookup"><span data-stu-id="d53ed-297">Contact information</span></span> 

- <span data-ttu-id="d53ed-298">基本 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-298">Primary (required)</span></span>
- <span data-ttu-id="d53ed-299">連絡先の電話番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-299">Contact number (required)</span></span>
- <span data-ttu-id="d53ed-300">内線</span><span class="sxs-lookup"><span data-stu-id="d53ed-300">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="d53ed-301">給与情報および所得コード</span><span class="sxs-lookup"><span data-stu-id="d53ed-301">Payroll information and earning codes</span></span>

<span data-ttu-id="d53ed-302">従業員は、指定された支払頻度で特定の所得が割り当てられ、希望の支払方法を有する場合があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-302">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="d53ed-303">次のフィールドは、それらの基本設定と設定が使用されることを保証するために Dayforce で使用されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-303">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="d53ed-304">所得コード</span><span class="sxs-lookup"><span data-stu-id="d53ed-304">Earning codes</span></span>

- <span data-ttu-id="d53ed-305">職位 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-305">Position (required)</span></span>
- <span data-ttu-id="d53ed-306">所得コード (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-306">Earning Code (required)</span></span>
- <span data-ttu-id="d53ed-307">頻度 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-307">Frequency (required)</span></span>
- <span data-ttu-id="d53ed-308">金額 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-308">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="d53ed-309">給与情報</span><span class="sxs-lookup"><span data-stu-id="d53ed-309">Payroll information</span></span>

- <span data-ttu-id="d53ed-310">支払方法</span><span class="sxs-lookup"><span data-stu-id="d53ed-310">Payment Method</span></span>
- <span data-ttu-id="d53ed-311">経済地域 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-311">Economic Region (required)</span></span>
- <span data-ttu-id="d53ed-312">従業員手当 ID</span><span class="sxs-lookup"><span data-stu-id="d53ed-312">Employee Benefits ID</span></span>
- <span data-ttu-id="d53ed-313">国民 ID 番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-313">National ID Number (required)</span></span>
- <span data-ttu-id="d53ed-314">兵役番号</span><span class="sxs-lookup"><span data-stu-id="d53ed-314">Military Service Number</span></span>
- <span data-ttu-id="d53ed-315">シフト ID (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-315">Shift ID (required)</span></span>
- <span data-ttu-id="d53ed-316">税番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-316">Tax Number (required)</span></span>
- <span data-ttu-id="d53ed-317">労働組合 ID (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-317">Union ID (required)</span></span>
- <span data-ttu-id="d53ed-318">作業日 ID (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-318">Work Day ID (required)</span></span>
- <span data-ttu-id="d53ed-319">労働許可番号</span><span class="sxs-lookup"><span data-stu-id="d53ed-319">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="d53ed-320">支払方法について、メキシコでは **現金**、**小切手** (会社の現物小切手)、および **電子支払** がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-320">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="d53ed-321">NP 支払方法が指定されている場合、既定で **小切手** が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-321">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="d53ed-322">従業員の詳細</span><span class="sxs-lookup"><span data-stu-id="d53ed-322">Employment details</span></span>

<span data-ttu-id="d53ed-323">雇用の詳細履歴は、Dayforce で従業員の採用、退職、および再雇用のステータスを派生させるため、重要な情報として使用されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-323">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="d53ed-324">Dayforce は、一度に 1 つだけ有効な雇用レコードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d53ed-324">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="d53ed-325">雇用開始日 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-325">Employment start date (required)</span></span>
- <span data-ttu-id="d53ed-326">雇用終了日</span><span class="sxs-lookup"><span data-stu-id="d53ed-326">Employment end date</span></span>
- <span data-ttu-id="d53ed-327">入社日</span><span class="sxs-lookup"><span data-stu-id="d53ed-327">Start date</span></span>
- <span data-ttu-id="d53ed-328">調整済開始日</span><span class="sxs-lookup"><span data-stu-id="d53ed-328">Adjusted start date</span></span>
- <span data-ttu-id="d53ed-329">退職日 (退職時は必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-329">Termination date (required upon termination)</span></span>
- <span data-ttu-id="d53ed-330">退職理由 (退職時は必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-330">Termination reason (required upon termination)</span></span>

<span data-ttu-id="d53ed-331">従業員の重要な日付は、次の情報を使用して派生されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-331">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="d53ed-332">人事管理</span><span class="sxs-lookup"><span data-stu-id="d53ed-332">Human Resources</span></span>                | <span data-ttu-id="d53ed-333">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d53ed-333">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d53ed-334">最新の採用日付</span><span class="sxs-lookup"><span data-stu-id="d53ed-334">Most recent hire date</span></span> | <span data-ttu-id="d53ed-335">現在の非退職雇用履歴レコードの雇用開始</span><span class="sxs-lookup"><span data-stu-id="d53ed-335">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="d53ed-336">退職日</span><span class="sxs-lookup"><span data-stu-id="d53ed-336">Termination date</span></span>      | <span data-ttu-id="d53ed-337">現在の非退職雇用履歴レコードの退職日</span><span class="sxs-lookup"><span data-stu-id="d53ed-337">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="d53ed-338">入社日</span><span class="sxs-lookup"><span data-stu-id="d53ed-338">Start date</span></span>            | <span data-ttu-id="d53ed-339">現在の非アクティブ雇用履歴レコードの調整済開始日、開始日、または雇用開始</span><span class="sxs-lookup"><span data-stu-id="d53ed-339">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="d53ed-340">元の採用日付</span><span class="sxs-lookup"><span data-stu-id="d53ed-340">Original hire date</span></span>    | <span data-ttu-id="d53ed-341">最も早い雇用履歴レコードの雇用開始</span><span class="sxs-lookup"><span data-stu-id="d53ed-341">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="d53ed-342">報酬</span><span class="sxs-lookup"><span data-stu-id="d53ed-342">Compensation</span></span>

<span data-ttu-id="d53ed-343">固定報酬計画は、雇用期間全体ですべての従業員の基本職位に関連付けられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-343">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="d53ed-344">この期間は、従業員が採用された日付 (または雇用の開始日) に開始し、退職するまで継続します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-344">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="d53ed-345">有効日 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-345">Effective Date (required)</span></span>
- <span data-ttu-id="d53ed-346">有効期限</span><span class="sxs-lookup"><span data-stu-id="d53ed-346">Expiration date</span></span>
- <span data-ttu-id="d53ed-347">支払レート (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-347">Pay Rate (required)</span></span>
- <span data-ttu-id="d53ed-348">支払レートの変換 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-348">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="d53ed-349">年間相当額 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-349">Annual equivalent (required)</span></span>
- <span data-ttu-id="d53ed-350">時間相当額 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-350">Hourly equivalent (required)</span></span>

<span data-ttu-id="d53ed-351">時給払いの従業員に複数の職位がある場合、基本職位の固定報酬が作業者レベルの基準レートまたは給与として Dayforce にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-351">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="d53ed-352">基本以外の職位については、時給のレートが Dayforce の対応する職位に保存されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-352">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="d53ed-353">月給払いの従業員に複数の職位がある場合、累計時間率およびすべての有効な職位全体での年間給与が派生され、従業員レベルの基準レートまたは給与として使用されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-353">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="d53ed-354">ID 番号</span><span class="sxs-lookup"><span data-stu-id="d53ed-354">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="d53ed-355">社会保障 ID</span><span class="sxs-lookup"><span data-stu-id="d53ed-355">Social Security identifier</span></span> 

<span data-ttu-id="d53ed-356">すべての従業員は、1 つの基本 ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="d53ed-356">Every employee must have one primary identifier.</span></span> <span data-ttu-id="d53ed-357">この ID は **SSN** ID タイプにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-357">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="d53ed-358">Dayforce では、採用に必要な従業員の社会保障 ID として自動的に派生されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-358">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="d53ed-359">基本 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-359">Primary (required)</span></span>
- <span data-ttu-id="d53ed-360">ID タイプ = "SSN"</span><span class="sxs-lookup"><span data-stu-id="d53ed-360">Identification Type = "SSN"</span></span>
- <span data-ttu-id="d53ed-361">発行日付</span><span class="sxs-lookup"><span data-stu-id="d53ed-361">Issued Date</span></span>
- <span data-ttu-id="d53ed-362">有効期限</span><span class="sxs-lookup"><span data-stu-id="d53ed-362">Expiration Date</span></span>

<span data-ttu-id="d53ed-363">従業員は、**SSN** ID タイプの複数の ID 番号を申告できます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-363">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="d53ed-364">ただし、その番号が有効かまたは期限切れかに関係なく、**基本** としてマークされているレコードのみ Dayforce に統合されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-364">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="d53ed-365">銀行口座および出金</span><span class="sxs-lookup"><span data-stu-id="d53ed-365">Bank accounts and disbursements</span></span>

<span data-ttu-id="d53ed-366">銀行口座振替による支払を選択した従業員すべてのために、有効な銀行口座情報を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-366">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="d53ed-367">人事管理</span><span class="sxs-lookup"><span data-stu-id="d53ed-367">Human Resources</span></span>                         | <span data-ttu-id="d53ed-368">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d53ed-368">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d53ed-369">銀行口座番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-369">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="d53ed-370">SWIFT コード (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-370">SWIFT code (required)</span></span>          | <span data-ttu-id="d53ed-371">メキシコの給与処理に使用される **銀行 ID** フィールド。</span><span class="sxs-lookup"><span data-stu-id="d53ed-371">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="d53ed-372">支店番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-372">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="d53ed-373">銀行口座の種類 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-373">Bank account type (required)</span></span>   | <span data-ttu-id="d53ed-374">メキシコの給与処理に使用される **口座の種類** フィールド。</span><span class="sxs-lookup"><span data-stu-id="d53ed-374">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="d53ed-375">サポートされている値には、**当座預金** および **給与** が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-375">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="d53ed-376">銀行口座振替による支払を選択した従業員は、メキシコに基本住所を持つ法人の下にあり、メキシコの銀行から有効な銀行口座に関連付けられている残余口座のリンクを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-376">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="d53ed-377">その他のすべての非残余口座は無視されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-377">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="d53ed-378">住所情報</span><span class="sxs-lookup"><span data-stu-id="d53ed-378">Address information</span></span>

<span data-ttu-id="d53ed-379">すべての従業員は、1 つの基本場所が必要です。</span><span class="sxs-lookup"><span data-stu-id="d53ed-379">Every employee must have one primary location.</span></span> <span data-ttu-id="d53ed-380">Dayforce において、この場所は課税額算出のために従業員の基本居住地を特定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-380">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="d53ed-381">基本 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-381">Primary (required)</span></span>
- <span data-ttu-id="d53ed-382">国/地域 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-382">Country/region (required)</span></span>
- <span data-ttu-id="d53ed-383">郵便番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-383">Zip/postal code (required)</span></span>
- <span data-ttu-id="d53ed-384">住所 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-384">Street (required)</span></span>
- <span data-ttu-id="d53ed-385">番地 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-385">Street Number (required)</span></span>
- <span data-ttu-id="d53ed-386">建物名</span><span class="sxs-lookup"><span data-stu-id="d53ed-386">Building Complement</span></span>
- <span data-ttu-id="d53ed-387">市町村 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-387">City (required)</span></span>
- <span data-ttu-id="d53ed-388">都道府県 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-388">State (required)</span></span>
- <span data-ttu-id="d53ed-389">国 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-389">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="d53ed-390">米国およびカナダでの給与を生成するために、データをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="d53ed-390">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="d53ed-391">米国およびカナダの従業員のために支払を生成している場合、次の要素をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-391">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="d53ed-392">職位に部門が必要です。</span><span class="sxs-lookup"><span data-stu-id="d53ed-392">Departments are required on positions.</span></span>
- <span data-ttu-id="d53ed-393">原価部門を財務分析コードとして設定し、既定の財務分析コード文字列の最初の要素とする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-393">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="d53ed-394">職位が部門を指定するように Human Resources を構成することができます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-394">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="d53ed-395">この作業を実行するには、**人事管理共有職位 > 職位 > 職位の部門を要求** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-395">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="d53ed-396">この設定は、システムの統合に適用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d53ed-396">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="d53ed-397">職務タイプ</span><span class="sxs-lookup"><span data-stu-id="d53ed-397">Job types</span></span>

<span data-ttu-id="d53ed-398">職務タイプは、類似した職務をカテゴリにグループ化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-398">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="d53ed-399">職務タイプは、米国およびカナダでの給与を処理するために必要です。</span><span class="sxs-lookup"><span data-stu-id="d53ed-399">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="d53ed-400">職務タイプの例には、フルタイムおよびパートタイム、または給与払いおよび時給払いが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-400">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="d53ed-401">職務タイプは、従業員が時給払いかあるいは給与払いなのかを示す支払タイプとして Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-401">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="d53ed-402">次の職務タイプと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="d53ed-402">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="d53ed-403">ジョブ タイプ</span><span class="sxs-lookup"><span data-stu-id="d53ed-403">Job type</span></span>   | <span data-ttu-id="d53ed-404">説明</span><span class="sxs-lookup"><span data-stu-id="d53ed-404">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="d53ed-405">時間</span><span class="sxs-lookup"><span data-stu-id="d53ed-405">Hourly</span></span>     | <span data-ttu-id="d53ed-406">時間</span><span class="sxs-lookup"><span data-stu-id="d53ed-406">Hourly</span></span>      |
| <span data-ttu-id="d53ed-407">給与払い</span><span class="sxs-lookup"><span data-stu-id="d53ed-407">Salaried</span></span>   | <span data-ttu-id="d53ed-408">給与払い</span><span class="sxs-lookup"><span data-stu-id="d53ed-408">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="d53ed-409">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="d53ed-409">Position types</span></span> 

<span data-ttu-id="d53ed-410">職位がフルタイム、パートタイム、またはその他のタイプかどうかを説明するために職位タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-410">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="d53ed-411">職位タイプは、従業員がフルタイムかあるいはパートタイムなのかを示す支払クラスとして Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-411">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="d53ed-412">次の職位タイプと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="d53ed-412">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="d53ed-413">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="d53ed-413">Position type</span></span>   | <span data-ttu-id="d53ed-414">説明</span><span class="sxs-lookup"><span data-stu-id="d53ed-414">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="d53ed-415">フルタイム</span><span class="sxs-lookup"><span data-stu-id="d53ed-415">Full-time</span></span>       | <span data-ttu-id="d53ed-416">フルタイム従業員</span><span class="sxs-lookup"><span data-stu-id="d53ed-416">Full time employee</span></span> |
| <span data-ttu-id="d53ed-417">パートタイム</span><span class="sxs-lookup"><span data-stu-id="d53ed-417">Part-time</span></span>       | <span data-ttu-id="d53ed-418">パートタイム従業員</span><span class="sxs-lookup"><span data-stu-id="d53ed-418">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="d53ed-419">理由コード</span><span class="sxs-lookup"><span data-stu-id="d53ed-419">Reason codes</span></span>

<span data-ttu-id="d53ed-420">理由コードは、従業員のステータスに関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-420">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="d53ed-421">理由コードは、従業員の職位または雇用ステータスへの変更の理由を示すステータス理由として Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-421">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="d53ed-422">次の理由コードと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="d53ed-422">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="d53ed-423">理由コード</span><span class="sxs-lookup"><span data-stu-id="d53ed-423">Reason code</span></span>    | <span data-ttu-id="d53ed-424">説明</span><span class="sxs-lookup"><span data-stu-id="d53ed-424">Description</span></span>      | <span data-ttu-id="d53ed-425">適用可能なシナリオ</span><span class="sxs-lookup"><span data-stu-id="d53ed-425">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="d53ed-426">辞職</span><span class="sxs-lookup"><span data-stu-id="d53ed-426">RESIGNATION</span></span>    | <span data-ttu-id="d53ed-427">辞職</span><span class="sxs-lookup"><span data-stu-id="d53ed-427">Resignation</span></span>      | <span data-ttu-id="d53ed-428">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="d53ed-428">Terminate worker</span></span>     |
| <span data-ttu-id="d53ed-429">終了</span><span class="sxs-lookup"><span data-stu-id="d53ed-429">TERMINATION</span></span>    | <span data-ttu-id="d53ed-430">終了</span><span class="sxs-lookup"><span data-stu-id="d53ed-430">Termination</span></span>      | <span data-ttu-id="d53ed-431">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="d53ed-431">Terminate worker</span></span>     |
| <span data-ttu-id="d53ed-432">定年退職</span><span class="sxs-lookup"><span data-stu-id="d53ed-432">RETIREMENT</span></span>     | <span data-ttu-id="d53ed-433">償却</span><span class="sxs-lookup"><span data-stu-id="d53ed-433">Retirement</span></span>       | <span data-ttu-id="d53ed-434">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="d53ed-434">Terminate worker</span></span>     |
| <span data-ttu-id="d53ed-435">その他</span><span class="sxs-lookup"><span data-stu-id="d53ed-435">OTHER</span></span>          | <span data-ttu-id="d53ed-436">その他の理由</span><span class="sxs-lookup"><span data-stu-id="d53ed-436">Other Reasons</span></span>    | <span data-ttu-id="d53ed-437">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="d53ed-437">Terminate worker</span></span>     |
| <span data-ttu-id="d53ed-438">死亡</span><span class="sxs-lookup"><span data-stu-id="d53ed-438">DEATH</span></span>          | <span data-ttu-id="d53ed-439">死亡</span><span class="sxs-lookup"><span data-stu-id="d53ed-439">Death</span></span>            | <span data-ttu-id="d53ed-440">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="d53ed-440">Terminate worker</span></span>     |
| <span data-ttu-id="d53ed-441">休暇</span><span class="sxs-lookup"><span data-stu-id="d53ed-441">LEAVEOFABSENCE</span></span> | <span data-ttu-id="d53ed-442">休暇</span><span class="sxs-lookup"><span data-stu-id="d53ed-442">Leave of Absence</span></span> | <span data-ttu-id="d53ed-443">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="d53ed-443">Terminate worker</span></span>     |
| <span data-ttu-id="d53ed-444">契約の終了</span><span class="sxs-lookup"><span data-stu-id="d53ed-444">CONTRACTEND</span></span>    | <span data-ttu-id="d53ed-445">契約の終了</span><span class="sxs-lookup"><span data-stu-id="d53ed-445">End of Contract</span></span>  | <span data-ttu-id="d53ed-446">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="d53ed-446">Terminate worker</span></span>     |
| <span data-ttu-id="d53ed-447">給与の変更</span><span class="sxs-lookup"><span data-stu-id="d53ed-447">SALARYCHANGE</span></span>   | <span data-ttu-id="d53ed-448">給与の変更</span><span class="sxs-lookup"><span data-stu-id="d53ed-448">Change of Salary</span></span> | <span data-ttu-id="d53ed-449">報酬</span><span class="sxs-lookup"><span data-stu-id="d53ed-449">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="d53ed-450">配偶者の有無</span><span class="sxs-lookup"><span data-stu-id="d53ed-450">Marital status</span></span>

<span data-ttu-id="d53ed-451">配偶者有無の値は、Dayforce にマップされ、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-451">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d53ed-452">次の表に、配偶者有無の値がどのように Dayforce にマップされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-452">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="d53ed-453">人事管理</span><span class="sxs-lookup"><span data-stu-id="d53ed-453">Human Resources</span></span>                 | <span data-ttu-id="d53ed-454">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d53ed-454">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="d53ed-455">既婚</span><span class="sxs-lookup"><span data-stu-id="d53ed-455">Married</span></span>                | <span data-ttu-id="d53ed-456">既婚</span><span class="sxs-lookup"><span data-stu-id="d53ed-456">Married</span></span>              |
| <span data-ttu-id="d53ed-457">未婚</span><span class="sxs-lookup"><span data-stu-id="d53ed-457">Single</span></span>                 | <span data-ttu-id="d53ed-458">未婚</span><span class="sxs-lookup"><span data-stu-id="d53ed-458">Single</span></span>               |
| <span data-ttu-id="d53ed-459">死別</span><span class="sxs-lookup"><span data-stu-id="d53ed-459">Widowed</span></span>                | <span data-ttu-id="d53ed-460">死別</span><span class="sxs-lookup"><span data-stu-id="d53ed-460">Widowed</span></span>              |
| <span data-ttu-id="d53ed-461">離婚</span><span class="sxs-lookup"><span data-stu-id="d53ed-461">Divorced</span></span>               | <span data-ttu-id="d53ed-462">離婚</span><span class="sxs-lookup"><span data-stu-id="d53ed-462">Divorced</span></span>             |
| <span data-ttu-id="d53ed-463">登録済パートナーシップ</span><span class="sxs-lookup"><span data-stu-id="d53ed-463">Registered Partnership</span></span> | <span data-ttu-id="d53ed-464">ドメスティック パートナーシップ</span><span class="sxs-lookup"><span data-stu-id="d53ed-464">Domestic Partnership</span></span> |
| <span data-ttu-id="d53ed-465">None</span><span class="sxs-lookup"><span data-stu-id="d53ed-465">None</span></span>                   | <span data-ttu-id="d53ed-466">None</span><span class="sxs-lookup"><span data-stu-id="d53ed-466">None</span></span>                 |
| <span data-ttu-id="d53ed-467">同棲中</span><span class="sxs-lookup"><span data-stu-id="d53ed-467">Cohabiting</span></span>             | <span data-ttu-id="d53ed-468">同棲中</span><span class="sxs-lookup"><span data-stu-id="d53ed-468">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="d53ed-469">種類</span><span class="sxs-lookup"><span data-stu-id="d53ed-469">Gender</span></span>

<span data-ttu-id="d53ed-470">性別の指定は、Dayforce にマップされ、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-470">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d53ed-471">次の表に、性別の指定がどのように Dayforce にマップされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-471">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="d53ed-472">人事管理</span><span class="sxs-lookup"><span data-stu-id="d53ed-472">Human Resources</span></span>       | <span data-ttu-id="d53ed-473">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d53ed-473">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="d53ed-474">男性</span><span class="sxs-lookup"><span data-stu-id="d53ed-474">Male</span></span>         | <span data-ttu-id="d53ed-475">男性</span><span class="sxs-lookup"><span data-stu-id="d53ed-475">Male</span></span>            |
| <span data-ttu-id="d53ed-476">女性</span><span class="sxs-lookup"><span data-stu-id="d53ed-476">Female</span></span>       | <span data-ttu-id="d53ed-477">女性</span><span class="sxs-lookup"><span data-stu-id="d53ed-477">Female</span></span>          |
| <span data-ttu-id="d53ed-478">不特定</span><span class="sxs-lookup"><span data-stu-id="d53ed-478">Non-specific</span></span> | <span data-ttu-id="d53ed-479">*サポートされていません*</span><span class="sxs-lookup"><span data-stu-id="d53ed-479">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="d53ed-480">所得コード</span><span class="sxs-lookup"><span data-stu-id="d53ed-480">Earning codes</span></span>

<span data-ttu-id="d53ed-481">所得コードは、作業者が受け取るすべての収益のタイプを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-481">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d53ed-482">コードには、会計ルール、税法、レポート要件、およびグロスアップ能力など、所得に関連付けられている複数のパラメーターが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-482">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="d53ed-483">サポートされていない頻度を使用する場合、既定で **すべての支払** 頻度が計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-483">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="d53ed-484">サポートされる頻度</span><span class="sxs-lookup"><span data-stu-id="d53ed-484">Supported frequencies</span></span>

- <span data-ttu-id="d53ed-485">All</span><span class="sxs-lookup"><span data-stu-id="d53ed-485">All</span></span>
- <span data-ttu-id="d53ed-486">すべての支払</span><span class="sxs-lookup"><span data-stu-id="d53ed-486">EVERYPAY</span></span>
- <span data-ttu-id="d53ed-487">各支払期間</span><span class="sxs-lookup"><span data-stu-id="d53ed-487">EACHPAYPERIOD</span></span>
- <span data-ttu-id="d53ed-488">他のすべての奇数支払</span><span class="sxs-lookup"><span data-stu-id="d53ed-488">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="d53ed-489">他のすべての偶数支払</span><span class="sxs-lookup"><span data-stu-id="d53ed-489">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="d53ed-490">1 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-490">1OFMTH</span></span>
- <span data-ttu-id="d53ed-491">月の最終日</span><span class="sxs-lookup"><span data-stu-id="d53ed-491">LASTOFMTH</span></span>
- <span data-ttu-id="d53ed-492">2 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-492">2OFMTH</span></span>
- <span data-ttu-id="d53ed-493">3 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-493">3OFMTH</span></span>
- <span data-ttu-id="d53ed-494">4 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-494">4OFMTH</span></span>
- <span data-ttu-id="d53ed-495">5 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-495">5OFMTH</span></span>
- <span data-ttu-id="d53ed-496">1 か月および 2 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-496">1N2OFMTH</span></span>
- <span data-ttu-id="d53ed-497">3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-497">3N4OFMTH</span></span>
- <span data-ttu-id="d53ed-498">1 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-498">1N3OFMTH</span></span>
- <span data-ttu-id="d53ed-499">1 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-499">1N4OFMTH</span></span>
- <span data-ttu-id="d53ed-500">2 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-500">2N3OFMTH</span></span>
- <span data-ttu-id="d53ed-501">2 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-501">2N4OFMTH</span></span>
- <span data-ttu-id="d53ed-502">1 か月、2 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-502">1N2N3OFMTH</span></span>
- <span data-ttu-id="d53ed-503">1 か月、2 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-503">1N2N4OFMTH</span></span>
- <span data-ttu-id="d53ed-504">1 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-504">1N3N4OFMTH</span></span>
- <span data-ttu-id="d53ed-505">2 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-505">2N3N4OFMTH</span></span>
- <span data-ttu-id="d53ed-506">1 か月、2 か月、3 か月および 4 か月 - 1 か月、2 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="d53ed-507">2 か月、3 か月、4 か月および 5 か月 - 2 か月、3 か月、4 か月および 5 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-507">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="d53ed-508">四半期の 1 - 四半期の 1</span><span class="sxs-lookup"><span data-stu-id="d53ed-508">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="d53ed-509">四半期の最終日 – 四半期の最終日</span><span class="sxs-lookup"><span data-stu-id="d53ed-509">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="d53ed-510">四半期の最後の月 – 四半期の最後の月</span><span class="sxs-lookup"><span data-stu-id="d53ed-510">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="d53ed-511">1 年 - 1 年</span><span class="sxs-lookup"><span data-stu-id="d53ed-511">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="d53ed-512">年の最終日 – 年の最終日</span><span class="sxs-lookup"><span data-stu-id="d53ed-512">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="d53ed-513">年の 11 月および 12 月 - 年の 11 月および 12 月</span><span class="sxs-lookup"><span data-stu-id="d53ed-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="d53ed-514">住所</span><span class="sxs-lookup"><span data-stu-id="d53ed-514">Addresses</span></span>

<span data-ttu-id="d53ed-515">特定の国または地域、都道府県、および市区郡 (自治体) の ID には、Dayforce および国内または地域内のプロバイダーが認識できる特定の形式が必要です。</span><span class="sxs-lookup"><span data-stu-id="d53ed-515">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="d53ed-516">市町村の形式は柔軟ですが、すべての市町村が都道府県と関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-516">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="d53ed-517">人事管理</span><span class="sxs-lookup"><span data-stu-id="d53ed-517">Human Resources</span></span>          | <span data-ttu-id="d53ed-518">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d53ed-518">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="d53ed-519">国/地域</span><span class="sxs-lookup"><span data-stu-id="d53ed-519">Country/Region</span></span>  | <span data-ttu-id="d53ed-520">国コード</span><span class="sxs-lookup"><span data-stu-id="d53ed-520">Country Code</span></span>          |
| <span data-ttu-id="d53ed-521">郵便番号</span><span class="sxs-lookup"><span data-stu-id="d53ed-521">Zip/Postal Code</span></span> | <span data-ttu-id="d53ed-522">郵便番号</span><span class="sxs-lookup"><span data-stu-id="d53ed-522">Postal Code</span></span>           |
| <span data-ttu-id="d53ed-523">行政単位 (区画)</span><span class="sxs-lookup"><span data-stu-id="d53ed-523">State</span></span>           | <span data-ttu-id="d53ed-524">都道府県コード</span><span class="sxs-lookup"><span data-stu-id="d53ed-524">State Code</span></span>            |
| <span data-ttu-id="d53ed-525">市町村</span><span class="sxs-lookup"><span data-stu-id="d53ed-525">City</span></span>            | <span data-ttu-id="d53ed-526">市町村</span><span class="sxs-lookup"><span data-stu-id="d53ed-526">City</span></span>                  |
| <span data-ttu-id="d53ed-527">郡</span><span class="sxs-lookup"><span data-stu-id="d53ed-527">County</span></span>          | <span data-ttu-id="d53ed-528">市区郡 (自治体)</span><span class="sxs-lookup"><span data-stu-id="d53ed-528">County (Municipality)</span></span> |
| <span data-ttu-id="d53ed-529">住所</span><span class="sxs-lookup"><span data-stu-id="d53ed-529">Street</span></span>          | <span data-ttu-id="d53ed-530">住所行 1</span><span class="sxs-lookup"><span data-stu-id="d53ed-530">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="d53ed-531">税地域</span><span class="sxs-lookup"><span data-stu-id="d53ed-531">Tax regions</span></span>

<span data-ttu-id="d53ed-532">税地域は、給与の生成時に適用する適切な税を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-532">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="d53ed-533">税地域は、場所の住所として Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-533">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="d53ed-534">既定の税地域は、作業者の有効な職位に関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-534">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="d53ed-535">税地域 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-535">Tax region (required)</span></span>
- <span data-ttu-id="d53ed-536">国/地域 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-536">Country/Region (required)</span></span>
- <span data-ttu-id="d53ed-537">都道府県 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-537">State (required)</span></span>
- <span data-ttu-id="d53ed-538">郡</span><span class="sxs-lookup"><span data-stu-id="d53ed-538">County</span></span> 
- <span data-ttu-id="d53ed-539">市町村 (必須)</span><span class="sxs-lookup"><span data-stu-id="d53ed-539">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="d53ed-540">メキシコの給与を生成するためのデータ コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d53ed-540">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="d53ed-541">メキシコの従業員のために支払を生成している場合、次の要素をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-541">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="d53ed-542">職位に部門が必要です。</span><span class="sxs-lookup"><span data-stu-id="d53ed-542">Departments are required on positions.</span></span>
- <span data-ttu-id="d53ed-543">原価部門を財務分析コードとして設定し、既定の財務分析コード文字列の最初の要素とする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-543">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="d53ed-544">ジョブ タイプ</span><span class="sxs-lookup"><span data-stu-id="d53ed-544">Job types</span></span>

<span data-ttu-id="d53ed-545">職務タイプは、類似した職務をカテゴリにグループ化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-545">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="d53ed-546">職務タイプは、メキシコでの給与を処理するために必要です。</span><span class="sxs-lookup"><span data-stu-id="d53ed-546">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="d53ed-547">職務タイプの例には、フルタイムおよびパートタイム、または給与払いおよび時給払いが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-547">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="d53ed-548">職務タイプは、従業員が時給払いかあるいは給与払いなのかを示す支払タイプとして Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-548">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="d53ed-549">次の職務タイプと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="d53ed-549">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="d53ed-550">ジョブ タイプ</span><span class="sxs-lookup"><span data-stu-id="d53ed-550">Job type</span></span>   | <span data-ttu-id="d53ed-551">説明</span><span class="sxs-lookup"><span data-stu-id="d53ed-551">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="d53ed-552">時間</span><span class="sxs-lookup"><span data-stu-id="d53ed-552">Hourly</span></span>     | <span data-ttu-id="d53ed-553">MX 時給払い</span><span class="sxs-lookup"><span data-stu-id="d53ed-553">MX Hourly</span></span>   |
| <span data-ttu-id="d53ed-554">給与払い</span><span class="sxs-lookup"><span data-stu-id="d53ed-554">Salaried</span></span>   | <span data-ttu-id="d53ed-555">MX 給与払い</span><span class="sxs-lookup"><span data-stu-id="d53ed-555">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="d53ed-556">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="d53ed-556">Position types</span></span> 

<span data-ttu-id="d53ed-557">職位がフルタイム、パートタイム、またはその他のタイプかどうかを説明するために職位タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-557">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="d53ed-558">職位タイプは、従業員がフルタイムかあるいはパートタイムなのかを示す支払クラスとして Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-558">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="d53ed-559">次の職位タイプと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="d53ed-559">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="d53ed-560">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="d53ed-560">Position type</span></span>   | <span data-ttu-id="d53ed-561">説明</span><span class="sxs-lookup"><span data-stu-id="d53ed-561">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="d53ed-562">フルタイム</span><span class="sxs-lookup"><span data-stu-id="d53ed-562">Full-time</span></span>       | <span data-ttu-id="d53ed-563">フルタイム従業員</span><span class="sxs-lookup"><span data-stu-id="d53ed-563">Full time employee</span></span> |
| <span data-ttu-id="d53ed-564">パートタイム</span><span class="sxs-lookup"><span data-stu-id="d53ed-564">Part-time</span></span>       | <span data-ttu-id="d53ed-565">パートタイム従業員</span><span class="sxs-lookup"><span data-stu-id="d53ed-565">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="d53ed-566">理由コード</span><span class="sxs-lookup"><span data-stu-id="d53ed-566">Reason codes</span></span>

<span data-ttu-id="d53ed-567">理由コードは、従業員のステータスに関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-567">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="d53ed-568">理由コードは、従業員の職位または雇用ステータスへの変更の理由を示すステータス理由として Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-568">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="d53ed-569">次の理由コードと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="d53ed-569">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="d53ed-570">理由コード</span><span class="sxs-lookup"><span data-stu-id="d53ed-570">Reason code</span></span>            | <span data-ttu-id="d53ed-571">説明</span><span class="sxs-lookup"><span data-stu-id="d53ed-571">Description</span></span>                    | <span data-ttu-id="d53ed-572">適用可能なシナリオ</span><span class="sxs-lookup"><span data-stu-id="d53ed-572">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="d53ed-573">支払前の除籍</span><span class="sxs-lookup"><span data-stu-id="d53ed-573">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="d53ed-574">最初の給与の前の除籍</span><span class="sxs-lookup"><span data-stu-id="d53ed-574">Departure before first payroll</span></span> | <span data-ttu-id="d53ed-575">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="d53ed-575">Terminate worker</span></span>     |
| <span data-ttu-id="d53ed-576">辞職</span><span class="sxs-lookup"><span data-stu-id="d53ed-576">RESIGNATION</span></span>            | <span data-ttu-id="d53ed-577">辞職</span><span class="sxs-lookup"><span data-stu-id="d53ed-577">Resignation</span></span>                    | <span data-ttu-id="d53ed-578">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="d53ed-578">Terminate worker</span></span>     |
| <span data-ttu-id="d53ed-579">年金</span><span class="sxs-lookup"><span data-stu-id="d53ed-579">PENSION</span></span>                | <span data-ttu-id="d53ed-580">年金</span><span class="sxs-lookup"><span data-stu-id="d53ed-580">Pension</span></span>                        | <span data-ttu-id="d53ed-581">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="d53ed-581">Terminate worker</span></span>     |
| <span data-ttu-id="d53ed-582">終了</span><span class="sxs-lookup"><span data-stu-id="d53ed-582">TERMINATION</span></span>            | <span data-ttu-id="d53ed-583">終了</span><span class="sxs-lookup"><span data-stu-id="d53ed-583">Termination</span></span>                    | <span data-ttu-id="d53ed-584">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="d53ed-584">Terminate worker</span></span>     |
| <span data-ttu-id="d53ed-585">定年退職</span><span class="sxs-lookup"><span data-stu-id="d53ed-585">RETIREMENT</span></span>             | <span data-ttu-id="d53ed-586">償却</span><span class="sxs-lookup"><span data-stu-id="d53ed-586">Retirement</span></span>                     | <span data-ttu-id="d53ed-587">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="d53ed-587">Terminate worker</span></span>     |
| <span data-ttu-id="d53ed-588">休暇者</span><span class="sxs-lookup"><span data-stu-id="d53ed-588">ABSENTEE</span></span>               | <span data-ttu-id="d53ed-589">休暇者</span><span class="sxs-lookup"><span data-stu-id="d53ed-589">Absentee</span></span>                       | <span data-ttu-id="d53ed-590">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="d53ed-590">Terminate worker</span></span>     |
| <span data-ttu-id="d53ed-591">その他</span><span class="sxs-lookup"><span data-stu-id="d53ed-591">OTHER</span></span>                  | <span data-ttu-id="d53ed-592">その他の理由</span><span class="sxs-lookup"><span data-stu-id="d53ed-592">Other Reasons</span></span>                  | <span data-ttu-id="d53ed-593">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="d53ed-593">Terminate worker</span></span>     |
| <span data-ttu-id="d53ed-594">休業</span><span class="sxs-lookup"><span data-stu-id="d53ed-594">CLOSURE</span></span>                | <span data-ttu-id="d53ed-595">業務休業</span><span class="sxs-lookup"><span data-stu-id="d53ed-595">Business Closure</span></span>               | <span data-ttu-id="d53ed-596">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="d53ed-596">Terminate worker</span></span>     |
| <span data-ttu-id="d53ed-597">死亡</span><span class="sxs-lookup"><span data-stu-id="d53ed-597">DEATH</span></span>                  | <span data-ttu-id="d53ed-598">死亡</span><span class="sxs-lookup"><span data-stu-id="d53ed-598">Death</span></span>                          | <span data-ttu-id="d53ed-599">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="d53ed-599">Terminate worker</span></span>     |
| <span data-ttu-id="d53ed-600">休暇</span><span class="sxs-lookup"><span data-stu-id="d53ed-600">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="d53ed-601">休暇</span><span class="sxs-lookup"><span data-stu-id="d53ed-601">Leave of Absence</span></span>               | <span data-ttu-id="d53ed-602">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="d53ed-602">Terminate worker</span></span>     |
| <span data-ttu-id="d53ed-603">契約の終了</span><span class="sxs-lookup"><span data-stu-id="d53ed-603">CONTRACTEND</span></span>            | <span data-ttu-id="d53ed-604">契約の終了</span><span class="sxs-lookup"><span data-stu-id="d53ed-604">End of Contract</span></span>                | <span data-ttu-id="d53ed-605">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="d53ed-605">Terminate worker</span></span>     |
| <span data-ttu-id="d53ed-606">給与の変更</span><span class="sxs-lookup"><span data-stu-id="d53ed-606">SALARYCHANGE</span></span>           | <span data-ttu-id="d53ed-607">給与の変更</span><span class="sxs-lookup"><span data-stu-id="d53ed-607">Change of Salary</span></span>               | <span data-ttu-id="d53ed-608">報酬</span><span class="sxs-lookup"><span data-stu-id="d53ed-608">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="d53ed-609">雇用条件</span><span class="sxs-lookup"><span data-stu-id="d53ed-609">Terms of employment</span></span>

<span data-ttu-id="d53ed-610">雇用条件は、雇用条件のカテゴリを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-610">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="d53ed-611">条件は、雇用インジケーターの値として Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-611">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="d53ed-612">次の雇用条件および説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="d53ed-612">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="d53ed-613">雇用条件</span><span class="sxs-lookup"><span data-stu-id="d53ed-613">Terms of employment</span></span>   | <span data-ttu-id="d53ed-614">説明</span><span class="sxs-lookup"><span data-stu-id="d53ed-614">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="d53ed-615">通常</span><span class="sxs-lookup"><span data-stu-id="d53ed-615">Regular</span></span>               | <span data-ttu-id="d53ed-616">通常</span><span class="sxs-lookup"><span data-stu-id="d53ed-616">Regular</span></span>     |
| <span data-ttu-id="d53ed-617">直接</span><span class="sxs-lookup"><span data-stu-id="d53ed-617">Direct</span></span>                | <span data-ttu-id="d53ed-618">直接</span><span class="sxs-lookup"><span data-stu-id="d53ed-618">Direct</span></span>      |
| <span data-ttu-id="d53ed-619">インターンシップ</span><span class="sxs-lookup"><span data-stu-id="d53ed-619">Internship</span></span>            | <span data-ttu-id="d53ed-620">インターンシップ</span><span class="sxs-lookup"><span data-stu-id="d53ed-620">Internship</span></span>  |
| <span data-ttu-id="d53ed-621">永続的</span><span class="sxs-lookup"><span data-stu-id="d53ed-621">Permanent</span></span>             | <span data-ttu-id="d53ed-622">永続的</span><span class="sxs-lookup"><span data-stu-id="d53ed-622">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="d53ed-623">配偶者の有無</span><span class="sxs-lookup"><span data-stu-id="d53ed-623">Marital status</span></span>

<span data-ttu-id="d53ed-624">配偶者有無の値は、Dayforce にマップされ、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-624">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d53ed-625">次の表に、配偶者有無の値がどのように Dayforce にマップされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-625">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="d53ed-626">人事管理</span><span class="sxs-lookup"><span data-stu-id="d53ed-626">Human Resources</span></span>                 | <span data-ttu-id="d53ed-627">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d53ed-627">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="d53ed-628">既婚</span><span class="sxs-lookup"><span data-stu-id="d53ed-628">Married</span></span>                | <span data-ttu-id="d53ed-629">既婚</span><span class="sxs-lookup"><span data-stu-id="d53ed-629">Married</span></span>                   |
| <span data-ttu-id="d53ed-630">未婚</span><span class="sxs-lookup"><span data-stu-id="d53ed-630">Single</span></span>                 | <span data-ttu-id="d53ed-631">未婚</span><span class="sxs-lookup"><span data-stu-id="d53ed-631">Single</span></span>                    |
| <span data-ttu-id="d53ed-632">死別</span><span class="sxs-lookup"><span data-stu-id="d53ed-632">Widowed</span></span>                | <span data-ttu-id="d53ed-633">死別</span><span class="sxs-lookup"><span data-stu-id="d53ed-633">Widowed</span></span>                   |
| <span data-ttu-id="d53ed-634">離婚</span><span class="sxs-lookup"><span data-stu-id="d53ed-634">Divorced</span></span>               | <span data-ttu-id="d53ed-635">離婚</span><span class="sxs-lookup"><span data-stu-id="d53ed-635">Divorced</span></span>                  |
| <span data-ttu-id="d53ed-636">登録済パートナーシップ</span><span class="sxs-lookup"><span data-stu-id="d53ed-636">Registered Partnership</span></span> | <span data-ttu-id="d53ed-637">ドメスティック パートナーシップ</span><span class="sxs-lookup"><span data-stu-id="d53ed-637">Domestic Partnership</span></span>      |
| <span data-ttu-id="d53ed-638">None</span><span class="sxs-lookup"><span data-stu-id="d53ed-638">None</span></span>                   | <span data-ttu-id="d53ed-639">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="d53ed-639">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d53ed-640">同棲中</span><span class="sxs-lookup"><span data-stu-id="d53ed-640">Cohabiting</span></span>             | <span data-ttu-id="d53ed-641">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="d53ed-641">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="d53ed-642">種類</span><span class="sxs-lookup"><span data-stu-id="d53ed-642">Gender</span></span>

<span data-ttu-id="d53ed-643">性別の指定は、Dayforce にマップされ、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-643">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d53ed-644">次の表に、性別の指定がどのように Dayforce にマップされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-644">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="d53ed-645">人事管理</span><span class="sxs-lookup"><span data-stu-id="d53ed-645">Human Resources</span></span>       | <span data-ttu-id="d53ed-646">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d53ed-646">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="d53ed-647">男性</span><span class="sxs-lookup"><span data-stu-id="d53ed-647">Male</span></span>         | <span data-ttu-id="d53ed-648">男性</span><span class="sxs-lookup"><span data-stu-id="d53ed-648">Male</span></span>                      |
| <span data-ttu-id="d53ed-649">女性</span><span class="sxs-lookup"><span data-stu-id="d53ed-649">Female</span></span>       | <span data-ttu-id="d53ed-650">女性</span><span class="sxs-lookup"><span data-stu-id="d53ed-650">Female</span></span>                    |
| <span data-ttu-id="d53ed-651">不特定</span><span class="sxs-lookup"><span data-stu-id="d53ed-651">Non-specific</span></span> | <span data-ttu-id="d53ed-652">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="d53ed-652">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="d53ed-653">支払方法</span><span class="sxs-lookup"><span data-stu-id="d53ed-653">Payment method</span></span>

<span data-ttu-id="d53ed-654">支払方法は、従業員に支払が行われる方法を従業員および会社に説明します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-654">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="d53ed-655">支払方法は、Dayforce にマップされ、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-655">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d53ed-656">次の表に、支払方法がどのように Dayforce にマップされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-656">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="d53ed-657">人事管理</span><span class="sxs-lookup"><span data-stu-id="d53ed-657">Human Resources</span></span>             | <span data-ttu-id="d53ed-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d53ed-658">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="d53ed-659">現金</span><span class="sxs-lookup"><span data-stu-id="d53ed-659">Cash</span></span>               | <span data-ttu-id="d53ed-660">現金</span><span class="sxs-lookup"><span data-stu-id="d53ed-660">Cash</span></span>                      |
| <span data-ttu-id="d53ed-661">電子支払</span><span class="sxs-lookup"><span data-stu-id="d53ed-661">Electronic Payment</span></span> | <span data-ttu-id="d53ed-662">転送</span><span class="sxs-lookup"><span data-stu-id="d53ed-662">Transfer</span></span>                  |
| <span data-ttu-id="d53ed-663">チェック</span><span class="sxs-lookup"><span data-stu-id="d53ed-663">Check</span></span>              | <span data-ttu-id="d53ed-664">小切手</span><span class="sxs-lookup"><span data-stu-id="d53ed-664">Cheque</span></span>                    |
| <span data-ttu-id="d53ed-665">銀行為替手形</span><span class="sxs-lookup"><span data-stu-id="d53ed-665">Bank Draft</span></span>         | <span data-ttu-id="d53ed-666">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="d53ed-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d53ed-667">外</span><span class="sxs-lookup"><span data-stu-id="d53ed-667">Other</span></span>              | <span data-ttu-id="d53ed-668">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="d53ed-668">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="d53ed-669">銀行口座の種類</span><span class="sxs-lookup"><span data-stu-id="d53ed-669">Bank account type</span></span>

<span data-ttu-id="d53ed-670">銀行口座の種類は、従業員への電子支払のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-670">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="d53ed-671">銀行口座の種類は、振替口座情報として Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-671">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="d53ed-672">銀行口座の種類は、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-672">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="d53ed-673">人事管理</span><span class="sxs-lookup"><span data-stu-id="d53ed-673">Human Resources</span></span>            | <span data-ttu-id="d53ed-674">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d53ed-674">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="d53ed-675">当座預金口座</span><span class="sxs-lookup"><span data-stu-id="d53ed-675">Checking Account</span></span>  | <span data-ttu-id="d53ed-676">当座預金口座</span><span class="sxs-lookup"><span data-stu-id="d53ed-676">CheckingAccount</span></span>           |
| <span data-ttu-id="d53ed-677">給与口座</span><span class="sxs-lookup"><span data-stu-id="d53ed-677">Payroll Account</span></span>   | <span data-ttu-id="d53ed-678">給与口座</span><span class="sxs-lookup"><span data-stu-id="d53ed-678">PayrollAccount</span></span>            |
| <span data-ttu-id="d53ed-679">普通預金口座</span><span class="sxs-lookup"><span data-stu-id="d53ed-679">Savings Account</span></span>   | <span data-ttu-id="d53ed-680">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="d53ed-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d53ed-681">BankGirot 口座</span><span class="sxs-lookup"><span data-stu-id="d53ed-681">BankGirot account</span></span> | <span data-ttu-id="d53ed-682">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="d53ed-682">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d53ed-683">PlusGirot 口座</span><span class="sxs-lookup"><span data-stu-id="d53ed-683">PlusGirot account</span></span> | <span data-ttu-id="d53ed-684">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="d53ed-684">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="d53ed-685">所得コード</span><span class="sxs-lookup"><span data-stu-id="d53ed-685">Earning codes</span></span>

<span data-ttu-id="d53ed-686">所得コードは、作業者が受け取るすべての収益のタイプを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="d53ed-686">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d53ed-687">コードには、会計ルール、税法、レポート要件、およびグロスアップ能力など、所得に関連付けられている複数のパラメーターが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-687">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="d53ed-688">サポートされていない頻度を使用する場合、既定で **すべての支払** 頻度が計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-688">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="d53ed-689">サポートされる頻度</span><span class="sxs-lookup"><span data-stu-id="d53ed-689">Supported frequencies</span></span>

- <span data-ttu-id="d53ed-690">All</span><span class="sxs-lookup"><span data-stu-id="d53ed-690">All</span></span>
- <span data-ttu-id="d53ed-691">すべての支払</span><span class="sxs-lookup"><span data-stu-id="d53ed-691">EVERYPAY</span></span>
- <span data-ttu-id="d53ed-692">各支払期間</span><span class="sxs-lookup"><span data-stu-id="d53ed-692">EACHPAYPERIOD</span></span>
- <span data-ttu-id="d53ed-693">他のすべての奇数支払</span><span class="sxs-lookup"><span data-stu-id="d53ed-693">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="d53ed-694">他のすべての偶数支払</span><span class="sxs-lookup"><span data-stu-id="d53ed-694">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="d53ed-695">1 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-695">1OFMTH</span></span>
- <span data-ttu-id="d53ed-696">月の最終日</span><span class="sxs-lookup"><span data-stu-id="d53ed-696">LASTOFMTH</span></span>
- <span data-ttu-id="d53ed-697">2 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-697">2OFMTH</span></span>
- <span data-ttu-id="d53ed-698">3 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-698">3OFMTH</span></span>
- <span data-ttu-id="d53ed-699">4 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-699">4OFMTH</span></span>
- <span data-ttu-id="d53ed-700">5 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-700">5OFMTH</span></span>
- <span data-ttu-id="d53ed-701">1 か月および 2 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-701">1N2OFMTH</span></span>
- <span data-ttu-id="d53ed-702">3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-702">3N4OFMTH</span></span>
- <span data-ttu-id="d53ed-703">1 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-703">1N3OFMTH</span></span>
- <span data-ttu-id="d53ed-704">1 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-704">1N4OFMTH</span></span>
- <span data-ttu-id="d53ed-705">2 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-705">2N3OFMTH</span></span>
- <span data-ttu-id="d53ed-706">2 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-706">2N4OFMTH</span></span>
- <span data-ttu-id="d53ed-707">1 か月、2 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-707">1N2N3OFMTH</span></span>
- <span data-ttu-id="d53ed-708">1 か月、2 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-708">1N2N4OFMTH</span></span>
- <span data-ttu-id="d53ed-709">1 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-709">1N3N4OFMTH</span></span>
- <span data-ttu-id="d53ed-710">2 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-710">2N3N4OFMTH</span></span>
- <span data-ttu-id="d53ed-711">1 か月、2 か月、3 か月および 4 か月 - 1 か月、2 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="d53ed-712">2 か月、3 か月、4 か月および 5 か月 - 2 か月、3 か月、4 か月および 5 か月</span><span class="sxs-lookup"><span data-stu-id="d53ed-712">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="d53ed-713">四半期の 1 - 四半期の 1</span><span class="sxs-lookup"><span data-stu-id="d53ed-713">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="d53ed-714">四半期の最終日 – 四半期の最終日</span><span class="sxs-lookup"><span data-stu-id="d53ed-714">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="d53ed-715">四半期の最後の月 – 四半期の最後の月</span><span class="sxs-lookup"><span data-stu-id="d53ed-715">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="d53ed-716">1 年 - 1 年</span><span class="sxs-lookup"><span data-stu-id="d53ed-716">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="d53ed-717">年の最終日 – 年の最終日</span><span class="sxs-lookup"><span data-stu-id="d53ed-717">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="d53ed-718">年の 11 月および 12 月 - 年の 11 月および 12 月</span><span class="sxs-lookup"><span data-stu-id="d53ed-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="d53ed-719">住所</span><span class="sxs-lookup"><span data-stu-id="d53ed-719">Addresses</span></span>

<span data-ttu-id="d53ed-720">特定の国または地域、都道府県、および市区郡 (自治体) の ID には、Dayforce および国内または地域内のプロバイダーが認識できる特定の形式が必要です。</span><span class="sxs-lookup"><span data-stu-id="d53ed-720">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="d53ed-721">市町村の形式は柔軟ですが、すべての市町村が都道府県と関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d53ed-721">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="d53ed-722">人事管理</span><span class="sxs-lookup"><span data-stu-id="d53ed-722">Human Resources</span></span>              | <span data-ttu-id="d53ed-723">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d53ed-723">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="d53ed-724">国/地域</span><span class="sxs-lookup"><span data-stu-id="d53ed-724">Country/Region</span></span>      | <span data-ttu-id="d53ed-725">国コード</span><span class="sxs-lookup"><span data-stu-id="d53ed-725">Country Code</span></span>          |
| <span data-ttu-id="d53ed-726">郵便番号</span><span class="sxs-lookup"><span data-stu-id="d53ed-726">Zip/Postal Code</span></span>     | <span data-ttu-id="d53ed-727">郵便番号</span><span class="sxs-lookup"><span data-stu-id="d53ed-727">Postal Code</span></span>           |
| <span data-ttu-id="d53ed-728">行政単位 (区画)</span><span class="sxs-lookup"><span data-stu-id="d53ed-728">State</span></span>               | <span data-ttu-id="d53ed-729">都道府県コード</span><span class="sxs-lookup"><span data-stu-id="d53ed-729">State Code</span></span>            |
| <span data-ttu-id="d53ed-730">市町村</span><span class="sxs-lookup"><span data-stu-id="d53ed-730">City</span></span>                | <span data-ttu-id="d53ed-731">市町村</span><span class="sxs-lookup"><span data-stu-id="d53ed-731">City</span></span>                  |
| <span data-ttu-id="d53ed-732">郡</span><span class="sxs-lookup"><span data-stu-id="d53ed-732">County</span></span>              | <span data-ttu-id="d53ed-733">市区郡 (自治体)</span><span class="sxs-lookup"><span data-stu-id="d53ed-733">County (Municipality)</span></span> |
| <span data-ttu-id="d53ed-734">住所</span><span class="sxs-lookup"><span data-stu-id="d53ed-734">Street</span></span>              | <span data-ttu-id="d53ed-735">住所行 1</span><span class="sxs-lookup"><span data-stu-id="d53ed-735">Address Line 1</span></span>        |
| <span data-ttu-id="d53ed-736">番地</span><span class="sxs-lookup"><span data-stu-id="d53ed-736">Street Number</span></span>       | <span data-ttu-id="d53ed-737">住所行 2</span><span class="sxs-lookup"><span data-stu-id="d53ed-737">Address Line 2</span></span>        |
| <span data-ttu-id="d53ed-738">建物名</span><span class="sxs-lookup"><span data-stu-id="d53ed-738">Building Complement</span></span> | <span data-ttu-id="d53ed-739">住所行 5</span><span class="sxs-lookup"><span data-stu-id="d53ed-739">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="d53ed-740">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="d53ed-740">Passport number</span></span>

<span data-ttu-id="d53ed-741">従業員は、パスポート情報を申告できます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-741">Employees can declare passport information.</span></span> <span data-ttu-id="d53ed-742">この情報は、**パスポート** ID タイプになり、従業員のメキシコ固有の情報の一部として Dayforce に統合されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-742">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="d53ed-743">ID タイプ = "Passport"</span><span class="sxs-lookup"><span data-stu-id="d53ed-743">Identification Type = "Passport"</span></span>
- <span data-ttu-id="d53ed-744">発行日付</span><span class="sxs-lookup"><span data-stu-id="d53ed-744">Issued Date</span></span>
- <span data-ttu-id="d53ed-745">有効期限</span><span class="sxs-lookup"><span data-stu-id="d53ed-745">Expiration Date</span></span>

<span data-ttu-id="d53ed-746">従業員は、**パスポート** ID タイプの複数の ID 番号を申告できます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-746">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="d53ed-747">ただし、現在の有効なパスポート入力のみが Dayforce に統合されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-747">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="d53ed-748">すべてのパスポート入力が期限切れの場合、最後に発行されたパスポートが Dayforce に統合されます。</span><span class="sxs-lookup"><span data-stu-id="d53ed-748">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]