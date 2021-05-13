---
title: タイプ登録
description: このトピックでは、プロセス自動化フレームワークでタイプを登録する方法について説明します。
author: RyanCCarlson2
ms.date: 09/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-09-10
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09798a76253f4cdb38e3b0f733d2bfa3e5dba1b3
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866116"
---
# <a name="type-registration"></a><span data-ttu-id="d083e-103">タイプ登録</span><span class="sxs-lookup"><span data-stu-id="d083e-103">Type registration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d083e-104">プロセス自動化フレームワークを使用してプロセスを実装するには、まずフレームワークの *タイプ* の概念を理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d083e-104">To implement a process by using the process automation framework, you must first understand the concept of a *type* in the framework.</span></span> <span data-ttu-id="d083e-105">タイプは、バッチ フレームワークに統合されている一意のプロセスで、**SysOperations** フレームワーク、特に **SysOperationServiceController** クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="d083e-105">A type is a unique process that is integrated with the batch framework and that uses the **SysOperations** framework, specifically the **SysOperationServiceController** class.</span></span> <span data-ttu-id="d083e-106">タイプは、**ProcessScheduleType** テーブルに格納されています。</span><span class="sxs-lookup"><span data-stu-id="d083e-106">The types are stored in the **ProcessScheduleType** table.</span></span>

<span data-ttu-id="d083e-107">次に、プロセス自動化フレームワークに登録されている異なるタイプの例をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="d083e-107">Here are a few examples of different types that are registered with the process automation framework:</span></span>

- <span data-ttu-id="d083e-108">仕入先支払提案 (**VendPaymProposalAutomationTypeRegistrationProvider** クラス)</span><span class="sxs-lookup"><span data-stu-id="d083e-108">Vendor Payment Proposal (**VendPaymProposalAutomationTypeRegistrationProvider** class)</span></span>
- <span data-ttu-id="d083e-109">仕入先請求書の転記 (**VendInvoicePostProcessScheduleTypeRegistration** クラス)</span><span class="sxs-lookup"><span data-stu-id="d083e-109">Vendor Invoice Posting (**VendInvoicePostProcessScheduleTypeRegistration** class)</span></span>
- <span data-ttu-id="d083e-110">総勘定元帳への補助元帳転送 (**SubledgerJournalVoucherTransferServiceRegistration** クラス)</span><span class="sxs-lookup"><span data-stu-id="d083e-110">Subledger transfer to general ledger (**SubledgerJournalVoucherTransferServiceRegistration** class)</span></span>

<span data-ttu-id="d083e-111">既存のプロセスが **RunBaseBatch** を使用している場合は、**SysOperationServiceController** を使用してラッピングすることを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="d083e-111">If an existing process uses **RunBaseBatch**, consider wrapping it with **SysOperationServiceController**.</span></span> <span data-ttu-id="d083e-112">プロセス自動化フレームワークは、**RunBaseBatch** をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="d083e-112">The process automation framework doesn't support **RunBaseBatch**.</span></span>

<span data-ttu-id="d083e-113">プロセス自動化フレームワークにタイプを登録するには、**ProcessScheduleITypeRegistration** インターフェースを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d083e-113">To register your type with the process automation framework, you must implement the **ProcessScheduleITypeRegistration** interface.</span></span> <span data-ttu-id="d083e-114">このインターフェイスには、**ProcessScheduleTypeRegistrationItem** のインスタンスを返す単一のメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="d083e-114">This interface has a single method that returns an instance of **ProcessScheduleTypeRegistrationItem**.</span></span>

<span data-ttu-id="d083e-115">プロセスで機能フラグを使用している場合は、機能を無効および有効にして、それぞれのタイプを無効および有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d083e-115">If your process uses a feature flag, you must disable and enable the type as the feature is disabled and enabled, respectively.</span></span>

