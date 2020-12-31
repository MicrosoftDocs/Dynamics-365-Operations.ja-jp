---
title: 電子申告 (ER) 拡張形式の検索
description: このトピックでは、必要な形式がグローバル リポジトリに格納されている場合に、ER 形式参照を ER 形式検索で設定する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f7c6cb99a6c5cc6fb92ce52041296af2d0c6722e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679489"
---
# <a name="allow-users-to-set-up-an-er-format-reference-inquiring-a-format-from-the-global-repository"></a><span data-ttu-id="8e2c5-103">ユーザーがグローバル リポジトリから形式を照会する ER 形式の参照を設定できるようにする</span><span class="sxs-lookup"><span data-stu-id="8e2c5-103">Allow users to set up an ER format reference inquiring a format from the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e2c5-104">[電子申告](general-electronic-reporting.md) (ER) フレームワークを使用して、さまざまな国/地域の法的要件に従って送信ドキュメントの [形式](general-electronic-reporting.md#FormatComponentOutbound) をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-104">You can use the [Electronic reporting](general-electronic-reporting.md) (ER) framework to configure [formats](general-electronic-reporting.md#FormatComponentOutbound) for outbound documents in accordance to the legal requirements of various countries/regions.</span></span> <span data-ttu-id="8e2c5-105">ER フレームワークを使用して、受信ドキュメントを解析するための [形式](general-electronic-reporting.md#FormatComponentInbound) をコンフィギュレーションすることができ、またそれらのドキュメントの情報を使用してアプリケーション データの追加または更新を行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-105">You can also use the ER framework to configure [formats](general-electronic-reporting.md#FormatComponentInbound) for parsing inbound documents and use the information from those documents to append or update application data.</span></span> <span data-ttu-id="8e2c5-106">これらの各形式は、特定のビジネス プロセスの一部として受信または送信ビジネス ドキュメントを処理するために、Dynamics 365 Finance インスタンス内で使用できます。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-106">Each of these formats can be used in your Dynamics 365 Finance instance for handling inbound or outbound business documents as part of a certain business process.</span></span>

