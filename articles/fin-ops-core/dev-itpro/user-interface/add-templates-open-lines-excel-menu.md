---
title: '[Excel で明細行を開く] メニューへのテンプレートの追加'
description: このトピックでは、仕訳帳のページで利用できる [Excel] メニューの [Open] 行にテンプレートを表示させる方法について説明します。
author: aprilolson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 77432
ms.assetid: 9793bf54-cfb8-4ba1-bc8f-ba49ef37884a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf9e8fb6cd5ceaa22d8f5436bb5431d76d43ce2d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745723"
---
# <a name="add-templates-to-the-open-lines-in-excel-menu"></a><span data-ttu-id="84579-103">[Excel で明細行を開く] メニューへのテンプレートの追加</span><span class="sxs-lookup"><span data-stu-id="84579-103">Add templates to the Open lines in Excel menu</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84579-104">このトピックでは、仕訳帳のページで利用できる [Excel] メニューの [Open] 行にテンプレートを表示させる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="84579-104">This topic describes how you can promote a template to the Open lines in the Excel menu that is available on journal pages.</span></span>

<span data-ttu-id="84579-105">頻繁に使用される一部のテンプレートは、仕訳帳テンプレートです。</span><span class="sxs-lookup"><span data-stu-id="84579-105">Some of the most frequently used templates are the journal templates.</span></span> <span data-ttu-id="84579-106">これらの仕訳帳テンプレートの一部はプロモーションされたため、**Excel で明細行を開く** メニューに既定で表示されます。</span><span class="sxs-lookup"><span data-stu-id="84579-106">Some of these journal templates have been promoted so that they appear on the **Open lines in Excel** menu by default.</span></span> <span data-ttu-id="84579-107">しかし、システムに新しいテンプレートを追加するときに、既定では、**Office で開く** メニューで利用可能です。</span><span class="sxs-lookup"><span data-stu-id="84579-107">However, when you add a new template to the system, it's available on the **Open in Office** menu by default.</span></span> <span data-ttu-id="84579-108">テンプレートを **Excel で行を開く** メニューで利用できるようにするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="84579-108">To promote the template so that it's available on the **Open lines in Excel** menu, follow these steps.</span></span>

1.  <span data-ttu-id="84579-109">Microsoft Excel テンプレートを作成し、ローカルに保存します。</span><span class="sxs-lookup"><span data-stu-id="84579-109">Create a Microsoft Excel template, and save it locally.</span></span> <span data-ttu-id="84579-110">詳細については、「Excel で開くエクスペリエンスの作成」の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84579-110">For more information, see the "Create Open in Excel experiences" article.</span></span>

2.  <span data-ttu-id="84579-111">Microsoft Visual Studio で、ApplicationSuite モデルへの参照を含むモデルに新しいプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="84579-111">In Microsoft Visual Studio, create a new project for a model that has a reference to the ApplicationSuite model.</span></span> 

       <span data-ttu-id="84579-112">[![Visual Studio で新しいプロジェクトを作成する](./media/110-1024x523.png)](./media/110.png)</span><span class="sxs-lookup"><span data-stu-id="84579-112">[![Creating a new project in Visual Studio](./media/110-1024x523.png)](./media/110.png)</span></span>