- <span data-ttu-id="d083e-116">タイプの機能フラグを無効にした場合、そのタイプはユーザー インターフェイス (UI) に表示されません。</span><span class="sxs-lookup"><span data-stu-id="d083e-116">If you disable the feature flag for a type, the type doesn't appear in the user interface (UI).</span></span> <span data-ttu-id="d083e-117">スケジューラは、そのタイプの発生またはバックグラウンド プロセスを実行するスケジュールをすることはなく、プロセス自動化フレームワークのランタイム側はそのタイプのバッチ ジョブを作成しません。</span><span class="sxs-lookup"><span data-stu-id="d083e-117">The scheduler won't schedule any occurrences or background processes of that type to run, and the runtime side of the process automation framework won't create any batch jobs for that type.</span></span>
- <span data-ttu-id="d083e-118">タイプの機能フラグを再度有効にすると、過去に実行するようスケジュールされた出来事またはバックグラウンド プロセスが直ちに実行されます。</span><span class="sxs-lookup"><span data-stu-id="d083e-118">If you enable the feature flag for a type, any occurrences or background processes that are scheduled to run in the past will be run immediately.</span></span> <span data-ttu-id="d083e-119">通常は、この動作が必要です。</span><span class="sxs-lookup"><span data-stu-id="d083e-119">Usually, this behavior is what you want.</span></span> <span data-ttu-id="d083e-120">ただし、それが必要ではない場合は、機能フラグを無効にする前に、そのタイプに関連するすべてのシリーズを無効にすることを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="d083e-120">However, if it isn't what you want, consider disabling any series that is related to the type before you disable the feature flag.</span></span>

<span data-ttu-id="d083e-121">機能管理には、購読可能なイベントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d083e-121">Feature management has events that you can subscribe to.</span></span> <span data-ttu-id="d083e-122">有効および無効にしたタイプを使用する方法は、**ProcessScheduleTypeRegistration.enableOrDisableType** となります。</span><span class="sxs-lookup"><span data-stu-id="d083e-122">The method that you use to enable and disable types is **ProcessScheduleTypeRegistration.enableOrDisableType**.</span></span>

<span data-ttu-id="d083e-123">データベースの同期が実行されるたびに、タイプとシリーズがコード内の定義から更新されます。</span><span class="sxs-lookup"><span data-stu-id="d083e-123">Every time that a database synchronization runs, types and series are updated from their definitions in code.</span></span> <span data-ttu-id="d083e-124">更新されない背景の設定は、システム管理者だけが編集できます。プロセス自動化フレームワークでは、**SysSetup** をフックすることによってこの更新が行われます。</span><span class="sxs-lookup"><span data-stu-id="d083e-124">The only background settings that aren't updated are those that can be edited by the system admin. The process automation framework does this update by hooking **SysSetup**.</span></span> <span data-ttu-id="d083e-125">システム管理者は、**システム管理\>設定\>バックグラウンドの初期化** の設定によりこのアップデートを手動で開始できます。</span><span class="sxs-lookup"><span data-stu-id="d083e-125">The system admin can manually trigger this update through the settings at **System administration \> Setup \> Initialize background**.</span></span>

<span data-ttu-id="d083e-126">次の例では、スケジュールされたタイプのプロセスを示します。</span><span class="sxs-lookup"><span data-stu-id="d083e-126">The following example shows a process for a scheduled type.</span></span> <span data-ttu-id="d083e-127">次のポイントに注意します。</span><span class="sxs-lookup"><span data-stu-id="d083e-127">Note the following points:</span></span>

