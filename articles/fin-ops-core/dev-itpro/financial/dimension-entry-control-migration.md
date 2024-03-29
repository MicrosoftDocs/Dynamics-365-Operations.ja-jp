---
title: 既定の分析コード コントロールの分析コード エントリ コントロールへの移行
description: この記事では、コードのアップグレードを実行した後、既定の分析コード コントロールを分析コード エントリ コントロールに移行するために必要な手順について説明します。
author: RyanCCarlson2
ms.date: 10/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: kfend
ms.custom: 25531
ms.assetid: 05e85771-44e1-4b0a-8dd2-a878be5a3309
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53522c1e44d20fb859b085fedab6aca613ce9455
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866789"
---
# <a name="migrate-default-dimensions-controls-to-dimension-entry-controls"></a>既定の分析コード コントロールの分析コード エントリ コントロールへの移行

[!include [banner](../includes/banner.md)]

この記事では、コードのアップグレードを実行した後、既定の分析コード コントロールを分析コード エントリ コントロールに移行するために必要な手順について説明します。 例として、PurchTable フォームを使用します。

## <a name="simple-migration-scenario---purchtable-form"></a>簡易移行シナリオ - PurchTable フォーム

1. **アプリケーション エクスプローラー** で **PurchTable** フォームを検索します。
2. 現在のプロジェクトにフォームを追加します。
3. デザイナーとコード エディタ ビューで、フォームを開きます。
4. フォームのデザイン ビューでは:
    1. コントロール ツリーから手動で、または **ファイル** タブ下の検索バーで「DimensionEntry」を検索して、分析コード エントリ コントロール (DEC) を検索します。
    2. 最初の **DEC** (DimensionEntryControlHeader) を選択し、以下を確認します。
        - コントロールの横にある括弧で指定されたコントロールのタイプは、Dimension Entry Control です。
        - Controller クラスのプロパティは空白になります。 このプロパティは、DEC のこのインスタンスで使用されるコントローラーのタイプを示し、これによってコントロールの動作が決まります。 このプロパティが空白のときは、コントローラーは、**値のデータ** フィールド (この場合は、**PurchTable** テーブルの **DefaultDimension** フィールド) で指定されたフィールドの EDT によって決定されます。 アプリケーション エクスプローラーで **PurchTable** テーブルを検索します。 **PurchTable** を右クリックし、**デザイナーを開く** を選択します。 **フィールド** ノードを展開し、**DefaultDimension** フィールドを選択します。 このフィールドの EDT プロパティは、LedgerDefaultDimensionValueSet に設定されます。 この EDT では、このコントロールが LedgerDefaultDimensionEntryController を使用することを意味します。

    3. **PurchTable** フォーム デザイン ビューに戻って、2 番目の `DEC` (DimensionEntryControlLine) を選択し、次のプロパティを確認してください。
        - コントロールの横にある括弧で指定されたコントロールのタイプは、Dimension Entry Control です。
        - Controller クラスのプロパティは空白になります。 コントローラーは、`DEC` の場合と同様に、**値データ** フィールドで指定されたフィールドの EDT によって決定されます。

5. コード エディター ビューに切り替えます。
6. フォーム ソース コードで、"TODO: (Code Upgrade) \[Dimension entry control\]" のすべての事例を検索します。
7. 残りの各 TODO コメントの実行は、次のようになります。

## <a name="data-source-purchtable"></a>データ ソース PurchTable

**(フォーム &gt; データ ソース &gt; PurchTable &gt; メソッド**)

|以前 | 変更後   |
|-------|--------|
| /\* TODO: (コード アップグレード) \[分析コード エントリ コントロール\]移行ガイダンスに基づいてこの TODO を置き換えます。 \*/DimensionEntryControlHeader.reactivate(); | このメソッド呼び出しには前に呼び出された parm メソッドがないため、削除することができます。 分析コード エントリ コントロールは、会社または表示されている分析コード セットが変化した場合にのみ再度有効化する必要があります。 メソッド呼び出しの再有効化の一般的なルールとして、必要でない場合は、呼び出しを削除し、正常に動作することを確認するためにコントロールをテストします。 そうでない場合は、再アクティブ化コール バックを追加します。 |

