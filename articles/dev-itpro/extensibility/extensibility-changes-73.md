---
title: "Finance and Operations, Enterprise Edition 7.3 の拡張機能の変更"
description: "このトピックでは、Dynamics 365 for Finance and Operations、Enterprise エディション 7.3 でリリースされた拡張機能を一覧表示します。"
author: FrankDahl
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: 
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: Platform update 4
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 2a0f2f047cb093b13614a807dde49bfdff44b87a
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="extensibility-changes-in-finance-and-operations-enterprise-edition-73"></a>Finance and Operations, Enterprise Edition 7.3 の拡張機能の変更

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 for Finance and Operations、Enterprise エディション 7.3 でリリースされた拡張機能を一覧表示します。 拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。

## <a name="soft-sealed-application-models"></a>ソフト シールされたアプリケーション モデル

このリリースは、すべてのモデルがハードシールになる前の最後のリリースとなり、このためのすべてのアプリケーション モデルはソフトシールされています。 ソフト シールされたモデルでもオーバーレイヤーされたコードを作成できますが、オーバーレイヤーされたコードをコンパイルするときに警告が生成されます。 

> [!NOTE]
> コードはオーバーレイすることができますが、推奨される方法は拡張です。

次のテーブルに、今回のリリースで現在ソフト シールされているモデルの一覧が含まれています。

| モジュール | モデル         |
| --------------- |-------------|
|ApplicationCommon | ApplicationCommon |
|ApplicationSuite | Electronic Reporting Application Suite Integration |
|ApplicationSuite | Foundation Upgrade |
|ApplicationSuite | Foundation |
|ApplicationSuite | SCMControls |
|ApplicationSuite | Tax Books Application Suite Integration |
|ApplicationSuite | Tax Engine Application Suite Integration |
|CaseManagement | CaseManagement |
|Currency | Currency |
|DataImpExpApplication | DataImpExpApplication |
|DataUpgrade | DataUpgrade |
|Directory | Directory |
|Directory | SecurityReports |
|GeneralLedger | GeneralLedger |
|Ledger | Ledger |
|PersonnelManagement | PersonnelManagement |
|Retail | Retail |
|SourceDocumentation | SourceDocumentation |
|SourceDocumentationTypes | SourceDocumentationTypes |
|補助元帳 | 補助元帳 |
|税申告 | 税申告 |

## <a name="hard-sealed-application-models"></a>ハード シールされたアプリケーション モデル

このリリースでは、ほとんどすべてのアプリケーションの主要なモデルはハード シールされています。 これらのモデルのオーバーレイ コードは、現在コンパイル エラーを発生します。 カスタマイズ モデルは拡張機能によってのみサポートされます。 拡張機能によってこれらのモデルをカスタマイズできない場合は、標準のアプリケーションを変更して拡張機能を有効にするよう、Microsoft に要求する必要があります。

次の表に、今回のリリースで現在ハード シールされているモデルの一覧が含まれています。

| モジュール| モデル         |
| --------------- |-------------|
| AccountsPayableMobile | AccountsPayableMobile |
| ApplicationWorkspaces | ApplicationWorkspaces |
| BankTypes | BankTypes |
| BusinessProcess | BusinessProcess |
| カレンダー | カレンダー |
| ContactPerson | ContactPerson |
| CostAccounting | CostAccounting |
| CostAccountingAX | CostAccountingAX |
| 分析コード | 分析コード |
| DirectoryUpgrade | DirectoryUpgrade |
| DOM | DOM |
| ElectronicReporting | ElectronicReporting |
| ElectronicReportingAppSuiteIntegration | ElectronicReportingAppSuiteIntegration |
| ElectronicReportingCore | ElectronicReportingCore |
| ElectronicReportingDotNetUtils | ElectronicReportingDotNetUtils |
| ElectronicReportingForAx | ElectronicReportingForAx |
| ElectronicReportingMapping | ElectronicReportingMapping |
| ExpenseMobile | ExpenseMobile |
| FinancialReporting | FinancialReporting |
| FinancialReportingEntityStore | FinancialReportingEntityStore |
| FiscalBooks | FiscalBooks |
| InventoryDimensionConversion | InventoryDimensionConversion |
| 測定 | 測定 |
| PaymentPredictor | PaymentPredictor |
| PerformanceTool | PerformanceTool |
| 担当者 | 担当者 |
| PersonnelCore | PersonnelCore |
| PersonnelMobile | PersonnelMobile |
| PersonnelUpgrade | PersonnelUpgrade |
| 保険証書 | 保険証書 |
| Project | Project |
| ProjectMobile | ProjectMobile |
| RegulatoryServices | RegulatoryServices |
| SCMMobile | SCMMobile |
| SelfHealing | SelfHealing |
| SelfHealingRules | SelfHealingRules |
| SystemHealth | SystemHealth |
| TaxEngine | TaxEngine |
| UnitOfMeasure | UnitOfMeasure |
| WMSAdvancedMigration | WMSAdvancedMigration |

## <a name="enumerations-that-have-been-made-extensible"></a>拡張可能になった列挙型

列挙の拡張をサポートするために以下の変更が行われました。
- 標準アプリケーションの多くの列挙が拡張可能になりました。 列挙を拡張可能にするには、列挙に関する 2 つのプロパティを設定します。 **IsExtensible** プロパティは **はい** に、**UseEnumValue** プロパティは **いいえ** に設定されます。 
- 一部の列挙型は状態を表します。 拡張機能によって列挙値の追加を可能にする新しいファサード メソッドが追加されました。 列挙型を拡張する方法については、「[列挙値の追加](add-enum-value.md)」を参照してください。
- 拡張機能をサポートするために、列挙を使用する一部のアプリケーション コードが変更されました。 一般的な変更の内容は以下の通りです。
    + ポストイベント サブスクリプションを許可するための、switch の default ケースの **throw** 例外ステートメントの削除。
    + 拡張機能の **SysExtension** サポートの追加。
    + 明示的なデリゲートを追加します。

| 列挙|
| --------------- |
|AssetCalendarYearType|
|AssetDepreciationConvention|
|AssetDepreciationMethod|
|AssetPeriodMonth|
|AssetSoldScrap|
|AssetStatusLVPFilter|
|AssetTransType|
|BaseDataProd|
|BOMRouteVersionSelect|
|BudgetPlanGenerateSource|
|BudgetPlanScenarioAccessLevel|
|BudgetPlanScenarioAttribute|
|BudgetTransactionColumnType|
|BusinessEvent_ActivityJournal|
|BusinessEvent_CustomerInvoice|
|BusinessEventRelievingMethod|
|CollabSiteEntityType|
|CollabSiteSharePointType|
|CostSheetNodeType|
|CreditCardAddEdit|
|CreditCardApprovalType|
|CreditCardDupCheckResult|
|CreditCardPaymType|
|CustAssessment|
|CustCollectionLetterCode|
|CustInterestFeeType|
|CustomerTransactionType|
|CustSettlementPriorityAttribute|
|CustSettlementTrans|
|CustTransRefType|
|CustVendDisputeStatus|
|CustVendForeignExchRefIndicator_US|
|CustVendGatewayOperatorOFACIndicator_US|
|CustVendorBlocked|
|CustVendOutPaymTrade|
|CustVendPaymStatus|
|CustVendSecondaryOFACIndicator_US|
|DimensionCacheScope|
|DirPartyRoleType|
|DirPartyRoleView|
|DistributionProcess|
|DistributionProcessingState|
|DistributionStatus|
|EPProjUpdateSubProjStage|
|HcmPositionForecastStatusSelection|
|JournalizingDefinitionLedgerEntryTypeId|
|LedgerBalanceExportFieldSeparator|
|LedgerBalanceExportHeaders|
|LedgerBalanceExportHiddenFields|
|LedgerBalanceExportInvertSign|
|LedgerBalanceExportSubcomponents|
|LedgerBalanceExportSubtotals|
|LedgerColumnType|
|LedgerConsDim|
|LedgerConsolidateAccountSource|
|LedgerDataExportFormat|
|LedgerReconciliationStatus|
|LedgerShowCurrency|
|LedgerSIEFileType|
|LedgerTransactionType|
|LedgerTransEnigneBuildQuery|
|LogisticsAddressElement|
|LogisticsAddrZipCodeImportCountryRegion|
|LogisticsLocationEntityType|
|LogisticsLocationSelectSourceType|
|MCROrderEventType|
|PaymManDocType|
|ProjAccountType|
|ProjAccountTypeCost|
|ProjAccountTypeSales|
|ProjActualVsForecastCategory|
|ProjActualVsForecastValue|
|ProjAlertType|
|ProjAssignConflictStatus|
|ProjCategoryType|
|ProjChoose|
|ProjContractType|
|ProjCostSales|
|ProjDimensionStrType|
|ProjectReportingAnalyticsWorkspaces|
|ProjEstimateMethod|
|ProjExportToExcelDimension|
|ProjFoundMethod|
|ProjFunctionType|
|ProjFundingRuleType|
|ProjInvoiceFrequency|
|ProjInvoiceProposalsTransSelectionTypes|
|ProjLevelFilterOption|
|ProjListLedgerTransType|
|ProjOrigin|
|ProjOriginOnAcc|
|projPostedProjectTransactionsListFilter|
|ProjProdTableListPageFilter|
|projProjectsListFilter|
|ProjQuotationTransTypeFilter|
|ProjResourceCapacityBooking|
|ProjResourceViewType|
|ProjSelectTransOnAcc|
|ProjServerProcessStatus|
|ProjStatementTypeSub|
|ProjStatus|
|ProjTransType|
|ProjValConnection|
|ProjValidateType|
|ProjViewSubProjects|
|ProjYearEndOptions|
|PSAActivityDisplayDefault|
|PSAActivityParent|
|PSADetailLevel|
|PSAExpenseProjValCategoryType|
|PSAInvoiceFormats|
|PSAProjInvoiceDetailGrouping|
|PSAProjInvoiceDetailSortBy|
|PSAProjOriginakVsCurrent|
|PSAPWPAssessment|
|PSAResAssignView|
|PSAResSchedStatus|
|PurchStatus|
|QuotationProjTransType|
|ReasonCodeAccountType|
|ResBasicSearchType|
|ResRollUpResourceType|
|ResTransferType|
|ResUtilizationCategoryEnum|
|RetailEventNotificationType|
|SourceDocument_ActivityJournal|
|SourceDocumentLine_ActivityJournalLine|
|SpecType|
|SyncProjTableAddSubProj|
|SyncProjTableDeleteSubProj|
|TrvCarRentalChargeType|
|TrvExpenseFilter|
|TrvExpenseReportGroupBy|
|TrvIntermediatePageOnCreateExpenseReport|
|TrvPayrollQtyOrDayes|
|TrvPBSTxtType|
|TrvPolicyViolationAction|
|TrvPosting|
|TrvPostStatus|
|TrvTaxType|
|TrvUDFDisplayOption|
|TSApprovalLevel|
|TSDocumentStatusReset|
|TSTimesheetFilter|
|TSTimesheetLineFilterType|
|TSTimesheetListPageFilters|
|TSVendorPerformanceThreshold|
|TypeOfCreditmaxCheck|
|VendInvoiceCloseCommand|
|VendorInvoiceSearchOptions|
|VendOutPaymFeeDistribution|

