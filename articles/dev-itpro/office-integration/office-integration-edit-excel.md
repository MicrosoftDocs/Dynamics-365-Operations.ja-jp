---
title: '[Excel で開く] エクスペリエンスの作成'
description: Excel と Word を Office エクスペリエンスで開く機能について学んで作成します。
author: ChrisGarty
manager: AnnBe
ms.date: 04/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 79223
ms.assetid: 05d8f7af-df6a-452f-a532-0f059eba4377
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c4ce8a671ba4b7035ff000a9d1a2cef33c00a2e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567457"
---
# <a name="create-open-in-excel-experiences"></a>[Excel で開く] エクスペリエンスの作成

[!include [banner](../includes/banner.md)]

Excel と Word を Office エクスペリエンスで開く機能について学んで作成します。

## <a name="what-are-open-in-excel-experiences"></a>[Excel で開く] エクスペリエンスとは

「Excel で開く」エクスペリエンスは：

-   エンティティと作成した OData サービスに基づいています。
-   動的に生成されるか、あらかじめ定義されたテンプレートに基づきます。
-   Excel アドインを使用して、編集および更新が可能です。

次の図は、**Excel アドイン** が仕訳入力に使用されている様子を示しています。

[![off101a](./media/off101a.png)](./media/off101a.png)

## <a name="where-are-the-open-in-excel-experiences"></a>[Excel で開く] エクスペリエンスが存在する場所は
Excel で開くエクスペリエンスは、通常Microsoft Office で開くメニューのExcel で開くセクションの下にありますが、これらのエクスペリエンスには明示的なボタンを追加することができます。

## <a name="whats-the-difference-between-export-to-excel-and-open-in-excel"></a>"Excel にエクスポート" と "Excel で開く" の違い
Excel にエクスポート オプションおよびエクスペリエンスは、どちらも Microsoft Office で開くメニューにあります。

-   Excel にエクスポート オプションは、グリッド データの静的エクスポートです。 それぞれ表示されているグリッドに対応しています。 現在のフィルター内にあるすべてのグリッド データはブックに格納されます。
-   [Excel で開く] エクスペリエンスは、Excel アドインを利用して更新と公開を行います。

次の図は、**フリート顧客**フォームの **Microsoft Office で開く**メニューをテンプレート **Excel で開く**オプション、生成された **Excel で開く**オプション、および静的な **Excel にエクスポート**オプションと共に示しています。

[![off101b](./media/off101b.png)](./media/off101b.png)

## <a name="when-will-an-entity-show-as-an-open-in-excel-option"></a>エンティティはいつ [Excel で開く] オプションとして表示されますか ?
エンティティにフォームと同じルート データ ソース (テーブル) が存在するとき、そのデータソースは、Microsoft Office で開くメニューの Excel で開くセクションのオプションとして追加されます。 これは、「生成済み」オプションと呼ばれます。

## <a name="what-fields-will-be-shown-in-the-workbook"></a>ブックに何というフィールドが表示されますか ?
ワークブックに追加される既定のフィールドは、エンティティのキー フィールドと必須フィールドです。 デフォルトで別のフィールドセットを提供する必要がある場合は、これらのフィールドをエンティティの**自動レポートのフィールド グループ**に追加できます。 次の図は、FMCustomerEntity の AutoReport フィールド グループの Visual Studio  ビューを示しています。

[![off101c](./media/off101c.png)](./media/off101c.png)

## <a name="what-fields-will-be-shown-when-an-entity-is-the-target-of-a-lookup"></a>エンティティが検索の対象のとき、何というフィールドが表示されますか ?
2 つのエンティティ間のリレーションシップが定義されると、1 つのエンティティの識別子が他のエンティティに表示されている場合、そのルックアップに表示されるフィールドは、キー フィールドであるか、または **AutoLookup フィールド グループ** が空でない場合はそのグループ内のフィールドです。 関係の参照は現在サポートされていませんが、最終的に列挙のルックアップを同様の方法でアプリに表示されます。 列挙ルックアップを持つ Excel アドインを次に示します。

[![off101d](./media/off101d.png)](./media/off101d.png)