## <a name="data-field-orderaccount"></a>データ フィールド OrderAccount

(**フォーム&gt;データ ソース &gt;PurchTable&gt; フィールド &gt;OrderAccount&gt; 方法**)

|以前 | 変更後   |
|-------|--------|
| /\* TODO: (コード アップグレード) \[分析コード エントリ コントロール\]移行ガイダンスに基づいてこの TODO を置き換えます。 \*/DimensionEntryControlHeader.reactivate(); | このメソッド呼び出しには前に呼び出された parm メソッドがないため、削除することができます。 分析コード エントリ コントロールは、会社または表示されている分析コード セットが変化した場合にのみ再度有効化する必要があります。 |

## <a name="data-field-projid-purchtable"></a>データ フィールド ProjId (PurchTable)

(**フォーム&gt;データ ソース &gt;PurchTable&gt; フィールド &gt;ProjId&gt; 方法**)

|以前 | 変更後   |
|-------|--------|
| /\* TODO: (コード アップグレード) \[分析コード エントリ コントロール\]移行ガイダンスに基づいてこの TODO を置き換えます。 \*/DimensionEntryControlHeader.reactivate(); | このメソッドの呼び出しには前に呼び出された parm メソッドがないため、削除することができます。 分析コード エントリ コントロールは、会社または表示されている分析コード セットが変化した場合にのみ再度有効化する必要があります。 super() 呼び出しがすべて残っているため、modified() メソッド全体を削除することもできます。 メソッドが含まれていないため、ProjId クラスを削除することができます。 |

## <a name="data-field-vendgroup"></a>データ フィールド VendGroup

(**フォーム&gt;データ ソース &gt;PurchTable&gt; フィールド &gt;VendGroup&gt; 方法**)

|以前 | 変更後   |
|-------|--------|
| /\* TODO: (コード アップグレード) \[分析コード エントリ コントロール\]移行ガイダンスに基づいてこの TODO を置き換えます。 \*/DimensionEntryControlHeader.reactivate(); | このメソッド呼び出しには前に呼び出された parm メソッドがないため、削除することができます。 分析コード エントリ コントロールは、会社または表示されている分析コード セットが変化した場合にのみ再度有効化する必要があります。 modified() メソッドと VendGroup クラス全体を削除することもできます。 |

## <a name="data-source-purchline"></a>データ ソース PurchLine

(**フォーム&gt;データ ソース &gt;PurchLine&gt; 方法**)

|以前 | 変更後   |
|-------|--------|
| /\* TODO: (コード アップグレード) \[分析コード エントリ コントロール\]移行ガイダンスに基づいてこの TODO を置き換えます。 \*/DimensionEntryControlLine.reactivate();**注記:** これはデータソースの itemIdModified メソッドにおけるメソッド呼び出しの再有効化です。 | このメソッド呼び出しには前に呼び出された parm メソッドがないため、削除することができます。 分析コード エントリ コントロールは、会社または表示されている分析コード セットが変化した場合にのみ再度有効化する必要があります。 |
| /\* TODO: (コード アップグレード) \[分析コード エントリ コントロール\]移行ガイダンスに基づいてこの TODO を置き換えます。 \*/DimensionEntryControlLine.reactivate();**注記:** これはデータソースの create() メソッドにおけるメソッド呼び出しの再有効化です。 | このメソッド呼び出しには前に呼び出された parm メソッドがないため、削除することができます。 分析コード エントリ コントロールは、会社または表示されている分析コード セットが変化した場合にのみ再度有効化する必要があります。 |

## <a name="data-field-assetgroup"></a>データ フィールド AssetGroup

(**フォーム&gt;データ ソース &gt;PurchLine&gt; フィールド &gt;AssetGroup&gt; 方法**)