拡張可能な列挙型のサポートを改善するために、Foundation の変更が行われました。 **IsExtensible** が **はい** に設定されている列挙型については、**SysPlugin** フレームワークが使用可能になりました。 列挙型の新しい名前に基づく構文で、ビューが使用可能になりました。

## <a name="data-manipulation-methods-that-do-not-raise-dataevents-or-missing-insert-update-delete-pre--and-post-data-events"></a>DataEvents または欠落している insert、update、delete プリおよびポストデータ イベントを生成しないデータ操作メソッド

一般なプラクティスとして、テーブルのデータ メソッドを使用して、アプリケーションの拡張に使用できるイベントを発生させます。 コード ベースは、必ずしもこのプラクティスに従っていませんでした。 たとえば、**doInsert**、**doUpdate**、および **doDelete** データ メソッドと特定のテーブルの実装では、データ メソッドで **super()** の呼び出しは行われませんでした。

タイプ クラスの **insert**、**update**、および **delete** メソッドはリファクターされました。 データ メソッドで **super()** が確実に呼び出されるように変更が行われました。 これらの変更により、これらのメソッドへの拡張機能の追加が可能になり、その結果、プリイベントとポストイベントが拡張機能で使用できるようになりました。 次の表に、**insert**、**update**、および **delete** イベントが拡張機能に対して有効になったテーブルを表示します。

| テーブルとメソッド |
| ----------------------|
|BOM|
|BOMTable|
|BOMVersion|
|ProjTableType.delete|
|ProjTableType.update|
|工順|
|RouteOpr|
|RouteTable|
|RouteVersion|
|SalesLineType::interCompanyResetDeliverNow|
|テーブル ForecastSales|

## <a name="exposing-class-members"></a>クラス メンバーを公開

