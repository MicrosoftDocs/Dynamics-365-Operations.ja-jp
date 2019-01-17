---
title: "Dynamics 365 for Operations プラットフォーム更新プログラム 7 (2017 年 5 月) の新機能および変更された機能"
description: "このトピックでは、Dynamics 365 for Operations プラットフォーム更新プログラム 7 における新機能または変更された機能について説明します。 このバージョンは 2017 年 5 月にリリースされ、ビルド番号は 7.0.4542.16189 です。"
author: tonyafehr
manager: AnnBe
ms.date: 05/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 
ms.assetid: 54cfeac5-e977-4c02-8e7a-4ddb4b336713
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 
ms.dyn365.ops.version: Platform update 7
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: c9af66dcaac3ca8dd8830f09bcc95efff2e67805
ms.contentlocale: ja-jp
ms.lasthandoff: 12/18/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-operations-platform-update-7-may-2017"></a>Dynamics 365 for Operations プラットフォーム更新プログラム 7 (2017 年 5 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 for Operations プラットフォーム更新プログラム 7 における新機能または変更された機能について説明します。 このバージョンは 2017 年 5 月にリリースされ、ビルド番号は 7.0.4542.16189 です。

## <a name="configuration-data-projects"></a>コンフィギュレーション データ プロジェクト

コンフィギュレーション データ プロジェクトを使用して、構成データを簡単にエクスポートし、それを 1 つのインスタンスから別のインスタンスに移動できます。 この機能は、更新されたユーザー インターフェイスを提供し、またテンプレートとプロジェクトを簡単に管理する機能を提供します。 詳細については、[コンフィギュレーション データ プロジェクト](../../dev-itpro/data-entities/configuration-data-projects.md) を参照してください。

## <a name="static-export-to-excel-limit-increase-from-2k-to-10k"></a>Excel への静的エクスポートの制限が 2000 から10000 に増加

静的な Excel エクスポートの制限が 2 kから 10k に増加し、より多くの行がグリッドからエクスポートされるようになりました。 グリッド内のデータを表すエンティティがある場合、ハード行の制限がないため、Excel の Open と Excel Add-in を使用することをお勧めします。 さらに、エンティティが存在し、ユーザーに管理者特権がある場合、DIXF (データ管理) もオプションとなります。 詳細については、[Excel アドインの使用](../../dev-itpro/office-integration/use-excel-add-in.md) を参照してください。

## <a name="development-tooling--new-tabbed-workspace-pattern"></a>開発ツール - 新しいタブ付きワークスペース パターン

新しいタブ付きのワークスペース フォーム パターンを使用できるようになりました。 埋め込み Power BI レポートを格納するタブ ページを含めることができるようになりました。 この機能は、水平スクロールのワークスペースから遠ざかる方向への第一歩です。 詳細については、[ワークスペース フォーム パターン](../../dev-itpro/user-interface/workspace-form-pattern.md) を参照してください。

## <a name="development-and-customization--extending-a-group-control"></a>開発およびカスタマイズ - グループ コントロールを拡張する

Dynamics 365 for Operations 開発ツールおよびランタイム プラットフォームは、参照されたモデルで既に拡張されているフォームを拡張するなど、拡張済みフォームの拡張をサポートするようになりました。 グループ コントロールがフォーム拡張に属している場合、元々はフィールド/ボタン グループ コントロールを拡張できないという問題が修正されました。

## <a name="development-and-customization--extending-the-country-region-codes-property"></a>開発およびカスタマイズ - 国の地域コードのプロパティを拡張する

**国/地域コード** プロパティにより、開発者は現在の法人のプライマリ住所に基づく特定の地域や国に機能を制限できます。 **国地域コード** プロパティは、メニュー拡張、メニュー項目拡張、表拡張 (およびフィールド)、フォーム拡張 (フォーム制御)、EDT 拡張、列挙拡張、および表示拡張の各拡張要素タイプで編集できます。

開発者は、拡張機能で追加の国/地域のコードを指定できます。 要素に関連付けられた有効な国/地域は、ベースライン要素とそのすべての拡張機能からのすべてのコードの結合になります。

## <a name="development-and-customization--validating-events-on-form-data-sources-and-form-data-source-fields"></a>開発およびカスタマイズ - フォーム データ ソースとフォーム データ ソース フィールドのイベントの検証

フォーム データ ソース (FormDataSourceEventType) とフォーム データ ソース フィールド (FormDataFieldEventType) の検証イベントは、ユーザー指定の値の無効化をサポートするようになりました。 詳細については、[拡張機能を使用してモデル要素をカスタマイズする](../../dev-itpro/extensibility/customize-model-elements-extensions.md) を参照してください。

次の例は、この機能を示しています。 この例では、**abTable** という名前のデータソース、および **FieldInt1** という名前のフィールドを含む **MyForm** と言う名前のフォームを使用します。

```
public class abFormEvent
{
    /// <summary>
    /// Disallows inserting records on the form data source if the Field1 field contains the integer value 1
    /// </summary>

    [FormDataSourceEventHandler(formDataSourceStr(MyForm, abTable), FormDataSourceEventType::ValidatingWrite)]

    public static void abTable_OnValidatingWrite(FormDataSource sender, FormDataSourceEventArgs e)
    {
        var datasource = sender as FormDataSource;
        var args = e as FormDataSourceCancelEventArgs;
        if (args != null && datasource != null)
        {
            var record = datasource.cursor() as abTable;
            if (record.recId == 0)
            {
                if (record.FieldInt1 == 1)
                {
                    boolean doCancel = !checkFailed("Value 1 is not allowed");
                    args.cancel(doCancel);
                }
            }
        }
    }

    /// <summary>
    /// Disallow changing the Field1 value on the form data source field, if the Field1 value contains the integer value 10
    /// </summary>

    [FormDataFieldEventHandler(formDataFieldStr(MyForm, abTable, FieldInt1), FormDataFieldEventType::Validating)]

    public static void FieldInt1_OnValidating(FormDataObject sender, FormDataFieldEventArgs e)
    {
        var dataObject = sender as FormDataObject;
        var args = e as FormDataFieldCancelEventArgs;
        if (args != null && dataObject != null)
        {
            var datasource = dataObject.datasource() as FormDataSource;
            if (datasource != null)
            {
                var record = datasource.cursor() as abTable;
                if (record.RecId > 0)
                {
                    if (record.FieldInt1 == 10)
                    {
                        boolean doCancel = !checkFailed("FormDataFieldEventType::Validating: Value 10 is not allowed");
                        args.cancel(doCancel);
                    }
                }
            }
        }
    }
```

