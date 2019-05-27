---
title: '[Microsoft Office で開く] メニューのカスタマイズ'
description: ほとんどのページには、Microsoft Office で開くメニューが含まれます。 このトピックでは、[Open in Office] メニューについての情報を提供し、オプションの追加、削除、変更によってカスタマイズする方法について説明します。
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270774
ms.assetid: 3ff1184b-1a8a-4102-9600-f1776634d95f
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: c6d3f9da66bba534cf666ef8dcb58467b0b45668
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537145"
---
# <a name="customize-the-open-in-microsoft-office-menu"></a>Microsoft Office で開くメニューのカスタマイズ

[!include [banner](../includes/banner.md)]

ほとんどのページには、Microsoft Office で開くメニューが含まれます。 このトピックでは、[Open in Office] メニューについての情報を提供し、オプションの追加、削除、変更によってカスタマイズする方法について説明します。

<a name="overview"></a>概要
--------

**Microsoft Office で開く**メニュー ボタン (**Office で開く**メニュー) は、ページに表示されるシステム定義ボタンです。 **Office で開く**メニューには、Microsoft Excel や Microsoft Word などのさまざまな Office 製品にデータをエクスポートできるようにするためのメニュー項目が含まれています。 次のテーブルは、**Office で開く** メニューのメニュー項目について説明しています。

| メニュー項目       | 説明                                                                                                                                                                                                                                                  |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Excel にエクスポート | データは Excel ワークブックにエクスポートされます。 このブックには Microsoft Dynamics 365 for Finance and Operations への逆参照が含まれていないため、データを更新することはできません。                                                                                               |
| Word にエクスポート  | データは Word 文書にエクスポートされます。 このドキュメントには、Finance and Operations の参照が含まれていないため、データを更新することはできません。                                                                                                           |
| Excel で開く   | Microsoft Dynamics Office アドインを含むブックが作成されます。 ワークブックには Finance and Operations の参照が含まれており、アドインでホストされているデータ コネクタからデータをリフレッシュ、更新、公開することができます。 |

## <a name="how-menu-items-are-added-to-the-open-in-office-menu"></a>Office で開くメニューに、どのようにメニュー項目が追加されますか。
エクスポート オプションは、次の方法で **Office で開く** メニューに追加されます。

1.  **Excel にエクスポート** グループで、メニュー項目が表示されている各グリッドに追加されます。
2.  ページのルート データ ソースごとに、同じルート データ ソースを持つ一連のデータ エンティティが決定されます。 これらの各データ エンティティについては、以下のメニュー項目が追加されます。
    -   **Excel で開く**グループで、メニュー項目がデータ エンティティの既定のエクスポートに追加されます。
    -   **Excel で開く**グループで、メニュー項目が同じルート データ エンティティを持つ **Excel** タイプのドキュメント テンプレート レコードごとに追加され、**Office で開く**メニューに含めるようマークされます。
    -   **Word にエクスポート** グループで、メニュー項目が同じルート データ エンティティを持つ **Word** タイプのドキュメント テンプレート レコードごとに追加され、**Office で開く**メニューに含めるようマークされます。

## <a name="default-exports"></a>既定のエクスポート
**Office で開く** メニューは、各データ エンティティの既定のエクスポートを提供します。 このエクスポートには、データ エンティティの **AutoReport** グループのすべてのフィールドが含まれます。 **SaveDataPerCompany**が**はい**に設定されている場合、現在の会社へのデータを制限するようフィルターが適用されます。

## <a name="document-templates"></a>ドキュメント テンプレート
ドキュメント テンプレートは、**ドキュメント テンプレート**ページから追加できます。 各ドキュメント テンプレート レコードに関連付けられているいくつかのフィールドは、**Office で開く** メニューでのそのテンプレートの動作を制御します。