アクセス修飾子と新しい parm メソッドの変更の結果、追加のプライベート メンバーをカスタマイズに使用できるようになりました。 コマンド プラットフォームのチェーン機能により、保護されたメソッドやメンバーへの拡張クラスのアクセスが可能になります。 コマンド チェーンの詳細については、「[拡張可能な X++: コマンド チェーン](https://blogs.msdn.microsoft.com/mfp/2017/07/04/extensible-x-chain-of-command/)」を参照してください。

| メンバー |
| -------------|
|BankPaymCancel.custTransToCancel|
|CustCollectionLetterCancel - メソッド queryBuildUpdate|
|CustCollectionLetterPost - メソッド queryBuildUpdate|
|CustCollectionLetterPost - メソッド updateFee|
|CustCollectionLetterPost - メソッド validateCollectionLetter|
|CustInterestCancel - メソッド updateQuery|
|CustInterestHelper - メソッド getFeeLedgerAccount|
|CustInterestHelper - メソッド getInterestRecord|
|CustInterestHelper - メソッド getPostingProfile|
|CustInterestHelper - メソッド getTransLedgerAccount|
|CustInterestHelper - メソッド getTransLineLedgerAccount|
|CustInterestHelper - メソッド getVerDetailLedgerDimensionByIntTrans|
|CustInterestPost - メソッド postVoucher|
|CustOutPaymControlController|
|CustVendCreatePaymJournal - メソッド dialogAddInvoiceSelectionCriteriaFields|
|CustVendPaymProposal - メソッド createProposalLine|
|CustVendPaymProposal - メソッド parmLedgerJournalId|
|CustVendPaymProposalLineInsertSetManager - 変数|
|CustVendPaymProposalOrg - 変数|
|CustVendPaymProposalTransferToJournal - メソッド trackSpecTransForUpdate|
|CustVendPaymProposalTransferToJournal - 変数|
|フォーム ProjWorkBreakdownStructure|
|フォーム/クラス CustPaymModeSpec|
|フォーム/クラス VendPaymModeSpec|
|InventUpd_ChildReference.initUpdate|
|InventUpd_ChildReference.parmInventDimId|
|LogisticsLocationFormHandler.callerGetAddressRecord|
|ProjAdjustmentSelect.newQuery.addAdditionalHeaderRange|
|ProjAdjustmentSelect.processProjCostTrans|
|ProjAdjustmentSplit.deleteTransaction|
|ProjAdjustmentSplit.splitTransaction|
|ProjInvoiceChoose.parmprojInvoiceProjId|
|ProjProposalTotals.projInvoiceExchRate|
|SalesInvoiceJournalCreateBase|
|smmActivityCreate.createOrPrompt|
|テーブル SalesQuotationTable.canSubmitToWorkflow|
|VendorInvoiceLineSourceDocLineItem.initializeProjectFields|
|WHSWorkUserSession.WorkExecuteMode|

## <a name="construct-methods-with-throw-statements"></a>throw ステートメントを使用した construct メソッド

特定の型の実装が欠落していた場合、いくつかの **construct** メソッドが **throw** ステートメントで実装されました。 これは拡張性に対してはうまく機能しません。この問題を軽減するため、例外をスローしないように、**construct** メソッドが変更されました。 以下のメソッドは、クラス拡張、またはポストイベント サブスクリプションによって、拡張性に対して使用できるようになりました。

| オブジェクト |
| -------------|
|AddressZipCodeImport|
|CaseCategoryHierarchyTree|
|CustInterestCancel|
|CustInterestHelper|
|CustInterestPost|
|CustOutPaymControlController|
|CustTransQueryBuild|
|CustVendCreatePaymJournal_Cust|
|CustVendFindSettlements|
|CustVendOpenTransBalances.new|
|CustVendOpenTransManager.initFromCaller|
|CustVendPaymProposalTransferToJournal|
|CustVendTransQueryBuild|
|フォーム PdsApprovedVendorList|
|フォーム WhsContainerTable.init|
|FormletterJournalCreate.newSalesJournalCreate|
|FormLetterJournalPost.newPostSales|
|InventUpd_Physical::newInventMovement|
|InventUpd_Physical::newProdReleaseLossProfit_RU|
|LogisticsLocationSelectForm|
|PdsApprovedVendorListCheck.newBasedOnTableType|
|ProjInvoiceChoose|
|ProjTrans|
|PurchReqAutoCreate.newAutoCreate|
|PurchTableForm_Project|
|SalesQuantity|
|SalesTotals|
|WHSReservation|

## <a name="find-methods-with-throw-statements"></a>throw ステートメントのメソッドを検索します

特定の型の実装が欠落していた場合、いくつかの **find** メソッドが **throw** ステートメントで実装されました。 これは拡張性に対してはうまく機能しません。この問題を軽減するため、例外をスローしないように、**find** メソッドが変更されました。 以下のメソッドは、クラス拡張、またはポストイベント サブスクリプションによって、拡張性に対して使用できるようになりました。

| メソッド |
| -------------|
|TradePostalAddress.partyTable|

## <a name="extracted-method-to-open-for-class-extensions"></a>クラス拡張子を開くための抽出されたメソッド

**コマンドのチェーン**機能では、拡張クラスを作成できます。 拡張子クラスは、保護されたメソッドとパブリック メソッドおよびメンバーの両方にアクセスできるため、他のオプションよりも強力な拡張方法を提供します。 これにより、デリゲートやプレイベントまたはポスト イベントによって拡張するよりも柔軟性が向上します。

変更のこのグループでは、長いメソッドが小さいメソッドに抽出されます。 新しいメソッドには、より具体的なフォーカスがあり、拡張機能の範囲をより詳細に制御できます。

**指揮命令系統**機能が導入された後、デリゲートを追加する代わりにメソッドを抽出して拡張性を使用することをお勧めします。このアプローチにより、より柔軟なソリューションを提供する事ができるからです。

次のテーブルに、拡張クラスをビルドするために抽出されて開かれた新しいメソッドを示します。

| 方法 |
| -------------|
|AssetPost|
|BankPrintTestCheque|
|CustCreditLimit.showErrorMsg|
|CustVendCheque|
|CustVendChequeSlipTextCalculator|
|フォーム CustBankAccounts|
|フォーム DirPartyQuickCreateForm.init|
|フォーム HierarchyDetail.contextChanged|
|フォーム HierarchyDetail: smmActiviate: initValue|
|フォーム HierarchyNameLookoup: 階層: init|
|フォーム LedgerJournalTransDimension.init|
|フォーム ProjInvoiceProposalDetail.editInvoiceFormat|
|フォーム SalesCopying.upDateRemainderCache|
|フォーム SalesQuotationProjLinkWizard-> changeType|
|フォーム smmActivities: ResponsibleWorker_Overview: lookupReference|
|フォーム smmActivities: smmActivities::initValue|
|FormletterJournalPrint|
|HierarchyTemplateCopying.run|
|HierarchyTemplateCopying_CRM.copyActivity|
|HierarchyTemplateCopyingDialog.main|
|HierarchyTree|
|HierarchyTree.buildSubTree|
|InventDimCtrl_Frm_Mov_QualityOrder.mustEnableField|
|InventDistinctProductValidator.checkProductNotStopped|
|InventMovement.createProjLedgerForUpdateLedgerAdjust|
|InventTransferUpdShip::populateIssueReceiptDimensions|
|JournalFormTable|
|JournalizingDefinitionManager.newJournalizingDefinitionManagerCustomer|
|LedgerJournalCheckPost.checkJournal|
|LedgerJournalCheckPost.postJournal|
|LedgerJournalEngine.parmLedgerJournalTrans_Project|
|LedgerJournalEngine_Server.addVoucher|
|LedgerJournalEngine_VendApprove.cancelVoucher|
|LedgerJournalizeReportDP_DE.processReport|
|LedgerJournalTransUpdateCust.checkAccountBlocked|
|LedgerJournalTransUpdateVend.checkVendorBlocked|
|LogisticsAddressFormatProcess.run|
|ProjAdjustmentUpdate.journalTableInsert|
|ProjAdjustmentUpdate_Post|
|projCategoryLookup.buildQuery_PSA_impl|
|ProjEstimate.add|
|ProjFormLetter_invoice.projPrintFormLetter|
|ProjIntercompanyVendorInvoiceCreator.createVendorInvoiceLine|
|ProjListTransDP.insertTmpProjTransList|
|ProjPostRevenueProposal.projTransCreate|
|projUnpostedTransactionsListPage.populateMenuFunction|
|PSAProjAndContractInvoiceController.preRunModifyContract|
|PSARetenetionRelease.run|
|PurchAutoCreate_SalesLine.setPurchTable|
|PurchCreateFromSalesOrder.run|
|PurchFormletterParmDataInvoice.createParmLinesAndTable|
|PurchTableForm_DlvScheduleSyncEnabled.syncDeliveryScheduleCommercialAttributes|
|ReqCalc.deleteItemRequirement|
|ReturnAcknowledgmentAndDocumentDP.insertIntoTempTable|
|ReturnAcknowledgmentAndDocumentDP.setReturnAckAndDocumentTemplate|
|SalesAgreementFormDatasourceManager.transferCustAccount|
|SalesCopying.copy|
|SalesFormLetterParmData.createParmSubTable|
|SalesFormLetterParmDataInvoice.reSelectInit|
|SalesQuotationConfirmationDP.processReport|
|SalesQuotationConfirmationDP.setSalesQuotationDetailsTmp|
|SalesQuotationEditLinesForm.createParmLine|
|SalesQuotationEditLinesForm_Sales_Confir.createSalesLines|
|SalesQuotationTableForm_Sales.syncDeliveryScheduleCommercialAttributes|
|SalesQuotationTableType.validateField|
|SalesTable2LineUpdate.update|
|SalesTableForm.interCompanySetLineAccess|
|SalesTableForm_DlvScheduleSyncEnabled.syncDeliveryScheduleCommercialAttributes|
|SalesUpdateRemain.updateICDeliverRemainder|
|SmmProcessInstance.openForm|
|SubledgerJournalizerProjectExtension.createProjectActualHeader|
|テーブル CustTable.createOneTimeAccount|
|テーブル CustTable.lookupCustomer|
|テーブル InventPosting.salesAccount2AccountType|
|テーブル InventTable.lookupItem|
|テーブル ReqPO.update|
|テーブル SalesLine -> createFromSalesQuotationLine|
|テーブル SalesTable::initFromCustTableIL|
|テーブル smmBusRelTable.relation2Customer|
|テーブル smmBusRelTable.updateCustTable|
|テーブル TSTimesheetTrans.updateCommentsFromLineWeekUpdateTSTimesheetTrans|
|テーブル TSTimesheetTrans.updateFromTimesheetLineWeekUpdateTSTimesheetTrans|
|テーブル VendTable.lookupVendor|
|テーブル WHSWorkTable ->deleteAndCleanupWorkLines|
|テーブル WHSWorkTable ->SetBlankFields|
|テーブル WHSWorkTable ->SetFields|
|テーブル WrkCtrActivity.getCompanyContext|
|Tax.insertLineInInternal|
|TransactionReversal_Cust.fld900_1_modified|
|whsLoadTemplateAssignmentForm: WHSLoadTable::clicked|
|WhsWorkExecuteDisplay.getNextFormState|
|WHSWorkExecuteDisplay.setBatchDetails|
|WhsWorkExecuteDisplayReturnOrder.buildReturnOrder|
|WhsWorkExecuteDisplayReturnOrder.displayForm|

## <a name="changes-using-other-methods-to-support-extensibility"></a>拡張性をサポートするための他の方法を使用した変更

このセクションの変更のグループには、いくつかの異なる拡張機能のアプローチが含まれており、**コマンド チェーン** が導入される前の行われた拡張機能の変更を表しています。 使用されるアプローチの一部は、メソッドの抽出、"スタブ" メソッドの追加、デリゲートの追加、メソッドでのアクセス修飾子の変更、SysExtension フレームワークの使用を行います。 実行したアプローチがカスタマイズで機能するかどうかを判断するには、カスタマイズに必要な所定の場所の実装を参照してください。 今後のリリースで、主に**コマンド チェーン**を使用するため、このグループは小さくなります。

| 方法 |
| -------------|
|AccDistRuleSaleOfProductExtendedPrice.parmLedgerDimensionAllocList|
|AssetPost.createInventorySoldTransaction|
|AssetSplit.validate|
|AxSalesLine.doSave|
|AxSalesLine.setLineAmount|
|AxSalesQuotationLine.setLineAmount|
|BankPaymCancel.main|
|BankPaymCancel.run|
|BankPaymCancel.serverRun|
|BomCalcJob.main|
|CustCollectionLetterCancel.main|
|CustCollectionLetterCancel.run|
|CustCollectionLetterCreate.checkCustTransOpen|
|CustCollectionLetterCreate.createJournal|
|CustCollectionLetterPost.updateFee|
|CustCollectionLetterPost.validate|
|CustCollectionsExcelStatement.setTransactionWorksheetRow|
|CustInterestCancel.run|
|CustInterestCreate|
|CustInterestCreate.dialog|
|CustInterestCreate.runOnce|
|CustInterestHelper.getFeeLedgerAccount|
|CustInterestHelper.getVerDetailLedgerDimensionByIntTrans|
|CustInterestPost.postVoucher|
|CustInterestPost.run|
|CustInterestPost.updateFee|
|CustInterestPost.validateInterestTrans|
|CustInvoiceSpecDP::insertIntoTempTable|
|CustOutPaymControlController.init|
|CustPostInvoiceJob.custPostInvoiceUpdate()|
|CustSettlementPriorityProcessing|
|CustSettlementPriorityProcessing.markAllSelected|
|CustSettlementPriorityProcessing.markTransByCreditNoteOnBillingClasses|
|CustVendCreatePaymJournal.initBalances|
|CustVendOpenTransManager::updateOriginatorForMarkedTrans|
|CustVendPaymProposalCalcPaym.calcPaymDueDate|
|CustVendReversePosting.updateNow|
|CustVendSettle.mustOffsetOriginalSummaryDistributions|
|CustVendVoucher.initLedgerPosting|
|DimensionDerivationRule.buildDimensionCombination|
|DimensionDerivationRule.initialize|
|EcoResProductReleaseManager.release|
|EcoResProductReleaseSessionBatch.runJob|
|EcoResProductReleaseSessionManager.executeOnServer|
|EcoResProductVariantCreationMgr.buildVariantSuggestions()|
|フォーム BankPaymCancel.closeOK|
|フォーム BOMChangeLine.init|
|フォーム BOMConsistOf: BOMCreate|
|フォーム ConfigPartOf: EcoResConfiguration|
|フォーム CustBankAccounts.write|
|フォーム CustCollections.showAgingIndicator|
|フォーム CustOpenTrans.editMarkTrans|
|フォーム CustOpenTrans.updateDesignStatic|
|フォーム CustPaymEntry.editIsMarkedForSettlement|
|フォーム CustPaymEntry.write|
|フォーム CustSettlementPrioritySetup.active|
|フォーム CustTable.PrintManagement.clicked|
|フォーム EcoResProductImage.init|
|フォーム EcoResProductImage.setProductRecId|
|フォーム HRMAbsenceRequest.init|
|フォーム LedgerJournalTransAccrual.enableFields|
|フォーム LedgerJournalTransAccrual.LedgerJournalTransAccrual.clicked|
|フォーム LedgerJournalTransCustPaym: LedgerJournalTrans.active|
|フォーム LedgerJournalTransDaily: SettlementButton.clicked|
|フォーム LedgerJournalTransDimension.init|
|フォーム MarkupTable.init|
|フォーム MCRItemListCopying.copyLines|
|フォーム PCProductModelVersion|
|フォーム ProjInvoiceProposalCreateLines.modifiedTransFilter|
|フォーム ProjTransItem: ProjItemTrans.salesAmount|
|フォーム PurchCreateFromSalesOrder.SalesLine.included|
|フォーム ReqItemTable.init|
|フォーム SalesCopying.canClose|
|フォーム SalesCreateQuotation.setFieldsActive|
|フォーム SalesQuotationTable.init|
|フォーム SalesTable: SalesLine.write|
|フォーム SalesTable: SalesLine_DS.ItemId.lookup|
|フォーム: VendEditInvoice|
|FormletterJournalPos::newPostSales|
|FormLetterJournalPost.post|
|FormletterService.run|
|ProjTable.init から|
|HierarchyTemplateCopying.copyHierachy|
|HrmAbsenceRequestAction.run|
|InterCompanyUpdateRemPhys_PurchLine::synchronizeExternal|
|InterCompanyUpdateRemPhys_PurchLine::synchronizeInternal|
|InterCompanyUpdateStatus_PurchLine::synchronizeExternal|
|InterCompanyUpdateStatus_PurchLine::synchronizeInternal|
|IntrastatTransfer::calcCustVendInvoiceTransQty|
|InventDim::dimReportStr|
|InventMov_Transfer::checkUpdateEstimated|
|InventMov_Transfer::defaultDimension|
|InventMovement::checkNotSubDelivery|
|InventQualityManagementCreate.createQualityOrder|
|InventTransferParmLine::createShipLines|
|InventTransferParmLine::initFromInventTransferParmTable|
|InventTransferUpdShip::updateInventTransferLine|
|InventUpd_Estimated::createEstimatedInventTrans|
|InventUpd_Financial::newInventTransferLineReceive|
|InventUpd_Financial::newInventTransferLineShip|
|InventUpd_Financial::updateFinancialIssue|
|InventUpd_Financial::updateFinancialReceipt|
|InventUpd_Physical::newInventMovement|
|InventUpd_Reservation::updateReserveBuffer|
|InventUpd_Reservation::updateReserveFromForm|
|InventUpdate::whsUpdateDimReservePhysical|
|InventUpdate::whsUpdateWorkTransDimIssue|
|LedgerJournalCheckPost.postJournal|
|LedgerJournalEngine - メソッド preDelete|
|LedgerJournalEngine::findSettledAmount|
|LedgerJournalEngine_CustPayment.allowEditTrans|
|LedgerJournalEngine_CustPayment.initDefaultDimension|
|LedgerJournalEngine_CustPayment.write|
|LedgerJournalFormTable.verifyCanDelete|
|LedgerVoucherTransObject.newTransLedgerJournal|
|LogisticsPostalAddressFormHandler.main|
|マップ SalesPurchLine.calcPrice2LineAmount|
|マップ SalesPurchLine.setPriceAgreement|
|Markup.calc|
|MarkupAdjustment::main|
|McrPriceHistoryForm.insertPotentialTradeAgreements|
|OffsetVoucherCust.updateNow|
|PcGenerateBOMTableAndVersion.generate|
|PriceDisc.findDisc|
|PriceDisc::findItemLineDiscAgreement|
|PriceDisc::findItemPriceAgreement|
|PriceDisc::findMultiLineDiscServer|
|PriceDisc::newFromPriceDiscHeading|
|PriceDisc_LineDisc::findLineDiscAgreement|
|PriceDisc_Price::findPriceAgreement|
|PriceDiscAdmCheckPost.checkJournal|
|PrintMgmtHierarchy_Project.getParentImplementation|
|ProjAdjustmentSplit.createNewTrans.getNewTotalCostAmount|
|ProjInvoiceJournalPost.createProjInvoiceRevenue|
|ProjInvoiceProposalInsertLines.doSalesLine|
|ProjPost.postCost|
|ProjPostCostJournal.projTransCreate|
|ProjPostCostTrans_AdjNeg.projTransCreate|
|PurchAutoCreate_PurchReq.prepareSort|
|PurchCalcItem.initListBOM|
|PurchFormLetter.mainOnServer|
|PurchFormLetterParmData::newChooseLines|
|PurchFormletterParmDataInvoice.createParmLineAndSubLines|
|PurchInvoiceJournalPost.checkSourceLine|
|PurchInvoiceJournalPost.postCustVend|
|PurchInvoiceJournalPost.postInventory|
|PurchLineType.initDimensionsSpecificDefaulting|
|PurchLineType.interCompanyMirror|
|ReqCalcExplodeSales.run|
|SalesAutoCreate_ReleaseOrder.createSalesLine|
|SalesConfirmDP::createData|
|SalesConfirmDP::printDimHistory|
|SalesConfirmDP::setSalesConfirmDetailsTmp|
|SalesCopying.copy|
|SalesFormLetter.mainOnServer|
|SalesFormletterParmData.calcAutomaticTotalDiscount|
|SalesFormletterParmDataPickingList.insertParmLine|
|SalesInvoiceController::main|
|SalesInvoiceDP.insertIntoSalesInvoiceTmp|
|SalesInvoiceDP::insertIntoSalesInvoiceTmp|
|SalesInvoiceDP::loadCustPackingSlipTrans|
|SalesInvoiceDPBase::createData|
|SalesInvoiceJournalCreate::initInvoiceLineFromSourceLine|
|SalesInvoiceJournalPost::postCustVend|
|SalesLine::initReleasedProductSpecificDefaulting|
|SalesLineType.initDimensionsSpecificDefaulting|
|SalesLineType.interCompanyMirror|
|SalesLineType::checkDelete|
|SalesLineType::delete|
|SalesLineType::insert|
|SalesLineType::interCompanyMirror|
|SalesLineType::setSalesStatus|
|SalesLineType::update|
|SalesLineType::validateWrite|
|SalesPickingListJournalCreate::createJournalLine|
|SalesQuotationConfirmationDP::processReport|
|SalesQuotationCopying.copy|
|SalesQuotationDP::processReport|
|SalesQuotationLine.modifySalesQty|
|SalesQuotationLineType.initReleasedProductSpecificDefaulting|
|SalesQuotationToLineField.getFieldDescription|
|SalesTable2LineUpdate.update|
|SalesTableListPageInteraction.setButtonInterCompany|
|SalesTableListPageInteraction.setButtonInvoice|
|SalesTableListPageInteraction.setButtonPickAndPack|
|SalesUpdateRemain|
|SalesUpdateRemain::updateDeliveryRemainder|
|smmActivityCreate.setup|
|smmAttendeeTable.insert|
|smmSalesCustItemStatisticsDP::processReport|
|SpecTransManager.updateFullSettlement|
|SubledgerJournalizer.loadAccDistTmpRelieveAccrual|
|SubledgerJournalizer.loadaccountingDistributionTmp|
|SubledgerJournalizer.recordSubledgerJourAccEntriesForRounding|
|SubledgerJournalizer.recordSubledgerJournalAccountEntries|
|SubLedgerJournalTransferUIBuilder::build|
|SuppItemCreate_SalesQuotation::createLine|
|テーブル - PurchLine.Insert|
|テーブル - PurchLine.Update|
|テーブル CostingVersion.validateField|
|テーブル CustBankAccount.lookupBankAccount|
|テーブル CustCollectionLetterJour.cancelCollectionLetterCodeCustTrans|
|テーブル CustInterestJour.feeLedgerDimension|
|テーブル CustInvoiceTable - メソッド validateWrite|
|テーブル CustTable.blocked|
|テーブル CustTrans.reverseTransact|
|テーブル InventNonConformanceTable.setEditableFields|
|テーブル InventPosting.accountItemLedgerDimension|
|テーブル InventTable.updateAutoSalesPrice|
|テーブル InventTestAssociationTable.checkDocumentType|
|テーブル InventTrans.accountLossProfitLedgerDimension|
|テーブル LedgerJournalTrans.checkVATNumJournal|
|テーブル MarkupTrans.checkMarkCode|
|テーブル PurchLine.convertCurrencyCode|
|テーブル ReqPO.validateWrite|
|テーブル SalesLine.checkAndUpdateLoadLines|
|テーブル SalesLine.setPriceDisc|
|テーブル SalesQuotationLine.setPriceDisc|
|テーブル SalesTable.createMarkupTrans|
|テーブル TmpInventTransMark.updateTmpMark|
|テーブル TMSAppointment.validateWrite|
|テーブル WHSLoadLine::inventTransferLine|
|テーブル WHSLoadLine::purchLine|
|テーブル WHSLoadLine::salesLine|
|テーブル WHSRFMenuItemTable.validateWrite|
|Tax.distributeTotalTax|
|TradeInterCompany::insertInterCompanyInventDim|
|TransactionReversal_Asset.checkStatusApplicable|
|TransactionReversal_Cust.main|
|TransactionReversal_Cust.reversal|
|TransactionReversal_CustVend.createCustVendTrans|
|TSTimesheetLineWeek.loadFromLine|
|VendInvoiceInfoListPageMultiSelect.determineSelectState|
|WHSInventReserveDeltaLevelsEnumerator::moveNext|
|WhsPostEngineBase::createLoadFromShipment|
|WHSWorkCreateProdPut.insertProdParmforProdItem|
|WmsArrivalCreateJournal.createWMSJournalTransFromTmp|
|WMSPickingList_OrderPick.RunPrintMgmt|
|WrkCtrlScheduler_Prod.loadJobsDetail|

## <a name="methods-made-hookable"></a>フック可能なメソッド

公開されずフック不可能な一部のメソッドでは、拡張性サポートが強化されています。 以下のメソッドはフック可能な動作で明示的に修飾されています。

| 方法 |
| -------------|
|Bank.checkBankIBAN|
|BankDepositCreateCancelJour.initValues|
|BankDepositCreateCancelJour.newDepositCreateCancelJour|
|BankPaymCancel.initParms|
|BankPaymCancel.updateCollectionsStatusAutomation|
|CustAccountStatementExtController|
|CustAccountStatementIntDP.insertCustAccountStatementIntTmp()|
|CustCollectionLetterPost.updateFee|
|CustInterestCreate.construct|
|CustProvisionalBalanceDP.insertCustProvisionalBalanceTmp()|
|CustSettlementPriorityProcessing|
|CustVendCreatePaymJournal.dialogAddDateSelectionFields|
|CustVendPaymReconciliationSetStatus|
|CustVendReversePosting.updateCustVendTrans|
|DataEntity EcoResTrackingDimensionGroupEntity.dataSourceDimensionFieldId|
|EcoResProductCrossTableManager.saveValuesToProduct|
|EcoResProductImage.getImageFrom2Records|
|EUSalesListTransfer - 3 つの方法|
|フォーム EcoResProductCreate.applyTemplate|
|フォーム EcoResProductCreate.createData2Controls|
|フォーム PriceDiscTable.initFromCallerTable|
|フォーム ProjCostControl.setButtonVisibility|
|フォーム projPostedTransRelInfoFormPart: ProjPostTransView: costPrice|
|フォーム ProjTable.lookup 参照|
|フォーム ProjWorkBreakdownStructure|
|フォーム WHSPack.updateSummaryFields|
|FormletterJournalPost|
|FreeTextInvoiceDP.bankGroupIdName_CH|
|FreeTextInvoiceDP.bankZipCode_CH|
|FreeTextInvoiceDP.insertGiroInformation|
|FreeTextInvoiceDP.insertIntoFreeTextInvoiceHeaderFooterTmp|
|FreeTextInvoiceDP.insertIntoFreeTextInvoiceLocalizationTmp|
|FreeTextInvoiceDP.insertIntoFreeTextInvoiceTmp|
|HierarchyCreate_CRM.initHierarchy|
|HierarchyTemplateCopying_Proj.copyEstimates|
|InventDimGroupSetup.combineInventDimParms|
|InventLookupItemIdByDefaultOrder.initializeQuery|
|InventStorageDimMap.modifiedInventSiteFromParent|
|InventUpd_Physical.updatePhysicalReceiptTrans|
|JournalFormTable.initJournalTypeFromCaller|
|LedgerJournalCheckPost.runInternal|
|マップ SalesPurchLine.setPriceAgreement|
|マップ VendDocumentLineMap.setPurchaseInventReceiveNow|
|OffsetVoucherCust.getAutoSettlementQuery|
|ProjAdjustmentSelect.doTransCost|
|ProjAdjustmentSelect.doTransSale|
|ProjAdjustmentSelect.processProjEmplTrans|
|ProjAdjustmentSelect.validate|
|ProjAdjustmentSplit|
|ProjAdjustmentSplit.createNewTrans|
|ProjAdjustmentSplit.run|
|ProjAdjustmentUpdate.newPostAdjustment|
|ProjBegBalJournalTrans_CostSales.createProjTransPosting|
|ProjBegBalJournalTrans_Fee.createProjTransPosting|
|ProjBegBalJournalTrans_OnAcc.createProjTransPosting|
|projCostControl.progressUpdate|
|ProjEstimatesDataContract.setRevenueSalesPrice|
|ProjForecastBudget.forecastCopy|
|ProjForecastBudget.forecastDelete|
|ProjForecastPostItemFixedInvest.checkEnterCost|
|ProjForecastTransferFromWBS.transferToForecast|
|ProjFormLetter。 mainOnServer|
|ProjFormLetter.printPreview|
|ProjInvoiceDP.insertIntoProjInvoiceLocalizationTmp|
|ProjInvoiceDP.insertIntoProjInvoiceTmp|
|ProjInvoiceJournalCreate.creditMaxOk|
|ProjInvoiceJournalPost.initProposalUpdate|
|ProjLedger.newInventCost|
|ProjPlanVersionManager.copyActivityData|
|ProjPlanVersionsMananger.createDraftVersion|
|ProjProjectTransListPageInteraction.linkActive|
|Projtask.getCorrespondingTaskElementNumber|
|ProjValCheckTrans.validateMandatory|
|projWbsUpdateController.getNodesMapSortedByPath|
|PSAProjInvoiceDP.processLinesFromInvoiceJournal|
|psaProjQuotationSubmitSend.validateProjectDates|
|PSAQuotationsDP.insertPSAQuotationsTmp|
|PurchaseOrderResponseCreate.createPurchaseOrderResponseLines|
|PurchCancel.cancelMarkup|
|PurchCreateFromSalesOrder.preMatchIncludedLinesWithAgreements|
|PurchPackingSlipDP.setPurchPackingSlipDetailsTmp|
|PurchPackingSlipDP.setPurchPackingSlipHeaderTmp|
|PurchReceiptsListDP.setPurchReceiptsListDetailsTmp|
|PurchReceiptsListDP.setPurchReceiptsListHeaderTmp|
|PurchSummary.checkFormLetterId|
|ReqPlanCopy.insertLog|
|ResRollupActivityWriter::updateRollupTableWithLockedCapacityForActivityResource()|
|ResRollupAvailabilityWriter.updateRollupTableWithLockedCapacityForNamedResource()|
|SalesConfirmDP.setSalesConfirmDetailsTmp|
|SalesConfirmDP.setSalesConfirmHeaderTmp|
|SalesInvoiceController::main|
|SalesInvoiceDP.bankGroupIdName_CH|
|SalesInvoiceDP.bankZipCode_CH|
|SalesInvoiceDP.insertIntoSalesInvoiceHeaderFooterTmp|
|SalesInvoiceDP.insertIntoSalesInvoiceLocalizationTmp|
|SalesInvoiceDP.insertIntoSalesInvoiceTmp|
|SalesPackingSlipDP.setSalesPackingSlipDetailsTmp|
|SalesPackingSlipDP.setSalesPackingSlipHeaderTmp|
|SalesQuotationLineType.validateDelete|
|SalesQuotationLineType.validateWrite|
|SalesQuotationTableForm.CreateABSFromTemplate|
|salesQuotationTransferToProject.initParameters|
|SalesTable.initFromCustTableMandatoryFields|
|SalesTableListPageInteraction.setButtonSell|
|smmActivityCreate.createActivity|
|smmActivityCreate.new|
|smmActivityParentLinkTablee.insert|
|SubledgerJournalizerProjectExtension.createLedgerUpdate|
|テーブル CustBankAccount.validatePreNote|
|テーブル InventItemGTIN.formatGTIN|
|テーブル PriceDiscAdmTrans.checkItemRelation|
|テーブル PriceDiscAdmTrans.checkproductDimensions|
|テーブル ProjCategory.lookupProjCategoryType|
|テーブル ProjTable.validateWriteServer|
|テーブル PSAActivityEstimates.checkUpdateQuotationLine|
|テーブル PSAActivityEstimates.setSalesPriceFromCostPrice|
|テーブル PurchLine.setPriceDisc|
|テーブル PurchTable.internalTableIdToTableId_W|
|テーブル SalesLine.setPriceAgreement|
|テーブル Salesline.setPriceDisc|
|テーブル SalesQuotationLine.setPriceAgreement|
|テーブル SalesQuotationLine.setPriceDisc|
|テーブル SalesTable.setSalesOrderReleaseStatus|
|テーブル TmpCustVendTrans.createLineCreditLimit|
|テーブル TmpCustVendTrans.createLineCreditRemain|
|テーブル TmpCustVendTrans.createLineOrdered|
|テーブル TmpCustVendTrans.createLinePackingSlip|
|テーブル TmpCustVendTrans.createLineTotal|
|テーブル TmpCustVendTrans.insertTmpCustVendTransForCustBalance|
|テーブル TSTimeSheetLine.checkActivity|
|TSTimesheetLine::buildQuerySmmActivities|
|TsTimesheetPost.validatePost|
|VendProvisionalBalanceDP.insertVendProvisionalBalanceTmp()|
|VendTransQueryBuild::construct|
|VersioningPurchaseOrderResponse.archiveResponseLines|
|VersioningPurchaseOrderResponse.restoreLines|
|WhsCycleCountCreateLocation.run|
|WhsLoadReplenishment.calculateReplenishQty|
|WHSLoadTable::initPurchOriginDestination|
|WhsReplenishment.calculateReplenishQty|
|WhsRFControlData.validateAndUpdateWorkClusterLPScan|
|WhsShipConfirm.tmsRouteConfirmation|
|WhsWarehouseRelease.buildReleaseQuery|
|WhsWarehouseRelease.createLoadLines|
|WHSWaveTable.createWaveTableFromTemplate|
|WHSWorkExecute.createAdjustmentWork|
|WHSWorkExecute.createCountingJournal|
|WHSWorkExecute.createInventLine|
|WHSWorkExecute.executeShortPick|
|WHSWorkExecute.shortPickAdjustOut|
|WHSWorkExecuteDisplayPOReceiving.createWork|
|WorkTimeTable.lookupTime|

## <a name="inline-delegates"></a>インライン デリゲート

インライン デリゲートを使用できるようになりました。 インライン デリゲートの最も一般的な使用方法は、メソッドをより粒度の細かいメソッドに分割して、より小規模なメソッドで拡張イベントを使用できるようにすることです。

|  方法 |
| -------------|
|AssetCopy.run|
|AssetPost.post|
|AssetSplit.createTrans|
|AssetSplit.run|
|BankDepositCreateCancelJour.createDepositCancelJournal|
|BankPaymCancel.createCancellingCustTrans|
|BankPaymCancel.reverseSettlement|
|BankPaymCancel.run|
|BankPositivePayExport.initPositivePayQuery|
|BankPrintTestCheque.createTestCheque|
|BOMCalcItem.initListBOM|
|BOMCalcJob.runBOMCalculation|
|BOMRouteCopyJob.checkTo|
|BOMRouteCopyJob.main|
|BomRouteCopyJob::main|
|BomSearch.init|
|bomVersionActivate.run|
|CaseDetailForm.lookupParentCase|
|CaseDetailFormCreate.main|
|CaseUpdateStatus.changeStatus|
|CaseUpdateStatus_Close.updateStatus|
|ChequeDP.insertChequeTmp|
|クラス SalesLineType.intercompanyMirror|
|Commission.run|
|CostControlPostingSourceDocumentLine.createCommittedCost|
|CostSheetPanel.build|
|CustAccountStatementExtController.insertCustAccountStatementExtTmp|
|CustAgingReportController.getReportName|
|CustAgingReportDP.insertCustAgingReportTmp|
|CustCollectionJourDP.collectionLetterTitle|
|CustCollectionJourDP.insertCustCollectionJourTmp|
|CustCollectionLetterCancel.main|
|CustCollectionLetterCreate.createJournal|
|CustCollectionLetterCreate.updateCreatedCollectionLetter|
|CustCollectionLetterPost.run|
|CustCollectionLetterPost.updateFee|
|CustInterestCancel.run|
|CustInterestCreate.createJournal|
|CustInterestCreate.insertCustInterestTrans|
|CustInterestCreate.insertCustInterestTransLine|
|CustInterestPost.updateCustInterestTransVoucherRef|
|CustInterestPost.updateFee|
|CustInvoiceDP::insertCustInvoiceTmp|
|CustInvoiceSpecDP::insertIntoTempTable|
|CustNsf.createFeeJournalTrans|
|CustOutPaymControlController.insert|
|CustPostInvoice.createJournalHeader|
|CustPostInvoice::createJournalHeader|
|CustSettlementPriorityProcessing.createTempData|
|CustSettlementPriorityProcessing.markTransByCreditNoteOnBillingClasses|
|CustTransOpenPerDateDP.insertCustTransOpenPerDateTmp|
|CustVendCreatePaymJournal.checkBlocked|
|CustVendCreatePaymJournal.dialogAddInvoiceSelectionCriteriaFields|
|CustVendCreatePaymJournal.runPaymentProposalGenerationProcess|
|CustVendCreatePaymJournal_Vend.UpdateQuery|
|CustVendFindSettlements.findSettledSettlements|
|CustVendOpenTransBalances.initAccountNumCurrencies|
|CustVendOpenTransBalances.new|
|CustVendOpenTransManager.initFromCaller|
|CustVendOpenTransManager.updateOriginatorForMarkedTrans|
|CustVendPaymProposal.createProposalLine|
|CustVendPaymProposalTransferToJournal.initLedgerJournalTransFromPaymLine|
|CustVendPaymProposalTransferToJournal.run|
|CustVendPaymProposalTransferToJournal.transferProposal|
|CustVendReversePosting.updateCustVendTrans|
|CustVendSettle.createSettlementForDebitOrCreditTrans|
|CustVendSumForPaym::Validate|
|CustVendVoucher.post|
|CustVoucher.createInvoiceJournal|
|DataEntityView FreeTextInvoiceEntity.insertFreeTextInvoiceLines|
|DataEntityView FreeTextInvoiceEntity.preTargetProcessSetBased|
|DimensionHierarchyHelper::getHierarchyTypeByAccountType|
|EcoResProductMasterManager.addProductDimensionValue|
|EcoResProductReleaseManager.createInventITable|
|EcoResProductReleaseManager.createInventItemSetupSupplyType|
|EcoResProductReleaseManager.setInventTableFields|
|EcoResProductTemplateManager.getBufferByDataSourceName|
|EcoResProductVariantManager.createProductVariant|
|デリゲートを拡張 (DirPartyPostalAddressFormHandler、defaultLocationRoles_delegate)|
|フォーム BankReconciliation: BankAccountReconcile::clicked|
|フォーム CustCreditLimitCreditPart.totalAgingByCompany|
|フォーム CustDirectDebitMandate.run|
|フォーム CustFormletterParameters.PrintMgMt.clicked|
|フォーム CustOpenTrans.init|
|フォーム CustOpenTrans.updateDesignStatic|
|フォーム CustOpenTrans: ボタン UpdateNow::clicked|
|フォーム CustOpenTrans::doesCallerAllowEdit|
|フォーム CustTable: CustTable::write|
|フォーム EcoResProductCreate.writeMoreFields|
|フォーム EcoResProductVariantsPerCompany: InventDimCombination::write|
|フォーム HierarchyTemplateCopying_Proj.copyEstimates|
|フォーム InventDimParmFixed: InventDimParm::create|
|フォーム InventOnhandReserve: InventSum::reserveNow|
|フォーム InventOnhandReserve: InventTransOriginMovement::movementOnOrderUnit|
|フォーム InventOnhandReserve: InventTransOriginMovement::movementReservOrderedUnit|
|フォーム InventOnhandReserve: InventTransOriginMovement::movementReservPhysicalUnit|
|フォーム InventTransRegister: TmpInventTransWMS::setEnabled|
|フォーム LedgerJournalTransCustPaym.accountNumModifiedPost|
|フォーム LedgerJournalTransCustPaym: ボタン ButtonSettlement::clicked|
|フォーム LedgerJournalTransVendPaym: buttonPaymReconciliation::Clicked|
|フォーム LedgerJournalTransVendPaym: PaymReconciliationReject::Clicked|
|フォーム MarkupTrans.MarkupTrans_DS.active()|
|フォーム MCRSalesQuickQuote.init|
|フォーム MCRSalesQuickQuote.prepareSearch|
|フォーム MCRSalesQuickQuote.tmpFrmVirtualInventDimId|
|フォーム MRCSalesQuickQuote.createLines|
|フォーム PriceDiscActual::init|
|フォーム ProcCategoryHierarchyManagement.init|
|フォーム ProjAdjustment.init|
|フォーム ProjAdjustment.selectAdjRecords|
|フォーム ProjCreditNoteSelect.canClose|
|フォーム ProjCreditNoteSelect.writeTmpFrmVirtual|
|フォーム ProjInvoiceProposalCreateLines.TransTypeSelectionCtrl.lookup|
|フォーム PurchTable: PurchTable::enableJournalButtons|
|フォーム SalesATP.SalesATP|
|フォーム SalesQuickQuote: InventDimCombination::getSetQuantyties|
|フォーム SalesQuickQuote: InventDimCombination::salesQty|
|フォーム SalesQuotationProjTable::SalesQuotationLine::ItemId::modified|
|フォーム SalesQuotationTable: SalesQuotationTable::write|
|フォーム SalesTable.modified|
|フォーム SalesTable.SalesTable_DS.linkActive|
|フォーム SalesTable.write|
|フォーム SalesTable: SalesLine::write|
|フォーム SalesTable: SalesTable::write|
|フォーム TMSRateRouteWorkbench.updateRoutes|
|フォーム VendEditInvoice: VendInvoiceInfoTable.write|
|フォーム WhsWorkTable.setFilter|
|FormLetterJournalPost.post|
|FormLetterService.run|
|フォーム WHSLoadPlanningWorkbench.init|
|フォーム WHSLoadPlanningWorkbench.restoreQuery|
|FreeTextInvoiceDP::insertIntoFreeTextInvoiceHeaderFooterTmp|
|ProjTableCreate.init から|
|HierarchyCreate.run|
|HierarchyTemplateCopyingDialog_proj.main|
|InterCompanyPost.formLetterCollect|
|InventAgeDimDP.calcAllDim|
|InventAgeDimDP.insertInventAgeDimTmp|
|InventAgeDimDP.insertOrMergeInventAgeDimTmp|
|InventCountCreate.dialog|
|InventDimCtrl_Frm_Lookup.initDisplayOrderDataSource|
|InventDimPhysDP.processReport|
|InventDimViewContract|
|InventMovement.updateSerialNumIssue|
|InventMovement.updateSerialNumReceipt|
|InventMovement::updateLedgerPhysical|
|InventOnhandReserve.updateReserveNow|
|InventSumDateEngine.clearNotSelectedDimensions|
|InventTransferMulti.insert|
|InventUpd_Picked.updatePickMore|
|InventUpd_Reservation.updateReserveLess|
|InventUpdateOnhand.checkOnHand|
|InventValueReportContract|
|InventValueReportController|
|InventValueReportPopulateResource.initReportLines|
|JmgPostStandardSystem.postProjTime|
|JournalFormTable.designLookupJournalName|
|JournalFormTable.initAllOpenPostedFromCaller|
|LedgerBalancesBase.CalculateBalance|
|LedgerInAccountStatement.main|
|LedgerJournalCheckPost.createReverseEntryJournalLine|
|LedgerJournalCheckPost.postJournal|
|LedgerJournalCheckPost.runInternal|
|LedgerJournalCheckPost::updateSystemBlockCheckedPostedJournal|
|LedgerJournalMultiPost.multiSelectPost|
|LedgerJournalTrans table.checkBankAccounts|
|LedgerJournalTransUpdateVend::postNewVendorVoucher|
|マップ ProjTableWizardCtrl::insertDB|
|マップ SalesPurchLine.calcPrice2LineAmount|
|マップ SalesPurchLine.resetPriceAgreement|
|マップ SalesPurchLine.setPriceAgreement|
|MarkupAllocation.sumValue|
|MCRInventSearch.executeSearch|
|MCROrderEventTable.Insert|
|McrPriceHistoryForm.insertPriceHistory|
|PmfFormCtrl.initPost|
|PriceDiscAdmCheckPost.checkForOverlapsAndGaps|
|PriceDiscAdmCopy.updateNow|
|ProdJournalCheckPostProd::checkTrans|
|ProdJournalCheckPostProd::postTransLedger|
|ProdJournalCheckPostProd::postVoucher|
|ProdJournalCheckPostRoute.updateProdRouteScheduling|
|ProdJournalCreateProd.createLines|
|ProdJournalCreateRoute.createLinesProdRoute|
|ProdJournalFormTable.datasourceExecuteQueryPre|
|ProdMultiBOMCalc.run|
|ProdMultiCostEstimation.run|
|ProdMultiHistoricalCost.run|
|ProdMultiRelease.insert|
|ProdMultiRelease.run|
|ProdMultiReportFinished.main|
|ProdMultiReportFinished.run|
|ProdMultiSchedulingJob.run|
|ProdMultiSchedulingOperation.run|
|ProdMultiStartUp.run|
|ProdPurch.createPurchTable|
|prodTableChangeQtySched.performActionFromDefaultValues|
|prodTableChangeQtySched.performActionFromPrompt|
|ProdUpdCostEstimation.costEstimateOperations|
|ProdUpdCostEstimation.createPurchLine|
|ProdUpdReportFinished.run|
|ProdUpdReportFinished.updateBOMConsumption|
|ProdUpdStartUp.updateBOMConsumption|
|ProdUpdStartUp.updateRouteConsumption|
|ProjAdjustmentSelect.doTrans|
|ProjAdjustmentSelect.newQuery|
|ProjAdjustmentSelect.Run|
|ProjAdjustmentUpdate.checkTransChanged|
|ProjBudgetTransactionsManager.adjustBudget|
|ProjCopyForecastItem.copyToSalesLine|
|ProjCOstControl.createActualCosts|
|ProjCOstControl.createActuals|
|ProjCostControl.createAverageForRemaining|
|ProjCostControl.createCommittedCosts|
|ProjCostControl.createForecastCosts|
|ProjCostControl.queryCommittedCosts|
|ProjCostControl.queryProjTransPosting|
|ProjCostControl.run|
|ProjCostControl.validate|
|ProjForecastBudgetCopy.do_cost|
|ProjForecastBudgetCopy.do_empl|
|ProjForecastBudgetCopy.do_OnaCC|
|ProjForecastBudgetCopy.do_Revenue|
|ProjForecastBudgetCopy.do_Sales|
|ProjForecastBudgetCopy.initQuery|
|ProjForecastBudgetCopy.validate|
|ProjForecastBudgetDelete.initQuery|
|ProjForecastTransferFromWbs. transferItemToForecast|
|ProjFundingEngine.allocate|
|ProjFundingEngine.isAmountWithinFundingLimits|
|ProjFundingEngine.updateFundingLimits|
|ProjInvoiceChooseNormal.dialog|
|ProjInvoiceJournalCreate.initTotals|
|ProjInvoiceJournalPost.createProjInvoiceCost|
|ProjInvoiceJournalPost.createProjInvoiceEmpl|
|ProjInvoiceJournalPost.createProjInvoiceItem|
|ProjInvoiceJournalPost.createProjInvoiceOnAcc|
|ProjInvoiceJournalPost.createProjInvoiceRevenue|
|ProjInvoiceJournalPost.postCustVend|
|ProjInvoiceProposalCreateLines.runSalesLineQuery|
|ProjInvoiceProposalCreateLines.runTransactions|
|ProjInvoiceProposalInsertLines.run|
|ProjInvoiceProposalNormalPeriodic.createParameters|
|ProjInvoiceProposalPeriodic.dialog|
|ProjJournalCheckPost.processHourJournalResourceRateCost|
|ProjLedger.initFromProjectPostingTransaction|
|ProjLedgerUpdate.insert|
|ProjPlanVersionsManager.copyTasks|
|ProjProposalTotals.calc|
|ProjSplitBill.buildRuleQR|
|ProjSplitBill.split|
|ProjStatisticCalc.mapPSAEntityToTmpProjStatistic|
|ProjValCheckTrans.setVariablesFromBuffer|
|PsaCustomerRetention.createFeeTransaction|
|PsaGenerateQuotationLines.createSalesQuotationLines|
|PsaProjInvoiceDP::insertPSAProjInvoiceHeaderTmp|
|PsaProjInvoiceDP::insertPSAProjInvoiceTmp|
|PSARetentionRelease.insertLineRecords|
|PurchAgreementGenerateReleaseOrder.check|
|PurchAutoCreate_RFQ.createPurchLine|
|PurchAutoCreate_Sales.createLine|
|PurchCancel.cancelMarkup|
|PurchCancel.run|
|PurchCopying.copyLine|
|PurchCreateFromSalesOrder.mcrDropChipCreateTmpFrmVirtual|
|PurchCreateFromSalesOrder.preMatchIncludedLinesWithAgreements|
|PurchFormLetter.PrePromptInit|
|PurchformLetter::Main|
|PurchFormLetter::MainOnServer|
|PurchFormletterParmData.createParmTable|
|PurchFormletterParmDataInvoice.chooseLinesFromPurchSelectLinesManager|
|PurchLineType.intercompanyMirror|
|PurchLineType_Project.initFromInventTable|
|PurchLineType_WithMultipleDeliveries.recalculateDeliveryScheduleOrderLine|
|PurchPackingSlipDP::setPurchPackingSlipDetailsTmp|
|PurchPackingSlipDP::setPurchPackingSlipHeaderTmp|
|PurchPurchaseOrderDP.createData|
|PurchPurchaseOrderDP.initializePurchPurchaseOrderHeader|
|PurchPurchaseOrderDP.processReport|
|PurchPurchaseOrderDP.setPurchPurchaseOrderDetails|
|PurchPurchaseOrderDP::setPurchPurchaseOrderDetails|
|PurchPurchaseOrderDP::setPurchPurchaseOrderHeader|
|PurchReceiptsListDP::setPurchReceiptsListDetailsTmp|
|PurchReceiptsListDP::setPurchReceiptsListHeaderTmp|
|PurchReqTable2LineField.lineUpdateDescription|
|PurchRFQCaseAutoCreate.newAutoCreate|
|PurchRFQCompare.BuildReplyLineList|
|PurchRFQSendDP::processReport|
|PurchRFQSendJournalCreate.createOrUpdateRFQ|
|PurchTable2LineField.getFieldDescription|
|PurchTableType.intercompanyMirror|
|ReqActionApplyPurchaseOrder.applyActionToReferencedOrder|
|ReqBOMCreate.createBOM|
|ReqCalc.mcrInsertItemContinuitySales|
|ReqCalcScheduleItemTable.run|
|ReqSetupDim.setReqItemTableGrouped|
|ReqSupplyDemandScheduleModel.executeQuery|
|ReqSupplyDemandScheduleModel.insertPeriodValue|
|ReqTransPoMarkChangeToRFQ.change2RFQ|
|ReqTransPoMarkFirm.create|
|ReqTransPoMarkFirm.createInventTransferLine|
|ReqTransPoMarkFirm.createPurchLine|
|ReqTransPoMarkFirm.createPurchTable|
|ReqTransPoMarkFirm.firmSelectedPlannedOrders|
|RouteCopyToProd.copyTo|
|SalesAgreementGenerateReleaseOrder.check|
|SalesAgreementGenerateReleaseOrder.main|
|SalesAutoCreate_ReleaseFromAgreement.createSalesLine|
|SalesAutoCreate_ReleaseFromAgreement.createSalesTable|
|SalesAutoCreate_ReleaseOrder.createSalesTable|
|SalesConfirmDP.setSalesConfirmDetailsTmp|
|SalesConfirmDP.setSalesConfirmHeaderTmp|
|SalesConfirmDP::setSalesConfirmDetailsTmp|
|SalesConfirmDP::setSalesConfirmHeaderTmp|
|SalesCopying.copy|
|SalesCopying.copyHeader|
|SalesCopying.deleteLines|
|SalesCopying_CreditNote.copy|
|SalesCopying_CreditNote.copyHeader|
|SalesFormLetter.mainOnServer|
|SalesFormLetter.reselect|
|SalesFormletterParmData.createParmLine|
|SalesFormletterParmData::createParmTable|
|SalesInvoiceController::outputReport|
|SalesInvoiceDP.useExistingReportData|
|SalesInvoiceDP::insertIntoSalesInvoiceHeaderFooterTmp|
|SalesInvoiceDP::insertIntoSalesInvoiceTmp|
|SalesLineExplodeBOM.explode|
|SalesLineType.canPickingListBeRegistered|
|SalesLineType.delete|
|SalesLineType.initDimensionsSpecificDefaulting|
|SalesLineType.initFromSalesLine|
|SalesLineType.interCompanyMirror|
|SalesLineType.setSalesStatus|
|SalesLineType.validateField フィールド ShippingDateRequested および ShippingDateConfirmed|
|SalesPackingSlipDP.printDimHistory|
|SalesPackingSlipDP::setSalesPackingSlipDetailsTmp|
|SalesPackingSlipDP::setSalesPackingSlipHeaderTmp|
|SalesPurchTableToLineUpdate.update|
|SalesQuantity_PackingSlip.calcQtySales|
|SalesQuantity_PickingList.calcQtySales|
|SalesQuotationConfirmationDP::setSalesQuotationDetailsTmp|
|SalesQuotationConfirmationDP::setSalesQuotationHeaderTmp|
|SalesQuotationCopying.buildTreeControl|
|SalesQuotationCopying.Copy|
|SalesQuotationDP::setSalesQuotationDetailsTmp|
|SalesQuotationDP::setSalesQuotationHeaderTmp|
|SalesQuotationEditLinesForm.mainOnServer|
|SalesQuotationEditLinesForm_Proj_Confirm.queryBuildSalesQuotationTable|
|SalesQuotationEditLinesForm_Proj_Send.queryBuildSalesQuotationTable|
|SalesQuotationEditLinesForm_Sales_Confir.updateNow|
|SalesQuotationEditLinesForm_Sales_Confirm.createSalesLine|
|SalesQuotationEditLinesForm_Sales_Send.checkLines|
|SalesQuotationJumpRef.main|
|SalesQuotationLineType.initFromSalesQuotationLine|
|SalesQuotationLineType_Proj.validateWrite|
|SalesQuotationProjLinkWizard.transferForecastToProject|
|SalesQuotationProjLinkWizard.transferItemReq|
|SalesQuotationTransferToProject.transferItemsToForecast|
|SalesQuotationTransferToProject.transferItemsToItemReq|
|SalesQuotationUpdate.getCallerModuleFromParm|
|SalesTableForm.initValues|
|SalesTableForm_DeliverySchedule.updateSalesLineTable|
|SalesTableType.intercompanyMirror|
|SalesTableType.update|
|SalesTableType.validateDelete|
|smmSalesCustItemStatisticsDP::processReport|
|テーブル CaseDetailBase.validateWrite|
|テーブル CustCollectionLetterJour.updateCollectionLetterCodeCustTrans()|
|テーブル EcoResProductTranslation.queryAddCompanyLanguage|
|テーブル InventLocation::lookupBySiteIdAllTypes|
|テーブル InventPosting.accountGroup|
|テーブル InventPosting.accountItemLedgerDimension|
|テーブル InventPosting.deleteFromCust|
|テーブル InventPosting.deleteFromVend|
|テーブル InventTable.defaultProductDescription|
|テーブル InventTable.defaultProductName|
|テーブル InventTable.lookupBOMId|
|テーブル InventTrans.updateMarkReqTransCov|
|テーブル PaymTerm.due|
|テーブル ProdBOM.updateStartUp|
|テーブル ProdBOM.updateSubPurch|
|テーブル ProdJournalBOM.insertJournalCreate|
|テーブル ProdJournalBOM.lookupTransId|
|テーブル ProdTable.validateRouteId|
|テーブル ProjBegBalJournalTrans_CostSales.postProjTransactionCost|
|テーブル ProjBegBalJournalTrans_CostSales.postProjTransactionHour|
|テーブル ProjBegBalJournalTrans_CostSales.postProjTransactionItem|
|テーブル ProjBegBalJournalTrans_Fee.postProjTransaction|
|テーブル ProjBegBalJournalTrans_OnAcc.postProjTransactionCost|
|テーブル PurchLine.initBarCode|
|テーブル PurchLine.priceDateDelegate|
|テーブル PurchLine.setPriceDisc|
|テーブル PurchTable.updateFromPurchReqLineMap|
|テーブル ReqPO.updateBOMRoute|
|テーブル ReqTrans.bulkInitFromInventTransOrigin|
|テーブル RouteOpr.validateFieldValue|
|テーブル RouteVersion.checkExistInventSiteId|
|テーブル SalesLine.checkPriceDate|
|テーブル Salesline.convertCurrencyCode|
|テーブル SalesLine.convertToDeliverySchedule|
|テーブル SalesLine.createFromTmpFrmVirtualIL|
|テーブル SalesLine.createReplacement|
|テーブル SalesLine.createSalesLine|
|テーブル SalesLine.expandBOM|
|テーブル Salesline.modifyInventDimSet|
|テーブル SalesLine.priceDateDelegate|
|テーブル salesLine.setPriceAgreement|
|テーブル Salesline.splitReturnLine|
|テーブル SalesLine::createFromSalesQuotationLine|
|テーブル SalesQuotationLine.createFromTmpFrmVirtual|
|テーブル SalesQuotationLine.modifiedField|
|テーブル SalesQuotationLine.modifyInventDim|
|テーブル SalesQuotationTable.copyAddressToLine|
|テーブル SalesQuotationTable.lookupTemplateName|
|テーブル SalesTable.copyAddressToLine|
|テーブル SalesTable.copyRMALines|
|テーブル SalesTable.copyThirdPartyBillingAddressToLine|
|テーブル SalesTable.existingJournals|
|テーブル SalesTable.initFromCustTableIL|
|テーブル SalesTable.initFromProjTable|
|テーブル SalesTable.initFromSalesQuotationTable|
|テーブル SalesTable.unlinkAgreement|
|テーブル WHSAccountItemStatusDefault.checkModuleAccountNum|
|テーブル WHSLoadLine.delete|
|テーブル WHSLoadLine.updateReleaseQty|
|テーブル WhsLoadLine.validateQty|
|テーブル WHSLoadTable.assignOriginInfo|
|テーブル WHSProdTable.pickMore|
|テーブル WhsWorkTabke.lockUnLockWork|
|テーブル WMSBillOfLading.constructFromInvoice|
|テーブル WMSBillOfLading.constructFromPackingSlip|
|テーブル WMSBillOfLading.constructFromShipment|
|テーブル WMSOrderTrans.loopWMSOrderTransMulti|
|テーブル WrkCtrActivityRequirementSet.copyRequirements|
|テーブル WrkCtrActivityRequirementSet.schedulingProperties|
|テーブル SalesLine/Methods/setPriceDisc|
|TamDeductionUpdate_Deny.update|
|TmsProcessXML_Container.readShipContainer|
|TmsProcessXML_Shipment.readShipContainer|
|TradeInterCompany.insertInterCompanyInventDim|
|TradeInterCompanyConv.axPurchItemId|
|TradeInterCompanyConv.axSalesItemId|
|TransactionReversal_Asset.reversalBook|
|TransactionReversal_Cust::reversal|
|TransactionReversal_CustVend.createCustVendTrans|
|VendInvoiceDocumentDP::insertVendInvoiceDocumentTmp|
|VendInvoiceTableToLineUpdate.convertPurchTableFieldToVendInvoice|
|VendorInvoiceLineSourceDocLineItem.calculateSourceDocumentAmountMap|
|VersioningDocument.change|
|VersioningPurchaseOrder.createChangeRequest|
|WhsCycleCountCreateThreshold.processCycleCountThresholdItem|
|WHSInventOnHandReserve.changeReservation|
|WHSLaborStandards.findLaborStandardByItem|
|WHSLoadLine.update|
|WHSLoadTable.tmsLoadConfirmation|
|WHSLocationBuild|
|WHSLocationDirective.findLocation|
|WHSLocationDirective.findPickPutLocation|
|WHSLocationDirectiveActionQuery.modifyPickLocDirActionQuery|
|WHSPool.pickFromWorkCenter|
|WHSPostEngineBase.prodCreateWork|
|WHSPostEngineBase.prodPickQty|
|WhsRfControlData.getClusterPickQty|
|WHSRFControlData.processControl|
|WhsShipConfirm.canShipConfirm|
|WHSShipConfirm.createInventTransferParmLineFromContainerTable|
|WHSShipConfirm.runTransferShip|
|WhsShipConfirn.validateAllAllowedForOverOrUnderdeliveryWorkQtyHasBeenPicked|
|WHSSplitWork.splitWork|
|WHSWorkClusterTable.cleanupCluster|
|WHSWorkCreateProdPut.insertProdParmforCoByProduct|
|WHSWorkCreateProdPut.insertProdParmforProdItem|
|WhsWorkExecute.getFirstOpenLineSystemDirected|
|WHSWorkExecute.overPickByItem|
|WHSWorkExecute.putAwayToLocation|
|WHSWorkExecute.scanLicensePlate|
|WHSWorkExecuteDisplay.buildPORecTrackingDimensions|
|WhsWorkExecuteDisplayCycleCount.findOrCreateCycleCountWorkLines|
|WhsWorkExecuteDisplayLPReceiving.displayForm|
|WHSWorkExecuteDisplayMixedLPReceiving.displayForm|
|WHSWorkLine.cancelLineMultiPick|
|WHSWorkLine.cancelLinePartial|
|WMSArrivalCreateJournal.createWMSJournalTrans|
|WMSArrivalCreateJournal.createWMSJournalTransFromTmp|
|WMSArrivalOverviewGeneration.buildReturnOrderFromSalesLine|
|WMSJournalCheckPostReception.checkReference|
|WMSJournalTransUpdateSerialId.dialog|
|WmsPickingList_OrderPickDP::insertIntoTempTable|
|WrkCrtScheduler.writeJobCapacityReservations|
|WrkCtrApplicableResourceQuery.query|
|WrkCtrlScheduler_Prod.loadJobsDetail|
|WrkCtrlScheduler_Prod.saveOrder|
|WrkCtrlScheduler_Proj.saveOrder|
|WrkCtrlScheduler_Proj.writeJobData|
|WrkCtrReservedSum.find|
|WrkCtrScheduler.computeJobTimes|
|WrkCtrScheduler.insertWrkCtrCapResUsingInsertList|
|WrkCtrScheduler.writeJobCapacityReservations|
|WrkCtrScheduler.writeJobData|

## <a name="sql-operations-made-extensible"></a>拡張可能になった SQL 操作

埋め込み SQL ステートメントを使用するアプリケーション コードは拡張機能を通じて変更できません。 次の表に示す方法で拡張性を有効にするために、標準のアプリケーションに変更が加えられました。 これは、一般に、埋め込み SQL ステートメントを、これらのメソッドで SQL ステートメントの構築方法を拡張をサポートするクエリ オブジェクトに変換すると有効になります。

|  方法 |
| -------------|
|CustCollectionLetterCreate.updateAllExisting|
|CustCollectionLetterCreate.updateExisting|
|CustProvisionalBalanceDP.insertCustProvisionalBalanceTmp|
|CustProvisionalBalanceDP.processReport|
|CustSettlementPriorityProcessing.createTempData|
|DirPartyTable.getLocationFromRole|
|InventQualityOrderTable.createInventQualityOrderLines|
|InventTransIdSum::calcSum|
|InventTransIdSum_InventLocation::calcSum|
|InventTransReference::setRefTrans|
|Markup.insertMarkupTrans|
|Markup.mcrCopyForReturn|
|PriceDisc.findDisc|
|PriceDisc.findPriceAgreement|
|PurchFormLetterParmDataInvoice.createLineProject|
|ReqPlanCopy.copyReqTransAndReqTransCov|
|ReqPlanCopy.copyReqTransKeep|
|ReqPlanCopy.copyWrkCtrCapRes|
|ReqPlanCopy.copyWrkCtrCapResForReqPO|
|SalesCopying.deleteLines|
|SalesLineType::deliveredInTotal|
|SalesTableType.parmPickingListRegistrationEnumerable|
|SalesTableType_Sales.canPickingListBeUpdated|
|SalesUpdateRemain.canclRemainderOnOpenSalesLines|
|SubledgerJournalizer.createSummaryFromJournalAccountEntry|
|SubledgerJournalizer.loadAccountingDistributionTmpJournalize|
|SubledgerJournalizer.loadFinalizeSubledgerJournalTmpDetail|
|SubledgerJournalizer.loadStandardSubledgerLedgerJournalTmpDetail|
|SubledgerJournalizer.loadSubledgerJourTmpDetailWithRelieving|
|SubledgerJournalizer.recordSubledgerJourAccEntriesForRounding|
|SubledgerJournalizer.summarizeJourAccountEntryDetailForRound|
|SubledgerJournalTransferCommand.insertGeneralJournalAccountEntryRelatedDetail|
|TmsProcessXML_Base.writeShipDeliveryAccessorials|
|VendProvisionalBalanceDP.insertVendProvisionalBalanceTmp|
|VersioningPurchaseOrder.archivePurchLine|
|WhsLoadPostEngineBase::createShipments|
|WHSPackForm.getShipmentId|
|WHSPostEngineBase.executeWaveSteps|
|WhsPostPackingSlip.preparePackingSlipPosting|
|WhsWarehouseRelease.createShipments|
|WhsWarehouseRelease::createOrConsolidateShipmentForSalesOrder|

## <a name="maps-enabled-for-extensibility"></a>拡張性に対して使用可能なマップ

拡張機能によるフィールドとメソッドの追加を可能にするマップ実装に対して、新しいパターンが導入されました。 これの実行方法の詳細は、インターフェイスとして使用されるマップが含まれるドキュメントとバージョン管理実装のためのドキュメントの両方にあります。

次のテーブルに、拡張性を有効にするために変更が適用されたマップとその関連テーブルを一覧表示します。

| マップおよびテーブル|
| -------------------|
|マップ CustVendInvoiceTrans|
|マップ SalesPurchLine の拡張機能または継承|
|マップ SalesPurchTable|
|マップ VendDocumentLineMap|
|テーブル PurchLine マッピング|
|テーブル PurchLineHistory マッピング|

## <a name="inventory-dimensions"></a>在庫分析コード

このリリースでは、在庫分析コードを追加するための新しいモデルが導入されました。 以前のリリースでは、在庫分析コードが含まれているすべての SQL ステートメントの拡張が必要な場合、新しい在庫分析コードのカスタマイズをサポートすることは実用的ではありませんでした。 代わりに、特定の指定された用途のない 10 個の在庫分析コードを追加しました。 パートナー ソリューションは、そのコードを保持している間接モデルを通じてコード化し、パートナー ソリューションでの使用に向けた作成済みの在庫分析コード 1 つ以上を配置する個々の実装プロジェクトのために他のモデルが作成されます。 このモデルで在庫分析コードを実装する方法および新しいモデルについて学ぶのに役立つフレーバーの分析コード アプリをリリースする方法については、ドキュメントを利用できます。 新しい在庫分析コードは、製品分析コードまたは追跡用分析コードとして自由に配置して使用できます。

この変更により、アプリケーション全体で、次のリストに示されている内容を含む複数の場所が変更されました。

| 計上額 |
| -------------|
|拡張可能な製品分析コード|
|フォーム WHSInventOnHandReserve.updateInventDimFixedControls|
|InterCompanyInventDim: スロー付きの条件|
|InventDimFieldsMap - 追加されたフィールド|
|在庫分析コード InventUpdateOnhand::checkOnHand|
|在庫分析コード - テーブル InventDim.create|
|InventTransferUpdShip.populateIssueReceiptDimensions|
|マップ InventInventoryDimensionEntityFieldsMapping::resolveInventDim()|
|InventDimFieldsMap::getFieldIdForDimensionOnMappedTable の名前を inventoryDimensionFieldIdOnMappedTable() に変更|
|テーブル BOMConsistOfTmp マッピング|
|テーブル BOMPartOfTmp マッピング|
|テーブル EcoResTrackingDimensionGroup.isDimFieldTrackingDimension|
|テーブル InterCompanyInventDim マッピング|
|テーブル InventAgeGroupDimTmp マッピング|
|テーブル InventCheckRecieptCostPricePcsTmp マッピング|
|テーブル InventCostTmpTransBreakdown マッピング|
|テーブル InventCountStatisticsTmp マッピング|
|テーブル InventDim マッピング|
|テーブル InventOnhandTmp マッピング|
|テーブル InventPhysicalPerWarehouseTransTmp_IT マッピング|
|テーブル InventPriceOverviewTmp マッピング|
|テーブル InventSumCriticalTmp マッピング|
|テーブル InventSumDateTransReport マッピング|
|テーブル InventSumDeltaDim マッピング|
|テーブル InventTable マッピング|
|テーブル InventTransferOrderOverviewTmp マッピング|
|テーブル InventValueReportTmpLine マッピング|
|テーブル ProdPickList マッピング|
|テーブル SalesInvoiceTmp マッピング|
|テーブル WHSPurchLine.registerPurchaseLine|
|テーブル WHSTmpCompleteWorkLine.lookupBatch|
|テーブル WHSTmpCompleteWorkLine.lookupTargetLicensePlateId|
|テーブル WMSCheckABCZonesTmp マッピング|
|テーブル WMSPickingList_OrderPickTmp マッピング|
|テーブル WMSPickingListReportTmp マッピング|

## <a name="metadata-changes-to-enable-extensibility"></a>拡張機能を有効にするメタデータの変更

次のテーブルに、これらのオブジェクトの特定のメタデータの拡張機能を有効にするために加えられた変更を示します。 これらの変更はインスタンスごとに異なります。変更を確認するには、特定の実装を参照してください。

| 計上額 |
| -------------|
|CountryRegionCodes プロパティ|
|CustCustomerEntity|
|EcoResProductCategoryAssignmentEntity が公開|
|フォーム AssetSplit : FormControls|
|フォーム CustCollections.Cases|
|フォーム CustGroup|
|フォーム LedgerJournalTransCustPaym - メニュー項目ボタン自動申告|
|フォーム LedgerJournalTransVendPaym - メニュー項目ボタン自動申告|
|テーブル DimensionAttributeValueSetItem|
|他のステージング テーブルと同様、ReplacementKey がないテーブル EcoResReleasedProductCreationStaging。|
|テーブル SubledgerJournalAccountEntry(Tmp...)|
|SubLedgerJournalAccountEntryView の表示|

## <a name="other-changes"></a>その他の変更

次のテーブルに、拡張機能に対して行われた追加の変更を一覧表示します。

| 計上額 |
| -------------|
|CustCollectionLetterCreate|
|CustCollectionLetterPost|
|通貨の小数点以下桁数に対する拡張性アプローチ|
|拡張可能な EDT 小数点以下桁数: AssetDepreciationAmountUnit|
|フォーム拡張機能 - DirPartyTable - registerOverrideMethod jumpRef|
|フォーム ProjCategoryLookup|
|メソッド シグネチャが変更されました: InventPostingSetupCache|
|メソッド シグネチャが変更されました: テーブル ProjCostPriceExpense.find|
|メソッド シグネチャが変更されました: テーブル ProjCostPriceExpense.findCostPrice|
|メソッド シグネチャが変更されました: テーブル ProjCostSalesPrice.find|
|メソッド シグネチャが変更されました: テーブル ProjCostSalesPrice.findCostSalesPrice|
|メソッド シグネチャが変更されました: テーブル ProjHourCostPrice.Find|
|メソッド シグネチャが変更されました: テーブル ProjHourCostPrice.FindCostPrice|
|メソッド シグネチャが変更されました: テーブル ProjHourSalesPrice.find|
|メソッド シグネチャが変更されました: テーブル ProjHourSalesPrice.findHourSalesPrice|
|ApplicationCommon に追加される新しい数量 EDT|
|その他: 価格と割引のフレームワークの新しい基本列挙型|
|Alternative Key = Yes に設定し、参照グループ ルックアップを有効にする|
|EcoResIProductCrossTableData インターフェイスの使用|

## <a name="bugs"></a>バグ

次のテーブルは、拡張機能のために要求されたが、バグとして認識され、標準アプリケーションで修正された変更を一覧表示したものです。


|                                   計上額                                   |
|----------------------------------------------------------------------------|
|             class CaseUpdateStatus_Close, method changeStatus              |
|               CustCollectionLetterJour での誤った関係               |
|            その他: CompanyHelper.testCreateParameter のバグ修正             |
| テーブル CustCollectionLetterJour - クラス cancelCollectionLetterCodeCustTrans |


