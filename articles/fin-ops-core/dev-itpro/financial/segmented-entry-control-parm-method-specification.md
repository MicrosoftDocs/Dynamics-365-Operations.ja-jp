---
title: セグメント化されたエントリ コントロールのための parm メソッド
description: セグメント化されたエントリ コントロールのインスタンスで、コード内で設定できる parm メソッドについて説明します。
author: robinarh
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 25631
ms.assetid: 0090efe3-3fd8-4988-83df-745d25b063d3
ms.search.region: Global
ms.author: ghenriks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab48920012e14e4dc5f78095cd9c4acdb9587cc5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681072"
---
# <a name="parm-methods-for-segmented-entry-controls"></a>セグメント化されたエントリ コントロールのための parm メソッド

[!include [banner](../includes/banner.md)]

セグメント化されたエントリ コントロールのインスタンスで、コード内で設定できる parm メソッドについて説明します。

セグメント化されたエントリ コントロールには、コントロールの動作に影響を与える複数の parm メソッドがあります。 各メソッドの説明を次に示します。

| 方法                               | 説明                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parmDataAreaId                       | コントロールが実行されている会社のコンテキスト。 ほとんどの場合、コンテキストは `curext()` ですが、フォームで異なる会社のコンテキストや異なる会社のサーフェス レコードなどを手動で設定できるシナリオもあります。 フォームは、フォームのさまざまな条件の下で SEC を実行するコンテキストを評価する必要があります。 |
| parmCurrency                         | このメソッドは、主勘定の検証のためのアカウント コントロールによって使用されます。 このプロパティが設定されている場合は、主勘定検証中に mainAccount.checkAccountCurrency() が呼び出されます。                                                                                                                                                       |
| parmControlDate                      | このメソッドは、セグメント値の検証や一部の内部クエリで使用されます。 既定では、現在の日付が使用されますが、フォームが業務要件に基づいてカスタム日付を設定する場合のシナリオがあります。    |
| parmDimensionAutoCompleteFilter      | 分析コード auto-Complete データをフィルター処理するために、追加の制限を追加します。                                                                     |
| parmJournalName                      | このメソッドは、仕訳帳コントロールを適用することで使用されます。                |
| parmAccountTypeEnumType              |                                               |
| parmDimensionAccountStorageUsageType | このメソッドにより、フォームまたはクラスは、フォーム上でセグメント化されたエントリ コントロールの使用方法を指定できます。 このプロパティは、DimensionAccountStorageUsage (値を持つ列挙型: 設定、トランザクション、エイリアス) 型です。                                                                                                          |
| parmTaxCode                          | このメソッドは使用しないため、削除されました。                                             |
| parmAccountType                      |  |
| parmIncludeFinancialAccounts         | デザイン時プロパティと関連します。 詳細については、「セグメント化されたエントリ コントロールのメタデータ詳細」を参照してください。                                                                                                                                                                                                          |
| parmIncludeTotalAccounts             | デザイン時プロパティと関連します。 詳細については、「セグメント化されたエントリ コントロールのメタデータ詳細」を参照してください。                                                                                                                                                                                                          |
| parmIsDefaultAccount                 | デザイン時プロパティと関連します。 詳細については、「セグメント化されたエントリ コントロールのメタデータ詳細」を参照してください。                                                                                                                                                                                                          |
| parmLockMainAccountSegment           | デザイン時プロパティと関連します。 詳細については、「セグメント化されたエントリ コントロールのメタデータ詳細」を参照してください。                                                                                                                                                                                                          |
| parmPostingType                      | デザイン時プロパティと関連します。  詳細については、「セグメント化されたエントリ コントロールのメタデータ詳細」を参照してください。                                                                                                                                                                                                         |
| parmValidateBlockedForManualEntry    | デザイン時プロパティと関連します。  詳細については、「セグメント化されたエントリ コントロールのメタデータ詳細」を参照してください。                                                                                                                                                                                                         |



<a name="additional-resources"></a>追加リソース
--------

[ダイアログのセグメント化されたエントリ コントロールのサポート](segmented-entry-control-dialog-support.md)

[セグメント化されたエントリ コントロールのデザイン時メタデータ](segmented-entry-control-metadata-specification.md)

[セグメント化されたエントリ コントロールの移行](segmented-entry-control-conversion.md)

[セグメント化されたエントリ コントロールに関する移行ガイダンス](segmented-entry-control-migration-guidance.md)