- <span data-ttu-id="d083e-128">バックグラウンド プロセスは、パラメータをサポートしていないので、**パラメータ** タブ リストを設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d083e-128">A background process doesn't have to set the **Parameter** tab list, because background processes don't support parameters.</span></span>
- <span data-ttu-id="d083e-129">タイプ名は UI に表示されません。</span><span class="sxs-lookup"><span data-stu-id="d083e-129">The type name isn't shown in the UI.</span></span> <span data-ttu-id="d083e-130">この名前は、開発者が作成した **VendorInvoiceBatchPosting** などの文字列にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d083e-130">The name should be a developer-created string such as **VendorInvoiceBatchPosting**.</span></span> <span data-ttu-id="d083e-131">さまざまな目的に応じて型を参照するためのキーとして内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="d083e-131">It's used internally as a key to reference your type for various purposes.</span></span> <span data-ttu-id="d083e-132">ラベルにすることは **できません**。</span><span class="sxs-lookup"><span data-stu-id="d083e-132">It **cannot** be a label.</span></span>
- <span data-ttu-id="d083e-133">タイプ名は、**SysPlugin** パターンで頻繁に使用されます。</span><span class="sxs-lookup"><span data-stu-id="d083e-133">The type name is used heavily with the **SysPlugIn** pattern.</span></span> <span data-ttu-id="d083e-134">プロセス自動化フレームワークに実装されているインターフェイスのほとんどは、**SysPlugin** パターンに従っており、タイプ名が **ExportMetadataAttribute** によって指定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d083e-134">Most of the interfaces that are implemented for the process automation framework follow the **SysPlugIn** pattern and require that the type name be supplied by the **ExportMetadataAttribute**.</span></span> <span data-ttu-id="d083e-135">このパターンでは、ほとんどの場合、フレームワークは操作しようとしているタイプに対してのみインターフェイスの実装を呼び出し、その他のタイプに対しては呼び出しません。</span><span class="sxs-lookup"><span data-stu-id="d083e-135">In most cases in this pattern, the framework invokes the implementation of an interface only for the type that is being operated on, not for other types.</span></span> <span data-ttu-id="d083e-136">このトピックおよび関連するトピックのコード例は、このパターンに従います。</span><span class="sxs-lookup"><span data-stu-id="d083e-136">Code examples in this topic and related topics follow this pattern.</span></span>

```xpp
using System.ComponentModel.Composition;

// The VendPaymProposalAutomationTypeRegistrationProvider class handles type registration for Vendor payment proposal automations.
[Export(identifierStr(Dynamics.AX.Application.ProcessScheduleITypeRegistration))]
public final class VendPaymProposalAutomationTypeRegistrationProvider
implements ProcessScheduleITypeRegistration
{
    private const LabelId Caption = literalStr('@CashManagement:VendPaymProposalAutomationTypeName');
    private const LabelId HelpText = literalStr('@CashManagement:VendPaymProposalAutomationSeriesWizardHelpText');
    private const MenuItemName SeriesFormMenuItemName = menuItemDisplayStr(VendPaymProposalAutomationCriteriaSeries);

    [Wrappable(false)]
    public ProcessScheduleTypeRegistrationItem getScheduleTypeRegistrationItem()
    {
        ProcessScheduleTypeRegistrationItem item =
        ProcessScheduleTypeRegistrationItem::construct();
        item.parmName(VendPaymProposalAutomationConstants::RegisteredTypeName);
        item.parmLabelId(Caption);
        item.parmScheduleType(ProcessScheduleProcessType::Scheduled);
        item.parmCompanyScope(ProcessScheduleTypeCompanyScope::SingleCompany);
        item.parmProcessAutomationTaskClassName(classStr(VendPaymProposalAutomationTask));
        item.parmParameterTabItemList(this.constructParameterTabItemList());
        item.parmIsEnabled(VendPaymProposalAutomationFeature::isEnabled());
        return item;
        }

    private List constructParameterTabItemList()
    {
        List criteriaTabItemList = new List(Types::Class);
        ProcessScheduleTypeRegistrationParameterTabItem criteriaTabItem =
        ProcessScheduleTypeRegistrationParameterTabItem::newFromMenuItem(SeriesFormMenuItemName);

        criteriaTabItem.parmCaption(Caption);
        criteriaTabItem.parmHelpText(HelpText);
        criteriaTabItemList.addEnd(criteriaTabItem);
        return criteriaTabItemList;
        }
}
```

<span data-ttu-id="d083e-137">次の例は、プロセス自動化フレームワーク タイプの機能管理を示しています。</span><span class="sxs-lookup"><span data-stu-id="d083e-137">The following example shows feature management for a process automation framework type.</span></span>