| フィールド                | 説明                                                                                                                                                         |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ルート データ エンティティ     | テンプレートのルート データ エンティティ。 ルート データ エンティティは、テンプレートが含まれるページを決定するために使用されます。                                        |
| Office メニューのリスト  | このフィールドが選択されている場合に、テンプレートは該当するページの **Office で開く**メニューに含まれます。 (該当するページは、ルート データ エンティティによって異なります。) |
| レコード フィルターの適用  | このフィールドが選択されている場合、そのページで現在選択されているレコードをベースにデータがフィルター処理されます。                                                   |
| 会社フィルターの適用 | このフィールドが選択されている場合、現在の会社をベースにデータがフィルター処理されます。                                                                                 |

### <a name="trimmed-template-columns-and-fields"></a>トリミングされたテンプレートの列とフィールド

**Office で開く**メニューに含まれる Excel テンプレートで、列およびフィールドは、システムおよび該当する国/地域コンテキストに適用されているコンフィギュレーション キーに基づいて、ワークブックからトリミングされます。 コンフィギュレーション キーがブック内の列またはフィールドに関連付けられている場合は、コンフィギュレーション キーが無効になっている場合は、列またはフィールドが削除されます。 国/地域コードのセットがブックの列またはフィールドに関連付けられている場合、その国/地域コードが有効範囲にない場合は、列またはフィールドが削除されます。

## <a name="open-in-office-menu-customization"></a>「Office で開く」メニューのカスタマイズ
特定のページの **Office で開** メニューに表示されるコンテンツをカスタマイズする方法はいくつかあります。 たとえば、モデル要素およびコード属性のメタデータ プロパティを通じて、静的にコンテンツをカスタマイズできます。 ただし、コード経由のカスタマイズによりコントロールの最高レベルを提供します。 コードでは、ページに 1 つまたは複数のインターフェイスを実装するか、拡張機能およびイベント サブスクリプションを使用できます。 次のセクションでは、最も頻繁に使用されるカスタマイズ シナリオについて説明します。

### <a name="modifying-the-open-in-office-menu-through-interfaces"></a>インターフェイスを通じた Office で開くメニューの変更

自分の所有するページを変更する必要がある場合、のページのすべてのプライベート メンバーへのアクセス権を付与し、より深いカスタマイズが可能になるため、インターフェイスは最適なカスタマイズ方法となります。 以下のインターフェイスをページのコードに適用することができます。

| インターフェイス                              | 説明                                                                                                    |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------|
| OfficeIMenuCustomizer                  | ページと見なされるデータ エンティティのセットを変更し、カスタムのメニュー項目を追加するには、このインターフェイスを使用します。 |
| OfficeIGeneratedWorkbookCustomExporter | 実行時に生成されるブックのカスタム エクスポートを行うには、このインターフェイスを使用します。                          |
| OfficeITemplateCustomExporter          | ドキュメント テンプレートのレコードに基づくカスタムのエクスポートを行うには、このインターフェイスを使用します。                          |

### <a name="modifying-the-open-in-office-menu-through-extensions-and-event-subscriptions"></a>拡張機能とイベント サブスクリプションを通じた Office で開くメニューの変更

所有していないページを変更する必要がある場合、オーバーレイが必要となるため、インターフェイスの使用を避ける必要があります。 代わりに、拡張機能およびイベント サブスクリプションを通じてカスタマイズを行う必要があります。 この方法を使用するには、カスタマイズするページの **OnIntializing** イベントにサブスクライブする拡張クラスを実装します。 このイベント ハンドラーから、ページの **OfficeFormRunHelper** を取得し、その **OfficeMenuInitializing** イベントにサブスクライブします。 次の例は、この方法のサンプル コードを示しています。

    public static class MyForm_Extension
    {
        [FormEventHandler(formStr(MyForm), FormEventType::Initializing)]
        public static void ExportToExcel_DataEntityCustom_OnInitializing(xFormRun sender, FormEventArgs e)
        {
            FormRun formRun = sender as FormRun;
            if (formRun)
            {
                OfficeFormRunHelper officeHelper = formRun.officeHelper();
                if (officeHelper)
                {
                    officeHelper.OfficeMenuInitializing += eventhandler(MyForm_Extension::officeMenuInitializingHandler);
                }
            }
        }
        private static void officeMenuInitializingHandler(FormRun _formRun, OfficeMenuEventArgs _eventArgs)
        {
            // Modify the OfficeMenuOptions available on the OfficeMenuEventArgs.menuOptions() as necessary.
        }
    }

