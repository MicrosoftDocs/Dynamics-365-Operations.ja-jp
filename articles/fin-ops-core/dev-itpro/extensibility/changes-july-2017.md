---
title: Finance and Operations, Enterprise Edition (2017 年 7 月) の拡張機能の変更
description: これは、(2017 年 7 月) に実装された拡張機能の一覧です。
author: FrankDahl
manager: AnnBe
ms.date: 11/08/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 056694597007e6707edf7e6dd5d42c43cb965c07
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812116"
---
# <a name="extensibility-changes-in-finance-and-operations-enterprise-edition-july-2017"></a>Finance and Operations, Enterprise Edition (2017 年 7 月) の拡張機能の変更

[!include [banner](../includes/banner.md)]

これは、Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月) に実装された拡張機能の一覧です。 このバージョンは 2017 年 7 月にリリースされ、ビルド番号は 7.2.11792.56024 です。 拡張性をサポートする変更スケジュールの詳細については、 [アプリケーション機能拡張ロードマップ](extensibility-roadmap.md)を参照してください。

## <a name="soft-sealed-application-models"></a>ソフト シールされたアプリケーション モデル

以下のアプリケーション中間層モデルは、今回のリリースでソフト シールされました。 これらのモデルのオーバーレイ コードは、コンパイル時に警告を生成します。

| カテゴリ       | モデル         |
| --------------- |-------------|
| アプリケーション フレームワーク | CaseManagement |
| アプリケーション フレームワーク | Dimensions |
| アプリケーション フレームワーク | Directory |
| アプリケーション フレームワーク | Organization |
| アプリケーション フレームワーク | Currency|
| アプリケーション フレームワーク | ApplicationCommon|
| HCM コア モデル| 3817938
|税モデル |Tax |
|税モデル |Tax Books |
|税モデル |Tax Books Application Suite Integration |
|税モデル |Tax Engine Application Suite Integration |
|税モデル |Tax Engine Configuration |
|税モデル |Tax Engine Interface |
|税モデル |Tax Engine Runtime Generation |
|税モデル |TaxEngine |
| 元伝票モデル |SourceDocumentation |
| 元伝票モデル |SourceDocumentationTypes |
| 元帳モデル |GeneralLedger |
| 元帳モデル |Ledger |
| 元帳モデル |Subledger |
| 中間層 SCM モデル | CostAccounting |
| 中間層 SCM モデル | CostAccountingAX |
| 中間層 SCM モデル | SCMControls |
| 中間層 SCM モデル | SCMMobile |
| 中間層 SCM モデル | UnitOfMeasure |
| 中間層 SCM モデル | WMSAdvancedMigration|
| 中間層 SCM モデル | InventoryDimensionConversion|
| ワークスペース| ApplicationWorkspaces |
| 財務| Fiscalbooks |
| 管理ツール | DataUpgrade |

## <a name="hard-sealed-application-models"></a>ハード シールされたアプリケーション モデル

以下のアプリケーション中間層モデルは、今回のリリースでハード シールされました。 これらのモデルのオーバーレイ コードは、コンパイル時にエラーを発生します。

| カテゴリ       | モデル         |
| --------------- |-------------|
| 買掛金勘定 | AccountsPayableMobile |
| 財務 | FinancialReportingEntityStore|
| ツール | PerformanceTool |
| 経費 | ExpenseMobile |
| GER | ElectronicReporting|
|GER | ElectronicReportingCore|
|GER | Electronic Reporting Application Suite Integration|

## <a name="enumerations-that-are-now-extensible"></a>拡張可能になった列挙型

列挙の拡張をサポートするために以下の変更が行われました。
- 標準アプリケーションの多くの列挙が拡張可能になりました。 列挙を拡張可能にするには、列挙に関する 2 つのプロパティを設定します。 **IsExtensible** プロパティは **はい** に、**UseEnumValue** プロパティは **いいえ** に設定されます。 
- 一部の列挙型は状態を表します。 拡張機能によって列挙値の追加を可能にする新しいファサード メソッドが追加されました。 列挙型を拡張する方法については、 [拡張機能を使用した列挙値の追加](add-enum-value.md)を参照してください。
- 拡張機能をサポートするために、列挙を使用する一部のアプリケーション コードが変更されました。 一般的な変更の内容は以下の通りです。
    + ポストイベント サブスクリプションを許可するための、switch の default ケースの **throw** 例外ステートメントの削除。
    + 拡張機能の **SysExtension** サポートの追加。
    + 明示的なデリゲートの追加。