```xpp
using System.ComponentModel.Composition;
using Microsoft.Dynamics.ApplicationPlatform.FeatureExposure;
using Microsoft.Dynamics.ApplicationPlatform.FeatureExposure.Implementation;

// The VendPaymProposalAutomationFeature class defines the Vendor Payment Proposal Automation feature.
[Export(identifierStr(Microsoft.Dynamics.ApplicationPlatform.FeatureExposure.IFeatureMetadata))]
internal final class VendPaymProposalAutomationFeature implements IFeatureMetadata, IFeatureMetadataEnablementNotifiable
{
    private static VendPaymProposalAutomationFeature instance;
    private void new()
    {
    }

    private static void typeNew()
    {
        instance = new VendPaymProposalAutomationFeature();
    }

    [Hookable(false)]
    public static VendPaymProposalAutomationFeature instance()
    {
        return VendPaymProposalAutomationFeature::instance;
    }

    [Hookable(false)]
    public FeatureLabelId label()
    {
        return literalStr("@CashManagement:VendPaymProposalAutomationFeatureName");
    }

    [Hookable(false)]
    public int module()
    {
        return FeatureModuleV0::AccountsPayable;
    }

    [Hookable(false)]
    public FeatureLabelId summary()
    {
        return literalStr("@CashManagement:VendPaymProposalAutomationFeatureSummary");
    }

    [Hookable(false)]
    public WebSiteURL learnMoreUrl()
    {
        return "<your URL>";
    }

    [Hookable(false)]
    public boolean isEnabledByDefault()
    {
        return false;
    }

    [Hookable(false)]
    public boolean canDisable()
    {
        return true;
    }

    [Hookable(false)]
    public void onEnabled()
    {
        this.enableOrDisableRegisteredType(NoYes::Yes);
    }

    [Hookable(false)]
    public void onDisabled()
    {
        this.enableOrDisableRegisteredType(NoYes::No);
    }

    private void enableOrDisableRegisteredType(NoYes _isEnabled)
    {
        ProcessScheduleTypeRegistration::enableOrDisableType(VendPaymProposalAutomationConstants::RegisteredTypeName,
    _isEnabled);
    }

    internal static boolean isEnabled()
    {
        return Dynamics.AX.Application.FeatureStateProvider::isFeatureEnabled(VendPaymProposalAutomationFeature::instance());
    }
}
```

## <a name="processscheduletyperegistrationitem-class"></a><span data-ttu-id="d083e-138">ProcessScheduleTypeRegistrationItem クラス</span><span class="sxs-lookup"><span data-stu-id="d083e-138">ProcessScheduleTypeRegistrationItem class</span></span>

<span data-ttu-id="d083e-139">**ProcessScheduleTypeRegistrationItem** クラスは、タイプ登録の一部として使用され、そのタイプに固有の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d083e-139">The **ProcessScheduleTypeRegistrationItem** class is used as a part of type registration and contains information that is specific to your type.</span></span>

