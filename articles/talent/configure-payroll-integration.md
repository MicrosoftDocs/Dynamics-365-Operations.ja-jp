---
title: Talent と Dayforce 間での給与統合のコンフィギュレーション
description: このトピックでは、Microsoft Dynamics 365 for Talent と Ceridian Dayforce 間での統合をコンフィギュレーションして、支払実行を処理する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
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
ms.openlocfilehash: c26dfed9909b0dbd05fc18c206e5adc947feaef5
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742918"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="27465-103">Talent と Dayforce 間の給与統合のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="27465-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="27465-104">Microsoft Dynamics 365 for Talent および Ceridian Dayforce 間での統合は、このトピックで説明するいくつかのコンフィギュレーション手順に依存します。</span><span class="sxs-lookup"><span data-stu-id="27465-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="27465-105">支払の実行を処理する前に、Talent および Dayforce の両方で、統合をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="27465-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="27465-106">支払の実行を完了するため Dayforce などのサービスを使用する場合、Talent 内の統合を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="27465-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="27465-107">統合には Talent からの固有データが必要です。</span><span class="sxs-lookup"><span data-stu-id="27465-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="27465-108">したがって、Dayforce にマップされているデータが、統合をサポートする方法で Talent 内でコンフィギュレーションされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27465-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="27465-109">統合は次の広範なデータ カテゴリを使用します。</span><span class="sxs-lookup"><span data-stu-id="27465-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="27465-110">人事管理データ</span><span class="sxs-lookup"><span data-stu-id="27465-110">Human resources data</span></span>
- <span data-ttu-id="27465-111">報酬データ</span><span class="sxs-lookup"><span data-stu-id="27465-111">Compensation data</span></span>
- <span data-ttu-id="27465-112">支払サイクル、支払期間、および所得コードなどの給与データ</span><span class="sxs-lookup"><span data-stu-id="27465-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="27465-113">作業者データ</span><span class="sxs-lookup"><span data-stu-id="27465-113">Worker data</span></span>

<span data-ttu-id="27465-114">このトピックでは、統合を有効にするために従う必要がある手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="27465-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="27465-115">統合に必要なデータの種類およびコンフィギュレーションの詳細についても説明します。</span><span class="sxs-lookup"><span data-stu-id="27465-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="27465-116">統合の有効化</span><span class="sxs-lookup"><span data-stu-id="27465-116">Enable the integration</span></span>

<span data-ttu-id="27465-117">Talent 内で統合を有効にし、Dayforce に接続するコンフィギュレーション情報を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27465-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="27465-118">生成される一般会計トランザクションを Microsoft Dynamics 365 for Finance and Operations にインポートしたい場合、Microsoft Azure ストレージ アカウントを設定し、Finance and Operations 内で、Azure Storage の接続文字列を入力する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="27465-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="27465-119">Talent 内で統合を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="27465-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="27465-120">**システム管理**ページで、**統合コンフィギュレーション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="27465-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="27465-121">セキュリティで保護された FTP (File Transfer Protocol) のエンドポイント、およびセキュリティで保護された FTP フォルダー パスを入力します。</span><span class="sxs-lookup"><span data-stu-id="27465-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="27465-122">セキュリティで保護された FTP エンドポイントおよびフォルダー パスにアクセスするユーザーのユーザー名とパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="27465-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="27465-123">必要に応じて接続をテストし、**給与統合の有効化**のオプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="27465-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="27465-124">統合が有効な場合、データのエクスポート パッケージおよびファイルが作成され、頻度が設定されます。</span><span class="sxs-lookup"><span data-stu-id="27465-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="27465-125">必要に応じて、この頻度を変更できます。</span><span class="sxs-lookup"><span data-stu-id="27465-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="27465-126">Azure ストレージ アカウント および Azure ストレージの接続文字列の詳細については、次の Azure のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="27465-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="27465-127">Azure ストレージ アカウントについて</span><span class="sxs-lookup"><span data-stu-id="27465-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="27465-128">Azure ストレージの接続文字列のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="27465-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="27465-129">給与統合が有効になっている場合の技術詳細</span><span class="sxs-lookup"><span data-stu-id="27465-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="27465-130">給与統合を有効にすることには、次の 2 つの主な効果があります。</span><span class="sxs-lookup"><span data-stu-id="27465-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="27465-131">「給与統合エクスポート」という名前のデータ エクスポート プロジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="27465-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="27465-132">このプロジェクトには、給与統合に必要なエンティティとフィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="27465-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="27465-133">プロジェクトを確認するには、**システム管理**に移動し、**データ管理**タイルを選択して、プロジェクトの一覧からデータ プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="27465-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="27465-134">このバッチ ジョブは、データ エクスポート プロジェクトを実行し、結果のデータ パッケージを暗号化し、**統合コンフィギュレーション**画面でコンフィギュレーションされた SFTP エンドポイントにデータ パッケージ ファイルを転送します。</span><span class="sxs-lookup"><span data-stu-id="27465-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="27465-135">SFTP エンドポイントに転送されるデータ パッケージは、そのパッケージに固有のキーを使用して暗号化されます。</span><span class="sxs-lookup"><span data-stu-id="27465-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="27465-136">キーは、Ceridian によってのみアクセス可能な Azure Key Vault にあります。</span><span class="sxs-lookup"><span data-stu-id="27465-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="27465-137">データ パッケージの内容を復号化して確認することはできません。</span><span class="sxs-lookup"><span data-stu-id="27465-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="27465-138">データ パッケージの内容を確認する必要がある場合は、"給与統合エクスポート" データ プロジェクトを手動でエクスポートし、ダウンロードしてから、それを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="27465-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="27465-139">手動エクスポートでは、暗号化が適用されないか、またはパッケージが転送されません。</span><span class="sxs-lookup"><span data-stu-id="27465-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="27465-140">データのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="27465-140">Configure your data</span></span> 

<span data-ttu-id="27465-141">給与を処理するには、Talent で人事管理のデータをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="27465-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="27465-142">職務と職位などの組織データを、給付金および報酬情報と共に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27465-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="27465-143">この情報は、雇用、支払、および従業員の給与を生成するために必要な控除情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="27465-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="27465-144">人事管理データ</span><span class="sxs-lookup"><span data-stu-id="27465-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="27465-145">福利厚生</span><span class="sxs-lookup"><span data-stu-id="27465-145">Benefits</span></span> 

<span data-ttu-id="27465-146">人事管理は、給付金、控除、および組織が作業者に対して提供または処理する作業者の報酬プランを設定および管理するツールを提供します。</span><span class="sxs-lookup"><span data-stu-id="27465-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="27465-147">給付金を作成する場合、Dayforce で使用される次のデータとコンフィギュレーションに留意してください。</span><span class="sxs-lookup"><span data-stu-id="27465-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="27465-148">福利厚生計画</span><span class="sxs-lookup"><span data-stu-id="27465-148">Benefit plans</span></span>

- <span data-ttu-id="27465-149">計画 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-149">Plan (required)</span></span>
- <span data-ttu-id="27465-150">種類 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-150">Type (required)</span></span>
- <span data-ttu-id="27465-151">給与の影響 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-151">Payroll impact (required)</span></span>
- <span data-ttu-id="27465-152">未払金の回収</span><span class="sxs-lookup"><span data-stu-id="27465-152">Recover arrears</span></span>
- <span data-ttu-id="27465-153">控除方式</span><span class="sxs-lookup"><span data-stu-id="27465-153">Deduction method</span></span>
- <span data-ttu-id="27465-154">控除の優先順位</span><span class="sxs-lookup"><span data-stu-id="27465-154">Deduction priority</span></span>
- <span data-ttu-id="27465-155">制限の期間</span><span class="sxs-lookup"><span data-stu-id="27465-155">Limit period</span></span>
- <span data-ttu-id="27465-156">限度金額</span><span class="sxs-lookup"><span data-stu-id="27465-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="27465-157">福利厚生</span><span class="sxs-lookup"><span data-stu-id="27465-157">Benefits</span></span>