| 列挙型|
| --------------- |
|AgreementState|
|AssetAccountType|
|AssetTransTypeJournal|
|BankAccountType|
|BankFormat|
|BarcodeContentType|
|BarcodeCoverPageEntityType|
|BarcodeType|
|BOMCalcCostingVersionUpdate|
|BOMCalcCostPriceUsed|
|BOMCalcSalesPriceUsed|
|BOMCalcType|
|BOMCheckLevel|
|BOMCopyContext|
|BOMCopyMethod|
|BOMCopyType|
|BOMCostCalculationMethod|
|BOMExplode|
|BOMRouteCopyDataType|
|BOMVersionFilter|
|BudgetReservation_BusinessEvent_PSN|
|BudgetReservation_SourceDocument_PSN|
|BudgetReservation_SourceDocumentLine_PSN|
|CatCallMethod|
|CatContentType|
|CatImportStatus|
|CatMaintenanceRequestWfStatus|
|CatProcurementErrorCode|
|CatPurchaseStatus|
|CatUserReviewApprovalStatus|
|CatVendorCatalogFileUploadType|
|CatVendorCatalogTemplateCategory|
|CatVendorCategoryHierarchyType|
|CatVendorConfigurationForImport|
|CatVendorLegalEntityStatus|
|CatVendorSiteType|
|ConsignmentReplenishmentOrderLineStatus|
|ConsignmentReplenishmentOrderStatus|
|CostBreakdown|
|CostCalculationCompareProductType|
|CostCalculationRole|
|CostCalculationState|
|CostCalculationSurchargeSubtype|
|CostingActivationType|
|CostingVersionCompareTo|
|CostingVersionPriceType|
|CostPriceBase|
|CostProfitSet|
|CostSalesPriceDisplay|
|CostSheetNodeListType|
|CostSheetPanelView|
|CostSheetProdFlowMode|
|CostStatementCacheAggregationAfter|
|CostWIPStatementCategory|
|CustPaymentValidate|
|CustSpecTransOverviewFormMode|
|CustTransRefType|
|CustVendPaymentStatus|
|CustVendTransportPointTypeTransfer|
|DlvScheduleMarkupConversionMode|
|EcoResAttributeModifier|
|EcoResCategoryAttributeModifier|
|EcoResCategoryChangeStatus|
|EcoResCategoryHierarchyModifier|
|EcoResCategoryNamedHierarchyRole|
|EcoResProductImageUsage|
|EcoResProductListPage|
|EcoResProductPerCompanyListPageType|
|EcoResProductTemplateType|
|EcoResReleaseProductToCompany|
|EcoResVariantConfigurationTechnologyType|
|ECPsalesOrdersViewType|
|EPCSSProductViewType|
|EUSalesTransMethod|
|FormLetterType|
|GanttCallerWrkCtr|
|GanttSetupType|
|GanttTimeUnit|
|GanttWrkCtrDisplayColumnsType|
|IntercompanyGoodsInTransitLineType|
|InterCompanyGoodsInTransitOrigin|
|InventAccountType|
|InventAccountTypeStdCostVariance|
|InventAdjustmentBy|
|InventAgingView|
|InventBatchJournalType|
|InventCostBundleState|
|InventCostCostDistribution|
|InventCostTransactionCategory|
|InventCostTransRefType|
|InventCountCode|
|InventItemCostingType|
|InventItemLookupDefaultTab|
|InventItemOrderSetupCallerType|
|InventItemOrderSetupType|
|InventItemPriceCompareLevel|
|InventItemPriceFilterType|
|InventItemPriceType|
|InventJournalOwnershipChangeLineCreateQueryStatusIssue|
|InventJournalType|
|InventLedgerConflictModule|
|InventLocationType|
|InventMovSubType|
|InventNonConformanceApproval|
|InventNonConformanceHistoryType|
|InventNonConformanceType|
|InventParameters|
|InventPhysicalReduction|
|InventRefType|
|InventReleaseOrderPickingType|
|InventReportDimHistoryLogType|
|InventStdCostConvItemStatus|
|InventStdCostPeriodType|
|InventSumFields|
|InventSupplyDlvModeSelectCust|
|InventSupplyDlvModeSelectSupply|
|InventSupplyLeadTimeSource|
|InventSupplyTmpLeadtimeType|
|InventTestActionOnFailure|
|InventTestBlockProcess|
|InventTestCorrectionPriority|
|InventTestCorrectionStatus|
|InventTestDocumentStatus|
|InventTestOrderStatusDisplay|
|InventTestOutcomeStatus|
|InventTestQtySpecification|
|InventTestQuarantineType|
|InventTestReferenceType|
|InventTestReport|
|InventTestType|
|InventTrackingDimNodeType|
|InventTrackingProductType|
|InventTrackingRegisterTransRegStatus|
|InventTransChildType|
|InventTransferRemainStatus|
|InventTransferStatus|
|InventTransferUpdateType|
|InventTransPickRegisterLineStatus|
|InventTransType|
|InventUpdType|
|InventValueReportLedgerAccountCategory|
|InventValueReportLedgerLineType|
|InventValueReportResourceType|
|ItemGroupLedgerDimensionGroup|
|ItemReservation|
|JmgAbsenceColumnLayout|
|JmgAbsenceMethodEnum|
|JmgAttendanceRegistrationType|
|JmgAttendanceReportType|
|JmgBarCodeType|
|JmgBreakDropEnum|
|JmgClockStyle|
|JmgControlType|
|JmgDaysTotalWorkflowStatus|
|JmgEmployeeSignInStatus|
|JmgFeedbackButtonFunction|
|JmgFeedbackStyle|
|JmgFieldName|
|JmgGetRegistrationTimeFrom|
|JmgGridAppearance|
|JmgJobTableSynchronizationMode|
|JmgJournalRegWorkflowStatus|
|JmgMark|
|JmgMessageType|
|JmgPayAdjustType|
|JmgPayEventsExportType|
|JmgPaySpecTypeEnum|
|JmgPaySpecTypeEnumPick|
|JmgPostAutomatically|
|JmgProdStatusUpdate|
|JmgProdStatusUpdateReportFinished|
|JmgProfileSpecTypeEnum|
|JmgProfileStartCodeBlankPrev|
|JmgProjStatusUpdate|
|JmgRegistrationTouchJobStatus|
|JmgSecondPresentationEnum|
|JmgShopFloorServiceStatus|
|JmgSignInButtonFunction|
|JmgStoppedCompletedStatus|
|JmgTermBaudeRate|
|JmgTermComPort|
|JmgTermDataBit|
|JmgTerminalInsertMode|
|JmgTermStopBit|
|KanbanBoardRefreshCycle|
|KanbanBoardType|
|KanbanCardAssignmentType|
|KanbanControlActionState|
|KanbanControlLegendFormat|
|KanbanControlSelectionChanged|
|KanbanDemandOriginType|
|KanbanJobPeggingType|
|KanbanJobPickingListLineType|
|KanbanLineEventType|
|KanbanMultiMode|
|KanbanPrintInstructions|
|KanbanProdBOMLineEventType|
|KanbanQuantityCalculationStatus|
|KanbanSalesLineEventType|
|KanbanStockReplenishmentEventType|
|LeanBOMLineReservationMethod|
|LeanCostingUnusedQtyType|
|LeanHandlingUnitEmptyPolicy|
|LeanInventoryControl|
|LeanPeggedEventType|
|LeanPlanJobReferenceTypes|
|LeanProductionFlowCostingStatus|
|LeanProductionFlowVisualizationViewMode|
|LeanProductTypes|
|LeanTaktStatus|
|LedgerPostingType|
|LedgerTransTxt|
|MarkupAllocateAfter|
|MarkupCategory|
|MCRBrokerContractStatus|
|MCRCustSearchType|
|MCRFullTextSearchType|
|MCRInstallPlanApplyMiscCharge|
|MCRItemListGenerationType|
|MCRPickingPrompt|
|MCRPickingSessionStatus|
|MCRPickingWaveStatus|
|MCRPriceHistoryType|
|MCRRoyaltyLineBreakType|
|MCRRoyaltyTakenFrom|
|MCRRoyaltyTransactionType|
|MCRRoyaltyUnitType|
|MCRRoyaltyUOMOption|
|MCRSalesOrderDetailStatus|
|ModuleInventCustVend|
|ModuleInventPurchSales|
|OriginalDocument|
|PaymDocumentType|
|PCExpressionEditorSymbolType|
|PCLookupMethod|
|PCNewSelectComponent|
|PCRequirement|
|PCTableConstraintType|
|PDSAdjustmentPrinciple|
|PdsBatchAttribToleranceAction|
|PdsBatchAttribUpdateType|
|PDSCalcElementBase|
|PDSCompensationPrincipleEnum|
|PDSElementTypeEnum|
|PDSIngredientTypeEnum|
|PdsMRCDocumentStatus|
|PdsMRCEffectiveDateBasis|
|PdsMRCEventModule|
|PdsMRCEventType|
|PdsMRCListType|
|PdsPaymtType|
|PDSPotencyAttribRecordingEnum|
|PdsRebateCalcDateType|
|PdsRebateTakenFrom|
|PdsRebateUOMOption|
|PdsSameLotError|
|pdsTMAJournalPosting|
|PdsUpdateBatchDate|
|PdsUpdateDispositionStatus_Quality|
|PlanActivityCreateRelationType|
|PlanActivityProductionFlowActivityType|
|PlanTypes|
|PmfCostAllocationMethod|
|PmfOrderType|
|PmfOrderTypeFilter|
|PmfProdType|
|PMFSeqCalendarPeriod|
|PriceBase|
|PriceDiscPurchasePromptSystemSource|
|PriceDiscSalesPromptSystemSource|
|PriceGroupType|
|PriceSalesPurch|
|PriceType|
|ProcCategoryAdministrationActivity|
|ProdBOMConsumpProposal|
|ProdBOMJournalQty|
|ProdBOMJournalSplit|
|ProdErrorCause|
|ProdGanttJobColorType|
|ProdGanttLoad|
|ProdGanttRouteColorType|
|ProdJournalCleanUpMode|
|ProdMode|
|ProdNotificationLevel|
|ProdParamInventDimLookup|
|ProdParmType|
|ProdRefLookUp|
|ProdRouteJobCurrentFormTabId|
|ProdSchedDirection|
|ProdScrapMethod|
|ProdStandardCostVariance|
|ProdStatusAll|
|ProdStatusType|
|ProductionTransType|
|ProdUpdateJour|
|ProdWHSReleasePolicy|
|ProdWIPType_NA|
|PurchaseOrderResponseAction|
|PurchaseType|
|PurchasingTransactionType|
|PurchCORReceivingMethod|
|PurchCORRejectStatus|
|PurchCovRef|
|PurchDlvAddr|
|PurchLineBackOrderViews|
|PurchLineDeliveryFulfillment|
|PurchLineDeliveryPrecision|
|PurchMatchingPolicyOverrideOption|
|PurchPrepayApplicationPolicy|
|PurchPriceDateType|
|PurchPurchaseOrderCreationMethod|
|PurchReApprovalPolicyRuleViewType|
|PurchReqAuthorizationSpecificReporting|
|PurchReqAutoCreatePurch|
|PurchReqCatalogAllNon|
|PurchReqConsolidationActiveStatus|
|PurchReqConsolidationPriority|
|PurchReqConsolidationStatus|
|PurchReqCreationStatus|
|PurchReqItemDescriptionTransfer|
|PurchReqItemFilterType|
|PurchReqOnBehalfReports|
|PurchReqOriginationAuthorizationView|
|PurchReqProcessingState|
|PurchReqQuestionnaireAggregateStatus|
|PurchReqQuestionnaireStatus|
|PurchReqReportSortOrder|
|PurchReqReportStatus|
|PurchReqReviewStatus|
|PurchReqRFQRequirement|
|PurchReqRFQType|
|PurchReqSaveChanges|
|PurchReqStatus|
|PurchReqType|
|PurchReqWorkflowState|
|PurchRFQQuestionnaireStatus|
|PurchRFQStatusVendor|
|PurchRFQType|
|PurchTableFormId|
|PurchTableListPage|
|PurchTableMode|
|PurchTotalsCachingMethod|
|PurchUpdate|
|PurchVendorPortalShowResponseType|
|QuotationType|
|ReqBOMRouteCreated|
|ReqCurrentDaySchedFrom|
|ReqDemPlanDataSourceType|
|ReqDemPlanDemandCategory|
|ReqDemPlanForecastAttributeType|
|ReqDemPlanForecastingStrategy|
|ReqDemPlanForecastType|
|ReqDisplayDelay|
|ReqForecastReducedBy|
|ReqGanttColorType|
|ReqGanttShow|
|ReqItemJournalType|
|ReqItemTableWizardPurpose|
|ReqMarkUpdate|
|ReqPeggingAssignmentType|
|ReqPeggingType|
|ReqPlannedOrderLeveling|
|ReqPlanType|
|ReqPOStatus|
|ReqQtyAmount|
|ReqRefType|
|ReqRefTypeShort|
|ReqRefTypeTrunc|
|ReqTraceMessageType|
|ReqTransFuturesActionPartType|
|ReturnCodeType|
|ReturnCycleTimeScope|
|ReturnReasonCodeDispExtended|
|ReturnReasonDispCode|
|ReturnUpdateAction|
|RouteFormula|
|RouteOprPriority|
|SalesBasketType|
|SalesBatch|
|SalesCheckForPickup|
|SalesCheckQtyCachKey|
|SalesDeliveryTimeState|
|SalesDocumentTimezonePreference|
|SalesPriceDateType|
|SalesPriceModelBasic|
|SalesPurchCopy|
|SalesPurchCycleAction|
|SalesPurchGroup|
|SalesPurchParmCleanUpMode|
|SalesQuotationFilter|
|SalesQuotationLinkToProject|
|SalesQuotationListPage|
|SalesQuotationPriceConversion|
|SalesQuotationPriceSimResult|
|SalesQuotationTypeListPage|
|SalesShipping|
|SalesSourcingOrigin|
|SalesStatus|
|SalesTableFormId|
|SalesTableListPage|
|SalesTableMode|
|SalesType|
|SalesUpdate|
|ShipCarrierDlvType|
|ShipCarrierFreightApplied|
|ShipCarrierMkUpFreight|
|SMAInvoiceProjectSelection|
|SMAItemSetupType|
|SMAProjectSelection|
|SMAReasonType|
|SMAServiceBOMChangeAction|
|SMAServiceFunctionType|
|SMAServiceLevelAgreementLogType|
|SMAServiceOrderActionType|
|SMAServiceOrderFilter|
|SMAServiceOrderOrigin|
|SMAServiceOrderProgress|
|SMAServiceTaskTitleOption|
|SMASubscriptionPeriodType|
|SMAWizardCreateType|
|smmAccountNumToCreate|
|smmActivityParentType|
|smmAppointmentNThInstance|
|smmBusinessRelationsListFilter|
|smmBusRelTypeSourceTable|
|smmCampaignBroadcastType|
|smmCampaignProjectJournalType|
|smmCampaignResponse|
|smmCampaignsListFilter|
|smmContactsListFilter|
|smmCreateOpportunityOptions|
|smmDisplayEMailInOutlook|
|smmDragDropObjectType|
|smmDupMethods|
|smmEMailSMS|
|smmEntityToCreate|
|smmFieldDelimiters|
|smmLeadsListFilter|
|smmLogType|
|smmOpportunitiesListFilter|
|smmOpportunityAssociation|
|smmOutlookContactDeleteAction|
|smmOutlookRecurrenceType|
|smmOutlookSyncPrinciple|
|smmOutlookUpdateAction|
|smmProjectNewExisting|
|smmQuotationAccountType|
|smmQuotationStatus|
|smmRecordDelimiters|
|smmSalesUnitMemberRelation|
|SmmSourceTypeList|
|smmSwotType|
|smmTransLogUpdateAction|
|smmUpdateOpportunityOptions|
|smmWarningError|
|SMAActiveAll|
|SMAAgreementFilter|
|SMAAgreementTableListPageType|
|TAMCustRebateApprovalStatus|
|TAMFundStatus|
|TAMFundType|
|TAMPromoCustomerType|
|TAMPromoMerchEvent|
|TAMPromoMgmtApprovalStatus|
|TAMPromotionDate|
|TAMPromotionMode|
|TAMRebateCustInclusive|
|TAMRebateLineBreakType|
|TAMRebateStatus|
|TAMRebateUnitType|
|TAMRebateUOMOption|
|TAMVendRebateApprovalStatus|
|TAMVendRebateCalcDateType|
|TAMVendRebateTakenFrom|
|TAMVendRebateTransactionType|
|TaxModuleType|
|TaxSourceType|
|TMSAccessorialAssignmentLevel|
|TMSAccessorialAssignmentTarget|
|TMSAccessorialDeliveryType|
|TMSAccessorialType|
|TMSAppointmentAlert|
|TMSDiscountResultType|
|TMSDiscountType|
|TMSFeeType|
|TMSFreightBillMatchStatus|
|TMSFreightBillReconcileType|
|TMSFwkErrorType|
|TMSHubPosition|
|TMSInvoiceAccountType|
|TMSLineType|
|TMSLoadBuildSessionState|
|TMSLoadTender|
|TMSLookupType|
|TMSNumberSequenceType|
|TMSOverrideLocationType|
|TMSRecurrenceDays|
|TMSRecurrenceType|
|TMSRecurrenceWeeks|
|TMSResponsibleForPayment|
|TMSRouteStatus|
|TMSSalesPurchTransfer|
|TMSTableRef|
|TMSTransportationType|
|TMSTransportRefType|
|TMSTransportTypeFilter|
|TMSUOM|
|TMSZoneType|
|TradeCurencyConversion|
|TradeLineDlvType|
|TradeNonStockedConversionChangeType|
|TradeNonStockedConversionIssue|
|TradeNonStockedConversionResolveUndo|
|TradePrintType|
|TradeTable2LineUpdate|
|VendNotificationCategorySelection|
|VendNotificationStatus|
|VendPackingSlipTransTimeStatus|
|VendRequestCompanyType|
|VendRequestOriginatedByType|
|VendRequestQuestionnairesCompleted|
|VendRequestRoleType|
|VendReviewRatingScore|
|VersioningAction|
|WHSAllowMaterialOverPick|
|WHSApplicableDemand|
|WHSAutoReleaseContainerAtContainerClose|
|WHSAutoReleaseOrderType|
|WHSBreakCluster|
|WHSContainerizationQueryType|
|WHSContainerPackingStrategy|
|WHSContainerTableFormViewType|
|WHSCrossDockFulfillmentStrategy|
|WHSCustJourType|
|WHSCycleCountPlanStatus|
|WHSDefaultDataField|
|WHSFilterModule|
|WHSHistoryEvent|
|WHSLoadPlanning|
|WHSLoadPostMethodsBase|
|WhsLoadReplenishment|
|WHSLoadTable|
|WHSLocDirStrategy|
|WHSLPAssignment|
|WHSLPWFilterType|
|WHSManifestAt|
|WHSManifestRequirementContainerGroup|
|WHSMenuItemDirectedBy|
|WHSMixedLPReceivingMode|
|WHSMixingLogicTables|
|WHSMobileAppPagePattern|
|WHSOriginType|
|WHSPickOldestBatch|
|WHSPostMethodBaseKanban|
|WHSPostMethodBaseKanbanOptional|
|WHSPostMethodBaseOptional|
|WHSPostMethodBaseProd|
|WHSPostMethodBaseProdOptional|
|WHSPostMethodsBase|
|WHSQtyPct|
|WHSReleaseQuantitySpecification|
|WHSReplenishmentDependentWorkBlockingPolicy|
|WHSReservationHierarchyLevelStrategyType|
|WHSReservationStatus|
|WHSUseFixedLocations|
|WHSWorkActivity|
|WHSWorkClusterStatus|
|WHSWorkCreationProcess|
|WHSWorkExceptionLogStatus|
|WHSWorkExecuteMode|
|WHSWorkListPageFilter|
|WHSWorkPrintOption|
|WHSWorkPutFlow|
|WHSWorkTransType|
|WHSWorkType|
|WHSWorkTypePickPut|
|WMSAutoAddStop|
|WMSFreightChargeTerms|
|WMSFreightCounted|
|WMSHandlingType|
|WMSLocationType|
|WMSPackageType|
|WMSPalletMovementProcessing|
|WMSPhysicalUpdateStatus|
|WMSReceiptStatus|
|WMSReservationMethod|
|WMSReservationMethodInternal|
|WMSShipmentStatus|
|WMSShipmentType|
|WMSSpaceUtilInconsistencyGroup|
|WMSSpaceUtilShowBy|
|WMSSpaceUtilStorageLoadUnitType|
|WMSStoreAreaType|
|WMSTrailerLoaded|
|WrkCtrActivityType|
|WrkCtrBulkResReqSearchType|
|WrkCtrCapacityType|
|WrkCtrCapRefType|
|WrkCtrCommitState|
|WrkCtrGroupWrkCtr|
|WrkCtrSchedulerCommand|
|WrkCtrSchedulerConstraintType|
|WrkCtrSchedulerLoggerMode|
|WrkCtrType|
|WrkCtrTypeFilter|

