---
title: 自動転記の既定の説明の設定
description: この記事は、一般会計に自動的に転記される、会計項目の説明に使用される既定のテキストの設定方法を説明します。 自由書式のテキストを使用するか、固定変数を選択することによって、既定の説明テキストを設定することができます。
author: aprilolson
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 71982a7d5b1bb08d3e238646ea0b15f17260bdcc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904502"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a>自動転記の既定の説明の設定

[!include [banner](../includes/banner.md)]

この記事は、一般会計に自動的に転記される、会計項目の説明に使用される既定のテキストの設定方法を説明します。 自由書式のテキストを使用するか、固定変数を選択することによって、既定の説明テキストを設定することができます。

> [!NOTE]
> 一部のトランザクション タイプに対し、一部の国または地域では、これらのトランザクション タイプに関連するフィールドからのテキストを含めることもできます。 トランザクション タイプ、および国と地域のリストについては、この記事で後述する [オプション: 既定の説明に他のテキストを追加する](#optional-add-other-text-to-default-descriptions) を参照してください。

## <a name="set-up-default-descriptions"></a>既定の説明を設定

1. **組織管理** \> **設定** \> **既定の説明** の順に移動します。
2. アクション ウィンドウで、**新規** を選択します。
3. **説明** フィールドで、既定の説明を作成するトランザクションのタイプを選択します。
4. **言語** フィールドで、この説明が適用される言語を選択します。
5. **テキスト** フィールドに、既定の説明を入力します。 フィールドにテキストを入力するか、次の自由書式の 1 つ以上の変数を使用できます。

    - **%1** – トランザクション日付を追加します。
    - **%2** – 一般会計に転記されるドキュメント タイプに対応する ID を追加します。 たとえば、請求書に関連するトランザクション タイプの場合、**%2** 変数によって請求書番号が追加されます。
    - **%3** – 一般会計に転記されるドキュメント タイプに対応する ID を追加します。 たとえば、請求書に関連するトランザクション タイプの場合、**%3** 変数によって顧客 ID 番号が追加されます。

## <a name="optional-add-other-text-to-default-descriptions"></a>オプション: 既定の説明に他のテキストを追加する

一部のトランザクション タイプに対し、一部の国または地域では、これらのトランザクション タイプに関連するデータのフィールドから取られたテキストを既定の説明に含めることができます。 次のリストは、このオプションが使用可能なトランザクション タイプ、および国と地域を示します。

**トランザクション タイプ**

次のドキュメント タイプに関連付けられているトランザクション タイプの既定の説明に、他のテキストを追加できます。

- 顧客請求書
- 顧客訂正票
- 顧客現金払い
- 仕入先支払
- 販売注文
- 発注書
- 在庫仕訳帳
- マスター プラン (MRP)
- 固定資産

**国と地域**

このオプションは、次の国および地域に対して使用できます。

- ブラジル
- 中国
- チェコ共和国
- 東ヨーロッパ
- ハンガリー
- インド
- 日本
- リトアニア
- ラトビア
- ポーランド
- ロシア

### <a name="add-text-to-default-descriptions"></a>既定の説明にテキストを追加する

この記事の前半の [既定の説明の設定](#set-up-default-descriptions) セクションの手順を完了した後、次の手順に従い、既定の説明に他のテキストを追加します。

1. **パラメーター** クイック タブで、**追加** を選択します。
2. **参照テーブル** フィールドで、パラメーター データを説明に追加するデータベース テーブルを選択します。
3. **参照フィールド** フィールドで、説明にパラメーター データを追加するフィールドを選択します。
4. 手順 1. ～ 3. を繰り返してパラメーターを追加します。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
