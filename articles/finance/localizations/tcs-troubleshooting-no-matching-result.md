---
title: 一致する結果が見つかりません
description: この記事では、税計算サービスの「一致する結果が見つかりませんでした」という内容のエラーのトラブルシューティングを行う方法について説明します。
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
ms.openlocfilehash: d3bbc76741fdd018d1b2987538b8de7f6d92ee53
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845147"
---
# <a name="no-matching-result-could-be-found"></a>一致する結果が見つかりません

[!include [banner](../includes/banner.md)]

この記事では、税計算サービスで「一致する結果が見つかりませんでした」という内容のエラーが表示された場合に実行できるトラブルシューティングの手順について説明します。

## <a name="symptom"></a>現象

「ヘッダー/明細行 - 1、税グループ、一致する結果が見つかりませんでした。」というエラー メッセージが表示されます。

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
                                "Code": "TaxSetup20000",
                                "Message": "Header/Lines - 1, Tax group applicability, no matching result could be found."
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

この問題は、Regulatory Configuration Service (RCS) の機能の設定が正しくない場合に発生します。

## <a name="troubleshoot"></a>トラブルシューティング

1. トラブルシューティング ファイルをダウンロードします。 詳細については、[トラブルシューティングのためにデバッグ モードを有効にする](tcs-troubleshooting-enable-debug-mode.md)を参照してください。
2. 税サービス計算の入力と機能の設定とを比較して、設定の問題を修正します。

    次の例で、税サービス計算入力を示します。

    ```json
    ===============================Tax service calculation input JSON:=====================================
    {
        "TaxableDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            ...
                        }
                    ],
                    "Business Process": "Sales",
                    "Ship From Zip Code": "30159",
                }
            ]
        },
        "Parameter": {
            ...
        },
        "Adjustment": {
            "Lines": {}
        }
    }
    ```

    次の表に、RCS の税グループの適用性を示します。

    | Header.Business プロセス | Lines.Business ユニット | 郵便番号からの Header.Ship | 税グループ |
    |-------------------------|---------------------|---------------------------|-----------|
    | 仕訳                 |                     |                           | グループ A   |
    | 営業                   |                     | 30160                     | グループ B   |

    税サービス計算入力のに従い、ヘッダーの **業務プロセス** の値は **販売**、ヘッダーの **郵便番号から出荷** の値は **30159** です。 この入力は、RCS の適用性ルールの設定に基づいています。 一致する行がないので、エラーが発生します。

    > [!NOTE]
    > 適用性ルールの値が空白の場合、そのルールは任意の値に適用できます。

## <a name="mitigation"></a>軽減策

エラーを軽減するには、次の手順に従います。

1. RCS で、**グローバリゼーション機能**\> **税計算** の順にクリックします。
2. 新しいバージョンの機能を作成します。
3. 対応する情報の明細行を追加します。

    | Header.Business プロセス | Lines.Business ユニット | 郵便番号からの Header.Ship| 税グループ |
    |-------------------------|---------------------|--------------------------|-----------|
    | 仕訳                 |                     |                          | グループ A   |
    | 営業                   |                     | 30160                    | グループ B   |
    | 営業                   |                     | 30159                    | グループ B   |

4. 機能設定バージョンを公開します。
5. Microsoft Dynamics 365 Finance で、**税** \> **設定** \> **税コンフィギュレーション** \> **税計算のパラメーター** の順に移動し、新しいバージョンを選択します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
