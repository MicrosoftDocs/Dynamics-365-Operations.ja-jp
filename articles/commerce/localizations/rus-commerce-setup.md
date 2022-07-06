---
title: ロシア向け Dynamics 365 Commerce ローカライズの設定
description: この記事では、ロシア向け Microsoft Dynamics 365 Commerce ローカライズの設定方法が説明されます。
author: akviklis
ms.date: 09/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: v-chgri
ms.search.region: Russia
ms.search.industry: Retail
ms.author: akviklis
ms.search.validFrom: 07/01/2021
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0026c71dda6275530e70d558132d6425b72571ac
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856944"
---
# <a name="set-up-the-dynamics-365-commerce-localization-for-russia"></a>ロシア向け Dynamics 365 Commerce ローカライズの設定

[!include[banner](../includes/banner.md)]

この記事では、ロシア向け Microsoft Dynamics 365 Commerce ローカライズの設定方法が説明されます。

ロシア向け Dynamics 365 Commerce ローカライズには、販売時点管理 (POS) コンポーネントの拡張機能が含まれます。 この拡張機能を使用すると、小売顧客向けの簡略化されたロシア語の住所形式を使用できます。

ロシア向け Commerce ローカライズの詳細については、[ロシアのローカライズ スコープ](../../finance/localizations/russia.md)および[ロシア向け Commerce ローカライズ](rus-commerce-localization.md)を参照してください。

## <a name="enable-russia-specific-commerce-functionality"></a>ロシア固有の Commerce 機能の有効化

このセクションでは、ロシア固有で推奨される Commerce 本社の設定を構成する方法について説明します。 詳細については、[Commerce のホーム ページ](../index.md) を参照してください。

ロシア固有の機能を有効にして使用するには、次の手順に従って Commerce 本社の設定を構成します。

1. 法人の基本住所で、**国/地域** フィールドを **RUS** (ロシア) に設定します。
1. ロシアにあるすべての店舗の POS 機能プロファイルで、**ISO** フィールドを **RU** (ロシア) に設定します。
1. **システム管理者 \> ワークスペース \> フィーチャー管理** の順に移動します。
1. **すべて** タブで、**ロシア語の簡略化された顧客住所形式の有効化** 機能を有効にします。

## <a name="enable-russia-specific-commerce-components"></a>ロシア固有の Commerce コンポーネントの有効化

このセクションは、ロシア向け Commerce のローカライズのコンポーネントを有効にするための配置ガイドを提供します。
    
### <a name="enable-modern-pos-extension-components"></a>Modern POS 拡張コンポーネントの有効化

Modern POS 拡張コンポーネントを有効にするには、次の手順に従います。

1. **RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。 また、**実行** コマンドを使用して、Visual Studio から Modern POS を実行できることを確認します。

    > [!NOTE]
    > Modern POS をカスタマイズしないでください。 ユーザー アカウント制御 (UAC) を有効にして、要求に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。

1. **extensions.json** ファイルで、次の明細行を追加することによって拡張機能が読み込まれるようにします。

    ```json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/Addresses.RU"
            },
            {
                "baseUrl": "Microsoft/FiscalCustomer.RU"
            }
        ]
    }
    ```

    > [!NOTE]
    > 詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。

1. ソリューションをリビルドします。
1. デバッガーでModern POS を実行し、機能をテストします。

### <a name="enable-cloud-pos-extension-components"></a>Cloud POS 拡張コンポーネントの有効化

Cloud POS の拡張機能コンポーネントを **extensions.json** ファイルに読み込むには、次の行をファイルの適切な部分に追加します。

```json
{
    "extensionPackages": [
        {
            "baseUrl": "Microsoft/Addresses.RU"
        },
        {
            "baseUrl": "Microsoft/FiscalCustomer.RU"
        }
    ]
}
``` 
    
## <a name="set-up-parameters-for-cash-management"></a>現金管理のパラメーターの設定

現金管理のパラメーターを設定するには、[POS での現金管理の設定](emea-eeu-petty-cash-for-retail.md#set-up-for-cash-management-for-pos)で説明されている手順に従います。
    
## <a name="set-up-aggregation-parameters-for-registering-pos-sales-and-return-transactions"></a>POS 販売トランザクションおよび返品トランザクションを登録する集計パラメーターの設定

これらのトランザクションが Commerce に登録された場合に POS 販売トランザクションおよび返品トランザクションを集計するために使用される集計パラメーターを設定できます。 集計パラメーターを選択すると、在庫分析コードが同じ品目のプラスの販売数量とマイナスの返品数量が集計されます。

Commerce 本社で集計パラメーターを設定するには、次の手順を実行します。

1. **Retail と Commerce \> 本社の設定 \> パラメーター \> Commerce パラメーター** の順にクリックします。
1. **転記** タブの、**集計** セクションで、**伝票トランザクション** チェック ボックスをオンにして、伝票トランザクションを集計します。
1. **販売と返品** チェック ボックスをオンにして、POS の販売トランザクションと返品トランザクションを集計します。

    > [!NOTE]
    > **販売と返品** チェック ボックスは、**伝票トランザクション** チェック ボックスをオンにした場合にのみ使用できます。

## <a name="set-up-miscellaneous-charges-for-customer-order-cancellations"></a>顧客注文のキャンセルに対する雑費の設定

Commerce 本社で顧客注文のキャンセル操作に適用する費用を設定するには、次の手順に従います。

1. **Retail と Commerce \> 本社の設定 \> パラメーター \> Commerce パラメーター** の順にクリックします。
1. **顧客注文** タブの **キャンセル料率** フィールドで、必要な値を指定します。
1. **売掛金 \> 諸費用の設定 \> 諸費用の転記** に移動します。
1. 顧客注文のキャンセルに対して費用を適用および転記できる勘定を設定します。

## <a name="additional-resources"></a>追加リソース

[Commerce のホーム ページ](../index.md)

[ロシアのローカライズ スコープ](../../finance/localizations/russia.md)

[東ヨーロッパにおける Commerce の小口現金管理](emea-eeu-petty-cash-for-retail.md)

[ロシア向け Commerce ローカライズ](rus-commerce-localization.md)
