---
title: Dynamics 365 for Operations プラットフォーム更新プログラム 7 (2017 年 5 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Operations プラットフォーム更新プログラム 7 の新機能または変更された機能について説明します。 このバージョンは 2017 年 5 月にリリースされ、ビルド番号は 7.0.4542.16189 です。
author: tonyafehr
manager: AnnBe
ms.date: 05/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: ''
ms.assetid: 54cfeac5-e977-4c02-8e7a-4ddb4b336713
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: ''
ms.dyn365.ops.version: Platform update 7
ms.openlocfilehash: c9af66dcaac3ca8dd8830f09bcc95efff2e67805
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369891"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-operations-platform-update-7-may-2017"></a><span data-ttu-id="4383b-104">Dynamics 365 for Operations プラットフォーム更新プログラム 7 (2017 年 5 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="4383b-104">What's new or changed in Dynamics 365 for Operations platform update 7 (May 2017)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4383b-105">このトピックでは、Dynamics 365 for Operations プラットフォーム更新プログラム 7 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="4383b-105">This topic describes features that are either new or changed in Dynamics 365 for Operations platform update 7.</span></span> <span data-ttu-id="4383b-106">このバージョンは 2017 年 5 月にリリースされ、ビルド番号は 7.0.4542.16189 です。</span><span class="sxs-lookup"><span data-stu-id="4383b-106">This version was released in May 2017 and has a build number of 7.0.4542.16189.</span></span>

## <a name="configuration-data-projects"></a><span data-ttu-id="4383b-107">コンフィギュレーション データ プロジェクト</span><span class="sxs-lookup"><span data-stu-id="4383b-107">Configuration data projects</span></span>

<span data-ttu-id="4383b-108">コンフィギュレーション データ プロジェクトを使用して、構成データを簡単にエクスポートし、それを 1 つのインスタンスから別のインスタンスに移動できます。</span><span class="sxs-lookup"><span data-stu-id="4383b-108">Using a configuration data project, you can easily export configuration data and move it from one instance to another instance.</span></span> <span data-ttu-id="4383b-109">この機能は、更新されたユーザー インターフェイスを提供し、またテンプレートとプロジェクトを簡単に管理する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="4383b-109">This feature provides an updated user interface, and the ability to easily manage templates and projects.</span></span> <span data-ttu-id="4383b-110">詳細については、[コンフィギュレーション データ プロジェクト](../../dev-itpro/data-entities/configuration-data-projects.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4383b-110">For more details, refer to [Configuration data projects](../../dev-itpro/data-entities/configuration-data-projects.md).</span></span>

## <a name="static-export-to-excel-limit-increase-from-2k-to-10k"></a><span data-ttu-id="4383b-111">Excel への静的エクスポートの制限が 2000 から10000 に増加</span><span class="sxs-lookup"><span data-stu-id="4383b-111">Static export to Excel limit increase from 2k to 10k</span></span>

<span data-ttu-id="4383b-112">静的な Excel エクスポートの制限が 2 kから 10k に増加し、より多くの行がグリッドからエクスポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4383b-112">The static Export to Excel limit has been increased from 2k to 10k to allow more rows to be exported from a grid.</span></span> <span data-ttu-id="4383b-113">グリッド内のデータを表すエンティティがある場合、ハード行の制限がないため、Excel の Open と Excel Add-in を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4383b-113">If there is an entity representing the data in the grid we recommended that you use Open in Excel and the Excel Add-in instead, since there is no hard row limit.</span></span> <span data-ttu-id="4383b-114">さらに、エンティティが存在し、ユーザーに管理者特権がある場合、DIXF (データ管理) もオプションとなります。</span><span class="sxs-lookup"><span data-stu-id="4383b-114">In addition, if there is an entity and the user has admin privileges then DIXF (data management) is also an option.</span></span> <span data-ttu-id="4383b-115">詳細については、[Excel アドインの使用](../../dev-itpro/office-integration/use-excel-add-in.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4383b-115">For more information, see [Use the Excel add-in](../../dev-itpro/office-integration/use-excel-add-in.md).</span></span>

## <a name="development-tooling--new-tabbed-workspace-pattern"></a><span data-ttu-id="4383b-116">開発ツール - 新しいタブ付きワークスペース パターン</span><span class="sxs-lookup"><span data-stu-id="4383b-116">Development tooling – New tabbed workspace pattern</span></span>

<span data-ttu-id="4383b-117">新しいタブ付きのワークスペース フォーム パターンを使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4383b-117">A new tabbed workspace form pattern is now available.</span></span> <span data-ttu-id="4383b-118">埋め込み Power BI レポートを格納するタブ ページを含めることができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4383b-118">You can now include tab pages that house embedded Power BI reports.</span></span> <span data-ttu-id="4383b-119">この機能は、水平スクロールのワークスペースから遠ざかる方向への第一歩です。</span><span class="sxs-lookup"><span data-stu-id="4383b-119">This feature is our first step toward moving away from horizontally-scrolling workspaces.</span></span> <span data-ttu-id="4383b-120">詳細については、[ワークスペース フォーム パターン](../../dev-itpro/user-interface/workspace-form-pattern.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4383b-120">For more information, see [Workspace form pattern](../../dev-itpro/user-interface/workspace-form-pattern.md).</span></span>

## <a name="development-and-customization--extending-a-group-control"></a><span data-ttu-id="4383b-121">開発およびカスタマイズ - グループ コントロールを拡張する</span><span class="sxs-lookup"><span data-stu-id="4383b-121">Development and customization – Extending a group control</span></span>

<span data-ttu-id="4383b-122">Dynamics 365 for Operations 開発ツールおよびランタイム プラットフォームは、参照されたモデルで既に拡張されているフォームを拡張するなど、拡張済みフォームの拡張をサポートするようになりました。</span><span class="sxs-lookup"><span data-stu-id="4383b-122">The Dynamics 365 for Operations development tools and runtime platform now support extending an extended form, for example, extending a form that is already extended in a referenced model.</span></span> <span data-ttu-id="4383b-123">グループ コントロールがフォーム拡張に属している場合、元々はフィールド/ボタン グループ コントロールを拡張できないという問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="4383b-123">This fixes an issue that originally prevented extending a field/button group control if the group control belongs to a form extension.</span></span>

## <a name="development-and-customization--extending-the-country-region-codes-property"></a><span data-ttu-id="4383b-124">開発およびカスタマイズ - 国の地域コードのプロパティを拡張する</span><span class="sxs-lookup"><span data-stu-id="4383b-124">Development and customization – Extending the Country Region Codes property</span></span>

<span data-ttu-id="4383b-125">**国/地域コード** プロパティにより、開発者は現在の法人のプライマリ住所に基づく特定の地域や国に機能を制限できます。</span><span class="sxs-lookup"><span data-stu-id="4383b-125">The **Country Region Codes** property enables developers to restrict functionality to certain regions or countries based on the current legal entity's primary address.</span></span> <span data-ttu-id="4383b-126">**国地域コード** プロパティは、メニュー拡張、メニュー項目拡張、表拡張 (およびフィールド)、フォーム拡張 (フォーム制御)、EDT 拡張、列挙拡張、および表示拡張の各拡張要素タイプで編集できます。</span><span class="sxs-lookup"><span data-stu-id="4383b-126">The **Country Region Codes** property is editable on the following extension element types: Menu extension, Menu Item extension, Table extension (and fields), Form extensions (form controls), EDT extensions, Enum extensions, and View extensions.</span></span>

<span data-ttu-id="4383b-127">開発者は、拡張機能で追加の国/地域のコードを指定できます。</span><span class="sxs-lookup"><span data-stu-id="4383b-127">A developer can specify additional country/region codes in their extension.</span></span> <span data-ttu-id="4383b-128">要素に関連付けられた有効な国/地域は、ベースライン要素とそのすべての拡張機能からのすべてのコードの結合になります。</span><span class="sxs-lookup"><span data-stu-id="4383b-128">The effective country/regions associated with an element will be the union of all codes from the baseline element and all its extensions.</span></span>

## <a name="development-and-customization--validating-events-on-form-data-sources-and-form-data-source-fields"></a><span data-ttu-id="4383b-129">開発およびカスタマイズ - フォーム データ ソースとフォーム データ ソース フィールドのイベントの検証</span><span class="sxs-lookup"><span data-stu-id="4383b-129">Development and customization – Validating events on form data sources and form data source fields</span></span>

<span data-ttu-id="4383b-130">フォーム データ ソース (FormDataSourceEventType) とフォーム データ ソース フィールド (FormDataFieldEventType) の検証イベントは、ユーザー指定の値の無効化をサポートするようになりました。</span><span class="sxs-lookup"><span data-stu-id="4383b-130">Validation events on form data source (FormDataSourceEventType) and form data source fields (FormDataFieldEventType) now support invalidating user-specified values.</span></span> <span data-ttu-id="4383b-131">詳細については、[拡張機能を使用してモデル要素をカスタマイズする](../../dev-itpro/extensibility/customize-model-elements-extensions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4383b-131">For more information, see [Customize model elements using extensions](../../dev-itpro/extensibility/customize-model-elements-extensions.md).</span></span>

<span data-ttu-id="4383b-132">次の例は、この機能を示しています。</span><span class="sxs-lookup"><span data-stu-id="4383b-132">The following example illustrates this feature.</span></span> <span data-ttu-id="4383b-133">この例では、**abTable** という名前のデータソース、および **FieldInt1** という名前のフィールドを含む **MyForm** と言う名前のフォームを使用します。</span><span class="sxs-lookup"><span data-stu-id="4383b-133">The example uses a form named **MyForm** that contains a data source named **abTable**, and a field named **FieldInt1**.</span></span>

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