3.  <span data-ttu-id="84579-113">新しいクラスを作成し、**LedgerIJournalExcelTemplate** インターフェイスを実装し、**DocuTemplateRegistrationBase** を拡張します。</span><span class="sxs-lookup"><span data-stu-id="84579-113">Create a new class, implement the **LedgerIJournalExcelTemplate** interface, and extend **DocuTemplateRegistrationBase**.</span></span> <span data-ttu-id="84579-114">実装 (仕訳帳タイプなどによってサポートされる) では、「Excel で開く」エクスペリエンスで、テンプレートをオプションとして使用できるコンテキストが定義されます。</span><span class="sxs-lookup"><span data-stu-id="84579-114">Your implementation (supported journal type, and so on) defines the context that your template will be available as an option for in the Open in Excel experience.</span></span> <span data-ttu-id="84579-115">この例では、LedgerJournalHeaderEntity と LedgerJournalLineEntity を使用していますが、これらのエンティティに限定されません。</span><span class="sxs-lookup"><span data-stu-id="84579-115">This example uses LedgerJournalHeaderEntity and LedgerJournalLineEntity, but you aren't limited to these entities.</span></span> <span data-ttu-id="84579-116">エンティティが仕訳帳ヘッダー/明細行のエンティティ パターンに従うという条件で、自分自身のエンティティを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="84579-116">You can define your own entities, provided that they entities follow the journal header/line entity pattern.</span></span> <span data-ttu-id="84579-117">**LedgerDailyJournalExcelTemplate** クラスからの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="84579-117">Here is an example from the **LedgerDailyJournalExcelTemplate** class.</span></span>

    ```xpp
    using Microsoft.Dynamics.Platform.Integration.Office;  
    public class TestNewTemplate extends DocuTemplateRegistrationBase implements LedgerIJournalExcelTemplate
    {
        private const DocuTemplateName ExcelTemplateName = resourceStr(TestNewTemplate);
        private const EntityName LineEntityName = tableStr(LedgerJournalLineEntity);
        private const FieldName LineEntityJournalNum = fieldStr(LedgerJournalLineEntity, JournalBatchNumber);
        private const FieldName LineEntityDataAreaId = fieldStr(LedgerJournalLineEntity, dataAreaId);
        private const FieldName HeaderEntityName = tableStr(LedgerJournalHeaderEntity);
        private const FieldName HeaderEntityJournalNum = fieldStr(LedgerJournalHeaderEntity, JournalBatchNumber);
        private const FieldName HeaderEntityDataAreaId = fieldStr(LedgerJournalHeaderEntity, dataAreaId);
        /// <summary>
        /// A boolean value which indicates whether the journal type is supported for the Excel template.
        /// </summary>
        /// <param name = "_ledgerJournalType">The ledger journal type.</param>
        /// <returns>True if the journal type is supported; otherwise, false.</returns>
        public boolean isJournalTypeSupported(LedgerJournalType _ledgerJournalType)
        {
            return _ledgerJournalType == LedgerJournalType::Daily;
        }
        /// <summary>
        /// Gets the document template name.
        /// </summary>
        /// <returns>The document template name</returns>
        public DocuTemplateName documentTemplateName()
        {
            return ExcelTemplateName;
        }
        /// <summary>
        /// Gets a collection of the supported account types for the entity.
        /// </summary>
        /// <returns>A collection of <c>LedgerJournalACType</c> values.</returns>
        public Set supportedAccountTypes()
        {
            Set accountTypeSet = new Set(Types::Integer);
            accountTypeSet.add(LedgerJournalACType::Ledger);
            return accountTypeSet;
        }
        /// <summary>
        /// Gets a collection of the supported offset account types for the entity.
        /// </summary>
        /// <returns>A collection of <c>LedgerJournalACType</c> values.</returns>
        public Set supportedOffsetAccountTypes()
        {
            Set offsetAccountTypeSet = new Set(Types::Integer);
            offsetAccountTypeSet.add(LedgerJournalACType::Ledger);
            return offsetAccountTypeSet;
        }
        /// <summary>
        /// Validates the journal is valid for the template.
        /// </summary>
        /// <param name = "_ledgerJournalTable">The <c>LedgerJournalTable</c> record.</param>
        /// <returns>True if the journal is valid for the template; otherwise, false.</returns>
        public boolean validateJournalForTemplate(LedgerJournalTable _ledgerJournalTable)
        {
            return LedgerJournalExcelTemplate::validateJournalForTemplate(_ledgerJournalTable, this);
        }
        public void registerTemplates()
        {
            this.addTemplate(
                OfficeAppApplicationType::Excel,
                ExcelTemplateName,
                ExcelTemplateName,
                'Test new template',
                'Test new template',
                NoYes::No,
                NoYes::No,
                NoYes::No);
        }
        /// <summary>
        /// The resource name of the header entity.
        /// </summary>
        /// <returns>The resource name of the header entity.</returns>
        public EntityName headerEntityName()
        {
            return HeaderEntityName;
        }
        /// <summary>
        /// The resource name of the line entity.
        /// </summary>
        /// <returns>The resource name of the line entity.</returns>
        public EntityName lineEntityName()
        {
            return LineEntityName;
        }
        /// <summary>
        /// The field name for the header journal batch number.
        /// </summary>
        /// <returns>The field name for the header journal batch number.</returns>
        public FieldName headerJournalBatchNumberFieldName()
        {
            return HeaderEntityJournalNum;
        }
        /// <summary>
        /// The field name for the header data area.
        /// </summary>
        /// <returns>The field name for the header data area.</returns>
        public FieldName headerDataAreaFieldName()
        {
            return HeaderEntityDataAreaId;
        }
        /// <summary>
        /// The field name for the line journal batch number.
        /// </summary>
        /// <returns>The field name for the line journal batch number.</returns>
        public FieldName lineJournalBatchNumberFieldName()
        {
            return LineEntityJournalNum;
        }
        /// <summary>
        /// The field name for the line data area.
        /// </summary>
        /// <returns>The field name for the line data area.</returns>
        public FieldName lineDataAreaFieldName()
        {
            return LineEntityDataAreaId;
        }
        /// <summary>
        /// Append additional filter to the default filtering behavior.
        /// </summary>
        /// <returns>The original filter with new filter(s) appended; Otherwise, the original filter</returns>
        public FilterCollectionNode appendHeaderEntityFilters(FilterCollectionNode _headerFilter, ExportToExcelFilterTreeBuilder _headerFilterBuilder)
        {
            return _headerFilter;
        }
        /// <summary>
        /// Append additional filter to the default filtering behavior.
        /// </summary>
        /// <returns>The original filter with new filter(s) appended; Otherwise, the original filter</returns>
        public FilterCollectionNode appendLineEntityFilters(FilterCollectionNode _lineFilter, ExportToExcelFilterTreeBuilder _lineFilterBuilder)
        {
            FilterCollectionNode lineFilter = _lineFilterBuilder.and(
                _lineFilterBuilder.areEqual(fieldStr(LedgerJournalLineEntity, AccountType), LedgerJournalACType::Ledger),
                _lineFilterBuilder.areEqual(fieldStr(LedgerJournalLineEntity, OffsetAccountType), LedgerJournalACType::Ledger));
            return _lineFilterBuilder.and(_lineFilter, lineFilter);
        }
    }
    ```