|以前 | 変更後   |
|-------|--------|
| /\* TODO: (コード アップグレード) \[分析コード エントリ コントロール\]移行ガイダンスに基づいてこの TODO を置き換えます。 \*/DimensionEntryControlLine.reactivate(); | このメソッドの呼び出しには前に呼び出された parm メソッドがないため、削除することができます。 分析コード エントリ コントロールは、会社または表示されている分析コード セットが変化した場合にのみ再度有効化する必要があります。 modified() メソッドと AssetGroup クラス全体を削除することもできます。 |

## <a name="data-field-assetidform-gt-data-sources-gt-purchline-gt-fields-gt-assetid-gt-methods"></a>データ フィールドの AssetId (**フォーム &gt; データ ソース &gt;PurchLine &gt; フィールド &gt; AssetId &gt; 方法**)

|以前 | 変更後   |
|-------|--------|
| /\* TODO: (コード アップグレード) \[分析コード エントリ コントロール\]移行ガイダンスに基づいてこの TODO を置き換えます。 \*/DimensionEntryControlLine.reactivate(); | このメソッドの呼び出しには前に呼び出された parm メソッドがないため、削除することができます。 分析コード エントリ コントロールは、会社または表示されている分析コード セットが変化した場合にのみ再度有効化する必要があります。 |

## <a name="data-field-procurementcategory"></a>データ フィールド ProcurementCategory

(**フォーム&gt;データ ソース &gt;PurchLine&gt; フィールド &gt;ProcurementCategory&gt; 方法**)

| 以前        |  変更後                                        |
|--------|--------------------------------------------------|
| /\* TODO: (コード アップグレード) \[分析コード エントリ コントロール\]移行ガイダンスに基づいてこの TODO を置き換えます。 \*/DimensionEntryControlLine.reactivate(); | このメソッド呼び出しには前に呼び出された parm メソッドがないため、削除することができます。 分析コード エントリ コントロールは、会社または表示されている分析コード セットが変化した場合にのみ再度有効化する必要があります。 |

## <a name="data-field-projid-purchline"></a>データ フィールド ProjId (PurchLine)

(**フォーム&gt;データ ソース &gt;PurchLine&gt; フィールド &gt;ProjId&gt; 方法**)

|以前 | 変更後   |
|-------|--------|
| /\* TODO: (コード アップグレード) \[分析コード エントリ コントロール\]移行ガイダンスに基づいてこの TODO を置き換えます。 \*/DimensionEntryControlLine.reactivate(); | このメソッド呼び出しには前に呼び出された parm メソッドがないため、削除することができます。 分析コード エントリ コントロールは、会社または表示されている分析コード セットが変化した場合にのみ再度有効化する必要があります。 |

## <a name="tabpage-tabfinancialdimensionsline"></a>TabPage TabFinancialDimensionsLine

(フォーム タブの下にある検索バーで「TabFinancialDimensionsLine」を検索してください。)

|以前 | 変更後   |
|-------|--------|
| /\* TODO: (コード アップグレード) \[分析コード エントリ コントロール\] この方法は、カスタム実装がない場合に削除することができます \*///dimensionDefaultingControllerHeader.pageActivated() | pageActivated メソッドをもう呼び出す必要はありません。 この全メソッドと TabFinancialDimensionsLine クラスは、pageActivated メソッドにカスタム ロジックがないため削除できます。 |

## <a name="tabpage-tabfinancialdimensionsheader"></a>TabPage TabFinancialDimensionsHeader

(フォーム タブの下にある検索バーで「TabFinancialDimensionsHeader」を検索してください。)

|以前 | 変更後   |
|-------|--------|
| /\* TODO: (コード アップグレード) \[分析コード エントリ コントロール\] この方法は、カスタム実装がない場合に削除することができます \*///dimensionDefaultingControllerHeader.pageActivated() | pageActivated メソッドをもう呼び出す必要はありません。 この全メソッドと TabFinancialDimensionsHeader クラスは、pageActivated メソッドにカスタム ロジックがないため削除できます。 |

## <a name="additional-resources"></a>追加リソース

- [分析コード エントリ コントロールの取得](dimension-entry-control-uptake.md)
- [ダイアログの分析コード エントリ コントロールのサポート](dimension-entry-control-dialog-support.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