## <a name="typical-customization-scenarios"></a>一般的なカスタマイズ シナリオ
次の例では、**\_menuOptions** 変数に、カスタマイズしている **OfficeMenuOptions** インスタンスが含まれていると想定しています。

### <a name="modifying-the-set-of-data-entities-that-is-considered-for-a-page"></a>ページで考慮されるデータ エンティティのセットの変更

**Office で開く**メニューにあるメニュー項目の多くは、ページとみなされるデータ エンティティに基づいて自動的に追加されます。 ただし、場合によっては、データ エンティティのセットを特定するために使用されるアルゴリズムが、正しいセットを特定しない可能性があります。 ページと見なされるデータ エンティティのセットを変更するには、**OfficeIMenuCustomizer.customizeMenuOptions** メソッドまたは **OfficeFormRunHelper.OfficeMenuInitializing** デリゲートから利用可能な **OfficeMenuOptions** を使用します。

    // Add an entity to the list
    OfficeMenuDataEntityOptions entityOptions  = OfficeMenuDataEntityOptions::construct(tableStr(MyEntity));
    _menuOptions.dataEntityOptions().addEnd(entityOptions);
    // Remove an entity from the list
    ListIterator dataEntityOptionsIterator = new ListIterator(_menuOptions.dataEntityOptions());
    while (dataEntityOptionsIterator.more())
    {
        OfficeMenuDataEntityOptions dataEntityOptions = dataEntityOptionsIterator.value();
        if (dataEntityOptions.dataEntityName() == tableStr(MyOtherEntity))
        {
            dataEntityOptionsIterator.delete();
        }
        else
        {
            dataEntityOptionsIterator.next();
        }
    }

### <a name="specifying-the-default-data-entityrelated-options-that-are-included"></a>含まれている既定のデータ エンティティ関連のオプションを指定します。

