---
title: TaxTrans の正しくないフィールド値
description: このトピックでは、TaxTrans の正しくないフィールド値のトラブルシューティングに関する情報を提供します。
author: bijian
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 5c1c034c6037d2e8920d9744903debebb2dc537f2644093d5e1eef66f2681191
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746347"
---
# <a name="incorrect-field-value-in-taxtrans"></a>TaxTrans の正しくないフィールド値

[!include [banner](../includes/banner.md)]

**TaxTrans** のフィールド値が正しくない場合は、このトピックの情報を使用して問題を解決してください。

## <a name="overview-of-values"></a>値の概要
次のリストは、**TaxTrans**、**TaxUncommitted**、および **TmpTaxWorkTrans** がどのように類似したデータ セットであるかを示していますが、動作が異なります。

  - **TaxTrans** は、データベースに保持される最終的な転記された税トランザクションの結果です。
  - **TaxUncommitted** は、データベースに保持される中間計算税結果 (該当する場合) であり、後で転記に使用されます。
  - **TmpTaxWorkTrans** は、メモリ内テーブル (テーブル タイプ = InMemory) で一時的に計算された税の結果です。

正しくない **TaxTrans** 列の根本原因が見つかった場合は、正しくない **TaxUncommitted** 列または **TmpTaxWorkTrans** 列の根本原因も見つけました。 これは、3 つの列が互いにコピーされているためです。

通常、税額計算時に **TmpTaxWorkTrans** が生成され、該当する場合は **TaxUncommitted** が生成されます。 税転記時に、**TaxTrans** が生成されます。


## <a name="add-breakpoints"></a>ブレークポイントの追加
ブレークポイントを追加するには、次の手順を完了してください。 

1. 次に示すように、拡張機能の *insert()* および *update()* に拡張機能とブレークポイントを追加します。

     - **TaxTrans**

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TaxUncommitted**

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TmpTaxWorkTrans**

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. または、**TaxUncommitted** が含まれていない場合、ブレークポイントを直接追加できます。

     - *TaxTrans.insert()*、*TaxTrans.update()*
     - *TmpTaxWorkTrans.insert()*、*TmpTaxWorkTrans.update()*

## <a name="reproduce-and-debug"></a>再現とデバッグ

ブレークポイントが設定された後、デバッグ中にすべてのデータ持続性の変更が表示されます。 **TaxTrans**、**TaxUncommitted**、または **TmpTaxWorkTrans** の正しくない列の根本原因を見つけるには、次の項目を確認してメモします。

- 列が正しい最後のブレークポイント。
- 列が正しくない最初のブレークポイント。
- これらの 2 つのポイントの間に何が起こるか。

## <a name="determine-whether-customization-exists"></a>カスタマイズが存在するかどうかの確認
前のセクションの手順を完了しても問題を解決できない場合は、カスタマイズが存在するかどうかを確認します。 カスタマイズが存在しない場合は、Microsoft サポートに問い合わせてください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