- <span data-ttu-id="27465-158">計画 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-158">Plan (required)</span></span>
- <span data-ttu-id="27465-159">種類 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-159">Type (required)</span></span>
- <span data-ttu-id="27465-160">オプション (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-160">Option (required)</span></span>
- <span data-ttu-id="27465-161">給付金 ID (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-161">Benefit ID (required)</span></span>
- <span data-ttu-id="27465-162">頻度</span><span class="sxs-lookup"><span data-stu-id="27465-162">Frequency</span></span>
- <span data-ttu-id="27465-163">基準</span><span class="sxs-lookup"><span data-stu-id="27465-163">Basis</span></span>
- <span data-ttu-id="27465-164">金額またはレート</span><span class="sxs-lookup"><span data-stu-id="27465-164">Amount or rate</span></span>
- <span data-ttu-id="27465-165">所得コード</span><span class="sxs-lookup"><span data-stu-id="27465-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="27465-166">サポートされる頻度</span><span class="sxs-lookup"><span data-stu-id="27465-166">Supported frequencies</span></span> 

- <span data-ttu-id="27465-167">毎週</span><span class="sxs-lookup"><span data-stu-id="27465-167">Weekly</span></span>
- <span data-ttu-id="27465-168">隔週</span><span class="sxs-lookup"><span data-stu-id="27465-168">Bi-weekly</span></span>
- <span data-ttu-id="27465-169">半月ごと</span><span class="sxs-lookup"><span data-stu-id="27465-169">Semi-monthly</span></span>
- <span data-ttu-id="27465-170">月 1 回</span><span class="sxs-lookup"><span data-stu-id="27465-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="27465-171">サポートされる基準</span><span class="sxs-lookup"><span data-stu-id="27465-171">Supported bases</span></span> 

- <span data-ttu-id="27465-172">固定金額</span><span class="sxs-lookup"><span data-stu-id="27465-172">Fixed amount</span></span>
- <span data-ttu-id="27465-173">所得の割合</span><span class="sxs-lookup"><span data-stu-id="27465-173">Percent of earnings</span></span>
- <span data-ttu-id="27465-174">生産時間</span><span class="sxs-lookup"><span data-stu-id="27465-174">Productive hours</span></span>

<span data-ttu-id="27465-175">Dayforce は、給付金の計画で定義される給与影響に基づいて次の控除を作成します。</span><span class="sxs-lookup"><span data-stu-id="27465-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="27465-176">Talent での選択</span><span class="sxs-lookup"><span data-stu-id="27465-176">Selection in Talent</span></span>        | <span data-ttu-id="27465-177">Dayforce での結果</span><span class="sxs-lookup"><span data-stu-id="27465-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="27465-178">None</span><span class="sxs-lookup"><span data-stu-id="27465-178">None</span></span>                       | <span data-ttu-id="27465-179">控除は作成されません。</span><span class="sxs-lookup"><span data-stu-id="27465-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="27465-180">控除のみ</span><span class="sxs-lookup"><span data-stu-id="27465-180">Deduction only</span></span>             | <span data-ttu-id="27465-181">従業員控除が作成されます。</span><span class="sxs-lookup"><span data-stu-id="27465-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="27465-182">貢献度のみ</span><span class="sxs-lookup"><span data-stu-id="27465-182">Contribution only</span></span>          | <span data-ttu-id="27465-183">雇用主控除が作成されます。</span><span class="sxs-lookup"><span data-stu-id="27465-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="27465-184">控除と貢献度</span><span class="sxs-lookup"><span data-stu-id="27465-184">Deduction and contribution</span></span> | <span data-ttu-id="27465-185">従業員および雇用主の控除が作成されます。</span><span class="sxs-lookup"><span data-stu-id="27465-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="27465-186">給付金プログラムを定義し、管理する方法の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="27465-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="27465-187">従業員手当プログラムの提供</span><span class="sxs-lookup"><span data-stu-id="27465-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="27465-188">新しい給付金の作成</span><span class="sxs-lookup"><span data-stu-id="27465-188">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="27465-189">給付金の適格性ルールおよびポリシーの定義</span><span class="sxs-lookup"><span data-stu-id="27465-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="27465-190">作業者の福利厚生の登録および削除</span><span class="sxs-lookup"><span data-stu-id="27465-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="27465-191">報酬</span><span class="sxs-lookup"><span data-stu-id="27465-191">Compensation</span></span> 

<span data-ttu-id="27465-192">基準賃金と報奨を管理するには、報酬管理を使用します。</span><span class="sxs-lookup"><span data-stu-id="27465-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="27465-193">従業員の固定基準賃金および昇給は固定報酬プランで管理されます。</span><span class="sxs-lookup"><span data-stu-id="27465-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="27465-194">インセンティブ支払 (賞与の支払、業績報奨、ストック オプション、付与など) の支払および一時報奨は変動報酬プランで管理します。</span><span class="sxs-lookup"><span data-stu-id="27465-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="27465-195">Dayforce は、報酬情報を使用して、従業員の時間または年間レートを計算します。</span><span class="sxs-lookup"><span data-stu-id="27465-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="27465-196">固定報酬プランと支払レートの換算が必要です。</span><span class="sxs-lookup"><span data-stu-id="27465-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="27465-197">従業員は固定報酬プランに関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="27465-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="27465-198">報酬プランの詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="27465-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="27465-199">固定報酬プランの作成</span><span class="sxs-lookup"><span data-stu-id="27465-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="27465-200">変動報酬プランの作成</span><span class="sxs-lookup"><span data-stu-id="27465-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="27465-201">給与/報酬構造および計画の作成</span><span class="sxs-lookup"><span data-stu-id="27465-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="27465-202">報酬の処理</span><span class="sxs-lookup"><span data-stu-id="27465-202">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="27465-203">報酬プロセスの定義と結果の計算</span><span class="sxs-lookup"><span data-stu-id="27465-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="27465-204">固定報酬プランへの従業員の登録</span><span class="sxs-lookup"><span data-stu-id="27465-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="27465-205">変動報酬プランへの従業員の登録</span><span class="sxs-lookup"><span data-stu-id="27465-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="27465-206">職務</span><span class="sxs-lookup"><span data-stu-id="27465-206">Jobs</span></span> 

<span data-ttu-id="27465-207">職務とは、職務を遂行する担当者に必要なタスクと職責の集合です。</span><span class="sxs-lookup"><span data-stu-id="27465-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="27465-208">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="27465-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="27465-209">職務のコンポーネントの設定</span><span class="sxs-lookup"><span data-stu-id="27465-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="27465-210">新しいジョブの定義</span><span class="sxs-lookup"><span data-stu-id="27465-210">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="27465-211">職位</span><span class="sxs-lookup"><span data-stu-id="27465-211">Positions</span></span>

<span data-ttu-id="27465-212">職位は、職務の個々のインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="27465-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="27465-213">たとえば、「販売マネージャー (東部)」という職位は、「販売マネージャー」という職務に関連付けられている職位の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="27465-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="27465-214">職位は、部門内に存在します。</span><span class="sxs-lookup"><span data-stu-id="27465-214">A position exists in a department.</span></span> <span data-ttu-id="27465-215">1 人の作業者は 1 つの職位にのみ関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="27465-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="27465-216">職位を設定する場合、次のデータとコンフィギュレーションに注意してください。</span><span class="sxs-lookup"><span data-stu-id="27465-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="27465-217">職位 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-217">Position (required)</span></span>
- <span data-ttu-id="27465-218">説明 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-218">Description (required)</span></span>
- <span data-ttu-id="27465-219">職務 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-219">Job (required)</span></span>
- <span data-ttu-id="27465-220">部門 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-220">Department (required)</span></span>
- <span data-ttu-id="27465-221">職位タイプ (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-221">Position type (required)</span></span>
- <span data-ttu-id="27465-222">フルタイム相当</span><span class="sxs-lookup"><span data-stu-id="27465-222">Full-time equivalent</span></span>
- <span data-ttu-id="27465-223">年間基本勤務時間 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="27465-224">法人による支払 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="27465-225">支払サイクル (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-225">Pay cycle (required)</span></span>
- <span data-ttu-id="27465-226">既定の財務分析コード – 原価部門 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="27465-227">作業者割り当て – 作業者、割り当ての開始、割り当ての終了、理由コード</span><span class="sxs-lookup"><span data-stu-id="27465-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="27465-228">同じ部門の複数の職位が同じジョブに関連付けられている場合、Dayforce で 1 つの職位に連結します。</span><span class="sxs-lookup"><span data-stu-id="27465-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="27465-229">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="27465-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="27465-230">部門、職務、職位を使用した従業員の編成</span><span class="sxs-lookup"><span data-stu-id="27465-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="27465-231">職位の設定</span><span class="sxs-lookup"><span data-stu-id="27465-231">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="27465-232">部門</span><span class="sxs-lookup"><span data-stu-id="27465-232">Departments</span></span>

<span data-ttu-id="27465-233">部門は、組織のカテゴリまたは機能領域を表す作業単位です。</span><span class="sxs-lookup"><span data-stu-id="27465-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="27465-234">部門は、販売、会計、または人事管理など、組織内の特定の領域を担当します。</span><span class="sxs-lookup"><span data-stu-id="27465-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="27465-235">機能領域の報告に部門を使用できます。</span><span class="sxs-lookup"><span data-stu-id="27465-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="27465-236">部門は損益の職責を持つ場合があります。</span><span class="sxs-lookup"><span data-stu-id="27465-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="27465-237">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="27465-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="27465-238">部門の作成と部門階層への関連付け</span><span class="sxs-lookup"><span data-stu-id="27465-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="27465-239">新しい部門の定義</span><span class="sxs-lookup"><span data-stu-id="27465-239">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="27465-240">支払サイクルと支払期間</span><span class="sxs-lookup"><span data-stu-id="27465-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="27465-241">給与計算頻度および作業者が支払を受ける特定の日は、支払サイクルによって決まります。</span><span class="sxs-lookup"><span data-stu-id="27465-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="27465-242">たとえば、支払サイクルが月単位で、その月の最後の日に従業員に支払われる場合があります。</span><span class="sxs-lookup"><span data-stu-id="27465-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="27465-243">または、支払サイクルが週単位で、支払期間終了日の次の火曜日に支払われる場合もあります。</span><span class="sxs-lookup"><span data-stu-id="27465-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="27465-244">支払サイクルは、それらの職位にある作業者にいつ支払われるかを制御するために、職位に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="27465-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="27465-245">支払サイクルを作成した後、各サイクルごとに支払期間を生成できます。</span><span class="sxs-lookup"><span data-stu-id="27465-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="27465-246">各支払期間には、入力した情報に基づく既定の支払期日が含まれます。</span><span class="sxs-lookup"><span data-stu-id="27465-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="27465-247">ただし、支払期日が休日になる場合などの例外を許可するため、支払期間の既定の支払期日を変更できます。</span><span class="sxs-lookup"><span data-stu-id="27465-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="27465-248">次の情報は、Dayforce で使用されます。</span><span class="sxs-lookup"><span data-stu-id="27465-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="27465-249">支払サイクル (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-249">Pay cycle (required)</span></span>
- <span data-ttu-id="27465-250">支払サイクル頻度 (頻度)</span><span class="sxs-lookup"><span data-stu-id="27465-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="27465-251">期間開始日 (最初の支払期間は必須)</span><span class="sxs-lookup"><span data-stu-id="27465-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="27465-252">既定の支払期日 (最初の支払期間は必須)</span><span class="sxs-lookup"><span data-stu-id="27465-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="27465-253">この情報は、支払グループとして Dayforce に統合され、各支払サイクルごとに国または地域で区切られます。</span><span class="sxs-lookup"><span data-stu-id="27465-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="27465-254">統合の前に、少なくとも 1 つの支払期間を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27465-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="27465-255">Dayforce は、最初の支払期日の開始日および Talent で設定された既定の支払期日に基づいて、支払グループのカレンダーと支払期日を生成します。</span><span class="sxs-lookup"><span data-stu-id="27465-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="27465-256">所得コード</span><span class="sxs-lookup"><span data-stu-id="27465-256">Earning codes</span></span>

<span data-ttu-id="27465-257">所得コードは、作業者が受け取るすべての収益のタイプを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="27465-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="27465-258">コードには、会計ルール、税法、レポート要件、およびグロスアップ能力など、所得に関連付けられているさまざまなパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="27465-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="27465-259">次の情報は、Dayforce で使用されます。</span><span class="sxs-lookup"><span data-stu-id="27465-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="27465-260">所得コード (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-260">Earning Code (required)</span></span>
- <span data-ttu-id="27465-261">説明</span><span class="sxs-lookup"><span data-stu-id="27465-261">Description</span></span>
- <span data-ttu-id="27465-262">計量単位</span><span class="sxs-lookup"><span data-stu-id="27465-262">Unit of measure</span></span>
- <span data-ttu-id="27465-263">生産</span><span class="sxs-lookup"><span data-stu-id="27465-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="27465-264">作業者データ</span><span class="sxs-lookup"><span data-stu-id="27465-264">Worker data</span></span>

<span data-ttu-id="27465-265">人事管理と給与システムにとって、所有しているさまざまなタイプの作業者のレコードは重要です。</span><span class="sxs-lookup"><span data-stu-id="27465-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="27465-266">入力された情報を使用して、作業者と個人情報を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="27465-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="27465-267">作業者には次の情報を管理できます。</span><span class="sxs-lookup"><span data-stu-id="27465-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="27465-268">**基本** – 連絡先情報、人口学的情報、識別情報、家族情報、兵役の状態、海外在住情報、自宅、緊急連絡先など、作業者に関する基本的な情報を管理します。</span><span class="sxs-lookup"><span data-stu-id="27465-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="27465-269">**雇用** – 法人や組織への所属、職位割り当て、開始日と終了日、業務適性、雇用条件、年金、休暇、再配置情報など、作業者の雇用に関する情報を管理します。</span><span class="sxs-lookup"><span data-stu-id="27465-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="27465-270">**休暇** – 作業カレンダー、休暇トランザクション、休暇設定など、作業者の休暇に関する情報を管理します。</span><span class="sxs-lookup"><span data-stu-id="27465-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="27465-271">**報酬と給与** – プラン登録、報奨、実績、手数料、税金情報、退職、給与控除など、作業者の報酬プランと給与情報に関する情報を管理します。</span><span class="sxs-lookup"><span data-stu-id="27465-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="27465-272">作業者情報を入力する場合、Dayforce で使用される次のデータとコンフィギュレーションに留意してください。</span><span class="sxs-lookup"><span data-stu-id="27465-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="27465-273">一般情報</span><span class="sxs-lookup"><span data-stu-id="27465-273">General information</span></span>

- <span data-ttu-id="27465-274">個人番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-274">Personnel number (required)</span></span>
- <span data-ttu-id="27465-275">名 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-275">First name (required)</span></span>
- <span data-ttu-id="27465-276">姓 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-276">Last name (required)</span></span>
- <span data-ttu-id="27465-277">ミドル ネーム</span><span class="sxs-lookup"><span data-stu-id="27465-277">Middle name</span></span>
- <span data-ttu-id="27465-278">勤続日数</span><span class="sxs-lookup"><span data-stu-id="27465-278">Seniority date</span></span>
- <span data-ttu-id="27465-279">呼称</span><span class="sxs-lookup"><span data-stu-id="27465-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="27465-280">個人情報</span><span class="sxs-lookup"><span data-stu-id="27465-280">Personal information</span></span>

- <span data-ttu-id="27465-281">配偶者の有無 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-281">Marital status (required)</span></span>
- <span data-ttu-id="27465-282">生年月日 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-282">Birth date (required)</span></span>
- <span data-ttu-id="27465-283">性別 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-283">Gender (required)</span></span>
- <span data-ttu-id="27465-284">障碍のあるユーザー</span><span class="sxs-lookup"><span data-stu-id="27465-284">Person with disabilities</span></span>
- <span data-ttu-id="27465-285">国籍 国 地域 (メキシコの場合のみ)</span><span class="sxs-lookup"><span data-stu-id="27465-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="27465-286">住所情報</span><span class="sxs-lookup"><span data-stu-id="27465-286">Address information</span></span>

- <span data-ttu-id="27465-287">基本 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-287">Primary (required)</span></span>
- <span data-ttu-id="27465-288">国/地域 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-288">Country/region (required)</span></span>
- <span data-ttu-id="27465-289">郵便番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-289">Postal code (required)</span></span>
- <span data-ttu-id="27465-290">番地 (必須) (メキシコの場合のみ)</span><span class="sxs-lookup"><span data-stu-id="27465-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="27465-291">建物名 (メキシコの場合のみ)</span><span class="sxs-lookup"><span data-stu-id="27465-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="27465-292">市町村 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-292">City (required)</span></span>
- <span data-ttu-id="27465-293">都道府県 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-293">State (required)</span></span>
- <span data-ttu-id="27465-294">国 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="27465-295">連絡先情報</span><span class="sxs-lookup"><span data-stu-id="27465-295">Contact information</span></span> 

- <span data-ttu-id="27465-296">基本 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-296">Primary (required)</span></span>
- <span data-ttu-id="27465-297">連絡先の電話番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-297">Contact number (required)</span></span>
- <span data-ttu-id="27465-298">内線</span><span class="sxs-lookup"><span data-stu-id="27465-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="27465-299">給与情報および所得コード</span><span class="sxs-lookup"><span data-stu-id="27465-299">Payroll information and earning codes</span></span>

<span data-ttu-id="27465-300">従業員は、指定された支払頻度で特定の所得が割り当てられ、希望の支払方法を有する場合があります。</span><span class="sxs-lookup"><span data-stu-id="27465-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="27465-301">次のフィールドは、それらの基本設定と設定が使用されることを保証するために Dayforce で使用されます。</span><span class="sxs-lookup"><span data-stu-id="27465-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="27465-302">所得コード</span><span class="sxs-lookup"><span data-stu-id="27465-302">Earning codes</span></span>

- <span data-ttu-id="27465-303">職位 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-303">Position (required)</span></span>
- <span data-ttu-id="27465-304">所得コード (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-304">Earning Code (required)</span></span>
- <span data-ttu-id="27465-305">頻度 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-305">Frequency (required)</span></span>
- <span data-ttu-id="27465-306">金額 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="27465-307">給与情報</span><span class="sxs-lookup"><span data-stu-id="27465-307">Payroll information</span></span>

- <span data-ttu-id="27465-308">支払方法</span><span class="sxs-lookup"><span data-stu-id="27465-308">Payment Method</span></span>
- <span data-ttu-id="27465-309">経済地域 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-309">Economic Region (required)</span></span>
- <span data-ttu-id="27465-310">従業員手当 ID</span><span class="sxs-lookup"><span data-stu-id="27465-310">Employee Benefits ID</span></span>
- <span data-ttu-id="27465-311">国民 ID 番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-311">National ID Number (required)</span></span>
- <span data-ttu-id="27465-312">兵役番号</span><span class="sxs-lookup"><span data-stu-id="27465-312">Military Service Number</span></span>
- <span data-ttu-id="27465-313">シフト ID (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-313">Shift ID (required)</span></span>
- <span data-ttu-id="27465-314">税番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-314">Tax Number (required)</span></span>
- <span data-ttu-id="27465-315">労働組合 ID (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-315">Union ID (required)</span></span>
- <span data-ttu-id="27465-316">作業日 ID (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-316">Work Day ID (required)</span></span>
- <span data-ttu-id="27465-317">労働許可番号</span><span class="sxs-lookup"><span data-stu-id="27465-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="27465-318">支払方法について、メキシコでは**現金**、**小切手** (会社の現物小切手)、および**電子支払**がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="27465-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="27465-319">NP 支払方法が指定されている場合、既定で**小切手**が使用されます。</span><span class="sxs-lookup"><span data-stu-id="27465-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="27465-320">従業員の詳細</span><span class="sxs-lookup"><span data-stu-id="27465-320">Employment details</span></span>

<span data-ttu-id="27465-321">雇用の詳細履歴は、Dayforce で従業員の採用、退職、および再雇用のステータスを派生させるため、重要な情報として使用されます。</span><span class="sxs-lookup"><span data-stu-id="27465-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="27465-322">Dayforce は、一度に 1 つだけ有効な雇用レコードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="27465-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="27465-323">雇用開始日 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-323">Employment start date (required)</span></span>
- <span data-ttu-id="27465-324">雇用終了日</span><span class="sxs-lookup"><span data-stu-id="27465-324">Employment end date</span></span>
- <span data-ttu-id="27465-325">入社日</span><span class="sxs-lookup"><span data-stu-id="27465-325">Start date</span></span>
- <span data-ttu-id="27465-326">調整済開始日</span><span class="sxs-lookup"><span data-stu-id="27465-326">Adjusted start date</span></span>
- <span data-ttu-id="27465-327">退職日 (退職時は必須)</span><span class="sxs-lookup"><span data-stu-id="27465-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="27465-328">退職理由 (退職時は必須)</span><span class="sxs-lookup"><span data-stu-id="27465-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="27465-329">従業員の重要な日付は、次の情報を使用して派生されます。</span><span class="sxs-lookup"><span data-stu-id="27465-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="27465-330">Talent</span><span class="sxs-lookup"><span data-stu-id="27465-330">Talent</span></span>                | <span data-ttu-id="27465-331">Dayforce</span><span class="sxs-lookup"><span data-stu-id="27465-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27465-332">最新の採用日付</span><span class="sxs-lookup"><span data-stu-id="27465-332">Most recent hire date</span></span> | <span data-ttu-id="27465-333">現在の非退職雇用履歴レコードの雇用開始</span><span class="sxs-lookup"><span data-stu-id="27465-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="27465-334">退職日</span><span class="sxs-lookup"><span data-stu-id="27465-334">Termination date</span></span>      | <span data-ttu-id="27465-335">現在の非退職雇用履歴レコードの退職日</span><span class="sxs-lookup"><span data-stu-id="27465-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="27465-336">入社日</span><span class="sxs-lookup"><span data-stu-id="27465-336">Start date</span></span>            | <span data-ttu-id="27465-337">現在の非アクティブ雇用履歴レコードの調整済開始日、開始日、または雇用開始</span><span class="sxs-lookup"><span data-stu-id="27465-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="27465-338">元の採用日付</span><span class="sxs-lookup"><span data-stu-id="27465-338">Original hire date</span></span>    | <span data-ttu-id="27465-339">最も早い雇用履歴レコードの雇用開始</span><span class="sxs-lookup"><span data-stu-id="27465-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="27465-340">報酬</span><span class="sxs-lookup"><span data-stu-id="27465-340">Compensation</span></span>

<span data-ttu-id="27465-341">固定報酬計画は、雇用期間全体ですべての従業員の基本職位に関連付けられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="27465-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="27465-342">この期間は、従業員が採用された日付 (または雇用の開始日) に開始し、退職するまで継続します。</span><span class="sxs-lookup"><span data-stu-id="27465-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="27465-343">有効日 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-343">Effective Date (required)</span></span>
- <span data-ttu-id="27465-344">有効期限</span><span class="sxs-lookup"><span data-stu-id="27465-344">Expiration date</span></span>
- <span data-ttu-id="27465-345">支払レート (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-345">Pay Rate (required)</span></span>
- <span data-ttu-id="27465-346">支払レートの変換 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="27465-347">年間相当額 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="27465-348">時間相当額 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="27465-349">時給払いの従業員に複数の職位がある場合、基本職位の固定報酬が作業者レベルの基準レートまたは給与として Dayforce にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="27465-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="27465-350">基本以外の職位については、時給のレートが Dayforce の対応する職位に保存されます。</span><span class="sxs-lookup"><span data-stu-id="27465-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="27465-351">月給払いの従業員に複数の職位がある場合、累計時間率およびすべての有効な職位全体での年間給与が派生され、従業員レベルの基準レートまたは給与として使用されます。</span><span class="sxs-lookup"><span data-stu-id="27465-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="27465-352">ID 番号</span><span class="sxs-lookup"><span data-stu-id="27465-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="27465-353">社会保障 ID</span><span class="sxs-lookup"><span data-stu-id="27465-353">Social Security identifier</span></span> 

<span data-ttu-id="27465-354">すべての従業員は、1 つの基本 ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="27465-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="27465-355">この ID は **SSN** ID タイプにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="27465-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="27465-356">Dayforce では、採用に必要な従業員の社会保障 ID として自動的に派生されます。</span><span class="sxs-lookup"><span data-stu-id="27465-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="27465-357">基本 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-357">Primary (required)</span></span>
- <span data-ttu-id="27465-358">ID タイプ = "SSN"</span><span class="sxs-lookup"><span data-stu-id="27465-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="27465-359">発行日付</span><span class="sxs-lookup"><span data-stu-id="27465-359">Issued Date</span></span>
- <span data-ttu-id="27465-360">有効期限</span><span class="sxs-lookup"><span data-stu-id="27465-360">Expiration Date</span></span>

<span data-ttu-id="27465-361">従業員は、**SSN** ID タイプの複数の ID 番号を申告できます。</span><span class="sxs-lookup"><span data-stu-id="27465-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="27465-362">ただし、その番号が有効かまたは期限切れかに関係なく、**基本**としてマークされているレコードのみ Dayforce に統合されます。</span><span class="sxs-lookup"><span data-stu-id="27465-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="27465-363">銀行口座および出金</span><span class="sxs-lookup"><span data-stu-id="27465-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="27465-364">銀行口座振替による支払を選択した従業員すべてのために、有効な銀行口座情報を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27465-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="27465-365">Talent</span><span class="sxs-lookup"><span data-stu-id="27465-365">Talent</span></span>                         | <span data-ttu-id="27465-366">Dayforce</span><span class="sxs-lookup"><span data-stu-id="27465-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27465-367">銀行口座番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="27465-368">SWIFT コード (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-368">SWIFT code (required)</span></span>          | <span data-ttu-id="27465-369">メキシコの給与処理に使用される**銀行 ID** フィールド。</span><span class="sxs-lookup"><span data-stu-id="27465-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="27465-370">支店番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="27465-371">銀行口座の種類 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-371">Bank account type (required)</span></span>   | <span data-ttu-id="27465-372">メキシコの給与処理に使用される**口座の種類**フィールド。</span><span class="sxs-lookup"><span data-stu-id="27465-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="27465-373">サポートされている値には、**当座預金**および**給与**が含まれます。</span><span class="sxs-lookup"><span data-stu-id="27465-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="27465-374">銀行口座振替による支払を選択した従業員は、メキシコに基本住所を持つ法人の下にあり、メキシコの銀行から有効な銀行口座に関連付けられている残余口座のリンクを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27465-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="27465-375">その他のすべての非残余口座は無視されます。</span><span class="sxs-lookup"><span data-stu-id="27465-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="27465-376">住所情報</span><span class="sxs-lookup"><span data-stu-id="27465-376">Address information</span></span>

<span data-ttu-id="27465-377">すべての従業員は、1 つの基本場所が必要です。</span><span class="sxs-lookup"><span data-stu-id="27465-377">Every employee must have one primary location.</span></span> <span data-ttu-id="27465-378">Dayforce において、この場所は課税額算出のために従業員の基本居住地を特定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="27465-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="27465-379">基本 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-379">Primary (required)</span></span>
- <span data-ttu-id="27465-380">国/地域 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-380">Country/region (required)</span></span>
- <span data-ttu-id="27465-381">郵便番号 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="27465-382">住所 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-382">Street (required)</span></span>
- <span data-ttu-id="27465-383">番地 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-383">Street Number (required)</span></span>
- <span data-ttu-id="27465-384">建物名</span><span class="sxs-lookup"><span data-stu-id="27465-384">Building Complement</span></span>
- <span data-ttu-id="27465-385">市町村 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-385">City (required)</span></span>
- <span data-ttu-id="27465-386">都道府県 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-386">State (required)</span></span>
- <span data-ttu-id="27465-387">国 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="27465-388">米国およびカナダでの給与を生成するために、データをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="27465-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="27465-389">米国およびカナダの従業員のために支払を生成している場合、次の要素をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="27465-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="27465-390">職位に部門が必要です。</span><span class="sxs-lookup"><span data-stu-id="27465-390">Departments are required on positions.</span></span>
- <span data-ttu-id="27465-391">原価部門を財務分析コードとして設定し、既定の財務分析コード文字列の最初の要素とする必要があります。</span><span class="sxs-lookup"><span data-stu-id="27465-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="27465-392">職位が部門を指定するように人材を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="27465-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="27465-393">この作業を実行するには、**人事管理共有職位 > 職位 > 職位の部門を要求**に移動します。</span><span class="sxs-lookup"><span data-stu-id="27465-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="27465-394">この設定は、システムの統合に適用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="27465-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="27465-395">職務タイプ</span><span class="sxs-lookup"><span data-stu-id="27465-395">Job types</span></span>

<span data-ttu-id="27465-396">職務タイプは、類似した職務をカテゴリにグループ化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="27465-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="27465-397">職務タイプは、米国およびカナダでの給与を処理するために必要です。</span><span class="sxs-lookup"><span data-stu-id="27465-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="27465-398">職務タイプの例には、フルタイムおよびパートタイム、または給与払いおよび時給払いが含まれます。</span><span class="sxs-lookup"><span data-stu-id="27465-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="27465-399">職務タイプは、従業員が時給払いかあるいは給与払いなのかを示す支払タイプとして Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="27465-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="27465-400">次の職務タイプと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="27465-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="27465-401">ジョブ タイプ</span><span class="sxs-lookup"><span data-stu-id="27465-401">Job type</span></span>   | <span data-ttu-id="27465-402">説明</span><span class="sxs-lookup"><span data-stu-id="27465-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="27465-403">時間</span><span class="sxs-lookup"><span data-stu-id="27465-403">Hourly</span></span>     | <span data-ttu-id="27465-404">時間</span><span class="sxs-lookup"><span data-stu-id="27465-404">Hourly</span></span>      |
| <span data-ttu-id="27465-405">給与払い</span><span class="sxs-lookup"><span data-stu-id="27465-405">Salaried</span></span>   | <span data-ttu-id="27465-406">給与払い</span><span class="sxs-lookup"><span data-stu-id="27465-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="27465-407">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="27465-407">Position types</span></span> 

<span data-ttu-id="27465-408">職位がフルタイム、パートタイム、またはその他のタイプかどうかを説明するために職位タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="27465-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="27465-409">職位タイプは、従業員がフルタイムかあるいはパートタイムなのかを示す支払クラスとして Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="27465-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="27465-410">次の職位タイプと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="27465-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="27465-411">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="27465-411">Position type</span></span>   | <span data-ttu-id="27465-412">説明</span><span class="sxs-lookup"><span data-stu-id="27465-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="27465-413">フルタイム</span><span class="sxs-lookup"><span data-stu-id="27465-413">Full-time</span></span>       | <span data-ttu-id="27465-414">フルタイム従業員</span><span class="sxs-lookup"><span data-stu-id="27465-414">Full time employee</span></span> |
| <span data-ttu-id="27465-415">パートタイム</span><span class="sxs-lookup"><span data-stu-id="27465-415">Part-time</span></span>       | <span data-ttu-id="27465-416">パートタイム従業員</span><span class="sxs-lookup"><span data-stu-id="27465-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="27465-417">理由コード</span><span class="sxs-lookup"><span data-stu-id="27465-417">Reason codes</span></span>

<span data-ttu-id="27465-418">理由コードは、従業員のステータスに関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="27465-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="27465-419">理由コードは、従業員の職位または雇用ステータスへの変更の理由を示すステータス理由として Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="27465-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="27465-420">次の理由コードと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="27465-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="27465-421">理由コード</span><span class="sxs-lookup"><span data-stu-id="27465-421">Reason code</span></span>    | <span data-ttu-id="27465-422">説明</span><span class="sxs-lookup"><span data-stu-id="27465-422">Description</span></span>      | <span data-ttu-id="27465-423">適用可能なシナリオ</span><span class="sxs-lookup"><span data-stu-id="27465-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="27465-424">辞職</span><span class="sxs-lookup"><span data-stu-id="27465-424">RESIGNATION</span></span>    | <span data-ttu-id="27465-425">辞職</span><span class="sxs-lookup"><span data-stu-id="27465-425">Resignation</span></span>      | <span data-ttu-id="27465-426">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="27465-426">Terminate worker</span></span>     |
| <span data-ttu-id="27465-427">終了</span><span class="sxs-lookup"><span data-stu-id="27465-427">TERMINATION</span></span>    | <span data-ttu-id="27465-428">終了</span><span class="sxs-lookup"><span data-stu-id="27465-428">Termination</span></span>      | <span data-ttu-id="27465-429">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="27465-429">Terminate worker</span></span>     |
| <span data-ttu-id="27465-430">定年退職</span><span class="sxs-lookup"><span data-stu-id="27465-430">RETIREMENT</span></span>     | <span data-ttu-id="27465-431">償却</span><span class="sxs-lookup"><span data-stu-id="27465-431">Retirement</span></span>       | <span data-ttu-id="27465-432">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="27465-432">Terminate worker</span></span>     |
| <span data-ttu-id="27465-433">その他</span><span class="sxs-lookup"><span data-stu-id="27465-433">OTHER</span></span>          | <span data-ttu-id="27465-434">その他の理由</span><span class="sxs-lookup"><span data-stu-id="27465-434">Other Reasons</span></span>    | <span data-ttu-id="27465-435">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="27465-435">Terminate worker</span></span>     |
| <span data-ttu-id="27465-436">死亡</span><span class="sxs-lookup"><span data-stu-id="27465-436">DEATH</span></span>          | <span data-ttu-id="27465-437">死亡</span><span class="sxs-lookup"><span data-stu-id="27465-437">Death</span></span>            | <span data-ttu-id="27465-438">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="27465-438">Terminate worker</span></span>     |
| <span data-ttu-id="27465-439">休暇</span><span class="sxs-lookup"><span data-stu-id="27465-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="27465-440">休暇</span><span class="sxs-lookup"><span data-stu-id="27465-440">Leave of Absence</span></span> | <span data-ttu-id="27465-441">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="27465-441">Terminate worker</span></span>     |
| <span data-ttu-id="27465-442">契約の終了</span><span class="sxs-lookup"><span data-stu-id="27465-442">CONTRACTEND</span></span>    | <span data-ttu-id="27465-443">契約の終了</span><span class="sxs-lookup"><span data-stu-id="27465-443">End of Contract</span></span>  | <span data-ttu-id="27465-444">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="27465-444">Terminate worker</span></span>     |
| <span data-ttu-id="27465-445">給与の変更</span><span class="sxs-lookup"><span data-stu-id="27465-445">SALARYCHANGE</span></span>   | <span data-ttu-id="27465-446">給与の変更</span><span class="sxs-lookup"><span data-stu-id="27465-446">Change of Salary</span></span> | <span data-ttu-id="27465-447">報酬</span><span class="sxs-lookup"><span data-stu-id="27465-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="27465-448">配偶者の有無</span><span class="sxs-lookup"><span data-stu-id="27465-448">Marital status</span></span>

<span data-ttu-id="27465-449">配偶者有無の値は、Dayforce にマップされ、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="27465-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="27465-450">次の表に、配偶者有無の値がどのように Dayforce にマップされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="27465-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="27465-451">Talent</span><span class="sxs-lookup"><span data-stu-id="27465-451">Talent</span></span>                 | <span data-ttu-id="27465-452">Dayforce</span><span class="sxs-lookup"><span data-stu-id="27465-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="27465-453">既婚</span><span class="sxs-lookup"><span data-stu-id="27465-453">Married</span></span>                | <span data-ttu-id="27465-454">既婚</span><span class="sxs-lookup"><span data-stu-id="27465-454">Married</span></span>              |
| <span data-ttu-id="27465-455">未婚</span><span class="sxs-lookup"><span data-stu-id="27465-455">Single</span></span>                 | <span data-ttu-id="27465-456">未婚</span><span class="sxs-lookup"><span data-stu-id="27465-456">Single</span></span>               |
| <span data-ttu-id="27465-457">死別</span><span class="sxs-lookup"><span data-stu-id="27465-457">Widowed</span></span>                | <span data-ttu-id="27465-458">死別</span><span class="sxs-lookup"><span data-stu-id="27465-458">Widowed</span></span>              |
| <span data-ttu-id="27465-459">離婚</span><span class="sxs-lookup"><span data-stu-id="27465-459">Divorced</span></span>               | <span data-ttu-id="27465-460">離婚</span><span class="sxs-lookup"><span data-stu-id="27465-460">Divorced</span></span>             |
| <span data-ttu-id="27465-461">登録済パートナーシップ</span><span class="sxs-lookup"><span data-stu-id="27465-461">Registered Partnership</span></span> | <span data-ttu-id="27465-462">ドメスティック パートナーシップ</span><span class="sxs-lookup"><span data-stu-id="27465-462">Domestic Partnership</span></span> |
| <span data-ttu-id="27465-463">None</span><span class="sxs-lookup"><span data-stu-id="27465-463">None</span></span>                   | <span data-ttu-id="27465-464">None</span><span class="sxs-lookup"><span data-stu-id="27465-464">None</span></span>                 |
| <span data-ttu-id="27465-465">同棲中</span><span class="sxs-lookup"><span data-stu-id="27465-465">Cohabiting</span></span>             | <span data-ttu-id="27465-466">同棲中</span><span class="sxs-lookup"><span data-stu-id="27465-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="27465-467">種類</span><span class="sxs-lookup"><span data-stu-id="27465-467">Gender</span></span>

<span data-ttu-id="27465-468">性別の指定は、Dayforce にマップされ、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="27465-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="27465-469">次の表に、性別の指定がどのように Dayforce にマップされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="27465-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="27465-470">Talent</span><span class="sxs-lookup"><span data-stu-id="27465-470">Talent</span></span>       | <span data-ttu-id="27465-471">Dayforce</span><span class="sxs-lookup"><span data-stu-id="27465-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="27465-472">男性</span><span class="sxs-lookup"><span data-stu-id="27465-472">Male</span></span>         | <span data-ttu-id="27465-473">男性</span><span class="sxs-lookup"><span data-stu-id="27465-473">Male</span></span>            |
| <span data-ttu-id="27465-474">女性</span><span class="sxs-lookup"><span data-stu-id="27465-474">Female</span></span>       | <span data-ttu-id="27465-475">女性</span><span class="sxs-lookup"><span data-stu-id="27465-475">Female</span></span>          |
| <span data-ttu-id="27465-476">不特定</span><span class="sxs-lookup"><span data-stu-id="27465-476">Non-specific</span></span> | <span data-ttu-id="27465-477">*サポートされていません*</span><span class="sxs-lookup"><span data-stu-id="27465-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="27465-478">所得コード</span><span class="sxs-lookup"><span data-stu-id="27465-478">Earning codes</span></span>

<span data-ttu-id="27465-479">所得コードは、作業者が受け取るすべての収益のタイプを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="27465-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="27465-480">コードには、会計ルール、税法、レポート要件、およびグロスアップ能力など、所得に関連付けられている複数のパラメーターが含まれます。</span><span class="sxs-lookup"><span data-stu-id="27465-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="27465-481">サポートされていない頻度を使用する場合、既定で**すべての支払**頻度が計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="27465-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="27465-482">サポートされる頻度</span><span class="sxs-lookup"><span data-stu-id="27465-482">Supported frequencies</span></span>

- <span data-ttu-id="27465-483">All</span><span class="sxs-lookup"><span data-stu-id="27465-483">All</span></span>
- <span data-ttu-id="27465-484">すべての支払</span><span class="sxs-lookup"><span data-stu-id="27465-484">EVERYPAY</span></span>
- <span data-ttu-id="27465-485">各支払期間</span><span class="sxs-lookup"><span data-stu-id="27465-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="27465-486">他のすべての奇数支払</span><span class="sxs-lookup"><span data-stu-id="27465-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="27465-487">他のすべての偶数支払</span><span class="sxs-lookup"><span data-stu-id="27465-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="27465-488">1 か月</span><span class="sxs-lookup"><span data-stu-id="27465-488">1OFMTH</span></span>
- <span data-ttu-id="27465-489">月の最終日</span><span class="sxs-lookup"><span data-stu-id="27465-489">LASTOFMTH</span></span>
- <span data-ttu-id="27465-490">2 か月</span><span class="sxs-lookup"><span data-stu-id="27465-490">2OFMTH</span></span>
- <span data-ttu-id="27465-491">3 か月</span><span class="sxs-lookup"><span data-stu-id="27465-491">3OFMTH</span></span>
- <span data-ttu-id="27465-492">4 か月</span><span class="sxs-lookup"><span data-stu-id="27465-492">4OFMTH</span></span>
- <span data-ttu-id="27465-493">5 か月</span><span class="sxs-lookup"><span data-stu-id="27465-493">5OFMTH</span></span>
- <span data-ttu-id="27465-494">1 か月および 2 か月</span><span class="sxs-lookup"><span data-stu-id="27465-494">1N2OFMTH</span></span>
- <span data-ttu-id="27465-495">3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="27465-495">3N4OFMTH</span></span>
- <span data-ttu-id="27465-496">1 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="27465-496">1N3OFMTH</span></span>
- <span data-ttu-id="27465-497">1 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="27465-497">1N4OFMTH</span></span>
- <span data-ttu-id="27465-498">2 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="27465-498">2N3OFMTH</span></span>
- <span data-ttu-id="27465-499">2 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="27465-499">2N4OFMTH</span></span>
- <span data-ttu-id="27465-500">1 か月、2 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="27465-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="27465-501">1 か月、2 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="27465-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="27465-502">1 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="27465-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="27465-503">2 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="27465-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="27465-504">1 か月、2 か月、3 か月および 4 か月 - 1 か月、2 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="27465-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="27465-505">2 か月、3 か月、4 か月および 5 か月 - 2 か月、3 か月、4 か月および 5 か月</span><span class="sxs-lookup"><span data-stu-id="27465-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="27465-506">四半期の 1 - 四半期の 1</span><span class="sxs-lookup"><span data-stu-id="27465-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="27465-507">四半期の最終日 – 四半期の最終日</span><span class="sxs-lookup"><span data-stu-id="27465-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="27465-508">四半期の最後の月 – 四半期の最後の月</span><span class="sxs-lookup"><span data-stu-id="27465-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="27465-509">1 年 - 1 年</span><span class="sxs-lookup"><span data-stu-id="27465-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="27465-510">年の最終日 – 年の最終日</span><span class="sxs-lookup"><span data-stu-id="27465-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="27465-511">年の 11 月および 12 月 - 年の 11 月および 12 月</span><span class="sxs-lookup"><span data-stu-id="27465-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="27465-512">住所</span><span class="sxs-lookup"><span data-stu-id="27465-512">Addresses</span></span>

<span data-ttu-id="27465-513">特定の国または地域、都道府県、および市区郡 (自治体) の ID には、Dayforce および国内または地域内のプロバイダーが認識できる特定の形式が必要です。</span><span class="sxs-lookup"><span data-stu-id="27465-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="27465-514">市町村の形式は柔軟ですが、すべての市町村が都道府県と関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="27465-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="27465-515">Talent</span><span class="sxs-lookup"><span data-stu-id="27465-515">Talent</span></span>          | <span data-ttu-id="27465-516">Dayforce</span><span class="sxs-lookup"><span data-stu-id="27465-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="27465-517">国/地域</span><span class="sxs-lookup"><span data-stu-id="27465-517">Country/Region</span></span>  | <span data-ttu-id="27465-518">国コード</span><span class="sxs-lookup"><span data-stu-id="27465-518">Country Code</span></span>          |
| <span data-ttu-id="27465-519">郵便番号</span><span class="sxs-lookup"><span data-stu-id="27465-519">Zip/Postal Code</span></span> | <span data-ttu-id="27465-520">郵便番号</span><span class="sxs-lookup"><span data-stu-id="27465-520">Postal Code</span></span>           |
| <span data-ttu-id="27465-521">行政単位 (区画)</span><span class="sxs-lookup"><span data-stu-id="27465-521">State</span></span>           | <span data-ttu-id="27465-522">都道府県コード</span><span class="sxs-lookup"><span data-stu-id="27465-522">State Code</span></span>            |
| <span data-ttu-id="27465-523">市町村</span><span class="sxs-lookup"><span data-stu-id="27465-523">City</span></span>            | <span data-ttu-id="27465-524">市町村</span><span class="sxs-lookup"><span data-stu-id="27465-524">City</span></span>                  |
| <span data-ttu-id="27465-525">郡</span><span class="sxs-lookup"><span data-stu-id="27465-525">County</span></span>          | <span data-ttu-id="27465-526">市区郡 (自治体)</span><span class="sxs-lookup"><span data-stu-id="27465-526">County (Municipality)</span></span> |
| <span data-ttu-id="27465-527">住所</span><span class="sxs-lookup"><span data-stu-id="27465-527">Street</span></span>          | <span data-ttu-id="27465-528">住所行 1</span><span class="sxs-lookup"><span data-stu-id="27465-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="27465-529">税地域</span><span class="sxs-lookup"><span data-stu-id="27465-529">Tax regions</span></span>

<span data-ttu-id="27465-530">税地域は、給与の生成時に適用する適切な税を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="27465-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="27465-531">税地域は、場所の住所として Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="27465-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="27465-532">既定の税地域は、作業者の有効な職位に関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="27465-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="27465-533">税地域 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-533">Tax region (required)</span></span>
- <span data-ttu-id="27465-534">国/地域 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-534">Country/Region (required)</span></span>
- <span data-ttu-id="27465-535">都道府県 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-535">State (required)</span></span>
- <span data-ttu-id="27465-536">郡</span><span class="sxs-lookup"><span data-stu-id="27465-536">County</span></span> 
- <span data-ttu-id="27465-537">市町村 (必須)</span><span class="sxs-lookup"><span data-stu-id="27465-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="27465-538">メキシコの給与を生成するためのデータ コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="27465-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="27465-539">メキシコの従業員のために支払を生成している場合、次の要素をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="27465-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="27465-540">職位に部門が必要です。</span><span class="sxs-lookup"><span data-stu-id="27465-540">Departments are required on positions.</span></span>
- <span data-ttu-id="27465-541">原価部門を財務分析コードとして設定し、既定の財務分析コード文字列の最初の要素とする必要があります。</span><span class="sxs-lookup"><span data-stu-id="27465-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="27465-542">ジョブ タイプ</span><span class="sxs-lookup"><span data-stu-id="27465-542">Job types</span></span>

<span data-ttu-id="27465-543">職務タイプは、類似した職務をカテゴリにグループ化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="27465-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="27465-544">職務タイプは、メキシコでの給与を処理するために必要です。</span><span class="sxs-lookup"><span data-stu-id="27465-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="27465-545">職務タイプの例には、フルタイムおよびパートタイム、または給与払いおよび時給払いが含まれます。</span><span class="sxs-lookup"><span data-stu-id="27465-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="27465-546">職務タイプは、従業員が時給払いかあるいは給与払いなのかを示す支払タイプとして Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="27465-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="27465-547">次の職務タイプと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="27465-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="27465-548">ジョブ タイプ</span><span class="sxs-lookup"><span data-stu-id="27465-548">Job type</span></span>   | <span data-ttu-id="27465-549">説明</span><span class="sxs-lookup"><span data-stu-id="27465-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="27465-550">時間</span><span class="sxs-lookup"><span data-stu-id="27465-550">Hourly</span></span>     | <span data-ttu-id="27465-551">MX 時給払い</span><span class="sxs-lookup"><span data-stu-id="27465-551">MX Hourly</span></span>   |
| <span data-ttu-id="27465-552">給与払い</span><span class="sxs-lookup"><span data-stu-id="27465-552">Salaried</span></span>   | <span data-ttu-id="27465-553">MX 給与払い</span><span class="sxs-lookup"><span data-stu-id="27465-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="27465-554">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="27465-554">Position types</span></span> 

<span data-ttu-id="27465-555">職位がフルタイム、パートタイム、またはその他のタイプかどうかを説明するために職位タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="27465-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="27465-556">職位タイプは、従業員がフルタイムかあるいはパートタイムなのかを示す支払クラスとして Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="27465-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="27465-557">次の職位タイプと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="27465-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="27465-558">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="27465-558">Position type</span></span>   | <span data-ttu-id="27465-559">説明</span><span class="sxs-lookup"><span data-stu-id="27465-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="27465-560">フルタイム</span><span class="sxs-lookup"><span data-stu-id="27465-560">Full-time</span></span>       | <span data-ttu-id="27465-561">フルタイム従業員</span><span class="sxs-lookup"><span data-stu-id="27465-561">Full time employee</span></span> |
| <span data-ttu-id="27465-562">パートタイム</span><span class="sxs-lookup"><span data-stu-id="27465-562">Part-time</span></span>       | <span data-ttu-id="27465-563">パートタイム従業員</span><span class="sxs-lookup"><span data-stu-id="27465-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="27465-564">理由コード</span><span class="sxs-lookup"><span data-stu-id="27465-564">Reason codes</span></span>

<span data-ttu-id="27465-565">理由コードは、従業員のステータスに関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="27465-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="27465-566">理由コードは、従業員の職位または雇用ステータスへの変更の理由を示すステータス理由として Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="27465-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="27465-567">次の理由コードと説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="27465-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="27465-568">理由コード</span><span class="sxs-lookup"><span data-stu-id="27465-568">Reason code</span></span>            | <span data-ttu-id="27465-569">説明</span><span class="sxs-lookup"><span data-stu-id="27465-569">Description</span></span>                    | <span data-ttu-id="27465-570">適用可能なシナリオ</span><span class="sxs-lookup"><span data-stu-id="27465-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="27465-571">支払前の除籍</span><span class="sxs-lookup"><span data-stu-id="27465-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="27465-572">最初の給与の前の除籍</span><span class="sxs-lookup"><span data-stu-id="27465-572">Departure before first payroll</span></span> | <span data-ttu-id="27465-573">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="27465-573">Terminate worker</span></span>     |
| <span data-ttu-id="27465-574">辞職</span><span class="sxs-lookup"><span data-stu-id="27465-574">RESIGNATION</span></span>            | <span data-ttu-id="27465-575">辞職</span><span class="sxs-lookup"><span data-stu-id="27465-575">Resignation</span></span>                    | <span data-ttu-id="27465-576">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="27465-576">Terminate worker</span></span>     |
| <span data-ttu-id="27465-577">年金</span><span class="sxs-lookup"><span data-stu-id="27465-577">PENSION</span></span>                | <span data-ttu-id="27465-578">年金</span><span class="sxs-lookup"><span data-stu-id="27465-578">Pension</span></span>                        | <span data-ttu-id="27465-579">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="27465-579">Terminate worker</span></span>     |
| <span data-ttu-id="27465-580">終了</span><span class="sxs-lookup"><span data-stu-id="27465-580">TERMINATION</span></span>            | <span data-ttu-id="27465-581">終了</span><span class="sxs-lookup"><span data-stu-id="27465-581">Termination</span></span>                    | <span data-ttu-id="27465-582">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="27465-582">Terminate worker</span></span>     |
| <span data-ttu-id="27465-583">定年退職</span><span class="sxs-lookup"><span data-stu-id="27465-583">RETIREMENT</span></span>             | <span data-ttu-id="27465-584">償却</span><span class="sxs-lookup"><span data-stu-id="27465-584">Retirement</span></span>                     | <span data-ttu-id="27465-585">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="27465-585">Terminate worker</span></span>     |
| <span data-ttu-id="27465-586">休暇者</span><span class="sxs-lookup"><span data-stu-id="27465-586">ABSENTEE</span></span>               | <span data-ttu-id="27465-587">休暇者</span><span class="sxs-lookup"><span data-stu-id="27465-587">Absentee</span></span>                       | <span data-ttu-id="27465-588">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="27465-588">Terminate worker</span></span>     |
| <span data-ttu-id="27465-589">その他</span><span class="sxs-lookup"><span data-stu-id="27465-589">OTHER</span></span>                  | <span data-ttu-id="27465-590">その他の理由</span><span class="sxs-lookup"><span data-stu-id="27465-590">Other Reasons</span></span>                  | <span data-ttu-id="27465-591">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="27465-591">Terminate worker</span></span>     |
| <span data-ttu-id="27465-592">休業</span><span class="sxs-lookup"><span data-stu-id="27465-592">CLOSURE</span></span>                | <span data-ttu-id="27465-593">業務休業</span><span class="sxs-lookup"><span data-stu-id="27465-593">Business Closure</span></span>               | <span data-ttu-id="27465-594">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="27465-594">Terminate worker</span></span>     |
| <span data-ttu-id="27465-595">死亡</span><span class="sxs-lookup"><span data-stu-id="27465-595">DEATH</span></span>                  | <span data-ttu-id="27465-596">死亡</span><span class="sxs-lookup"><span data-stu-id="27465-596">Death</span></span>                          | <span data-ttu-id="27465-597">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="27465-597">Terminate worker</span></span>     |
| <span data-ttu-id="27465-598">休暇</span><span class="sxs-lookup"><span data-stu-id="27465-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="27465-599">休暇</span><span class="sxs-lookup"><span data-stu-id="27465-599">Leave of Absence</span></span>               | <span data-ttu-id="27465-600">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="27465-600">Terminate worker</span></span>     |
| <span data-ttu-id="27465-601">契約の終了</span><span class="sxs-lookup"><span data-stu-id="27465-601">CONTRACTEND</span></span>            | <span data-ttu-id="27465-602">契約の終了</span><span class="sxs-lookup"><span data-stu-id="27465-602">End of Contract</span></span>                | <span data-ttu-id="27465-603">作業者の退職</span><span class="sxs-lookup"><span data-stu-id="27465-603">Terminate worker</span></span>     |
| <span data-ttu-id="27465-604">給与の変更</span><span class="sxs-lookup"><span data-stu-id="27465-604">SALARYCHANGE</span></span>           | <span data-ttu-id="27465-605">給与の変更</span><span class="sxs-lookup"><span data-stu-id="27465-605">Change of Salary</span></span>               | <span data-ttu-id="27465-606">報酬</span><span class="sxs-lookup"><span data-stu-id="27465-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="27465-607">雇用条件</span><span class="sxs-lookup"><span data-stu-id="27465-607">Terms of employment</span></span>

<span data-ttu-id="27465-608">雇用条件は、雇用条件のカテゴリを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="27465-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="27465-609">条件は、雇用インジケーターの値として Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="27465-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="27465-610">次の雇用条件および説明が必要です。</span><span class="sxs-lookup"><span data-stu-id="27465-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="27465-611">雇用条件</span><span class="sxs-lookup"><span data-stu-id="27465-611">Terms of employment</span></span>   | <span data-ttu-id="27465-612">説明</span><span class="sxs-lookup"><span data-stu-id="27465-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="27465-613">通常</span><span class="sxs-lookup"><span data-stu-id="27465-613">Regular</span></span>               | <span data-ttu-id="27465-614">通常</span><span class="sxs-lookup"><span data-stu-id="27465-614">Regular</span></span>     |
| <span data-ttu-id="27465-615">直接</span><span class="sxs-lookup"><span data-stu-id="27465-615">Direct</span></span>                | <span data-ttu-id="27465-616">直接</span><span class="sxs-lookup"><span data-stu-id="27465-616">Direct</span></span>      |
| <span data-ttu-id="27465-617">インターンシップ</span><span class="sxs-lookup"><span data-stu-id="27465-617">Internship</span></span>            | <span data-ttu-id="27465-618">インターンシップ</span><span class="sxs-lookup"><span data-stu-id="27465-618">Internship</span></span>  |
| <span data-ttu-id="27465-619">永続的</span><span class="sxs-lookup"><span data-stu-id="27465-619">Permanent</span></span>             | <span data-ttu-id="27465-620">永続的</span><span class="sxs-lookup"><span data-stu-id="27465-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="27465-621">配偶者の有無</span><span class="sxs-lookup"><span data-stu-id="27465-621">Marital status</span></span>

<span data-ttu-id="27465-622">配偶者有無の値は、Dayforce にマップされ、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="27465-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="27465-623">次の表に、配偶者有無の値がどのように Dayforce にマップされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="27465-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="27465-624">Talent</span><span class="sxs-lookup"><span data-stu-id="27465-624">Talent</span></span>                 | <span data-ttu-id="27465-625">Dayforce</span><span class="sxs-lookup"><span data-stu-id="27465-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="27465-626">既婚</span><span class="sxs-lookup"><span data-stu-id="27465-626">Married</span></span>                | <span data-ttu-id="27465-627">既婚</span><span class="sxs-lookup"><span data-stu-id="27465-627">Married</span></span>                   |
| <span data-ttu-id="27465-628">未婚</span><span class="sxs-lookup"><span data-stu-id="27465-628">Single</span></span>                 | <span data-ttu-id="27465-629">未婚</span><span class="sxs-lookup"><span data-stu-id="27465-629">Single</span></span>                    |
| <span data-ttu-id="27465-630">死別</span><span class="sxs-lookup"><span data-stu-id="27465-630">Widowed</span></span>                | <span data-ttu-id="27465-631">死別</span><span class="sxs-lookup"><span data-stu-id="27465-631">Widowed</span></span>                   |
| <span data-ttu-id="27465-632">離婚</span><span class="sxs-lookup"><span data-stu-id="27465-632">Divorced</span></span>               | <span data-ttu-id="27465-633">離婚</span><span class="sxs-lookup"><span data-stu-id="27465-633">Divorced</span></span>                  |
| <span data-ttu-id="27465-634">登録済パートナーシップ</span><span class="sxs-lookup"><span data-stu-id="27465-634">Registered Partnership</span></span> | <span data-ttu-id="27465-635">ドメスティック パートナーシップ</span><span class="sxs-lookup"><span data-stu-id="27465-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="27465-636">None</span><span class="sxs-lookup"><span data-stu-id="27465-636">None</span></span>                   | <span data-ttu-id="27465-637">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="27465-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="27465-638">同棲中</span><span class="sxs-lookup"><span data-stu-id="27465-638">Cohabiting</span></span>             | <span data-ttu-id="27465-639">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="27465-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="27465-640">種類</span><span class="sxs-lookup"><span data-stu-id="27465-640">Gender</span></span>

<span data-ttu-id="27465-641">性別の指定は、Dayforce にマップされ、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="27465-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="27465-642">次の表に、性別の指定がどのように Dayforce にマップされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="27465-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="27465-643">Talent</span><span class="sxs-lookup"><span data-stu-id="27465-643">Talent</span></span>       | <span data-ttu-id="27465-644">Dayforce</span><span class="sxs-lookup"><span data-stu-id="27465-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="27465-645">男性</span><span class="sxs-lookup"><span data-stu-id="27465-645">Male</span></span>         | <span data-ttu-id="27465-646">男性</span><span class="sxs-lookup"><span data-stu-id="27465-646">Male</span></span>                      |
| <span data-ttu-id="27465-647">女性</span><span class="sxs-lookup"><span data-stu-id="27465-647">Female</span></span>       | <span data-ttu-id="27465-648">女性</span><span class="sxs-lookup"><span data-stu-id="27465-648">Female</span></span>                    |
| <span data-ttu-id="27465-649">不特定</span><span class="sxs-lookup"><span data-stu-id="27465-649">Non-specific</span></span> | <span data-ttu-id="27465-650">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="27465-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="27465-651">支払方法</span><span class="sxs-lookup"><span data-stu-id="27465-651">Payment method</span></span>

<span data-ttu-id="27465-652">支払方法は、従業員に支払が行われる方法を従業員および会社に説明します。</span><span class="sxs-lookup"><span data-stu-id="27465-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="27465-653">支払方法は、Dayforce にマップされ、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="27465-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="27465-654">次の表に、支払方法がどのように Dayforce にマップされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="27465-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="27465-655">Talent</span><span class="sxs-lookup"><span data-stu-id="27465-655">Talent</span></span>             | <span data-ttu-id="27465-656">Dayforce</span><span class="sxs-lookup"><span data-stu-id="27465-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="27465-657">現金</span><span class="sxs-lookup"><span data-stu-id="27465-657">Cash</span></span>               | <span data-ttu-id="27465-658">現金</span><span class="sxs-lookup"><span data-stu-id="27465-658">Cash</span></span>                      |
| <span data-ttu-id="27465-659">電子支払</span><span class="sxs-lookup"><span data-stu-id="27465-659">Electronic Payment</span></span> | <span data-ttu-id="27465-660">転送</span><span class="sxs-lookup"><span data-stu-id="27465-660">Transfer</span></span>                  |
| <span data-ttu-id="27465-661">確認</span><span class="sxs-lookup"><span data-stu-id="27465-661">Check</span></span>              | <span data-ttu-id="27465-662">小切手</span><span class="sxs-lookup"><span data-stu-id="27465-662">Cheque</span></span>                    |
| <span data-ttu-id="27465-663">銀行為替手形</span><span class="sxs-lookup"><span data-stu-id="27465-663">Bank Draft</span></span>         | <span data-ttu-id="27465-664">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="27465-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="27465-665">外</span><span class="sxs-lookup"><span data-stu-id="27465-665">Other</span></span>              | <span data-ttu-id="27465-666">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="27465-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="27465-667">銀行口座の種類</span><span class="sxs-lookup"><span data-stu-id="27465-667">Bank account type</span></span>

<span data-ttu-id="27465-668">銀行口座の種類は、従業員への電子支払のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="27465-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="27465-669">銀行口座の種類は、振替口座情報として Dayforce にマップされます。</span><span class="sxs-lookup"><span data-stu-id="27465-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="27465-670">銀行口座の種類は、統合時に必要に応じて許容される値に翻訳されます。</span><span class="sxs-lookup"><span data-stu-id="27465-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="27465-671">Talent</span><span class="sxs-lookup"><span data-stu-id="27465-671">Talent</span></span>            | <span data-ttu-id="27465-672">Dayforce</span><span class="sxs-lookup"><span data-stu-id="27465-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="27465-673">当座預金口座</span><span class="sxs-lookup"><span data-stu-id="27465-673">Checking Account</span></span>  | <span data-ttu-id="27465-674">当座預金口座</span><span class="sxs-lookup"><span data-stu-id="27465-674">CheckingAccount</span></span>           |
| <span data-ttu-id="27465-675">給与口座</span><span class="sxs-lookup"><span data-stu-id="27465-675">Payroll Account</span></span>   | <span data-ttu-id="27465-676">給与口座</span><span class="sxs-lookup"><span data-stu-id="27465-676">PayrollAccount</span></span>            |
| <span data-ttu-id="27465-677">普通預金口座</span><span class="sxs-lookup"><span data-stu-id="27465-677">Savings Account</span></span>   | <span data-ttu-id="27465-678">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="27465-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="27465-679">BankGirot 口座</span><span class="sxs-lookup"><span data-stu-id="27465-679">BankGirot account</span></span> | <span data-ttu-id="27465-680">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="27465-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="27465-681">PlusGirot 口座</span><span class="sxs-lookup"><span data-stu-id="27465-681">PlusGirot account</span></span> | <span data-ttu-id="27465-682">*メキシコではサポートされていません*</span><span class="sxs-lookup"><span data-stu-id="27465-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="27465-683">所得コード</span><span class="sxs-lookup"><span data-stu-id="27465-683">Earning codes</span></span>

<span data-ttu-id="27465-684">所得コードは、作業者が受け取るすべての収益のタイプを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="27465-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="27465-685">コードには、会計ルール、税法、レポート要件、およびグロスアップ能力など、所得に関連付けられている複数のパラメーターが含まれます。</span><span class="sxs-lookup"><span data-stu-id="27465-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="27465-686">サポートされていない頻度を使用する場合、既定で**すべての支払**頻度が計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="27465-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="27465-687">サポートされる頻度</span><span class="sxs-lookup"><span data-stu-id="27465-687">Supported frequencies</span></span>

- <span data-ttu-id="27465-688">All</span><span class="sxs-lookup"><span data-stu-id="27465-688">All</span></span>
- <span data-ttu-id="27465-689">すべての支払</span><span class="sxs-lookup"><span data-stu-id="27465-689">EVERYPAY</span></span>
- <span data-ttu-id="27465-690">各支払期間</span><span class="sxs-lookup"><span data-stu-id="27465-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="27465-691">他のすべての奇数支払</span><span class="sxs-lookup"><span data-stu-id="27465-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="27465-692">他のすべての偶数支払</span><span class="sxs-lookup"><span data-stu-id="27465-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="27465-693">1 か月</span><span class="sxs-lookup"><span data-stu-id="27465-693">1OFMTH</span></span>
- <span data-ttu-id="27465-694">月の最終日</span><span class="sxs-lookup"><span data-stu-id="27465-694">LASTOFMTH</span></span>
- <span data-ttu-id="27465-695">2 か月</span><span class="sxs-lookup"><span data-stu-id="27465-695">2OFMTH</span></span>
- <span data-ttu-id="27465-696">3 か月</span><span class="sxs-lookup"><span data-stu-id="27465-696">3OFMTH</span></span>
- <span data-ttu-id="27465-697">4 か月</span><span class="sxs-lookup"><span data-stu-id="27465-697">4OFMTH</span></span>
- <span data-ttu-id="27465-698">5 か月</span><span class="sxs-lookup"><span data-stu-id="27465-698">5OFMTH</span></span>
- <span data-ttu-id="27465-699">1 か月および 2 か月</span><span class="sxs-lookup"><span data-stu-id="27465-699">1N2OFMTH</span></span>
- <span data-ttu-id="27465-700">3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="27465-700">3N4OFMTH</span></span>
- <span data-ttu-id="27465-701">1 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="27465-701">1N3OFMTH</span></span>
- <span data-ttu-id="27465-702">1 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="27465-702">1N4OFMTH</span></span>
- <span data-ttu-id="27465-703">2 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="27465-703">2N3OFMTH</span></span>
- <span data-ttu-id="27465-704">2 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="27465-704">2N4OFMTH</span></span>
- <span data-ttu-id="27465-705">1 か月、2 か月および 3 か月</span><span class="sxs-lookup"><span data-stu-id="27465-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="27465-706">1 か月、2 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="27465-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="27465-707">1 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="27465-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="27465-708">2 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="27465-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="27465-709">1 か月、2 か月、3 か月および 4 か月 - 1 か月、2 か月、3 か月および 4 か月</span><span class="sxs-lookup"><span data-stu-id="27465-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="27465-710">2 か月、3 か月、4 か月および 5 か月 - 2 か月、3 か月、4 か月および 5 か月</span><span class="sxs-lookup"><span data-stu-id="27465-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="27465-711">四半期の 1 - 四半期の 1</span><span class="sxs-lookup"><span data-stu-id="27465-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="27465-712">四半期の最終日 – 四半期の最終日</span><span class="sxs-lookup"><span data-stu-id="27465-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="27465-713">四半期の最後の月 – 四半期の最後の月</span><span class="sxs-lookup"><span data-stu-id="27465-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="27465-714">1 年 - 1 年</span><span class="sxs-lookup"><span data-stu-id="27465-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="27465-715">年の最終日 – 年の最終日</span><span class="sxs-lookup"><span data-stu-id="27465-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="27465-716">年の 11 月および 12 月 - 年の 11 月および 12 月</span><span class="sxs-lookup"><span data-stu-id="27465-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="27465-717">住所</span><span class="sxs-lookup"><span data-stu-id="27465-717">Addresses</span></span>

<span data-ttu-id="27465-718">特定の国または地域、都道府県、および市区郡 (自治体) の ID には、Dayforce および国内または地域内のプロバイダーが認識できる特定の形式が必要です。</span><span class="sxs-lookup"><span data-stu-id="27465-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="27465-719">市町村の形式は柔軟ですが、すべての市町村が都道府県と関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="27465-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="27465-720">Talent</span><span class="sxs-lookup"><span data-stu-id="27465-720">Talent</span></span>              | <span data-ttu-id="27465-721">Dayforce</span><span class="sxs-lookup"><span data-stu-id="27465-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="27465-722">国/地域</span><span class="sxs-lookup"><span data-stu-id="27465-722">Country/Region</span></span>      | <span data-ttu-id="27465-723">国コード</span><span class="sxs-lookup"><span data-stu-id="27465-723">Country Code</span></span>          |
| <span data-ttu-id="27465-724">郵便番号</span><span class="sxs-lookup"><span data-stu-id="27465-724">Zip/Postal Code</span></span>     | <span data-ttu-id="27465-725">郵便番号</span><span class="sxs-lookup"><span data-stu-id="27465-725">Postal Code</span></span>           |
| <span data-ttu-id="27465-726">行政単位 (区画)</span><span class="sxs-lookup"><span data-stu-id="27465-726">State</span></span>               | <span data-ttu-id="27465-727">都道府県コード</span><span class="sxs-lookup"><span data-stu-id="27465-727">State Code</span></span>            |
| <span data-ttu-id="27465-728">市町村</span><span class="sxs-lookup"><span data-stu-id="27465-728">City</span></span>                | <span data-ttu-id="27465-729">市町村</span><span class="sxs-lookup"><span data-stu-id="27465-729">City</span></span>                  |
| <span data-ttu-id="27465-730">郡</span><span class="sxs-lookup"><span data-stu-id="27465-730">County</span></span>              | <span data-ttu-id="27465-731">市区郡 (自治体)</span><span class="sxs-lookup"><span data-stu-id="27465-731">County (Municipality)</span></span> |
| <span data-ttu-id="27465-732">住所</span><span class="sxs-lookup"><span data-stu-id="27465-732">Street</span></span>              | <span data-ttu-id="27465-733">住所行 1</span><span class="sxs-lookup"><span data-stu-id="27465-733">Address Line 1</span></span>        |
| <span data-ttu-id="27465-734">番地</span><span class="sxs-lookup"><span data-stu-id="27465-734">Street Number</span></span>       | <span data-ttu-id="27465-735">住所行 2</span><span class="sxs-lookup"><span data-stu-id="27465-735">Address Line 2</span></span>        |
| <span data-ttu-id="27465-736">建物名</span><span class="sxs-lookup"><span data-stu-id="27465-736">Building Complement</span></span> | <span data-ttu-id="27465-737">住所行 5</span><span class="sxs-lookup"><span data-stu-id="27465-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="27465-738">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="27465-738">Passport number</span></span>

<span data-ttu-id="27465-739">従業員は、パスポート情報を申告できます。</span><span class="sxs-lookup"><span data-stu-id="27465-739">Employees can declare passport information.</span></span> <span data-ttu-id="27465-740">この情報は、**パスポート** ID タイプになり、従業員のメキシコ固有の情報の一部として Dayforce に統合されます。</span><span class="sxs-lookup"><span data-stu-id="27465-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="27465-741">ID タイプ = "Passport"</span><span class="sxs-lookup"><span data-stu-id="27465-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="27465-742">発行日付</span><span class="sxs-lookup"><span data-stu-id="27465-742">Issued Date</span></span>
- <span data-ttu-id="27465-743">有効期限</span><span class="sxs-lookup"><span data-stu-id="27465-743">Expiration Date</span></span>

<span data-ttu-id="27465-744">従業員は、**パスポート** ID タイプの複数の ID 番号を申告できます。</span><span class="sxs-lookup"><span data-stu-id="27465-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="27465-745">ただし、現在の有効なパスポート入力のみが Dayforce に統合されます。</span><span class="sxs-lookup"><span data-stu-id="27465-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="27465-746">すべてのパスポート入力が期限切れの場合、最後に発行されたパスポートが Dayforce に統合されます。</span><span class="sxs-lookup"><span data-stu-id="27465-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
