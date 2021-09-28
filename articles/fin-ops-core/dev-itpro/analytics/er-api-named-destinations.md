---
title: コードを変更して、ユーザーが名前付き送信先を構成して使用できるようにする
description: このトピックでは、電子申告 (ER) API を使用して、ユーザーが名前付き ER 送信先を構成および使用する方法について説明します。
author: NickSelin
ms.date: 08/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERFormatDestinationTable
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: bf8e8b5121752d80a1fb73eea7d84bdc1230d7fd
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413625"
---
# <a name="change-code-to-enable-users-to-configure-and-use-named-er-destinations"></a>コードを変更して、ユーザーが名前付き送信先を構成して使用できるようにする

[!include [banner](../includes/banner.md)]

[送信ドキュメント](general-electronic-reporting.md#configuring-data-model-mappings-for-outgoing-documents) を生成するには、ER  [形式マッピング](general-electronic-reporting.md#FormatComponentInbound) を実行する必要があります。 ER フレームワークの[初期](er-apis-app73.md#code-to-run-a-format-mapping-for-data-export) API を使用して ER 形式マッピングを呼び出す場合、形式のコンポーネントに対して構成されている[送信先](electronic-reporting-destinations.md#applicability)はすべて常に実行されます。 このタイプの呼び出しのサンプル コードを確認するには、[レポート サービス クラスを追加する](er-quick-start1-new-solution.md#ServiceClass)を参照してください。

ER 形式の[アクション依存の ER 送信先](er-action-dependent-destinations.md)を構成することもできます。 次に、ER フレームワークの[拡張](er-apis-app10-0-17.md#er-api-run-format-with-action-code) API を使用して、ユーザー アクション コードを提供する ER 形式のマッピングを呼び出すこともできます。 アクション コードは、設定されているアクション用に構成された送信先に対して実行されます。

場合によっては、[印刷管理](document-reporting-services.md)を構成し、異なる印刷管理レコードに対して同じ ER 形式を選択して、その形式を実行するときに生成されたドキュメントに異なる ER 送信先を適用できるようにする必要があります。 たとえば、元のドキュメントを電子メールで送信したり、ドキュメントのコピーをネットワーク プリンターで印刷するために、同じ ER 形式を実行できるように印刷管理を構成できます。 この目的のために、Microsoft Dynamics 365 Finance バージョン 10.0.21 の ER フレームワークの新しい [API](er-apis-app10-0-21.md) を使用できます。

## <a name="api-to-enable-users-to-configure-er-destinations-that-are-print-management-record-specific"></a><a name="er-api-set-print-management-record-specific-destination"></a>ユーザーが印刷管理レコード固有の ER 送信先を構成できるようにする API

現在、ビジネス ドキュメントの種類ごとに **印刷管理設定** ページを開いて、ビジネス ドキュメントの生成方法と配信方法を指定できます。 印刷管理ツリーの使用可能なすべてのレコードに対して、次のアクションを実行できます。

- **レポート形式** フィールドを使用して、実行する SQL Server Reporting Services (SSRS) レポートまたは ER 形式のいずれかを選択します。
- **送信先** ボタンを使用して **送信先設定** ダイアログ ボックスを開き、生成されたレポートの送信先を変更できるようにします。
- 定義された送信先を示す **送信先** フィールドを確認します。

> [!IMPORTANT]
> **レポート形式** フィールドで ER 形式が選択されている場合、構成された SSRS 送信先は生成されたレポートに適用されません。

この動作を変更し、印刷管理レコードに固有の ER 送信先を構成できます。 一般的な ER 送信先とは異なり、これらの送信先には名前が付けられます。 複数の印刷管理レコードに対して、1 つの名前付き送信先を選択できます。 詳細については、[印刷管理レコード固有の ER 送信先の構成](er-named-destinations.md)を参照してください。

まず、[機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace)ワークスペースで、**印刷管理品目ごとの ER 送信先設定を許可する** 機能を有効にする必要があります。

次に、この機能が既定で有効になっていない場合は、ユーザーが特定タイプのビジネス ドキュメントの印刷管理レコード固有の ER 送信先を構成できるようにする必要があります。 Finance バージョン 10.0.21 では、提供されているすべての `PrintMgmtDocumentType` ドキュメント タイプに対して `ERNamedDestinationReportEnabler` クラスの `isNamedDestinationEnabledByDocumentType` メソッドが *false* を返すため、すべてのビジネス ドキュメントに対して機能が有効になっているわけではありません。 

```xpp
/// <summary>Class for enabling NamedDestinationFeature for current document type.</summary>
/// <remarks>To enable the document type you should wrap a <c>isNamedDestinationEnabledByDocumentType</c> method.</remarks>
public class ERNamedDestinationReportEnabler
{
    /// <summary>Checks that feature enabled for current document type. Make extension for this method.</summary>
    /// <param name = "_typeId">Print mgmt document type</param>
    /// <returns>True if feature enabled.</returns>
    [Wrappable(true), SuppressBPWarning('BPParameterNotUsed', 'Required by signature')]
    public static boolean isNamedDestinationEnabledByDocumentType(PrintMgmtDocumentType _typeId)
    {
        return false;
    }
}
```

ユーザーがそのタイプのドキュメントの印刷管理レコード固有の ER 送信先を構成できるようにするには、特定のドキュメント タイプの `isNamedDestinationEnabledByDocumentType` メソッドをラップする必要があります。 次の例は、自由書式の請求書機能を有効にする方法を示しています。

```xpp
[ExtensionOf(classStr(ERNamedDestinationReportEnabler))]
final class ERNamedDestinationReportEnablerContoso_Extension
{
    public static boolean isNamedDestinationEnabledByDocumentType(PrintMgmtDocumentType _typeId)
    {
        var ret = next isNamedDestinationEnabledByDocumentType(_typeid);
        if(_typeId == PrintMgmtDocumentType::SalesFreeTextInvoice)
        {
            return true;
        }
        else
        {
            return ret;
        }
    }
}
```

## <a name="api-to-run-a-format-mapping-where-the-destination-that-is-provided-is-print-management-record-specific"></a><a name="er-api-pass-print-management-record-specific-destination"></a>提供される送信先が印刷管理レコード固有である形式マッピングを実行するための API

ユーザーが印刷管理レコード固有の送信先を構成できるようにする場合、名前付きの送信先が印刷管理レコード用に構成されていることが期待されます。 印刷管理レコードを使用して ER 形式を実行し、送信ドキュメントを生成する場合は、その名前付き送信先を ER フレームワークに渡して、実行中の ER 形式用に構成されている可能性のある他の送信先ではなく、ER が強制的にその送信先のみを実行するようにする必要があります。 

`ERPrintMgmtReportFormatSubscriber` クラスの次のコードは、自由書式の請求書を生成するために ER フレームワークが現在どのように呼び出されているかを示しています。

```xpp
/// <summary>
/// Runs a format mapping based on incoming arguments.
/// </summary>
/// <param name = "_args">Event arguments object.</param>
public static void runFreeTextInvoiceReport(NonSSRSPrintMgmtAdapterReportExecutedEventArgs _args)
{
    ERIFormatMappingRun formatMappingRun = ERPrintMgmtReportFormatSubscriber::buildFreeTextInvoiceReportMappingRun(_args);

    if (_args.parmArgs() && _args.parmArgs().parmEnumType() == enumNum(PrintCopyOriginal))
    {
        Args args = _args.parmArgs();
        boolean doUsePrintManagement = true;

        if (args.caller() is SalesFormLetter)
        {
            SalesFormLetter caller = args.caller();
            doUsePrintManagement = caller.usePrintManagement();
        }

        ERDestinationAction action;
        if (doUsePrintManagement || !isFlightEnabled(LocalizationFlights::ForcePrintJobSettings))
        {
            action = ReportDestinationContract::getPrintDestinationAction(args.parmEnum());
        }
        else
        {
            action = ERDestinationAction::View;
        }

        ERIFormatMappingRunWithDestinationAction mappingRunWithAction = formatMappingRun as ERIFormatMappingRunWithDestinationAction;

        if (mappingRunWithAction && action != ERDestinationAction::NoAction)
        {
            mappingRunWithAction.withDestinationAction(action);
        }
    }

    formatMappingRun.withCreatingObjectParameter(
        CustomersInvoicingModelName,
        classStr(PrintMgmtPrintSettingDetail),
        _args.parmSettingDetail());
    formatMappingRun.run();
}
```

次の例では、サンプル コードを変更して新しい API を使用して ER 形式を実行し、印刷管理レコード固有の名前付き ER の送信先を指定する方法を示します。

```xpp
/// <summary>
/// Runs a format mapping based on incoming arguments.
/// </summary>
/// <param name = "_args">Event arguments object.</param>
public static void runFreeTextInvoiceReport(NonSSRSPrintMgmtAdapterReportExecutedEventArgs _args)
{
    ERIFormatMappingRun formatMappingRun = ERPrintMgmtReportFormatSubscriber::buildFreeTextInvoiceReportMappingRun(_args);

    if (_args.parmArgs() && _args.parmArgs().parmEnumType() == enumNum(PrintCopyOriginal))
    {
        Args args = _args.parmArgs();
        boolean doUsePrintManagement = true;

        if (args.caller() is SalesFormLetter)
        {
            SalesFormLetter caller = args.caller();
            doUsePrintManagement = caller.usePrintManagement();
        }

        ERDestinationAction action;
        if (doUsePrintManagement || !isFlightEnabled(LocalizationFlights::ForcePrintJobSettings))
        {
            action = ReportDestinationContract::getPrintDestinationAction(args.parmEnum());
        }
        else
        {
            action = ERDestinationAction::View;
        }

        ERIFormatMappingRunWithDestinationAction mappingRunWithAction = formatMappingRun as ERIFormatMappingRunWithDestinationAction;

        if (mappingRunWithAction && action != ERDestinationAction::NoAction)
        {
            mappingRunWithAction.withDestinationAction(action);
        }

        // Check whether a named destination is provided.
        // If so, pass it to ER to specify a single destination for a generated document

        RefRecId NamedDestination;
        if (doUsePrintManagement || !isFlightEnabled(LocalizationFlights::ForcePrintJobSettings))
        {
            NamedDestination = ReportDestinationContract::getNamedDestination(args.parmEnum());
        }
        else
        {
            NamedDestination = 0;
        }

        ERIFormatMappingRunWithNamedDestination RunWithNamedDestination = formatMappingRun as ERIFormatMappingRunWithNamedDestination;

        if (RunWithNamedDestination && NamedDestination)
        {
            RunWithNamedDestination.withDestinationNamed(NamedDestination);
        }
    }

    formatMappingRun.withCreatingObjectParameter(
        CustomersInvoicingModelName,
        classStr(PrintMgmtPrintSettingDetail),
         _args.parmSettingDetail());
    formatMappingRun.run();
}
```

名前付き送信先への参照は、`PrintMgmtSettings` テーブルの `NamedDestination` フィールドで提供されます。 この参照を、`ReportDestinationContract` を拡張する処理済みの印刷管理レコードから、`runFreeTextInvoiceReport` メソッドに渡す必要があります。

## <a name="applicability"></a>適用性

名前付きの送信先を設定し、提供された名前付き送信先を ER フレームワークに使用させるには、最初に [機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace)ワークスペースで、**印刷管理品目ごとの ER 送信先設定を許可する** 機能を有効にする必要があります。

ER フレームワークを使用して Finance で生成できるすべてのタイプのビジネス ドキュメントの名前付き ER の送信先が有効になります。 詳細については、**コンフィギュレーション可能なビジネス ドキュメント – レポートの印刷管理設定を介した特定の送信先** 機能を参照してください。Dynamics 365 および業界のクラウド リリース プラン [2021 リリース ウェーブ 2](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance) にある Dynamics 365 Finance アプリケーションの「グローバリゼーション」 セクションにあります。

## <a name="additional-resources"></a>追加リソース

[電子申告 (ER) の概要](general-electronic-reporting.md)

[電子申告 (ER) の送信先](electronic-reporting-destinations.md)

[アクション依存の ER 送信先を構成する](er-action-dependent-destinations.md)

[印刷管理レコード固有の ER 送信先を構成する](er-named-destinations.md)

[Application update 10.0.21 での電子申告フレームワーク API の変更](er-apis-app10-0-21.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
