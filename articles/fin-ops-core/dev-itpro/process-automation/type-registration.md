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
ms.openlocfilehash: c241794700907b086629d5d2a4d45e7fb16736d5f8469d0c4b9afa8b43e4297f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712287"
---
# <a name="type-registration"></a>タイプ登録

[!include [banner](../includes/banner.md)]

プロセス自動化フレームワークを使用してプロセスを実装するには、まずフレームワークの *タイプ* の概念を理解する必要があります。 タイプは、バッチ フレームワークに統合されている一意のプロセスで、**SysOperations** フレームワーク、特に **SysOperationServiceController** クラスを使用します。 タイプは、**ProcessScheduleType** テーブルに格納されています。

次に、プロセス自動化フレームワークに登録されている異なるタイプの例をいくつか示します。

- 仕入先支払提案 (**VendPaymProposalAutomationTypeRegistrationProvider** クラス)
- 仕入先請求書の転記 (**VendInvoicePostProcessScheduleTypeRegistration** クラス)
- 総勘定元帳への補助元帳転送 (**SubledgerJournalVoucherTransferServiceRegistration** クラス)

既存のプロセスが **RunBaseBatch** を使用している場合は、**SysOperationServiceController** を使用してラッピングすることを考慮してください。 プロセス自動化フレームワークは、**RunBaseBatch** をサポートしていません。

プロセス自動化フレームワークにタイプを登録するには、**ProcessScheduleITypeRegistration** インターフェースを実装する必要があります。 このインターフェイスには、**ProcessScheduleTypeRegistrationItem** のインスタンスを返す単一のメソッドがあります。

プロセスで機能フラグを使用している場合は、機能を無効および有効にして、それぞれのタイプを無効および有効にする必要があります。

- タイプの機能フラグを無効にした場合、そのタイプはユーザー インターフェイス (UI) に表示されません。 スケジューラは、そのタイプの発生またはバックグラウンド プロセスを実行するスケジュールをすることはなく、プロセス自動化フレームワークのランタイム側はそのタイプのバッチ ジョブを作成しません。
- タイプの機能フラグを再度有効にすると、過去に実行するようスケジュールされた出来事またはバックグラウンド プロセスが直ちに実行されます。 通常は、この動作が必要です。 ただし、それが必要ではない場合は、機能フラグを無効にする前に、そのタイプに関連するすべてのシリーズを無効にすることを考慮してください。

機能管理には、購読可能なイベントが含まれています。 有効および無効にしたタイプを使用する方法は、**ProcessScheduleTypeRegistration.enableOrDisableType** となります。

データベースの同期が実行されるたびに、タイプとシリーズがコード内の定義から更新されます。 更新されない背景の設定は、システム管理者だけが編集できます。プロセス自動化フレームワークでは、**SysSetup** をフックすることによってこの更新が行われます。 システム管理者は、**システム管理\>設定\>バックグラウンドの初期化** の設定によりこのアップデートを手動で開始できます。

次の例では、スケジュールされたタイプのプロセスを示します。 次のポイントに注意します。

- バックグラウンド プロセスは、パラメータをサポートしていないので、**パラメータ** タブ リストを設定する必要はありません。
- タイプ名は UI に表示されません。 この名前は、開発者が作成した **VendorInvoiceBatchPosting** などの文字列にする必要があります。 さまざまな目的に応じて型を参照するためのキーとして内部的に使用されます。 ラベルにすることは **できません**。
- タイプ名は、**SysPlugin** パターンで頻繁に使用されます。 プロセス自動化フレームワークに実装されているインターフェイスのほとんどは、**SysPlugin** パターンに従っており、タイプ名が **ExportMetadataAttribute** によって指定されている必要があります。 このパターンでは、ほとんどの場合、フレームワークは操作しようとしているタイプに対してのみインターフェイスの実装を呼び出し、その他のタイプに対しては呼び出しません。 このトピックおよび関連するトピックのコード例は、このパターンに従います。

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

次の例は、プロセス自動化フレームワーク タイプの機能管理を示しています。

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

## <a name="processscheduletyperegistrationitem-class"></a>ProcessScheduleTypeRegistrationItem クラス

**ProcessScheduleTypeRegistrationItem** クラスは、タイプ登録の一部として使用され、そのタイプに固有の情報が含まれます。