| <span data-ttu-id="d083e-140">メソッド</span><span class="sxs-lookup"><span data-stu-id="d083e-140">Method</span></span> | <span data-ttu-id="d083e-141">説明</span><span class="sxs-lookup"><span data-stu-id="d083e-141">Description</span></span> |
|---|---|
| `public ProcessScheduleTypeName parmName(ProcessScheduleTypeName _name = name)` | <span data-ttu-id="d083e-142">**item.parmName** メソッドへ渡されるタイプ名はユーザーには表示されません。</span><span class="sxs-lookup"><span data-stu-id="d083e-142">The type name that is passed to the **item.parmName** method isn't shown to users.</span></span> <span data-ttu-id="d083e-143">この値は、さまざまなイベントが呼び出されたときに使用される開発者定義の文字列です。</span><span class="sxs-lookup"><span data-stu-id="d083e-143">This value is a developer-defined string that is used when various events are invoked.</span></span> <span data-ttu-id="d083e-144">ラベルとしてではなく、定数として割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d083e-144">It should be assigned as a constant, not as a label.</span></span> <span data-ttu-id="d083e-145">**タイプ名にはラベルを使用しないでください。**</span><span class="sxs-lookup"><span data-stu-id="d083e-145">**Never use a label as a type name.**</span></span> <span data-ttu-id="d083e-146">**VendPaymentProposal** などの名前を使用します。</span><span class="sxs-lookup"><span data-stu-id="d083e-146">Use names such as **VendPaymentProposal**.</span></span> |
| `public ProcessScheduleProcessType parmScheduleType(ProcessScheduleProcessType _scheduleType = scheduleType)` | <span data-ttu-id="d083e-147">このメソッドは、プロセスをスケジュールするか、ポーリングするかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d083e-147">This method determines whether the process is scheduled or polled.</span></span> |
| `public ProcessScheduleTypeCompanyScope parmCompanyScope(ProcessScheduleTypeCompanyScope _companyScope = companyScope)` | <span data-ttu-id="d083e-148">この方法は、プロセスが単一の会社のプロセスであるかグローバル プロセスであるかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d083e-148">This method determines whether the process is a single-company process or a global process.</span></span> <span data-ttu-id="d083e-149">単一会社のプロセスでは、シリーズの作成時にユーザーが所属する会社に応じて、バッチ内の会社コンテキストが設定されます。</span><span class="sxs-lookup"><span data-stu-id="d083e-149">A single-company process sets the company context in a batch, depending on the company that the user is in when a series is created.</span></span> <span data-ttu-id="d083e-150">スコープがグローバルである場合、会社コンテキストは無視され、すべてのジョブが **dat** に含まれます。</span><span class="sxs-lookup"><span data-stu-id="d083e-150">If the scope is global, the company context is ignored, and all jobs are in **dat**.</span></span> |
| `public LabelId parmLabelId(LabelId _labelId = labelId)` | <span data-ttu-id="d083e-151">このメソッドが返すラベルは、ユーザーに対して表示され、タイプの表示名を表します。</span><span class="sxs-lookup"><span data-stu-id="d083e-151">The label that this method returns is shown to users and represents the display name for your type.</span></span> <span data-ttu-id="d083e-152">たとえば、**仕入先支払提案** があります。</span><span class="sxs-lookup"><span data-stu-id="d083e-152">An example is **Vendor payment proposal**.</span></span> |
| `public className parmProcessAutomationTaskClassName(ClassName _processAutomationTaskClassName = processAutomationTaskClassName)` | <span data-ttu-id="d083e-153">このメソッドが返すクラス名は、**ProcessAutomationTask** インターフェースを実装するクラスのクラス名です。</span><span class="sxs-lookup"><span data-stu-id="d083e-153">The class name that this method returns is the class name of the class that will implement the **ProcessAutomationTask** interface.</span></span> |
| `public NoYes parmIsEnabled(NoYes _isEnabled = isEnabled)` | <span data-ttu-id="d083e-154">このメソッドは、登録しているタイプが既定で有効になっているかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d083e-154">This method determines whether the type that you're registering is enabled by default.</span></span> <span data-ttu-id="d083e-155">タイプが機能管理されている場合は、機能の状態から既定値が取得されます。</span><span class="sxs-lookup"><span data-stu-id="d083e-155">If your type is feature-managed, a default value is taken from the state of the feature.</span></span> <span data-ttu-id="d083e-156">有効化および無効化された機能管理イベントを必ず実装してください。</span><span class="sxs-lookup"><span data-stu-id="d083e-156">Be sure to implement the enabled and disabled feature management events.</span></span> <span data-ttu-id="d083e-157">**ProcessScheduleTypeRegistration.enableOrDisableType** メソッドを使用して、適切な方法でプロセス自動化フレームワークのタイプを有効および無効にします。</span><span class="sxs-lookup"><span data-stu-id="d083e-157">Enable and disable your type in the process automation framework in the appropriate way, by using **ProcessScheduleTypeRegistration.enableOrDisableType** method.</span></span> <span data-ttu-id="d083e-158">このトピックでは、先ほどの例となるコードを示します。</span><span class="sxs-lookup"><span data-stu-id="d083e-158">Example code is shown earlier in this topic.</span></span> |
| `public List parmParameterTabItemList(List _parameterTabList = parameterTabList)` | <span data-ttu-id="d083e-159">プロセスには、UI で多数のパラメーター ページを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d083e-159">A process can have many parameter pages in the UI.</span></span> <span data-ttu-id="d083e-160">これらのパラメーター ページには、プロセスに固有のパラメーターが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d083e-160">These parameter pages contain parameters that are specific to the process.</span></span> <span data-ttu-id="d083e-161">これらは、**シリーズの作成** ウィザードおよび出来事の編集ダイアログ ボックスでフォーム パーツとして示されます。</span><span class="sxs-lookup"><span data-stu-id="d083e-161">They are surfaced as form parts in the **Create series** wizard and edit occurrence dialog box.</span></span> <span data-ttu-id="d083e-162">パラメータ ページごとに、**ProcessSchedulelTypeRegistrationParameterTabItem** クラスのインスタンスは、構築されてリストに返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d083e-162">For each parameter page, an instance of the **ProcessSchedulelTypeRegistrationParameterTabItem** class must be constructed and returned in the list.</span></span> <span data-ttu-id="d083e-163">プロセスでパラメーター ページが不要な場合は、**null** を返します。</span><span class="sxs-lookup"><span data-stu-id="d083e-163">If the process doesn't require parameter pages, return **null**.</span></span> <span data-ttu-id="d083e-164">このプロセスの詳細については、[プロセス パラメーター](process-parameters.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d083e-164">For more information, see [Process parameters](process-parameters.md).</span></span> |
| `public static ProcessScheduleTypeRegistrationItem construct()` | <span data-ttu-id="d083e-165">このメソッドで、**ProcessScheduleTypeRegistrationItem** クラスのインスタンスを構築します。</span><span class="sxs-lookup"><span data-stu-id="d083e-165">This method constructs an instance of the **ProcessScheduleTypeRegistrationItem** class.</span></span> |