## <a name="what-should-be-done-to-make-an-entity-ready-for-use-in-excel"></a>エンティティを Excel で使用できるようにするには何を行う必要がありますか ?
AutoReport および AutoLookup フィールド グループを定義し、Excel アプリ デザイン エクスペリエンスを使用してテストします。

## <a name="why-does-an-automatically-added-entity-option-have-unfiltered-after-the-entity-name"></a>自動的に追加されたエンティティ オプションでエンティティ名の後に「(フィルターなし)」と表示されるのはなぜですか。
現在、フィルターはこれらのオプションに追加されないため、「(フィルターなし)」という用語になります。 今後、フォームからこれらのオプションへのフィルターの適用が試行されます。 たとえば、顧客の一覧がカリフォルニア州で顧客だけにフィルター処理された場合、今後エンティティは州フィールドに対してスキャンされ、見つかるとフィルターは自動で追加されます。

## <a name="how-can-an-entity-be-added-as-an-open-in-excel-option-on-a-form-that-doesnt-share-the-same-root-datasource"></a>同じルート データソースを共有しないフォーム上で、Excel で開くオプションとしてエンティティを追加するにはどうしたらいいですか。
生成された Excel で開くオプションは、ExportToExcelIGeneratedCustomExport インターフェイスを実装することにより、任意のフォームに追加できます。 生成されたオプションをプログラムで追加するとき、一組のフィールドを明示的に指定できます。

## <a name="what-are-the-region-specific-considerations-for-defining-entities"></a>エンティティを定義するための地域固有の考慮事項
[Excel で開く] により生成されたエクスペリエンスは、AutoLookup グループに地域固有のフィールドを追加することで地域固有にできます。 これらの領域固有のフィールドは、生成されたワークブックに含まれます。

## <a name="how-can-i-create-a-custom-lookup-for-an-entity-field-in-excel"></a>Excel でのエンティティ フィールドに対してどのようにカスタム ルックアップを作成しますか。
カスタム ルックアップでは、エンティティ フィールドを表示できます。

-   名前 - メソッドには、「lookup\_&lt;フィールド名&gt;」の名前が必要です。例: フィールド「MyField」は、ルックアップ メソッド「lookup\_MyField」とすることができます。
-   属性 – 属性をメソッドに追加する必要があります。
    -   SysODataActionAttribute(str &lt;name&gt;, Boolean &lt;isInstanceMethod&gt;)
    -   SysODataCollectionAttribute(str &lt;name&gt;, Types &lt;type&gt;, “Value”)
-   戻り値: メソッドは、文字列のリストを返す必要があります。

例 :  

    public class ExportToExcel_SimpleEntity extends common
    {
        [SysODataActionAttribute("Lookup_StringLookupField", true),
        SysODataCollectionAttribute("return", Types::String, "Value")]
        public List lookup_StringLookupField()
        {
            List lookupList = new List(Types::String);
            const int items = 5;

            for (int item = 0; item < items; item++)
            {
                lookupList.addEnd(strfmt('%1 - %2 (%3)', this.StringField, this.IntField, item));
            }

            return lookupList;
        }
    }

## <a name="how-does-the-app-get-injected-into-a-workbook-to-start-building-a-template"></a>アプリはどのようにテンプレートの構築を開始するブックに挿入されますか。

Excel アドインは、生成された [Excel で開く] エクスペリエンスがトリガーされたとき、または **一般** &gt; **一般** &gt; **Office 統合** &gt; **Excel ブック デザイナー** フォームを使用してブックが作成されたときに、ブックに挿入されます。

-   **ブックの作成** ボタンは、選択したエンティティおよびフィールド、ポインターをサーバーに、アプリをブックに追加します。
-   **空白ブックの作成** ボタンは、ポインターをサーバーに、アプリをブックにそのまま追加します。
-   **ビュー関連** フォームは、Excel で加えられたデータの変更の影響をより簡単に確認するため、現在選択されているエンティティに関連するフォームに移動します。
-   **エンティティ レコード数を取得** ボタンは、現在選択されているエンティティのレコード数を表示します。 Excel アドインは、ユーザーのコンピューターのメモリ制限内の大量のデータを処理します。 既定の Excel アドインにはデータ サイズが 100 万個のセルに制限されるデータ 調整がありますが、ユーザーのマシンの性能に応じて通常 250 万個程度のセルに拡張できます。

