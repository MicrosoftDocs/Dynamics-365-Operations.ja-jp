---
title: 税コードを特定できません
description: この記事では、税計算サービスの「税コードを決定できません」という内容のエラーをトラブルシューティングする方法について説明します。
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 6a74724de38cf362900277ab9addc8e6894f7689
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877862"
---
# <a name="tax-code-cannot-be-determined"></a>税コードを特定できません

[!include [banner](../includes/banner.md)]

この記事では、税計算サービスで「税コードを決定できません」という内容のエラーが表示された場合に実行できるトラブルシューティングの手順について説明します。

## <a name="symptom"></a>現象

「ヘッダー/明細行 - 1、税コードを決定できません。」というエラー メッセージが表示されます。 または、次の例に示すように、トラブルシューティング ファイル内でエラーが見つかります。 詳細については、[トラブルシューティングのためにデバッグ モードを有効にする](tcs-troubleshooting-enable-debug-mode.md)を参照してください。

```json
======================Tax service calculation result JSON:===========================
{
    "taxDocument": {
        "Header": [
            {
                "Lines": [
                    {
                        ...
                        "Errors": [
                            {
                                "Code": "TaxSetup20001",
                                "Message": "Header/Lines - 1, tax code cannot be determined."
                            }
                        ],
                        "Adjustment": null
                    }
                ],
                "Measures": {
                    ...
                },
                ...
            }
        ]
    },
    ...
}
```

## <a name="cause"></a>原因

税グループと品目税グループが一致していないので問題が発生している可能性があります。

## <a name="troubleshoot"></a>トラブルシューティング

次の手順に従って問題をトラブルシューティングします。

1. トラブルシューティング ファイルで、税グループと品目税グループが決定されていることを確認します。 **税グループ** および **品目税グループ** の値が空白の場合、税グループと品目税グループは決定されていません。 決定されている場合、結果が正しく表示されない場合があります。

    トラブルシューティング ファイルの例を次に示します。

    ```json
    ======================Tax service calculation result JSON:===========================
    {
        "taxDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            "Tax Codes": {},
                            "Measures": {
                                "Tax Group": "Group A",
                                "Item Tax Group": "Group B"
                            },
                            "Adjustment": null
                        }
                    ],
                    "Measures": {
                        ...
                    },
                    ...
                }
            ]
        },
        ...
    }
    ```

2. 販売注文明細行の詳細の **設定** タブの **消費税の上書き** オプションが有効になっていることを確認します。

    - 有効な場合、税コードは、トランザクション明細行で入力する **税グループ** および **品目別税グループ** の値によって決定されます。 これらの値が正しく入力されていることを確認します。
    - 有効になっていない場合、**税グループの適用性** および **品目別税グループの適用性** フィールドに正しい値が設定されていることを確認します。 詳細については、[一致する結果が見つかりませんでした](tcs-troubleshooting-no-matching-result.md)を参照してください。

3. 税グループと品目別税グループが正しく決定されている場合、共通部分があるかどうかを判別します。

    1. RCS で、**税機能** \> **税のコードとグループ** \> **税グループ** に移動します。

        | Line.Tax グループ | 税コード |
        |----------------|-----------|
        | グループ A        | A         |

    2. **税機能** \> **税のコードとグループ** \> **品目別税グループ** に移動します。

        | Line.Item 税グループ | 税コード |
        |---------------------|-----------|
        | グループ B             | B         |

    税グループおよび品目別税グループに共通部分がない場合、税コードは決定できません。

## <a name="mitigation"></a>軽減策

1. この記事の[トラブルシューティング](#troubleshoot) セクションの各ステップを実行し、必要に応じて設定を修正します。 税グループと品目別税グループが正しく決定されていない場合、[一致する結果が見つかりませんでした](tcs-troubleshooting-no-matching-result.md)を参照してください。
2. 税グループと品目別税グループに共通部分がない場合は、RCS で新しい機能バージョンを作成し、設定を修正します。

    - **税機能** \> **税のコードとグループ**  >  **品目別税グループ** に移動します。

        | Line.Item 税グループ | 税コード |
        |---------------------|-----------|
        | グループ B             | A;B       |

    税コードは **A** として決定されます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