## <a name="processscheduleltyperegistrationparametertabitem-class"></a><span data-ttu-id="d083e-166">ProcessSchedulelTypeRegistrationParameterTabItem クラス</span><span class="sxs-lookup"><span data-stu-id="d083e-166">ProcessSchedulelTypeRegistrationParameterTabItem class</span></span>

<span data-ttu-id="d083e-167">**ProcessSchedulelTypeRegistrationParameterTabItem** クラスは、単一パラメーター ページに固有の情報を表します。</span><span class="sxs-lookup"><span data-stu-id="d083e-167">The **ProcessSchedulelTypeRegistrationParameterTabItem** class represents information that is specific to a single parameter page.</span></span>

| <span data-ttu-id="d083e-168">メソッド</span><span class="sxs-lookup"><span data-stu-id="d083e-168">Method</span></span> | <span data-ttu-id="d083e-169">説明</span><span class="sxs-lookup"><span data-stu-id="d083e-169">Description</span></span> |
|---|---|
| `public MenuItemName parmMenuItemName(MenuItemName _menuItemName = menuItemName)` | <span data-ttu-id="d083e-170">**シリーズの作成** ウィザードは、埋め込みフォーム パーツを使用してパラメーター ページをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d083e-170">The **Create series** wizard supports parameter pages by using embedded form parts.</span></span> <span data-ttu-id="d083e-171">この値は、プロセスを所有するチームによって作成されたフォーム パーツに移動するメニュー項目です。</span><span class="sxs-lookup"><span data-stu-id="d083e-171">This value is the menu item that goes to the form part that is created by the team that owns the process.</span></span> |
| `public LabelId parmCaption(LabelId _caption = caption)` | <span data-ttu-id="d083e-172">パラメーター ページのキャプション。</span><span class="sxs-lookup"><span data-stu-id="d083e-172">The caption on the parameter page.</span></span> |
| `public LabelId parmHelpText(LabelId _helpText = helpText)` | <span data-ttu-id="d083e-173">パラメーター ページのヘルプ テキスト。</span><span class="sxs-lookup"><span data-stu-id="d083e-173">The Help text for the parameter page.</span></span> |
| `public static ProcessScheduleTypeRegistrationParameterTabItem newFromMenuItem(MenuItemName _menuItemName)` | <span data-ttu-id="d083e-174">指定されたメニュー項目名でインスタンスを初期化するコンストラクター。</span><span class="sxs-lookup"><span data-stu-id="d083e-174">Constructor that initializes the instance with the specified menu item name.</span></span> |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]