次の図は、**Excel ブック デザイナー** フォームを示しています。

[![off101e](./media/off101e.png)](./media/off101e.png) 

Excel アドインを含むワークブックを取得すると、追加のデータソースは、**デザイン** ボタンを使用して追加することができます。 現在、データ ソースを削除することはできません。 次の図は、**デザイン** ボタンが強調表示された Excel アドインを示しています。

[![off101f](./media/off101f.png)](./media/off101f.png)

## <a name="when-will-a-template-show-as-an-open-in-excel-option"></a>テンプレートはいつ [Excel で開く] オプションとして表示されますか ?
**共通** &gt; **共通** &gt; **Office 統合** &gt; **ドキュメント テンプレート** フォーム (DocuTemplate) に表示されているテンプレートで、ShowInOpenInOfficeMenu が "はい" に設定されていて、ルート データ ソース (テーブル) が現在のフォームと同じとき、そのテンプレートは、Microsoft Office で開くメニューの Excel で開くセクションのオプションとして追加されます。 次の図は、**ドキュメント テンプレート** フォームを示しています。

[![off101g](./media/off101g.png)](./media/off101g.png)

## <a name="will-a-filter-be-added-to-the-template"></a>フィルターはテンプレートに追加されますか。
**ドキュメント テンプレート** フォームでは、「現在のレコード」の標準フィルターを有効または無効にします。 テンプレートが Excel で開くオプションとして呼び出されたときにフィルターがオンになっている場合、現在のレコードのフィルターがワークブックに追加されます。 フィルターはキー フィールドとその値になります。

## <a name="how-can-templates-be-defined-in-metadata-and-code-and-loaded-automatically"></a>テンプレートはどのようにメタデータとコードで定義されるおよび自動的に読み込まれますか。
**ドキュメント テンプレートの** フォームにテンプレートを追加するとき、それはそのインスタンスに追加され、「ユーザー定義」のテンプレートと呼ばれます。 テンプレートは、メタデータおよびコードで定義することもでき、自動的に読み込まれるため、「システム定義」のテンプレートになります。 メタデータとコードを使用してシステム定義のテンプレートを作成するには、以下を実行する必要があります。

-   テンプレートの定義。
-   プロジェクトに新しいリソースを作成します。
-   DocuTemplateRegistrationBase クラスを拡張する新しいクラスを定義し、registerTemplates メソッドの実装を追加します。

LedgerJournalLineEntryTemplateRegistration および FMTemplateRegistrations クラスは、コードで定義されたテンプレート登録の良い例です。 LedgerJournalLineEntryTemplate および FMTemplateCustomersWithLocations リソースは、リソースとしてメタデータに格納された対応するテンプレートです。 テンプレートに登録クラスが存在するとき、そのテンプレートは、**ドキュメント テンプレート** フォームの **システム テンプレートの再読み込み** ボタンがクリックされたときに読み込まれます。

## <a name="how-do-templates-get-loaded-into-a-fresh-deployment"></a>テンプレートはどのように新しい展開に読み込まれますか？
システム定義のテンプレートを読み込むには、次に示すように、**Common**&gt;**Common**&gt;**Office 統合**&gt;**ドキュメント テンプレート** フォームの **システム テンプレートを再読込み** ボタンをクリックします。

[![off101h](./media/off101h.png)](./media/off101h.png) 

今後、配置の際にそのボタンのクリックに相当する操作を実行します。

## <a name="how-do-i-decide-if-i-should-create-a-template"></a>テンプレートを作成する必要があるかどうかをどのように決定しますか。
テンプレートは、管理とバージョン管理する必要なコンポーネントです。 ユーザー エクスペリエンスを低下させることがなく、テンプレートを定義することを避けることができれば、おそらくテンプレートを使用する必要があります。 次の場合にテンプレートを作成します。

-   テンプレートに追加のコンテンツまたは書式が必要な場合。
-   同じブック内の複数のエンティティとデータ ソースを結合する必要があります。

テンプレートを作成しない場合:

-   テーブル バインドに表示するフィールドのセットを指定するだけです。