4.  <span data-ttu-id="84579-118">新しいリソースを含むプロジェクト/モデルを構築します。</span><span class="sxs-lookup"><span data-stu-id="84579-118">Build the project/model that has the new resources.</span></span> <span data-ttu-id="84579-119">新しいリソース 1 つと、新しいクラス 1 つが必要です。</span><span class="sxs-lookup"><span data-stu-id="84579-119">You should have one new resource and one new class.</span></span> 

       <span data-ttu-id="84579-120">[![構築されたプロジェクト](./media/22.png)](./media/22.png)</span><span class="sxs-lookup"><span data-stu-id="84579-120">[![Built project](./media/22.png)](./media/22.png)</span></span>

5.  <span data-ttu-id="84579-121">クライアントで、**共通** &gt; **共通** &gt; **Office 統合** &gt; **ドキュメント テンプレート** &gt; **システム テンプレートの再読み込み** と移動します。</span><span class="sxs-lookup"><span data-stu-id="84579-121">In the client, go to **Common** &gt; **Common** &gt; **Office integration** &gt; **Document templates** &gt; **Reload system templates**.</span></span> <span data-ttu-id="84579-122">一覧に新しいテンプレートが表示され、そのテンプレートを仕訳帳ページに追加した場合、そのテンプレートは **Excel で明細行を開く** メニューにも表示されます。</span><span class="sxs-lookup"><span data-stu-id="84579-122">You will see the new template in the list, and if you open the journal page that you added the template to, you will also see that template on the **Open lines in Excel** menu.</span></span>


<a name="additional-resources"></a><span data-ttu-id="84579-123">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="84579-123">Additional resources</span></span>
--------

<span data-ttu-id="84579-124">[[Excel で開く] エクスペリエンスの作成](../office-integration/office-integration-edit-excel.md)</span><span class="sxs-lookup"><span data-stu-id="84579-124">[Create Open in Excel experiences](../office-integration/office-integration-edit-excel.md)</span></span>





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]