**OfficeMenuDataEntityOptions** クラスを使用すると、既定のエクスポートのためのメニュー項目またはドキュメント テンプレートに関連するメニュー項目を含めるかどうかを指定できます。

    // Find the entity options if they were included by default.
    OfficeMenuDataEntityOptions entityOptions = _menuOptions.getOptionsForEntity(tableStr(MyEntity));
    if (!entityOptions)
    {
        // The entity options were not included. Add them.
        entityOptions = OfficeMenuDataEntityOptions::construct(tableStr(MyEntity);
        _menuOptions.dataEntityOptions().addEnd(entityOptions);
    }
    entityOptions.includeDefault(false); // Don't include the default export menu item.
    entityOptions.includeTemplates(false); // Don’t include Document Template related menu items.

### <a name="adding-a-custom-export-menu-item--generating-a-workbook"></a>カスタム エクスポート メニュー項目の追加 – ブックの生成

明示的にメニュー項目を追加するには、それを **OfficeMenuOptions.customMenuItems()** リストに追加する必要があります。 実行時に生成されるブックに対応するメニュー項目を追加するには、**OfficeGeneratedExportMenuItem** を使用します。

    OfficeGeneratedExportMenuItem menuItem = OfficeGeneratedExportMenuItem::construct(tableStr(MyEntity), "MyCustomGeneratedExportId");
    menuItem.setDisplayNameWithDataEntity();
    _menuOptions.customMenuItems().addEnd(menuItem);

実際にエクスポートする内容を定義するには、**ExportToExcelDataEntityContext** を使用します。 **ExportToExcelDataEntityContext** を指定するメソッドは、インターフェイスまたは拡張機能とイベント サブスクリプションを使用して、**Office で開く** メニューをカスタマイズするかどうかによって異なります。

#### <a name="using-interfaces"></a>インターフェイスの使用

インターフェイスを使用している場合、**OfficeIGeneratedWorkbookCustomExporter.getDataEntityContext()** メソッドを実装する必要があります。

    public ExportToExcelDataEntityContext getDataEntityContext(OfficeGeneratedExportMenuItem _menuItem)
    {
        ExportToExcelDataEntityContext context = null;
        if (_menuItem.id() == "MyCustomGeneratedExportId")
        {
            context = ExportToExcelDataEntityContext::construct(tableStr(MyEntity), tableFieldGroupStr(MyEntity, MyFieldGroup);
        }
        return context;
    }

#### <a name="using-extensions-and-event-subscriptions"></a>拡張機能とイベント サブスクリプションの使用

拡張機能とイベント サブスクリプションを使用している場合、**OfficeGeneratedExportMenuItem.getDataEntityContext** デリゲートはメニュー項目を **OfficeMenuOptions.customMenuItems()** リストに追加する前にサブスクライブする必要があります。 イベント ハンドラーのコードは、インターフェイスの先行するコードと同様である必要があります。 次の例は、イベント サブスクリプションの実行方法を示しています。

    menuItem.getDataEntityContext += eventhandler(MyForm_Extension::getDataEntityContextHandler);

### <a name="adding-a-custom-export-menu-item--specifying-a-document-template"></a>カスタム エクスポート メニュー項目の追加 – ドキュメント テンプレートの指定

明示的にメニュー項目を追加するには、それを **OfficeMenuOptions.customMenuItems()** リストに追加する必要があります。 ドキュメント テンプレート レコードに対応するメニュー項目を追加するには、**OfficeTemplateExportMenuItem** を使用します。

    OfficeTemplateExportMenuItem menuItem = OfficeTemplateExportMenuItem::construct(OfficeAppApplicationType::Excel, "MyTemplateId", "MyCustomTemplateExportId");
    _menuOptions.customMenuItems().addEnd(menuItem);

実行時にテンプレートを変更するには、一連の初期フィルターを指定します。 これらのフィルターは、指定されたデータ エンティティのテンプレート内のフィルターを置き換えます。 また、**WorkbookSettingsManager** を使用してフィルターを変更し、多くの設定を指定できます。 次のセクションに例を示します。

#### <a name="using-interfaces"></a>インターフェイスの使用

インターフェイスを使用している場合、**OfficeITemplateCustomExporter.getInitialTemplateFilters()** および **OfficeITemplateCustomExporter.updateTemplateSettings()** メソッドを実装する必要があります。

    public Map getInitialTemplateFilters(OfficeTemplateExportMenuItem _menuItem)
    {
        Map initialFilters = new Map(Types::String, Types::Class);
        if (_menuItem.id() == "MyCustomTemplateExportId")
        {
            // Add an initial filter.
            ExportToExcelFilterTreeBuilder bldr = new ExportToExcelFilterTreeBuilder(_menuItem.dataEntityName());
            FilterNode filter = // create the filter…
            initialFilters.insert(_menuItem.dataEntityName(), filter);
        }
        return initialFilters;
    }
    public void updateTemplateSettings(OfficeTemplateExportMenuItem _menuItem, Microsoft.Dynamics.Platform.Integration.Office.SettingsManager _settingsManager)
    {
        if (_menuItem.id() == "MyCustomTemplateExportId")
        {
            // Set a new filter.
            ExportToExcelFilterTreeBuilder bldr = new ExportToExcelFilterTreeBuilder(_menuItem.dataEntityName());
            FilterNode filter = // create the filter…
            Excel.WorkbookSettingsManager workbookSettingsManager = _settingsManager as Excel.WorkbookSettingsManager;
            workbookSettingsManager.SetEntityFilter(entityMetadata.PublicEntityName, filter);
            // Adjust settings.
            DataConnectorAppletSettings settings = settingsManager.DataConnectorSettings;
            DataConnectorAppletUserOptions options = settings.DataOptions;
            options.RefreshOnOpen = true;
            options.EnableDesign = false;
            workbookSettingsManager.DataConnectorSettings = settings;
        }
    }

#### <a name="using-extensions-and-event-subscriptions"></a>拡張機能とイベント サブスクリプションの使用

拡張機能とイベント サブスクリプションを使用している場合、**OfficeTemplateExportMenuItem.getInitialTemplateFilters** および **OfficeTemplateExportMenuItem.updateTemplateSettings** デリゲートはメニュー項目を **OfficeMenuOptions.customMenuItems()** リストに追加する前にサブスクライブする必要があります。 イベント ハンドラーのコードは、インターフェイスの先行するコードと同様である必要があります。 次の例は、イベント サブスクリプションの実行方法を示しています。

    menuItem.getInitialTemplateFilters += eventhandler(MyForm_Extension::getInitialTemplateFiltersHander);
    menuItem.updateTemplateSettings += eventhandler(MyForm_Extension::updateTemplateSettingsHandler);

## <a name="additional-customizations"></a>追加のカスタマイズ
次のカスタマイズを使用すると、インターフェイス、拡張機能、およびイベント ハンドラーを使用せずに、**Office で開く** メニューの内容を変更できます。

### <a name="removing-an-export-to-excel-menu-item-for-a-grid"></a>グリッドの [Excel にエクスポート] メニュー項目を削除

**Office で開く**メニューで、**Excel にエクスポート**グループには、表示されている各グリッドのメニュー項目が含まれます。 **Office で開く** メニューからグリッドを削除するには、グリッドの **ExportAllowed** メタデータ プロパティを **いいえ** に設定します。 この変更を行なった後、ユーザーはグリッドのショートカット メニューを使用してグリッドをエクスポートすることはできません。

### <a name="renaming-an-export-to-excel-menu-item-for-a-grid"></a>グリッドの [Excel にエクスポート] メニュー項目を名前変更

グリッドに関連する **Excelにエクスポート** メニュー項目の名前を変更するには、グリッドの **ExportLabel** メタデータ プロパティを適切なラベルに設定します。

### <a name="removing-all-menu-items-for-a-data-entity-from-all-pages"></a>すべてのページからデータ エンティティのすべてのメニュー項目を削除

統合シナリオでは、一部のデータ エンティティを OData サービス経由で公開して使用できるようにする必要があります。 ただし、既定で **Office で開く**メニューでこれらのデータ エンティティが表示されるのは、常に適切とは言えません。 このシナリオでは、**OfficeMenuOmit** コード属性をエンティティ申告に追加できます。

    [OfficeMenuOmit]
    public class MyEntity extends common
    {
        // Entity code…
    }

この変更を行なった後、既定では、エンティティは一致するルート データ ソースのページを持つ **Office で開く**メニューには表示されません。 ただし、エンティティが特定のページに追加される必要がある場合、それを追加するのにその他のカスタマイズ メカニズムを使用できます。

### <a name="adding-a-menu-item-button-to-a-page-that-corresponds-to-an-open-in-office-menu-entry"></a>Office メニュー エントリの開くに対応するページへのメニュー項目ボタンの追加

ページのアクション ウィンドウに、**Office で開く** メニューのカスタム メニュー項目に対応するメニュー項目ボタンを配置するのが適切なことがあります。 この場合、次のプロパティを持つメニュー項目ボタンをモデル化できます。

-   **メニュー項目タイプ:** **アクション**
-   **メニュー項目名:** **ExportToExcelExportForm**
-   **パラメーター:** メニュー項目の ID

その後、このメニュー項目ボタンをマウスでクリックすると、**Office で開く** メニューの対応するメニュー項目をマウスでクリックしたのと同じになります。