## <a name="what-are-the-region-specific-considerations-for-templates"></a>テンプレートのための地域固有の考慮事項
地域固有フィールドを持つエンティティのテンプレートを作成するとき、テンプレートからそれらの地域固有フィールドを除外する必要があります。そうしない場合、すべてのユーザーに地域固有フィールドが表示されます。 テンプレートは、ユーザーの大半に既定で提供される必要があり、地域に固有のユーザーは Excel アドインの使いやすいデザイン エクスペリエンスを使用してこれらのフィールドを追加できます。  必要に応じて、ユーザーはリージョン固有のフィールドと列を追加できます。 そのテンプレートは、1 人のユーザーが再利用するためにローカル コンピューターに保存するか、そのインスタンスの任意のユーザーが再利用するためにドキュメント テンプレートを通じてアップロードすることができます。 いくつかの他の考慮事項。

-   領域に領域固有のエンティティがある場合、領域固有のテンプレートを作成できます。
-   地域が十分に重要な場合は、地域固有テンプレートと地域汎用テンプレートを定義できます。

## <a name="how-do-i-add-an-explicit-button-for-a-template-open-in-excel-option"></a>テンプレート Excel を開くオプションに明示的なボタンを追加する方法がありますか。

Excel で開くエクスペリエンスに明示的なボタンを追加できます。 ボタンに表示されるラベルは、通常、「Excel で開くターゲット」である必要があります。ターゲットは、「明細行」や「カタログ」などのターゲット データの名前です。 そのようなボタンの背後にあるコードは次のようになります:

-   使用されるテンプレートを取得します。
-   フィルターを追加します。
-   テンプレートをユーザーに渡します。

このコードの例としては、**LedgerJournalTable** フォーム (**一般会計**&gt;**仕訳帳**&gt;**一般仕訳帳**) の**クリック済み**メソッド内の **OpenLinesInExcel** ボタン上で見つけることができます。

        [Control("Button")]
        class OpenLinesInExcel
        {
            /// <summary>
            /// Opens the current journal in Excel for line entry and editing
            /// </summary>
            public void clicked()
            {
                super();

                const str templateName = resourceStr(LedgerJournalLineEntryTemplate);
                DocuTemplate template = DocuTemplate::findTemplate(OfficeAppApplicationType::Excel, templateName);

                // Ensure the template was present
                if (template && template.TemplateID == templateName)
                {
                    Map filtersToApply = new Map(Types::String, Types::String);

                    // Create lines filter
                    ExportToExcelFilterBuilder filterBuilder = new ExportToExcelFilterBuilder(tablestr(LedgerJournalLineEntity));
                    str filterString = filterBuilder.areEqual(fieldstr(LedgerJournalLineEntity, JournalBatchNumber), LedgerJournalTable.JournalNum);
                    filtersToApply.insert(tablestr(LedgerJournalLineEntity), filterString);

                    // Create header filter
                    filterBuilder = new ExportToExcelFilterBuilder(tablestr(LedgerJournalHeaderEntity));
                    filterString = filterBuilder.areEqual(fieldstr(LedgerJournalHeaderEntity, JournalBatchNumber), LedgerJournalTable.JournalNum);
                    filtersToApply.insert(tablestr(LedgerJournalHeaderEntity), filterString);

                    // Generate the workbook using the template and filters
                    DocuTemplateRender renderer = new DocuTemplateRender();
                    str documentUrl = renderer.renderTemplateToStorage(template, filtersToApply);

                    // Pass the workbook to the user
                    if (documentUrl)
                    {
                        Browser b = new Browser();
                        b.navigate(documentUrl, false, false);
                    }
                    else
                    {
                        error(strFmt("@ApplicationFoundation:DocuTemplateGenerationFailed", templateName));
                    }
                }
                else
                {
                    warning(strFmt("@ApplicationFoundation:DocuTemplateNotFound", templateName));
                }
            }

        }

次の図は、**総勘定元帳** &gt; **仕訳帳** &gt; **一般仕訳帳** フォームを強調表示された **Excel で明細行を開く**ボタンと共に示しています。 
[![off101i](./media/off101i.png)](./media/off101i.png)

