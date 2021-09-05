---
title: 販売注文の状態列のマッピングを設定する
description: このトピックでは、販売注文の状態列を二重書き込み用に設定する方法について説明します。
author: dasani-madipalli
ms.date: 06/25/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: damadipa
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: eb3e3e87f7615a289f019a5d47dbc596f0266aa5
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416579"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a>販売注文の状態列のマッピングを設定する

[!include [banner](../../includes/banner.md)]

販売注文の状態を示す列は、Microsoft Dynamics 365 Supply Chain Management と Dynamics 365 Sales で異なる列挙値を持っています。 これらの列を二重書き込みでマップするには、追加の設定が必要です。

## <a name="columns-in-supply-chain-management"></a>Supply Chain Management の列

Supply Chain Management では、2 つの列が販売注文の状態を反映します。 マップする必要がある列は **状態** と **ドキュメントの状態** です。

**状態** 列挙型では、注文の全体的な状態を指定します。 この状態は、注文ヘッダーに表示されます。

**状態** 列挙型の値は次のとおりです:

- オープン注文
- 配送済
- 請求済
- キャンセル済

**ドキュメントの状態** 列挙型は、注文に対して生成された最新のドキュメントを指定します。 たとえば、注文が確定された場合、このドキュメントは販売注文の確認書になります。 販売注文が部分的に請求され、残りの明細行が確認された場合、プロセスの後で請求書が生成されるため、ドキュメントの状態は **請求書** のままになります。

**ドキュメントの状態** 列挙型の値は次のとおりです:

- 確認書
- ピッキング リスト
- 梱包明細
- 請求書

## <a name="columns-in-sales"></a>Sales の列

Sales では、2 つの列が注文の状態を示します。 マップする必要がある列は **状態** と **処理状態** です。

**状態** 列挙型では、注文の全体的な状態を指定します。 次の値があります:

- 使用可能
- 提出済
- 履行済
- 請求済
- キャンセル済

**処理状態** 列挙型は、状態をより正確に Supply Chain Management でマップできるように導入されました。

次の表に、Supply Chain Management における **処理状態** のマッピングを示します。

| 処理状態   | Supply Chain Management の状態 | Supply Chain Management におけるドキュメントの状態 |
|---------------------|-----------------------------------|--------------------------------------------|
| 使用可能              | オープン注文                        | None                                       |
| 確定済           | オープン注文                        | 確認書                               |
| ピッキング済              | オープン注文                        | ピッキング リスト                               |
| 一部出荷済 | オープン注文                        | 梱包明細                               |
| 配送済           | 配送済                         | 梱包明細                               |
| 一部請求済  | 配送済                         | 請求書                                    |
| 請求済            | 請求済                          | 請求書                                    |
| キャンセル済           | キャンセル済                         | 適用できません                             |

次の表に、Sales と Supply Chain Management 間の **処理状態** のマッピングを示します。

| 処理状態   | Sales の状態 | Supply Chain Management の状態 |
|---------------------|-----------------|-----------------------------------|
| 使用可能              | 使用可能          | オープン注文                        |
| 確定済           | 提出済       | オープン注文                        |
| ピッキング済              | 提出済       | オープン注文                        |
| 一部出荷済 | 使用可能          | オープン注文                        |
| 一部請求済  | 使用可能          | オープン注文                        |
| 一部請求済  | 履行済       | 配送済                         |
| 請求済            | 請求済        | 請求済                          |
| キャンセル済           | キャンセル済       | キャンセル済                         |

## <a name="setup"></a>段取り

販売注文状態の列のマッピングを設定するには、**IsSOPIntegrationEnabled** 属性と **isIntegrationUser** 属性を有効にする必要があります。

**IsSOPIntegrationEnabled** 属性を有効にするには、次の手順を実行します。

1. ブラウザーで `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations` に移動します。 **\<test-name\>** を会社の Sales リンクに置き換えます。
2. 開いたページで、**organizationid** を検索し、値をメモします。

    ![organizationid の検索。](media/sales-map-orgid.png)

3. Sales では、ブラウザー コンソールを開き、次のスクリプトを実行します。 手順 2 の **organizationid** 値を使用します。

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![ブラウザー コンソールの JavaScript コード。](media/sales-map-script.png)

4. **IsSOPIntegrationEnabled** が **true** に設定されていることを確認します。 手順 1 の URL を使用して、値を確認します。

    ![IsSOPIntegrationEnabled を true に設定。](media/sales-map-integration-enabled.png)

**isIntegrationUser** 属性を有効にするには、次の手順を実行します。

1. Sales では **設定 \> カスタマイズ \> システムのカスタマイズ** に移動し、**ユーザー テーブル** を選択して、**フォーム \> ユーザー** を開きます。

    ![ユーザー フォームを開く。](media/sales-map-user.png)

2. フィールド エクスプローラーで **統合ユーザーモード** を検索し、それをダブルクリックして、フォームに追加します。 変更を保存します。

    ![統合ユーザーモード列のフォームへの追加。](media/sales-map-field-explorer.png)

3. Sales では、**設定 \> セキュリティ \> ユーザー** に移動し、表示を **有効なユーザー** から **アプリケーション ユーザー** に変更します。

    ![表示を有効なユーザーからアプリケーション ユーザーに変更。](media/sales-map-enabled-users.png)

4. **DualWrite IntegrationUser** の 2 つのエントリを選択します。

    ![アプリケーション ユーザーの一覧。](media/sales-map-user-mode.png)

5. **統合ユーザー モード** 列の値を **はい** に変更します。

    ![統合ユーザー モード列の値の変更。](media/sales-map-user-mode-yes.png)

これで、販売注文がマップされました。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]