| メソッド | 説明 |
|---|---|
| `public ProcessScheduleTypeName parmName(ProcessScheduleTypeName _name = name)` | **item.parmName** メソッドへ渡されるタイプ名はユーザーには表示されません。 この値は、さまざまなイベントが呼び出されたときに使用される開発者定義の文字列です。 ラベルとしてではなく、定数として割り当てる必要があります。 **タイプ名にはラベルを使用しないでください。** **VendPaymentProposal** などの名前を使用します。 |
| `public ProcessScheduleProcessType parmScheduleType(ProcessScheduleProcessType _scheduleType = scheduleType)` | このメソッドは、プロセスをスケジュールするか、ポーリングするかを決定します。 |
| `public ProcessScheduleTypeCompanyScope parmCompanyScope(ProcessScheduleTypeCompanyScope _companyScope = companyScope)` | この方法は、プロセスが単一の会社のプロセスであるかグローバル プロセスであるかを決定します。 単一会社のプロセスでは、シリーズの作成時にユーザーが所属する会社に応じて、バッチ内の会社コンテキストが設定されます。 スコープがグローバルである場合、会社コンテキストは無視され、すべてのジョブが **dat** に含まれます。 |
| `public LabelId parmLabelId(LabelId _labelId = labelId)` | このメソッドが返すラベルは、ユーザーに対して表示され、タイプの表示名を表します。 たとえば、**仕入先支払提案** があります。 |
| `public className parmProcessAutomationTaskClassName(ClassName _processAutomationTaskClassName = processAutomationTaskClassName)` | このメソッドが返すクラス名は、**ProcessAutomationTask** インターフェースを実装するクラスのクラス名です。 |
| `public NoYes parmIsEnabled(NoYes _isEnabled = isEnabled)` | このメソッドは、登録しているタイプが既定で有効になっているかどうかを決定します。 タイプが機能管理されている場合は、機能の状態から既定値が取得されます。 有効化および無効化された機能管理イベントを必ず実装してください。 **ProcessScheduleTypeRegistration.enableOrDisableType** メソッドを使用して、適切な方法でプロセス自動化フレームワークのタイプを有効および無効にします。 このトピックでは、先ほどの例となるコードを示します。 |
| `public List parmParameterTabItemList(List _parameterTabList = parameterTabList)` | プロセスには、UI で多数のパラメーター ページを含めることができます。 これらのパラメーター ページには、プロセスに固有のパラメーターが含まれています。 これらは、**シリーズの作成** ウィザードおよび出来事の編集ダイアログ ボックスでフォーム パーツとして示されます。 パラメータ ページごとに、**ProcessSchedulelTypeRegistrationParameterTabItem** クラスのインスタンスは、構築されてリストに返す必要があります。 プロセスでパラメーター ページが不要な場合は、**null** を返します。 このプロセスの詳細については、[プロセス パラメーター](process-parameters.md) を参照してください。 |
| `public static ProcessScheduleTypeRegistrationItem construct()` | このメソッドで、**ProcessScheduleTypeRegistrationItem** クラスのインスタンスを構築します。 |

## <a name="processscheduleltyperegistrationparametertabitem-class"></a>ProcessSchedulelTypeRegistrationParameterTabItem クラス

**ProcessSchedulelTypeRegistrationParameterTabItem** クラスは、単一パラメーター ページに固有の情報を表します。

| メソッド | 説明 |
|---|---|
| `public MenuItemName parmMenuItemName(MenuItemName _menuItemName = menuItemName)` | **シリーズの作成** ウィザードは、埋め込みフォーム パーツを使用してパラメーター ページをサポートします。 この値は、プロセスを所有するチームによって作成されたフォーム パーツに移動するメニュー項目です。 |
| `public LabelId parmCaption(LabelId _caption = caption)` | パラメーター ページのキャプション。 |
| `public LabelId parmHelpText(LabelId _helpText = helpText)` | パラメーター ページのヘルプ テキスト。 |
| `public static ProcessScheduleTypeRegistrationParameterTabItem newFromMenuItem(MenuItemName _menuItemName)` | 指定されたメニュー項目名でインスタンスを初期化するコンストラクター。 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]