作成された Open in Excel オプションとテンプレートの Open in Excel オプションをプログラムで追加するには、ExportToExcelIGeneratedCustomExport および ExportToExcelITemplateCustomExport インターフェイスを実装して、Open in Excel オプションを追加します。 これにより、エンティティまたはテンプレートがルート データ ソースと同じテーブルを持たないフォームにオプションを追加できます。 この機能を使用する場合の例としてはデータソースのないフォーム、フォーム パーツのコレクションのみを含む可能性があります。 次の例では、**FMRental** フォームに、生成されたテンプレートと ExcelのOpen in Excel オプションをプログラムによって追加します。

    [Form]
    public class FMRental extends FormRun implements ExportToExcelIGeneratedCustomExport, ExportToExcelITemplateCustomExport
    {    
    ...
        public List getExportOptions()
        {
            List exportOptions = new List(Types::Class);

            ExportToExcelExportOption exportOption = ExportToExcelExportOption::construct(ExportToExcelExportType::CustomGenerated, int2str(1));
            exportOption.setDisplayNameWithDataEntity(tablestr(FMRentalEntity));
            exportOptions.addEnd(exportOption);

            ExportToExcelExportOption exportOption2 = ExportToExcelExportOption::construct(ExportToExcelExportType::CustomTemplate, int2str(2));
            exportOption2.displayName("Analyze rentals");
            exportOptions.addEnd(exportOption2);

            return exportOptions;
        }

        public ExportToExcelDataEntityContext getDataEntityContext(ExportToExcelExportOption _exportOption)
        {
            ExportToExcelDataEntityContext context = null;

            if (_exportOption.id() == int2str(1))
            {
                context = ExportToExcelDataEntityContext::construct(tablestr(FMRentalEntity), tablefieldgroupstr(FMRentalEntity, AutoReport));
            }

            return context;
        }

        public System.IO.Stream getTemplate(ExportToExcelExportOption _exportOption)
        {
            System.IO.Stream stream = null;

            if (_exportOption.id() == int2str(2))
            {
                stream = Microsoft.Dynamics.Ax.Xpp.MetadataSupport::GetResourceContentStream(resourcestr(FMRentalEditableExportTemplate));
            }

            return stream;
        }

        public void updateTemplateSettings(ExportToExcelExportOption _exportOption, Microsoft.Dynamics.Platform.Integration.Office.ExportToExcelHelper.SettingsEditor _settingsEditor)
        {
        }
    ...

## <a name="how-do-i-add-a-filter-for-a-programmatically-added-template-open-in-excel-option"></a>プログラムにより追加するテンプレート Excel を開くオプション用のフィルターを追加する方法がありますか。

Excel で開く オプション テンプレートは、ExportToExcelITemplateCustomExport インターフェイスを実装し、getTemplate メソッドでテンプレートを提供することで、プログラムにより追加できます。 このオプションのフィルターは、updateTemplateSettings メソッドの ExportToExcelFilterBuilder API を使用してプログラムで追加できます。

    public void updateTemplateSettings(ExportToExcelExportOption _exportOption, Microsoft.Dynamics.Platform.Integration.Office.ExportToExcelHelper.SettingsEditor _settingsEditor)

    {

    _settingsEditor.SetFilterExpression(tableStr(RetailTmpBulkProductAttributeValueEntity), element.getExportToExcelFilterExpression());

    DictDataEntity dictDataEntity = new DictDataEntity(tableNum(RetailTmpBulkProductAttributeValueEntity));

    _settingsEditor.SetFilterExpressionByPublicName(dictDataEntity.publicEntityName(), element.getExportToExcelFilterExpression());

    }

フィルターがプログラムで追加された後、結果のフィルターは、**フィルター** ボタンを使用して Excel アドインで表示できます。 次の図は、**フィルター** ボタンが強調表示された Excel アドインを示しています。

[![off101j](./media/off101j.png)](./media/off101j.png) 

次の図は、**フィルター** ダイアログ ボックスが強調表示された Excel アドインを示しています。

[![off101k](./media/off101k.png)](./media/off101k.png)

## <a name="how-do-i-enable-relationship-lookups-in-excel"></a>Excel でリレーションシップ ルックアップをどのように有効にしますか。
Excel データ コネクタでリレーションシップ ルックアップを有効にするには、次のメタデータが設定されていることを確認する必要があります。

- 関係で定義されているロールと関連データ エンティティ ロールは、ソースおよびターゲット エンティティの両方のすべての関係間で一意である必要があります。 これは、DimensionCombinationEntity など多くのリレーションシップを持つエンティティのリレーションシップにとって特に重要です。 予想されるルックアップが表示されない場合は、ロール名を次の形式に変更してみます。

   - **ロール**: \[このエンティティのパブリック名\] + \[ターゲット エンティティのパブリック名\] + \[ターゲット エンティティ フィールド\] + 「ソース」
   - **関連データ エンティティ ロール**: \[このエンティティのパブリック名\] + \[ターゲット エンティティのパブリック名\] + \[ターゲット エンティティ フィールド\] + 「ターゲット」

  - カーディナリティと関連データ エンティティ カーディナリティは、適切に設定する必要があります。
  -  少なくとも 1 つの制約がリレーションシップに追加される必要があます。 特殊なケースである、分析コード関係の例外により、制約されたプロパティは両方とも公開する必要があります。

## <a name="how-can-i-enable-users-to-create-new-header-records-as-well-as-lines-in-a-workbook"></a>ブック内の明細行と共に新しいヘッダー レコードを作成するユーザーをどのように有効にできますか。
ヘッダー レコードと関連行の作成を有効にするには、ヘッダー データソースを「フィールド」のセットとして追加し、行データ ソースを関連テーブルとして追加する必要があります。 このパターンは、仕訳入力などの文書データ入力シナリオでうまく機能します。

ヘッダー レコードと関連行の詳細については、「[Dynamics 365 for Finance and Operations でヘッダーと明細行のパターンの Excel テンプレートを作成する](https://youtu.be/RTicLb-6dbI)」ビデオをご覧ください。

ヘッダーの作成を有効にするヘッダー フィールドと行テーブルを含むブックを設計するには、次の手順を実行します。
1. Excel アドインで、**デザイン**をクリックしてデザイナーを開きます。 **フィールドを追加** を選択してヘッダー データ ソースを追加します。
2. 使用するヘッダー フィールドを選択します。 すべてのキー フィールドを含めるか、**新規**ボタンを有効にしないでください。
3. すべての文字列ヘッダー値フィールドでは、ドロップダウン メニューの形式で **Excel リボン > ホーム タブ > 番号グループ > 「数値」の設定**を使用するそのセルの「テキスト」形式を手動で適用します。 文字列フィールドにテキスト形式が手動で設定されておらず、"00045" のような先行ゼロの文字列値がある場合、Excel は自動的に "45" に変更し、*"PurchaseOrderHeader の PurchaseOrderNumber フィールドの値はキー フィールドであるため変更できません"* というようなエラーが表示されます。 現在、API を個々のセル (対応するテーブルの列) にテキスト形式を自動的に適用することはできません。
4. デザイナーのヘッダー データ ソースで、2 つのプラス アイコンで表された**関連するテーブルの追加**ボタンをクリックします。
5. 使用する行フィールドを選択します。

関連するテーブル データ ソースのヘッダー データ ソースの例を次に示します。
- PurchaseOrderHeader (フィールド)
   - dataAreaId
   - PurchaseOrderNumber
   - PurchaseOrderName
   - OrderVendorAccountNumber
- PurchaseOrderLine (テーブル - 関連)
   - LineNumber
   - ItemNumber
   - LineDescription
   - OrderedPurchaseQuantity
   - LineAmount

ヘッダーと明細行のブックを使用して、新しいヘッダーと明細行を作成するには、次の手順を実行します。
1. ブック内で、ヘッダーの値を持つセルにフォーカスを移動します。
2. Excel アドインで**新規**をクリックします。
3. 必要に応じて、値のヘッダーと明細行を入力します。
4. **公開**を選択します。

## <a name="how-can-fields-be-added-removed-or-moved-within-an-existing-template-workbook"></a>既存のテンプレート ブック内で、どのようにフィールドを追加、削除、または移動できますか。
**ドキュメント テンプレート**で保存されるワークブックを編集することによって、既存のテンプレート ワークブックにフィールドを追加することができます。

1. 元のテンプレート ブックを取得します。
   1. **ドキュメント テンプレート**フォームを開きます。
   2. 既存のテンプレート ワークブックを検索します。
   3. ブックをダウンロードします。
   4. ブックを開いて、Excel アドインが実行されるように編集を有効にします。
2. テンプレートに変更を加えます。 
   1. Excel アドインで**デザイン**を選択します。
   2. フィールドを追加するデータソースの横にある**編集**ボタン (鉛筆アイコン) をクリックします。
   3. **利用可能なフィールド** リストから**選択されたフィールド** リストに移動して、フィールドを追加します。 フィールドをダブルクリックすると移動します。 **選択したフィールド** ボックスの一覧から **使用可能なフィールド** ボックスの一覧にフィールドを移動して削除します。**上へ** および **下へ** ボタンを使ってフィールドを移動します。
   6. 変更が完了したら、**更新**を選択して、**はい**を選択して確定し、**完了**を選択してデザイナーを終了します (必要に応じて、**更新**を選択して、データが正しく入力されていることを確認します)。
   7. アップロードする前に**オプション** (ギア アイコン) をクリックし、**データ コネクタ** セクションを展開し、**バインディング データのクリア** ボタンをクリックしてテンプレートのデータを消去します
   8. **名前を付けて保存** を使用して、テンプレートを一時的にどこかに保存します。
3. 変更したテンプレートをアップロードします。
   1. **ドキュメント テンプレート** フォームに戻り、変更されたテンプレートをアップロードします。
   2.  **新規**をクリックして表示し、変更されたテンプレートを検索します。
   3. 保存されたテンプレート ファイルを選択してから、**開く** をクリックします。
   4. **テンプレートのアップロード** ダイアログ ボックスで、名前からアンダースコアと末尾のランダムな数字を削除します。たとえば「CustInvoiceJournalTemplate_636564840743000567」は、「CustInvoiceJournalTemplate」になります。
   5. 確認ダイアログボックスに「この名前のテンプレートが既に存在します ...」と表示されたら、**はい**をクリックして前のテンプレートの置換を確認します。 この確認が表示されない場合、テンプレート名が異なっており、新しいテンプレートとしてアップロードされていることに注意してください。
4. テンプレートが使用されるフォームを開いて、変更されたテンプレートを使用します。

## <a name="troubleshooting"></a>トラブルシューティング

予想されるルックアップを参照しない場合は、\[YourSiteURL\]/data/$metadata で利用できるメタデータ フィードを確認して、リレーションシップ メタデータを検証します。 エンティティのパブリック名の $metadat フィードを検索してその EntityType 要素を検索し、関係のロールの値と同じ名前を持つ子 NavigationProperty 要素があることを確認します。 ナビゲーション プロパティが存在する場合、Excel データ コネクターが使用され、関係の参照を表示します。 ルックアップは、次の条件下では表示されません。

  - エンティティのすべてのキー フィールドは関係の中に制約として含まれています。
  - 選択されたフィールドはキーであり、選択されたレコードは新規ではありません。
  - 認証されたユーザーには、ルックアップの対象となるエンティティにアクセスするためのアクセス許可がありません。

## <a name="how-do-dimensions-work"></a>分析コードはどのように機能しますか。
データ エンティティに分析コード メタデータを設定する最も簡単な方法は、データ エンティティ作成ウィザードを使用することで、これにより、分析コード フレームワークが必要とするものとまったく同じプライベート リレーションシップおよび公開表示値フィールドが自動的に作成されます。 分析コードの設定をカスタマイズする場合は、「[分析コードの概要](../financial/dimensions-overview.md)」を参照します。 ルックアップは非元帳分析コードに対してのみ自動的に生成されます。 カスタム分析コードは現在サポートされていません。 勘定分析コード (MainAccount、Department、CostCenter など) のルックアップを有効にする場合は、DimensionCombationEntity および DimensionSetEntity フィールドのリレーションシップの作成に関するガイダンスについては、「[分析コードの概要](../financial/dimensions-overview.md)」を参照します。 これらのリレーションシップが存在するときは、Excel データ コネクタに、リレーションシップ ルックアップが表示されます。 Excel Data Connector は、表示値を直接編集したり、別の列にある表示値の各属性を編集したりという、2 つのタイプの分析コード データ入力をサポートしています。 表示値の列と個々の属性の列の両方を連結した場合、両方を編集して、個別に公開できます。 表示値と個々の属性の両方を同じ行で編集した場合、個々の属性の変更は表示値の変更を上書きします。

## <a name="how-do-i-create-formula-table-columns"></a>フォーミュラ テーブル列をどのように作成しますか。
テーブルに式が必要な場合は、式の列を追加します。 テーブル バインドのフィールド選択ページで、[選択済のフィールド] リストの上にある **式** ボタンをクリックして、新しい式列を追加します。 式のラベルと値は、選択したフィールド リストのすぐ下のフィールドに入力されます。 新しい式の列を追加すると、値を空白のままにして、**更新**をクリックします。 フィールドがテーブルに追加されると、Excel の標準機能を使用して数式を作成し、数式をコピーして数式列の値フィールドに貼り付けます。 式を定義するときは、テーブルに複数の行が存在することを確認してください。そうでない場合、Excel が提供する式は、該当する行ではなく、すべての行を対象としている場合があります。 現在の行だけを指定するには、アット マーク (@) が必要です。 たとえば、すべての行に対する 4 つの列の合計「=SUM(Table1\[\[ColumnA\]:\[ColumnD\]\])」と現在の行の 4 つの列の合計「=SUM (Table1\[@\[ColumnA\]:\[ColumnD\]\])」。

## <a name="known-issues"></a>既知の問題
### <a name="refresh-doesnt-automatically-occur-in-old-templates"></a>更新は、以前のテンプレートでは自動的に行われません

「開くときの更新」を制御する機能が設定として追加されました。 これをデフォルトの動作に追加するには、既存のテンプレートとブックで、**Options** &gt; **Data Connector** &gt; **Refresh Options** にある **Refresh on open** チェック ボックスをオンにする必要があります。

### <a name="error-finding-entity"></a>エンティティ検索中のエラー

エンティティへの参照が、プライベート エンティティ名 (DataEntity.Name) からパブリック エンティティ名 (DataEntity.PublicEntityName) に変更されました。 エンティティのパブリックおよびプライベート名が異なっており、Excel テンプレートまたはブックで使用されている場合、「エラー検索エンティティ」というメッセージが Excel アプリに表示されます。 詳細: エンティティ "&lt;DataEntity.Name&gt;" は見つかりません"。

[![off101l](./media/off101l.png)](./media/off101l.png) 

これを解決するには、影響を受けるテンプレートのバインド情報を変更して、DataEntity.Name の代わりに DataEntity.PublicEntityName を指すようにします。

1.  置き換える必要のある DataEntity.Name については、DataEntity.PublicEntityName を決定し、たとえば FMCustomerEntity を FleetCustomer に置き換えます。
2.  影響を受けるテンプレートを検索します。
3.  テンプレートのファイル拡張子を .xlsx から .zip に変更します。
    [![off101m](./media/off101m.png)](./media/off101m.png)
4.  変更するファイルは、2015-05-25-FleetCustomersWithLocations.zipxlwebextensionswebextension2.xml など、xlwebextensions ディレクトリ内の webextension\*.xml ファイルのいずれかになります。
5.  ファイルを開き、適切な場所であることを確認します。
6.  FMCustomerEntity などの、DataEntity.Name を検索します。
    [![off101n](./media/off101n.png)](./media/off101n.png)
7.  ZIP ファイルを抽出します。
    [![off101o](./media/off101o.png)](./media/off101o.png)
8.  webextension xml ファイルを開きます。
9.  DataEntity.Name を対応する DataEntity.PublicEntityName に置き換えます。
10. webextension .xml ファイルの変更を保存します。
11. たとえば、古い zip ファイルの名前を変更し、名前に ".old" を追加します。
12. 以前に抽出したすべてのコンテンツの新しい ZIP ファイルを作成します。 これは通常、アーカイブ/zip フォルダ内のコンテンツを強調表示し、そのコンテンツを使用して zip フォルダを作成する必要があります。
    [![off101p](./media/off101p.png)](./media/off101p.png)
13. ZIP ファイルには ZIP ファイルのルートに \_rels"、"docProps"、および "xl" の各フォルダがあることを確認します。
14. 必要に応じて zip ファイルの名前を変更します。たとえば、ファイル 2015-05-25-FleetCustomersWithLocations.zip の名前を変更します。
15. zip ファイル拡張子を .xlsx に変更します。
16. 必要な場合は、ブック .xlsx ファイルを再発行します。
