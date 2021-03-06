---
title: TDS の税コードを TDS 税グループに添付し、TDS の計算に使用する式を定義する
description: このトピックでは、源泉徴収税 (TDS) のグループを設定し、TDS の税コードを TDS の税グループに関連付ける方法について説明します。 TDS 税グループの TDS を計算するには、TDS 税グループに関連付けられた TDS 税コードの式を定義する必要があります。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: ec0d683153bd5ab731035159d32881fbdb352d70
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023397"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a>TDS の税コードを TDS 税グループに添付し、TDS の計算に使用する式を定義する

[!include [banner](../includes/banner.md)]

このトピックでは、源泉徴収税 (TDS) のグループを設定し、TDS の税コードを TDS の税グループに関連付ける方法について説明します。 TDS 税グループの TDS を計算するには、TDS 税グループに関連付けられた TDS 税コードの式を定義する必要があります。

次の手順に従って、TDS の税グループを設定し、TDS の税コードを関連付け、TDS の計算で使用する式を定義します。

1. **税 \> 間接税\> 源泉徴収税\> 源泉徴収税グループ** の順に移動します。

    [![源泉徴収税グループ ページ](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)

2. アクション ペインで、**新規** を選択して、 TDS の源泉徴収税を作成し、必要な詳細を入力します。
3. **税タイプ** フィールドで、**TDS** を選択します。
4. **設定** クイック タブで、**追加** を選択して明細行を作成します。
5. **源泉徴収税コード** フィールドで、TDS の税グループに使用する TDS 税を選択します。 **源泉徴収税の名前** フィールドには TDS 税コードの名前が表示され、**値** フィールドに値が表示されます。
6. TDS トランザクションの TDS 税コードに添付されている TDS 税コンポーネントに定義されているしきい値制限およびしきい値の制限例外を無視するには、**しきい値を無視する** チェックボックスを選択します。
7. トランザクションで税グループを計算しないようにするには、**除外する** のチェックボックスを選択します。
8. アクション ウィンドウで、**デザイナー** を選択してフォーミュラ デザイナーを開きます。このデザイナーで、TDS 税グループの TDS を計算する式を定義できます。 **デザイナー** ページの **税金** タブには、TDS 税グループに対して選択されている TDS 税コードが表示されます。

    [![デザイナーのページ](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)

9. **計算** タブ で 、**Alt+N** キーを押して行を作成します。 **ID フィールド** には、自動的に生成されたTDS の計算に使用するプライオリティー ID が表示されます。
10. **税コード** フィールドで、計算式を定義する TDS の税コードを選択します。 TDS 税グループで選択されているすべての TDS 税コードがこのフィールドで選択可能です。
11. **課税 対象基準** フィールドで、TDS の計算基準を選択します:

    - **総額** - 税コードに定義されている計算式を用いて、取引総額 (請求額) をもとに TDS を計算します。
    - **総額を除外** - コードに定義されている計算式に基づいて TDS を計算します。

    > [!NOTE]
    > 優先 ID が **1** の TDS 税コードでは、**課税基準** フィールドを **Excl 総額** に設定できません。

12. TDS の計算は、TDS の税グループにアタッチ関連付けられている各税コードの **計算式** フィールドに定義されている計算式に基づいて行われます。 プラス記号 (**+**)、マイナス記号 (**-**)、乗算記号 (**\**_)、または区分記号 (_*/**) ボタンを選択し、**計算式** フィールドに選択した TDS 税コードの計算式を入力します。

    > [!NOTE]
    > 優先度 ID が **1** の TDS の税コードには、計算式を定義できません。

13. **計算式** フィールドで TDS 税コードの計算式を定義するには、**税** タブで使用できる TDS 税コードを追加します。**計算式** フィールドに TDS 税コードを追加するには、次の方法があります:

    - **税** タブから **計算式** フィールドに必要な税コードをドラッグします。
    - **税** タブで必要な税コードをダブル タップ (またはダブル クリック) します。
    - **税** タブで必要な税コードを選択してホールド (または右クリック) し、**税コードの追加** を選択します。

    > [!NOTE]
    > 各 TDS 税コードの前に計算式を挿入します。 計算式に追加された TDS の税コードが括弧内 (\[...\]) に表示されています。

14. **計算式** フィールドの税コードに対して定義されている計算式をクリアするには、**C** ボタンを選択します。
15. **計算** タブでレコード 削除するには 、**削除** を選択 します。
16. ページを閉じます。
