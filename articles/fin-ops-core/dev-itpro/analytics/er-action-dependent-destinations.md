---
title: アクション依存の ER 送信先を構成する
description: このトピックでは、送信ドキュメントを生成するように構成された電子申告 (ER) 形式に対して、アクション依存の送信先を構成する方法について説明します。
author: NickSelin
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 7decdb1d759284c616ecf928c10f99098627472d
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893581"
---
# <a name="configure-action-dependent-er-destinations"></a><span data-ttu-id="ff086-103">アクション依存の ER 送信先を構成する</span><span class="sxs-lookup"><span data-stu-id="ff086-103">Configure action-dependent ER destinations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff086-104">送信ドキュメントの生成に使用する [電子申告 (ER)](general-electronic-reporting.md) [形式](general-electronic-reporting.md#FormatComponentOutbound) の [構成](general-electronic-reporting.md#Configuration) の各出力コンポーネント (フォルダーまたはファイル) に対して、[送信先](electronic-reporting-destinations.md) を構成できます。</span><span class="sxs-lookup"><span data-stu-id="ff086-104">You can configure [destinations](electronic-reporting-destinations.md) for each output component (folder or file) of an [Electronic reporting (ER)](general-electronic-reporting.md) [format](general-electronic-reporting.md#FormatComponentOutbound) [configuration](general-electronic-reporting.md#Configuration) that is used to generate an outbound document.</span></span> <span data-ttu-id="ff086-105">このタイプの ER 形式を実行し、適切なアクセス権を持つユーザーは、実行時に構成した送信先設定を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="ff086-105">Users who run an ER format of this type, and who have appropriate access rights, can also change the configured destination settings at runtime.</span></span>

<span data-ttu-id="ff086-106">Microsoft Dynamics 365 Finance **バージョン 10.0.17以降** では、その ER 形式を実行することによりユーザーが実行するアクション コードを [プロビジョニング](er-apis-app10-0-17.md) することで、ER 形式を実行できます。</span><span class="sxs-lookup"><span data-stu-id="ff086-106">In Microsoft Dynamics 365 Finance **version 10.0.17 and later**, an ER format can be run by [provisioning](er-apis-app10-0-17.md) an action code that the user performs by running that ER format.</span></span> <span data-ttu-id="ff086-107">たとえば、**売掛金勘定モジュール** では、印刷管理の設定で、自由書式の請求書などの特定のビジネス ドキュメントを生成する ER 形式を選択できます。</span><span class="sxs-lookup"><span data-stu-id="ff086-107">For example, in the **Accounts receivable** module, in the Print management settings, you can select an ER format that generates a specific business document, such as a free text invoice.</span></span> <span data-ttu-id="ff086-108">**表示** を選択して請求書をプレビューするか、**印刷** を選択してプリンタに送信できます。</span><span class="sxs-lookup"><span data-stu-id="ff086-108">You can then select **View** to preview the invoice or **Print** to send it to a printer.</span></span> <span data-ttu-id="ff086-109">実行時に実行中の ER 形式に対してユーザー アクションが渡される場合、ユーザー アクションごとに異なる ER 送信先を構成できます。</span><span class="sxs-lookup"><span data-stu-id="ff086-109">If a user action is passed for the running ER format at runtime, you can configure different ER destinations for different user actions.</span></span> <span data-ttu-id="ff086-110">このトピックでは、このタイプの ER 形式に対して ER の送信先を構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ff086-110">This topic explains how to configure ER destinations for this type of ER format.</span></span>

## <a name="make-action-dependent-er-destinations-available"></a><span data-ttu-id="ff086-111">アクション依存の ER 送信先を使用可能にする</span><span class="sxs-lookup"><span data-stu-id="ff086-111">Make action-dependent ER destinations available</span></span>