<span data-ttu-id="8e2c5-107">通常、特定のビジネス プロセスで使用する必要がある ER 形式を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-107">Usually, you must specify what ER format must be used in a certain business process.</span></span> <span data-ttu-id="8e2c5-108">この操作を行うには、ビジネス プロセス固有のパラメーターの一部としてコンフィギュレーションされているルックアップ フィールドで 1 つの ER 形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-108">To do that, select a single ER format in a lookup field that is configured as part of business process-specific parameters.</span></span> <span data-ttu-id="8e2c5-109">通常、これらのルックアップ フィールドは ER フレームワークの適切な API を使用することにより実装されます。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-109">These lookup fields are usually implemented by using the appropriate API of the ER framework.</span></span> <span data-ttu-id="8e2c5-110">詳細については、[ER フレームワーク API - 形式マッピングのルックアップを表示するコード](er-apis-app73.md#code-to-display-a-format-mapping-lookup) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-110">For more information, see [ER framework API - code to display a format mapping lookup](er-apis-app73.md#code-to-display-a-format-mapping-lookup).</span></span>

<span data-ttu-id="8e2c5-111">たとえば、[対外貿易パラメーター](https://docs.microsoft.com/dynamics365/finance/localizations/emea-intrastat#set-up-foreign-trade-parameters) をコンフィギュレーションする場合、イントラスタット申告およびイントラスタット申告理レポートの生成に使用される個別の ER 形式への参照を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-111">For example, when you configure [foreign trade parameters](https://docs.microsoft.com/dynamics365/finance/localizations/emea-intrastat#set-up-foreign-trade-parameters), you need to set up the references to individual ER formats that will be used to generate the Intrastat declaration and the Intrastat declaration control report.</span></span> <span data-ttu-id="8e2c5-112">下のスクリーンショットは、**対外貿易パラメーター** のページの ER 形式のルックアップ フィールドの外観を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-112">The screenshots below show how the ER formats lookup field looks like in the **Foreign trade parameters** page.</span></span>

<span data-ttu-id="8e2c5-113">現在の Finance インスタンスにイントラスタット業務プロセスに関連する ER 形式が含まれていない場合、このルックアップ フィールドは空になります。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-113">If the current Finance instance contains no Intrastat business process-related ER formats, this lookup field will be empty.</span></span>

<span data-ttu-id="8e2c5-114">[![対外貿易パラメーターのページ](./media/ER-ExtLookup-Lookup1.gif)](./media/ER-ExtLookup-Lookup1.gif)</span><span class="sxs-lookup"><span data-stu-id="8e2c5-114">[![Foreign trade parameters page](./media/ER-ExtLookup-Lookup1.gif)](./media/ER-ExtLookup-Lookup1.gif)</span></span>

<span data-ttu-id="8e2c5-115">現在の Finance インスタンスにイントラスタット業務プロセスに関連する ER 形式が含まれている場合、このルックアップ フィールドでは ER 形式が提供されます。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-115">If the current Finance instance contains Intrastat business process related ER formats, this lookup field offers the ER formats.</span></span>

<span data-ttu-id="8e2c5-116">[![対外貿易パラメーターのページ](./media/ER-ExtLookup-Lookup2.png)](./media/ER-ExtLookup-Lookup2.png)</span><span class="sxs-lookup"><span data-stu-id="8e2c5-116">[![Foreign trade parameters page](./media/ER-ExtLookup-Lookup2.png)](./media/ER-ExtLookup-Lookup2.png)</span></span>

<span data-ttu-id="8e2c5-117">このルックアップでは、現在の Finance インスタンスに既にインポートされている ER 形式のみが提供されます。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-117">This lookup offers only the ER formats that have already been imported to the current Finance instance.</span></span> <span data-ttu-id="8e2c5-118">ER ソリューションを現在の Finance インスタンスに [インポート](./tasks/er-import-configuration-lifecycle-services.md) するには、ER 形式を含む ER ソリューションの [ライフサイクル](general-electronic-reporting-manage-configuration-lifecycle.md) をサポートする ER フレームワークの適切な機能を実行するためのアクセス許可を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-118">To [import](./tasks/er-import-configuration-lifecycle-services.md) ER solutions to the current Finance instance, you need to have permissions to run the appropriate function of the ER framework that supports the [lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md) of ER solutions that contain ER formats.</span></span>

<span data-ttu-id="8e2c5-119">Finance 10.0.9 (2020 年 4 月リリース) 以降では、ER フレームワーク API を使用して実装される ER 形式検索のユーザー インターフェイスが拡張されました。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-119">Starting in the Finance version 10.0.9 (April 2020 release), the user interface of the ER format lookup that is implemented by using the ER framework API, has been extended.</span></span> <span data-ttu-id="8e2c5-120">**形式のコンフィギュレーションの選択** クイックタブで既存の ER 形式を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-120">You can still select the existing ER formats, which on the **Select format configuration** FastTab.</span></span> <span data-ttu-id="8e2c5-121">さらに、拡張検索は、グローバル レポジトリ (GR) を検索して特定の ER 形式を見つけるための新しいオプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-121">In addition, the extended lookup offers the new option to search the Global repository (GR) to locate specific ER formats.</span></span> <span data-ttu-id="8e2c5-122">GR のすべての ER 形式は、**グローバル リポジトリからのインポート** クイックタブで提供されます。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-122">All ER formats of the GR are offered on the **Import from Global repository** FastTab.</span></span>

<span data-ttu-id="8e2c5-123">[![対外貿易パラメーターのページ](./media/ER-ExtLookup-Lookup3.png)](./media/ER-ExtLookup-Lookup3.png)</span><span class="sxs-lookup"><span data-stu-id="8e2c5-123">[![Foreign trade parameters page](./media/ER-ExtLookup-Lookup3.png)](./media/ER-ExtLookup-Lookup3.png)</span></span>

<span data-ttu-id="8e2c5-124">**形式のコンフィギュレーションの選択** クイックタブと同様に、**グローバル リポジトリからのインポート** クイックタブには、このルックアップ フィールドで ER 形式が選択されている業務プロセスに適用される ER 形式のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-124">Similar to the **Select format configuration** FastTab, the **Import from Global repository** FastTab shows only the ER formats that are applicable to the business process for which an ER format is selected in this lookup field.</span></span> <span data-ttu-id="8e2c5-125">この例では、イントラスタット申告の生成です。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-125">In this example, the generation of Intrastat declaration.</span></span> <span data-ttu-id="8e2c5-126">ER 形式は、会社の国コンテキストに応じて、ユーザーが現在ログインしている会社に対して適用されます。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-126">The ER format is applicable for the company to which the user is currently signed in, depending on the company country context.</span></span>

<span data-ttu-id="8e2c5-127">**グローバル リポジトリからのインポート** クイックタブで ER 形式を選択した場合、選択した ER 形式 [コンフィギュレーション](general-electronic-reporting.md#Configuration) は GR から現在の Finance インスタンスにインポートされます。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-127">When you select an ER format on the **Import from Global repository** FastTab, the selected ER format [configuration](general-electronic-reporting.md#Configuration) is imported from the GR to the current Finance instance.</span></span>

<span data-ttu-id="8e2c5-128">[![対外貿易パラメーターのページ](./media/ER-ExtLookup-FormatImport.png)](./media/ER-ExtLookup-FormatImport.png)</span><span class="sxs-lookup"><span data-stu-id="8e2c5-128">[![Foreign trade parameters page](./media/ER-ExtLookup-FormatImport.png)](./media/ER-ExtLookup-FormatImport.png)</span></span>

<span data-ttu-id="8e2c5-129">インポートが正常に完了すると、インポートされた ER 形式への参照が、このルックアップ フィールドに格納されます。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-129">Then, if the import completes successfully, the reference to the imported ER format is stored in this lookup field.</span></span> <span data-ttu-id="8e2c5-130">初めて GR にアクセスする場合、提供されたリンクに従って、GR ストレージへのアクセスを管理するために使用される [Regulatory Configuration Service](https://aka.ms/rcs) (RCS) にサインアップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-130">When you access the GR for the first time, you need to follow the link provided to sign up for the [Regulatory Configuration Service](https://aka.ms/rcs) (RCS) that is used to manage access to the GR storage.</span></span>

<span data-ttu-id="8e2c5-131">[![対外貿易パラメーターのページ](./media/ER-ExtLookup-RepoSignUp.png)](./media/ER-ExtLookup-RepoSignUp.png)</span><span class="sxs-lookup"><span data-stu-id="8e2c5-131">[![Foreign trade parameters page](./media/ER-ExtLookup-RepoSignUp.png)](./media/ER-ExtLookup-RepoSignUp.png)</span></span>

<span data-ttu-id="8e2c5-132">既定では、**グローバル リポジトリからのインポート** クイックタブには、パフォーマンス向上のために GR コンテンツに基づいて自動的に作成される一時的な記憶域から ER 形式のリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-132">By default, the **Import from Global repository** FastTab presents the list of ER formats from the temporary storage that is automatically created based on the GR content for performance improvements.</span></span> <span data-ttu-id="8e2c5-133">これは、**グローバル リポジトリからのインポート** クイックタブを初めて開いた時に発生し、数秒かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-133">This happens when the **Import from Global repository** FastTab is opened the first time, which may take several seconds.</span></span>

<span data-ttu-id="8e2c5-134">**グローバル リポジトリからのインポート** クイックタブで必要な ER 形式が表示されないが、この ER 形式が GR に保存されていることが確実な場合、**同期** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-134">If you do not see the required ER format in the **Import from Global repository** FastTab, but you are sure that this ER format is stored in the GR, select the **Synchronize** option.</span></span> <span data-ttu-id="8e2c5-135">このオプションは、一時的な記憶域を更新し、GR の現在のコンテンツと同期します。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-135">This option will update the temporary storage and synchronize it with the current content of the GR.</span></span>

## <a name="feature-activation"></a><span data-ttu-id="8e2c5-136">機能の有効化</span><span class="sxs-lookup"><span data-stu-id="8e2c5-136">Feature activation</span></span>

<span data-ttu-id="8e2c5-137">この機能の可用性は、できるかどうかは、**機能の管理** の **グローバル リポジトリを照会できるようにする ER 形式コンフィギュレーションの拡張ルックアップ** 機能によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-137">The availability of this functionality is controlled by the feature **Extended lookup of ER format configurations allowing to inquire the Global repository** in the **Feature management**.</span></span> <span data-ttu-id="8e2c5-138">この機能は、既定で有効になっています。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-138">This feature is enabled by default.</span></span>

<span data-ttu-id="8e2c5-139">[![機能管理のページ](./media/ER-ExtLookup-FeatureMngt.png)](./media/ER-ExtLookup-FeatureMngt.png)</span><span class="sxs-lookup"><span data-stu-id="8e2c5-139">[![Feature management page](./media/ER-ExtLookup-FeatureMngt.png)](./media/ER-ExtLookup-FeatureMngt.png)</span></span>

## <a name="security-considerations"></a><span data-ttu-id="8e2c5-140">セキュリティ上の注意事項</span><span class="sxs-lookup"><span data-stu-id="8e2c5-140">Security considerations</span></span>

<span data-ttu-id="8e2c5-141">**コンフィギュレーション リポジトリのメンテナンス** (**ERMaintainSolutionRepositories**) 権限により、有効化された **グローバル リポジトリからのインポート** クイックタブで、ER 形式検索を開いているユーザーの GR へのアクセス許可が制御されます。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-141">The **Maintain configuration repositories** (**ERMaintainSolutionRepositories**) privilege controls access to the GR for a user opening the ER format lookup with the enabled **Import from Global repository** FastTab.</span></span> <span data-ttu-id="8e2c5-142">ユーザーが ER 形式検索から GR コンテンツにアクセスできるようにするには、**ERMaintainSolutionRepositories** 権限をユーザーに与えることにより、またはすでに割り当てられているロールと職務を使用することによりセキュリティ設定を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-142">To allow users to access the GR content from the ER format lookups, you need to change the security settings by granting the **ERMaintainSolutionRepositories** privilege to users either directly or by using already assigned roles and duties.</span></span>

<span data-ttu-id="8e2c5-143">次のスクリーンショットは、**経理担当** ロールに割り当てられているユーザーにこの権限を与える方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-143">The following screenshot shows how this privilege can be granted to users who are assigned to the **Accountant** role.</span></span> <span data-ttu-id="8e2c5-144">このロールにより、ユーザーは対外貿易パラメーターをコンフィギュレーションして、**対外貿易パラメーター** ページの **ファイル形式マッピング** および **レポート形式マッピング** フィールドで ER 形式への参照を設定できます。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-144">This role allows users to configure foreign trade parameters and set up references to the ER formats in the **File format mapping** and **Report format mapping** fields on the **Foreign trade parameters** page.</span></span>

<span data-ttu-id="8e2c5-145">[![セキュリティのコンフィギュレーションのページ](./media/ER-ExtLookup-SecuritySetting.png)](./media/ER-ExtLookup-SecuritySetting.png)</span><span class="sxs-lookup"><span data-stu-id="8e2c5-145">[![Security configuration page](./media/ER-ExtLookup-SecuritySetting.png)](./media/ER-ExtLookup-SecuritySetting.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="8e2c5-146">制限</span><span class="sxs-lookup"><span data-stu-id="8e2c5-146">Limitations</span></span>

<span data-ttu-id="8e2c5-147">ER 形式検索の GR へのアクセスは、現在、送信ドキュメントの生成に使用される ER 形式の選択にのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-147">Access to the GR in the ER format lookup is currently only supported for the selection of ER formats that are used to generate outbound documents.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="8e2c5-148">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="8e2c5-148">Frequently asked questions</span></span>

### <a name="why-cant-i-access-the-global-repository-from-the-er-format-lookup"></a><span data-ttu-id="8e2c5-149">ER 形式検索からグローバル リポジトリにアクセスできないのはなぜですか?</span><span class="sxs-lookup"><span data-stu-id="8e2c5-149">Why can't I access the Global repository from the ER format lookup?</span></span>

<span data-ttu-id="8e2c5-150">**機能管理** ページで **グローバル リポジトリを照会できるようにする ER 形式コンフィギュレーションの拡張ルックアップ** を有効にしているが、**グローバル リポジトリからのインポート** クイックタブで ER 形式が表示されず、**同期** オプションが表示されていても無効化されている場合、**コンフィギュレーション リポジトリのメンテナンス** (**ERMaintainSolutionRepositories**) 権限がユーザーに与えられているか確認してください。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-150">If you have enabled the **Extended lookup of ER format configurations allowing to inquire the Global repository** feature on the **Feature management** page, but users can't see ER formats on the **Import from Global repository** FastTab and the **Synchronize** option is visible but disabled, make sure that the **Maintain configuration repositories** (**ERMaintainSolutionRepositories**) privilege has been granted to the user.</span></span> <span data-ttu-id="8e2c5-151">システム管理者に問い合わせて、権限を受けてください。</span><span class="sxs-lookup"><span data-stu-id="8e2c5-151">Contact your system administrator to receive this privilege.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e2c5-152">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8e2c5-152">Additional resources</span></span>

- [<span data-ttu-id="8e2c5-153">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="8e2c5-153">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="8e2c5-154">電子申告 (ER) のフレームワーク API</span><span class="sxs-lookup"><span data-stu-id="8e2c5-154">Electronic reporting (ER) framework API</span></span>](er-apis-app73.md)
- [<span data-ttu-id="8e2c5-155">電子申告 (ER) コンフィギュレーション ライフサイクルの管理</span><span class="sxs-lookup"><span data-stu-id="8e2c5-155">Manage Electronic reporting (ER) configurations lifecycle</span></span>](general-electronic-reporting-manage-configuration-lifecycle.md)