以下の列挙型は削除され、拡張可能になりませんでした。

| 削除された列挙型 |
| --------------- |
|BackorderLinesListPageMode|
|BackorderPurchLinesListPageMode |
|EcoResProductPerCompanyListPageType |
|ReturnTableListPageType |
|SMAAgreementTableListPageType|

拡張可能な列挙型のサポートを改善するために、Foundation の変更が行われました。 **IsExtensible** が **はい** に設定されている列挙型については、**SysPlugin** フレームワークが使用可能になりました。 列挙型の新しい名前に基づく構文で、ビューが使用可能になりました。

## <a name="data-manipulation-methods-that-do-not-raise-dataevents-or-missing-insert-update-delete-pre--and-post-data-events"></a>DataEvents または欠落している insert、update、delete プリおよびポストデータ イベントを生成しないデータ操作メソッド

一般なプラクティスとして、テーブルのデータ メソッドを使用して、アプリケーションの拡張に使用できるイベントを発生させます。 コード ベースは、必ずしもこのプラクティスに従っていませんでした。 たとえば、**doInsert**、**doUpdate**、および **doDelete** データ メソッドと特定のテーブルの実装では、データ メソッドで **super()** の呼び出しは行われませんでした。

タイプ クラスの **insert**、**update**、および **delete** メソッドはリファクターされました。 データ メソッドで **super()** が確実に呼び出されるように変更が行われました。 これらの変更により、これらのメソッドへの拡張機能の追加が可能になり、その結果、プリイベントとポストイベントが拡張機能で使用できるようになりました。 次の表に、**insert**、**update**、および **delete** イベントが拡張機能に対して有効になったテーブルを表示します。

