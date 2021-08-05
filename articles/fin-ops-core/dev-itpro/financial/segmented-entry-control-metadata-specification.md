---
title: セグメント化されたエントリ コントロールのためのデザイン時メタデータ
description: セグメント化エントリ コントロールのデザイン時メタデータ プロパティについて説明します。
author: RyanCCarlson2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 25591
ms.assetid: b8c5d7a4-ee2b-4ab1-b042-88472b97f035
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2916ba5828abeaeef8676aaa7f26a988ff37dc2
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359745"
---
# <a name="design-time-metadata-for-segmented-entry-controls"></a>セグメント化されたエントリ コントロールのためのデザイン時メタデータ

[!include [banner](../includes/banner.md)]

セグメント化エントリ コントロールのデザイン時メタデータ プロパティについて説明します。

セグメント化エントリ コントロールのカスタム プロパティは、コントローラー グループの下にあります。 次に例を示します。

[![SEC プロパティ シート例。](./media/10.jpg)](./media/10.jpg)

一部のプロパティは、選択されたコントローラ クラスに基づいて編集できない場合があります。 これは、特定のプロパティのみがさまざまなコントローラー クラスのそれぞれに関連するためです。  詳細については、[有効なプロパティ](#valid-properties) を参照してください。

## <a name="property-details"></a>プロパティの詳細

| プロパティ | 有効な値   | 用途            |
|----------------|--------------------------|------------------------------------|
| 勘定タイプ フィールド                | データ ソースからのフィールド。                                                      | 使用されるアカウントの種類を決定します。 通常、複数セグメントの勘定科目から、Cust、Vend、Bank、Project などの他のバッキング テーブルの単一セグメント値への仕訳入力に使用します。 |
| コントローラー クラス                  | 7 つのコントローラー クラスのうちの 1 つです。 たとえば LedgerDimensionDefaultAccountController です。 | セグメント化されたエントリ コントロールの動作およびパターンを決定します。                                                                                                                                          |
| 財務勘定を含む        | NoYes                                                                             | 財務勘定である主勘定が有効であるかどうかを決定します。                                                                                                                                   |
| 勘定合計を含む            | NoYes                                                                             | タイプが "合計" の主勘定が有効であるかどうかを判断します。                                                                                                                                                 |
| 既定の勘定です。                | TrueFalse                                                                         | 動的アカウントで、アカウントが既定または完全アカウントであるべきかどうかを決定します。                                                                                                                        |
| 主勘定セグメントのロック         | NoYes                                                                             | 主勘定セグメントがロックされているかどうかをコントロールします。  通常は仕訳帳や構成に基づく配分に使用されます。                                                                                   |
| 転記タイプ                      | LedgerPostingType 列挙の値。                                   | 主勘定が検証され、そのアカウントで転記タイプを使用できるかどうかが確認されます。                                                                                                            |
| 手動入力のブロック状態の検証 | NoYes                                                                             | 分析コードの「手動入力のブロック」ステータスを優先するかを決定します。                                                                                                                    |

## <a name="valid-properties"></a>有効なプロパティ

次のセクションでは、各コントローラー タイプに対して有効なプロパティを示します。

### <a name="validate-blocked-for-manual-entry"></a>手動入力のブロック状態の検証

BudgetLedgerDimension: はい

BudgetPlanningLedgerDimension: はい

DimensionDynamicAccount: Yes

LedgerDimensionAccount: はい

LedgerDimensionDefaultAccount: はい

LedgerDimensionAccountAlias: はい

### <a name="account-type-field"></a>勘定タイプ フィールド

BudgetLedgerDimension: いいえ

BudgetPlanningLedgerDimension: いいえ

DimensionDynamicAccount: Yes

LedgerDimensionAccount: いいえ

LedgerDimensionDefaultAccount: いいえ

LedgerDimensionAccountAlias: いいえ

### <a name="is-default-account"></a>既定の勘定です。

BudgetLedgerDimension: いいえ

BudgetPlanningLedgerDimension: いいえ

DimensionDynamicAccount: Yes

LedgerDimensionAccount: いいえ

LedgerDimensionDefaultAccount: いいえ

LedgerDimensionAccountAlias: いいえ

### <a name="lock-main-account-segment"></a>主勘定セグメントのロック

BudgetLedgerDimension: いいえ

BudgetPlanningLedgerDimension: はい

DimensionDynamicAccount: Yes

LedgerDimensionAccount: はい

LedgerDimensionDefaultAccount: はい

LedgerDimensionAccountAlias: いいえ

### <a name="posting-type"></a>転記タイプ

BudgetLedgerDimension: いいえ

BudgetPlanningLedgerDimension: はい

DimensionDynamicAccount: Yes

LedgerDimensionAccount: はい

LedgerDimensionDefaultAccount: はい

LedgerDimensionAccountAlias: はい

### <a name="include-total-accounts"></a>勘定合計を含む

BudgetLedgerDimension: いいえ

BudgetPlanningLedgerDimension: いいえ

DimensionDynamicAccount: Yes

LedgerDimensionAccount: いいえ

LedgerDimensionDefaultAccount: はい

LedgerDimensionAccountAlias: いいえ

### <a name="include-financial-accounts"></a>財務勘定を含む

BudgetLedgerDimension: いいえ

BudgetPlanningLedgerDimension: いいえ

DimensionDynamicAccount: Yes

LedgerDimensionAccount: いいえ

LedgerDimensionDefaultAccount: はい

LedgerDimensionAccountAlias: いいえ

## <a name="additional-resources"></a>追加リソース

[ダイアログのセグメント化されたエントリ コントロールのサポート](segmented-entry-control-dialog-support.md)

[セグメント化されたエントリ コントロールの Parm メソッド](segmented-entry-control-parm-method-specification.md)

[セグメント化されたエントリ コントロールの移行](segmented-entry-control-conversion.md)

[セグメント化されたエントリ コントロールに関する移行ガイダンス](segmented-entry-control-migration-guidance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]