<span data-ttu-id="ff086-112">現在の Finance インスタンスでアクション依存の ER 送信先を構成し、[新しい](er-apis-app10-0-17.md) ER API を有効にするには、[機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) ワークスペースを開き、**異なる PM アクションに対して使用する特定の ER 送信先を構成する** 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="ff086-112">To configure action-dependent ER destinations in the current Finance instance and enable the [new](er-apis-app10-0-17.md) ER API, open the [Feature management](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) workspace, and turn on the **Configure specific ER destinations to be used for different PM actions** feature.</span></span> <span data-ttu-id="ff086-113">実行時に [特定](#reports-list-wave1) のレポートに対して構成された ER 送信先を使用するには、機能 **ユーザー アクション固有の ER 送信先に基づく PM レポートのルート出力 (ウェーブ 1)** を有効にします。</span><span class="sxs-lookup"><span data-stu-id="ff086-113">To use configured ER destinations for [specific](#reports-list-wave1) reports at runtime, enable the feature, **Route output of PM reports based on ER destinations that are user action specific (wave 1)**.</span></span>

## <a name="configure-action-dependent-er-destinations"></a><span data-ttu-id="ff086-114">アクション依存の ER 送信先を構成する</span><span class="sxs-lookup"><span data-stu-id="ff086-114">Configure action-dependent ER destinations</span></span>

<span data-ttu-id="ff086-115">**異なる PM アクションに対して使用する特定の ER 送信先を構成する** 機能を有効にすると、**電子申告の送信先** ページの **ファイルの送信先** クイックタブで、アクション依存の ER 送信先を構成できます。</span><span class="sxs-lookup"><span data-stu-id="ff086-115">When you turn on the **Configure specific ER destinations to be used for different PM actions** feature, you can configure action-dependent ER destinations on the **File destination** FastTab of the **Electronic reporting destination** page.</span></span> <span data-ttu-id="ff086-116">各コンポーネントに対して、レコードを追加し、特定の ER 送信先を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="ff086-116">For each component, you can add a record and enable specific ER destinations.</span></span> <span data-ttu-id="ff086-117">各レコードに対して、ER 送信先を適用するドキュメント タイプを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff086-117">For each record, you must specify the type of document that the configured ER destinations should be applied for.</span></span> <span data-ttu-id="ff086-118">**ドキュメント タイプ** フィールドで、次のいずれかの値を選択します:</span><span class="sxs-lookup"><span data-stu-id="ff086-118">In the **Document type** field, select one of the following values:</span></span>

- <span data-ttu-id="ff086-119">実行時にユーザー アクション コードが指定されていない場合は、**電子** を選択して、構成した送信先を適用します。</span><span class="sxs-lookup"><span data-stu-id="ff086-119">Select **Electronic** to apply the configured destinations if no user action code is provided at runtime.</span></span>
- <span data-ttu-id="ff086-120">実行時にユーザー アクション コードが指定されていない場合は、**印刷管理** を選択して、構成した送信先を適用します。</span><span class="sxs-lookup"><span data-stu-id="ff086-120">Select **Print management** to apply the configured destinations if a user action code is provided at runtime.</span></span>
- <span data-ttu-id="ff086-121">**任意** を選択して、実行時にユーザー アクションが指定されているかどうかに関係なく、常に構成した送信先を適用します。</span><span class="sxs-lookup"><span data-stu-id="ff086-121">Select **Any** to always apply the configured destinations, regardless of whether a user action is provided at runtime.</span></span>

<span data-ttu-id="ff086-122">**印刷管理** ドキュメント タイプ を選択した場合は、構成した ER 送信先を適用するユーザー アクションを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff086-122">If you select the **Print management** document type, you must specify the user actions that the configured ER destinations should be applied for.</span></span> <span data-ttu-id="ff086-123">**印刷管理アクション** フィールドで、次のいずれかの値を選択します:</span><span class="sxs-lookup"><span data-stu-id="ff086-123">In the **Print management action** field, select one of the following values:</span></span>

- <span data-ttu-id="ff086-124">**表示** ユーザー アクションが実行時に指定されている場合は、**表示** を選択して、構成した送信先を適用します。</span><span class="sxs-lookup"><span data-stu-id="ff086-124">Select **View** to apply the configured destinations if the **View** user action is provided at runtime.</span></span>
- <span data-ttu-id="ff086-125">**印刷** ユーザー アクションが実行時に指定されている場合は、**印刷** を選択して、構成した送信先を適用します。</span><span class="sxs-lookup"><span data-stu-id="ff086-125">Select **Print** to apply the configured destinations if the **Print** user action is provided at runtime.</span></span>
- <span data-ttu-id="ff086-126">**送信** ユーザー アクションが実行時に指定されている場合は、**送信** を選択して、構成した送信先を適用します。</span><span class="sxs-lookup"><span data-stu-id="ff086-126">Select **Send** to apply the configured destinations if the **Send** user action is provided at runtime.</span></span>

> [!NOTE]
> <span data-ttu-id="ff086-127">1 つの送信先レコードに対して複数のアクションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="ff086-127">Multiple actions can be selected for a single destination record.</span></span>

<span data-ttu-id="ff086-128">**任意** のドキュメント タイプを選択した場合、**自動検出** が **印刷管理アクション** フィールドでユーザー アクションとして自動的に選択され、次の動作が発生します:</span><span class="sxs-lookup"><span data-stu-id="ff086-128">If you select the **Any** document type, **Autodetect** is automatically selected in the **Print management action** field as a user action, and the following behavior occurs:</span></span>

- <span data-ttu-id="ff086-129">実行時にユーザー アクション コードが指定されていない場合は、構成済みのすべての ER 送信先が適用されます。</span><span class="sxs-lookup"><span data-stu-id="ff086-129">If no user action code is provided at runtime, all configured ER destinations are applied.</span></span>
- <span data-ttu-id="ff086-130">実行時にユーザー アクション コードが指定された場合、特定のアクションに対してあらかじめ定義されている ER 送信先が、**有効になっているかどうかに関係なく** 適用されます:</span><span class="sxs-lookup"><span data-stu-id="ff086-130">If a user action code is provided at runtime, an ER destination that is predefined for a specific action is applied, **regardless of whether it has been enabled**:</span></span>

    - <span data-ttu-id="ff086-131">**表示** アクションを実行時に指定すると、**画面** ER 送信先が適用されます。</span><span class="sxs-lookup"><span data-stu-id="ff086-131">When the **View** action is provided at runtime, the **Screen** ER destination is applied.</span></span>
    - <span data-ttu-id="ff086-132">**送信** アクションを実行時に指定すると、**メール** ER 送信先が適用されます。</span><span class="sxs-lookup"><span data-stu-id="ff086-132">When the **Send** action is provided at runtime, the **Email** ER destination is applied.</span></span>
    - <span data-ttu-id="ff086-133">**印刷** アクションを実行時に指定すると、**プリンター** ER 送信先が適用されます。</span><span class="sxs-lookup"><span data-stu-id="ff086-133">When the **Print** action is provided at runtime, the **Printer** ER destination is applied.</span></span>

<span data-ttu-id="ff086-134">たとえば、**自由書式の請求書 (Excel)** ER 形式を使用して、転記時に [自由書式の請求書](../../../finance/accounts-receivable/create-free-text-invoice-new.md) を印刷できます。</span><span class="sxs-lookup"><span data-stu-id="ff086-134">For example, you can use the **Free text invoice (Excel)** ER format to print a [free text invoice](../../../finance/accounts-receivable/create-free-text-invoice-new.md) when you post it.</span></span> <span data-ttu-id="ff086-135">生成されたドキュメントを転送するには、この ER 形式用に ER 送信先を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff086-135">To route a generated document, you must configure ER destinations for this ER format.</span></span> <span data-ttu-id="ff086-136">たとえば、生成されたドキュメントで次の処理を実行するには、これらの ER 送信先を構成する必要があります:</span><span class="sxs-lookup"><span data-stu-id="ff086-136">For example, you may need to configure these ER destinations to perform the following on a generated document:</span></span>

- <span data-ttu-id="ff086-137">ER 形式が実行されているが、アクション コードが指定されていない場合 (例えば、ドキュメントが電子的に送信される場合など) は、ドキュメントをアーカイブします。</span><span class="sxs-lookup"><span data-stu-id="ff086-137">Archive the document if the ER format is run but no action code is provided (for example, when the document is sent electronically).</span></span>
- <span data-ttu-id="ff086-138">ユーザーが **表示** アクションを実行すると、Web ブラウザーでドキュメントをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="ff086-138">Preview the document in a web browser when a user performs the **View** action.</span></span>
- <span data-ttu-id="ff086-139">ユーザーが **印刷** アクションを実行すると、ドキュメントをアーカイブして印刷します。</span><span class="sxs-lookup"><span data-stu-id="ff086-139">Archive and print the document when a user performs the **Print** action.</span></span>
- <span data-ttu-id="ff086-140">ユーザーが **送信** アクションを実行すると、ドキュメントをアーカイブし、電子メールで送信電子メール メッセージの添付ファイルとして送信します。</span><span class="sxs-lookup"><span data-stu-id="ff086-140">Archive the document and email it as the attachment of an outbound email message when a user performs the **Send** action.</span></span>

<span data-ttu-id="ff086-141">次の図は、各レコードが個別のユーザー アクションに構成されている場合に、この ER 送信先を個別の送信先レコードのセットとして構成を行う方法を示しています:</span><span class="sxs-lookup"><span data-stu-id="ff086-141">The following illustration shows how you can achieve this configuring ER destinations as the set of individual destination records when every record is configured for an individual user action:</span></span>

![1 つのユーザー アクションに対してすべての送信先レコードが構成されている場合に、ER 形式のアクション依存の送信先設定を持つ電子申告の送信先ページ](./media/er-destination-action-dependent-01.png)

<span data-ttu-id="ff086-143">次の図は、各レコードが個別の送信先に構成されている場合に、ER 送信先を個別の送信先レコードのセットとして代わりに同じ構成を行う方法を示しています:</span><span class="sxs-lookup"><span data-stu-id="ff086-143">The following illustration shows how you can achieve the same alternatively configuring ER destinations as the set of individual destination records when every record is configured for an individual destination:</span></span>

![1 つの送信先に対してすべての送信先レコードが構成されている場合に、ER 形式のアクション依存の送信先設定を持つ電子申告の送信先ページ](./media/er-destination-action-dependent-01a.png)

> [!NOTE]
> <span data-ttu-id="ff086-145">実行している ER 形式のアクション コードが指定されている一方で、そのアクション コードに送信先が構成されていない場合は、[既定](electronic-reporting-destinations.md#default-behavior) の送信先の動作が適用されます。</span><span class="sxs-lookup"><span data-stu-id="ff086-145">If an action code is provided for the running ER format, but no destinations have been configured for that action code, the [default](electronic-reporting-destinations.md#default-behavior) destination behavior is applied.</span></span>

## <a name="change-action-dependent-er-destinations-at-runtime"></a><span data-ttu-id="ff086-146">アクション依存の ER 送信先を実行時に変更する</span><span class="sxs-lookup"><span data-stu-id="ff086-146">Change action-dependent ER destinations at runtime</span></span>

<span data-ttu-id="ff086-147">ER 形式を実行するときに、構成済の送信先設定を実行時に変更するための適切な [アクセス許可](electronic-reporting-destinations.md#security-considerations) を持つユーザが、ユーザー アクションをプロビジョニングした場合は、構成した送信先設定を変更するためのオプションを示すダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ff086-147">When an ER format is run, if user actions have been provisioned by users who have the appropriate [permissions](electronic-reporting-destinations.md#security-considerations) to change configured destination settings at runtime, a dialog box appears that gives the option to change the configured destination settings.</span></span> <span data-ttu-id="ff086-148">このダイアログ ボックスはオプションであり、その外観は、ER フレームワークが ER 形式を実行するために呼び出しがどのように実装されたかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="ff086-148">This dialog box is optional, and its appearance depends on how the call that the ER framework makes to run an ER format has been implemented.</span></span> <span data-ttu-id="ff086-149">このダイアログ ボックスが表示される場合、指定したユーザー アクションに従って、ボックス内の ER 送信先が有効になります。</span><span class="sxs-lookup"><span data-stu-id="ff086-149">If this dialog box appears, the ER destinations in it will be enabled according to the user action that is provided.</span></span>

<span data-ttu-id="ff086-150">次の図では、このトピックで前述したように、**プリンター** アクションがプロビジョニングされ、ER 送信先がこの形式に対して構成されている場合に、自由書式の請求書が [転記](../../../finance/accounts-receivable/create-free-text-invoice-new.md) され、**自由書式の請求書 (Excel)** ER 形式が実行されて、このドキュメントが生成されるときに表示される **電子申告形式の送信先** ダイアログ ボックスの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="ff086-150">The following illustration shows an example of the **Electronic reporting format destinations** dialog box that appears when a free text invoice is [posted](../../../finance/accounts-receivable/create-free-text-invoice-new.md) and the **Free text invoice (Excel)** ER format is run to generate this document, if the **Printer** action was provisioned and ER destinations were configured for this format as shown earlier in this topic.</span></span>

![実行中の ER 形式に対して初期構成された ER 送信先を変更するオプションを表示するダイアログ ボックス](./media/er-destination-action-dependent-02.gif)

> [!NOTE]
> <span data-ttu-id="ff086-152">実行中の ER 形式の複数のコンポーネントに ER 送信先を構成した場合、ER 形式の構成済コンポーネントごとにオプションが個別に提供されます。</span><span class="sxs-lookup"><span data-stu-id="ff086-152">If you configured ER destinations for several components of the running ER format, an option will be offered separately for every configured component of the ER format.</span></span>

## <a name="verify-the-provided-user-action"></a><span data-ttu-id="ff086-153">指定されたユーザー アクションの検証</span><span class="sxs-lookup"><span data-stu-id="ff086-153">Verify the provided user action</span></span>

<span data-ttu-id="ff086-154">特定のユーザー アクションを実行するときに、実行中の ER 形式に提供されるユーザー アクション (該当する場合) を検証できます。</span><span class="sxs-lookup"><span data-stu-id="ff086-154">You can verify what user action, if any, is provided for the running ER format when you perform a specific user action.</span></span> <span data-ttu-id="ff086-155">この検証は、アクション依存の ER 送信先を構成する必要があるが、どのユーザー アクション コードが提供されているかが不明な場合に重要です。</span><span class="sxs-lookup"><span data-stu-id="ff086-155">This verification is important when you must configure action-dependent ER destinations, but you aren't sure which user action code, if any, is provided.</span></span> <span data-ttu-id="ff086-156">たとえば、自由形式の請求書の転記を開始し、**自由形式請求書の転記** ダイアログ ボックスで **請求書の印刷** オプションを **はい** に設定した場合、**印刷管理先の使用** オプションを **はい** または **いいえ** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="ff086-156">For example, when you start to post a free text invoice and set the **Print invoice** option to **Yes** in the **Post free text invoice** dialog box, you can set the **Use print management destination** option to **Yes** or **No**.</span></span>

<span data-ttu-id="ff086-157">次の手順に従って、指定されたユーザー アクション コードを検証します。</span><span class="sxs-lookup"><span data-stu-id="ff086-157">Follow these steps to verify the user action code that is provided.</span></span>

1. <span data-ttu-id="ff086-158">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ff086-158">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ff086-159">**構成** ページ、アクション ウィンドウ、**構成** タブ、**詳細設定** グループで、**ユーザー パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff086-159">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="ff086-160">**ユーザー パラメーター** ダイアログ ボックスで、[デバッグ モードの実行](er-trace-reports-compare-baseline.md#configure-er-parameters-to-use-the-baseline-feature) オプションを **はい** に **設定** します。</span><span class="sxs-lookup"><span data-stu-id="ff086-160">In the **User parameters** dialog box, [set](er-trace-reports-compare-baseline.md#configure-er-parameters-to-use-the-baseline-feature) the **Run in debug mode** option to **Yes**.</span></span>
4. <span data-ttu-id="ff086-161">ER 形式を実行してユーザー アクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="ff086-161">Perform a user action by running an ER format.</span></span> <span data-ttu-id="ff086-162">ER ユーザー パラメーターは、会社固有およびユーザ固有であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ff086-162">Remember that ER user parameters are company-specific and user-specific.</span></span>
5. <span data-ttu-id="ff086-163">**組織管理** \> **電子申告** \> **構成デバッグ ログ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ff086-163">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>
6. <span data-ttu-id="ff086-164">**構成デバッグ ログ** ページで、ER の実行ログをフィルター処理して、ER 形式の実行のログを検索します。</span><span class="sxs-lookup"><span data-stu-id="ff086-164">On the **Configuration debug logs** page, filter the ER run logs to find the log for your ER format run.</span></span>
7. <span data-ttu-id="ff086-165">ER 形式の実行にアクションが指定されている場合は、指定されたユーザー アクション コードを示すレコードを含む必要があるログのエントリを確認します。</span><span class="sxs-lookup"><span data-stu-id="ff086-165">Review the log entries that must contain the record that presents the provided user action code, if any action has been provided for the ER format run.</span></span>

    ![ER 形式のフィルター処理された実行に対して指定されたユーザー アクション コードに関する情報を含む電子申告実行ログ ページ](./media/er-destination-action-dependent-03.png)

## <a name=""></a><span data-ttu-id="ff086-167"><a name="reports-list-wave1">ビジネス ドキュメントの一覧 (ウェーブ 1)</a></span><span class="sxs-lookup"><span data-stu-id="ff086-167"><a name="reports-list-wave1">List of business documents (wave 1)</a></span></span>

<span data-ttu-id="ff086-168">以下のビジネス ドキュメントの一覧は、**ユーザー アクション固有の ER 送信先に基づく PM レポートのルート出力 (ウェーブ 1)** 機能によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="ff086-168">The following list of business documents are controlled by the feature, **Route output of PM reports based on ER destinations that are user action specific (wave 1)**:</span></span>

- <span data-ttu-id="ff086-169">顧客請求書 (自由書式の請求書)</span><span class="sxs-lookup"><span data-stu-id="ff086-169">Customer invoice (Free text invoice)</span></span>
- <span data-ttu-id="ff086-170">顧客請求書 (売上請求書)</span><span class="sxs-lookup"><span data-stu-id="ff086-170">Customer invoice (Sales invoice)</span></span>
- <span data-ttu-id="ff086-171">発注書</span><span class="sxs-lookup"><span data-stu-id="ff086-171">Purchase order</span></span>
- <span data-ttu-id="ff086-172">発注書の購買照会</span><span class="sxs-lookup"><span data-stu-id="ff086-172">Purchase order purchase inquiry</span></span>
- <span data-ttu-id="ff086-173">販売注文確認</span><span class="sxs-lookup"><span data-stu-id="ff086-173">Sales order confirmation</span></span>
- <span data-ttu-id="ff086-174">督促状</span><span class="sxs-lookup"><span data-stu-id="ff086-174">Collections letter note</span></span>
- <span data-ttu-id="ff086-175">顧客勘定明細書</span><span class="sxs-lookup"><span data-stu-id="ff086-175">Customer account statement</span></span>
- <span data-ttu-id="ff086-176">利子計算書</span><span class="sxs-lookup"><span data-stu-id="ff086-176">Interest note</span></span>
- <span data-ttu-id="ff086-177">仕入先支払通知</span><span class="sxs-lookup"><span data-stu-id="ff086-177">Vendor payment advice</span></span>
- <span data-ttu-id="ff086-178">見積依頼</span><span class="sxs-lookup"><span data-stu-id="ff086-178">Request for quotation</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff086-179">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ff086-179">Additional resources</span></span>

[<span data-ttu-id="ff086-180">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="ff086-180">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="ff086-181">電子申告 (ER) の送信先</span><span class="sxs-lookup"><span data-stu-id="ff086-181">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)

[<span data-ttu-id="ff086-182">Application update 10.0.17 での電子申告フレームワーク API の変更</span><span class="sxs-lookup"><span data-stu-id="ff086-182">Electronic reporting framework API changes for Application update 10.0.17</span></span>](er-apis-app10-0-17.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]