| テーブル |
| -------------|
| InventBlocking|
| InventTransferLine|
| Kanban|
| KanbanJob|
| KanbanJobPickingList|
| MCRRoyaltyVendTable|
| PdsRebateTable|
| PmfProdCoBy|
| ProdBOM|
| ProdRoute|
| ProdTable|
| PurchLine|
| PurchRFQCaseLine|
| PurchRFQCaseTable|
| PurchRFQLine|
| PurchTable|
| SalesLine|
| SalesQuotationLine|
| SalesQuotationTable|
| SalesTable|
| TAMVendRebateTable|
| WMSOrder|
| WMSOrderTrans|

## <a name="exposing-class-members"></a>クラス メンバーの公開

アクセス修飾子または新しい parm メソッドの変更の結果、追加のプライベート メンバーをカスタマイズに使用できるようになりました。 コマンド チェーン プラットフォーム機能により、保護されたメソッドとメンバーへの拡張クラスのアクセスが有効になります。 コマンド チェーンの詳細については、「[拡張可能な X++: コマンド チェーン](https://blogs.msdn.microsoft.com/mfp/2017/07/04/extensible-x-chain-of-command/)」を参照してください。

| メンバー |
| -------------|
|AssetPost.ledgerJournalTrans|
|クラス DimensionDerivationRule.ledgerDimensionAllocationList|
|クラス PurchInvoiceJournalCreate.purchTable|
|クラス PurchTableType.purchTable|
|クラス SalesInvoiceJournalPost.salesLine|
|クラス SalesQuotationLineType|
|クラス SalesQuotationTableType|
|クラス VendorInvoiceLineSourceDocLineItem.purchLine|
|CustCreditLimit.balanceTotalsCalculated|
|CustCreditLimit_SalesTable.salesTable|
|フォーム LedgerJournalTransCustPaym.ledgerJournalEngine|
|PurchLineType.purchLine|
|PurchLineType.purchLine_orig|
|SalesLineType.salesLine|
|SalesLineType.salesLine_orig|
|SalesTableType.checkSalesQty|
|SalesTableType.SalesTable_orig|
|WHSControl.data|
|WHSLocationDirective.targetLicensePlateId|

## <a name="construct-methods-with-throw-statements"></a>throw ステートメントを使用した construct メソッド

特定の型の実装が欠落していた場合、いくつかの **construct** メソッドが **throw** ステートメントで実装されました。 これは拡張性に対してはうまく機能しません。この問題を軽減するため、例外をスローしないように、**construct** メソッドが変更されました。 以下のメソッドは、クラス拡張、またはポストイベント サブスクリプションによって、拡張性に対して使用できるようになりました。

| オブジェクト |
| -------------|
|BarcodeEAN128.string()|
|CustCreditLimit.Construct|
|FormLetterReport|
|JournalStatic|
|MarkupAllocation|
|PurchTable2LineField|
|SalesCalcTax|
|SalesEditLinesForm|
|SalesFormLetter|
|SalesFormLetterContract.newFromPackedVersion|
|SalesFormletterParmData.newData|
|SalesQuantity|
|SalesQuotationEditLinesForm.construct|
|SalesSummaryFields|
|SalesTable2LineField|
|VendInvoiceTableToLineUpdate|

## <a name="find-methods-with-throw-statements"></a>throw ステートメントを使用した find メソッド

特定の型の実装が欠落していた場合、いくつかの **find** メソッドが **throw** ステートメントで実装されました。 これは拡張性に対してはうまく機能しません。この問題を軽減するため、例外をスローしないように、**find** メソッドが変更されました。 以下のメソッドは、クラス拡張、またはポストイベント サブスクリプションによって、拡張性に対して使用できるようになりました。

| メソッド |
| -------------|
|JournalStatic.findJournalTableFromTrans|
|JournalStatic.findJournalTableId|

## <a name="methods-made-hookable"></a>フック可能なメソッド

パブリックでない一部のメソッドおよびフック可能でない一部のメソッドについて、拡張性サポートが強化されました。 以下のメソッドはフック可能な動作で明示的に修飾されています。

| メソッド |
| -------------|
|クラス CustVendReversePosting.updateCustVendTrans|
|クラス JournalTableData.construct|
|クラス PriceDisc.makeKey|
|クラス PurchInvoiceJournalCreate.initJournalHeader|
|クラス SalesInvoiceJournalPost.checkSourceLine|
|クラス SalesInvoiceJournalPost.postCustVend|
|フォーム LedgerTransVoucher.addDynaLink|
|ReqCalc.deleteItemRequirement|
|ReqCalc.initTransFromInventTrans|
|ReqCalcForecastItemTable.deleteRequirement|
|テーブル TmpCustVendTrans.createLineCreditLimit|
|テーブル TmpCustVendTrans.createLineCreditRemain|
|テーブル TmpCustVendTrans.createLineOrdered|
|テーブル TmpCustVendTrans.createLinePackingSlip|
|WHSLocationDirective.addRangeByTransType|
|WhsWorkCreate.createWorkLine|

## <a name="inline-delegates"></a>インライン デリゲート

インライン デリゲートを使用できるようになりました。 インライン デリゲートの最も一般的な使用方法は、メソッドをより粒度の細かいメソッドに分割して、より小規模なメソッドで拡張イベントを使用できるようにすることです。

|  メソッド |
| -------------|
|AxClass - ChequeDP - Method - insertChequeTmp|
|AxClass - VendInvoiceTableToLineUpdate - Method - convertPurchTableFieldToVendInvoice|
|クラス JournalStatic.findJournalTableFromTrans|
|クラス JournalStatic.findJournalTableId|
|クラス WhsLocationDirective.findLocationMultiSKU|
|EcoResReleasedProductVariantEntity.insertEntityDataSource|
|ForecastSales.ForecastSales_ds.updateForecastSalesFields|
|フォーム SalesTable - メソッド updateDesign|
|ReqTransPoMarkFirm.firmSelectedPlannedOrders|
|SalesLineType.insert|
|SalesLineType.update|
|SalesTable2LineUpdatePrompt.dialog|
|テーブル ExtCodeTable|
|テーブル InventItemGroup.getGroupForAccountType|
|テーブル InventItemGroup.ledgerDimensionDescription|
|テーブル InventTestAssociationTable|
|テーブル LedgerJournalName - メソッド validateWrite|
|テーブル PaymTerm - メソッド due|
|TaxCalculation.newForSourceType|
|TaxCalculation.newForSourceTypeWithTaxUncommitted|
|WHSLoadLine.getOrderCommonFromLoadLine|
|WhsLocationDirective.findLocation|
|WHSRFControlData.populateData|
|WHSRFControLData.processControl|
|WHSRFMenuItemTable.getWHSWorkExecuteMode|

## <a name="other-changes"></a>その他の変更

次の表に、拡張機能に対して行われた追加の変更を一覧表示します。


|                                                           変更                                                           |
|----------------------------------------------------------------------------------------------------------------------------|
|                                      既存の製品分析コードの間接参照の追加                                       |
|                                  クラス FormLetterParmDataOutputContract は拡張可能ではありません                                  |
|             1 つ以上の引数をサポートする SysExtensionFramework のインスタンス化戦略の作成             |
|                      カスタマイズ: TableField: 拡張モデル: テーブル フィールドの EDT タイプの変更                       |
|                          CustVendOpenTransBalances - initAccountNumCurrencies() switch ステートメント                           |
|                                     CustVendOpenTransBalances - new() switch ステートメント                                     |
|                                  CustVendOutPaym (クラス) には拡張性の改善が必要                                   |
|                        CustVendPaymReconciliationSetStatus (クラス) には拡張性の改善が必要                         |
|                                 CustVendSumForPaym (クラス) には拡張性の改善が必要                                 |
|                               SysGroup からの AddressCountyId と AddressStateId EDT の切り離し                               |
|                          ドキュメント管理イベントの処理には拡張性サポートの改善が必要                           |
|            為替レート プロバイダー フレームワークには、通貨モデルにカスタムの組み込みプロバイダーを配置することが必要             |
|                                                      GS-128 の拡張                                                      |
|                         拡張モデル: CountryRegionCodes プロパティでのカスタマイズを許可する。                          |
|                  フォーム拡張機能 - 新しいコントロールによって "拡張された" フォーム要素の拡張機能は動作しません                  |
|                                              InventDim: throw 付きの条件                                               |
|                                                  InventDimRenameDimValue                                                   |
|                メソッドのオーバーレイ - クラス VendInvoiceTableToLineUpdate.convertPurchTableFieldToVendInvoice                |
|                                     メソッドのオーバーレイ: クラス Markup - メソッド delete                                      |
|                       メソッドのオーバーレイ: クラス McrPriceHistoryForm.insertPotentialTradeAgreements                        |
|                             メソッドのオーバーレイ: クラス OffsetVoucher - メソッド markTransaction                              |
|                                 メソッドのオーバーレイ: フォーム LedgerJournalTransDimension.init                                 |
|                                 メソッドのオーバーレイ: フォーム LedgerTransVoucher - メソッド init                                 |
|                             メソッドのオーバーレイ: テーブル CustInvoiceTable - メソッド validateWrite                             |
|                       メソッド シグネチャが変更されました: RetailCreateLinesFromProductsToAdd.parmCallerCommon                        |
|                               メソッド シグネチャが変更になりました: WHSInvent.getCommonFromWorkTransType                               |
|                                  メソッド シグネチャが変更されました: WHSPoolProdBom.movementBuffer                                   |
|                          construct メソッドがありません: クラス SMAServiceOrderTableButtonStateProvider                           |
|                                         必要な番号順序スコープの拡張性                                         |
|                           Runbase には、クラスの拡張機能がメンバーをパック/アンパックする方法が必要                            |
|                                              文字列 EDT のサイズの拡張の問題                                              |
|                              カスタムの InventDim に基づく手持在庫フォームのオープンのサポート                              |
|          SysExtension フレームワーク: SysExtensionIInstantiationStrategy と SysExtensionIAttribute は互換性がありません          |
| 要求/応答シナリオで使用されるデリゲートがより堅牢になるために、EventHandlerResult のバリエーションが必要 |
|                                                WHS モバイル フレームワーク: 合格                                                |
|                                     WhsLocationDirectiveLine To/FromQty は拡張可能ではありません                                     |
|                                                 WHSMobileApp の拡張性                                                 |
|         WHSMobileAppAttachedImageDetails.removeLabelFromDimValue() は製品分析コードについて十分な汎用性がありません          |
|         WHSMobileAppAttachedImageDetails.removeLabelFromDimValue() は製品分析コードについて十分な汎用性がありません          |
|            WhsRFControlData.processControl は switch ブロック内の _data ではなく WhsControl.data を参照する必要があります             |

