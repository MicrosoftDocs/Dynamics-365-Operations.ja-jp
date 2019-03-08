---
title: 口座取引明細書ファイルのインポートのトラブルシューティング
description: 銀行からの口座取引明細書ファイルが、Microsoft Dynamics 365 for Finance and Operations がサポートするレイアウトと一致することが重要です。 口座取引明細書の基準が厳しいために、ほとんどの統合が正しく動作します。 ただし、明細書ファイルがインポートできない場合または不正確な結果が含まれている場合があります。 通常、これらの問題は口座取引明細書ファイルの小さな差異によって引き起こされます。 この記事は、これらの差異を修正し問題を解決する方法を説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4006bf35673e3bb61bcf11619ecc68d295f29eb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "324448"
---
# <a name="bank-statement-file-import-troubleshooting"></a>口座取引明細書ファイルのインポートのトラブルシューティング

[!include [banner](../includes/banner.md)]

銀行からの口座取引明細書ファイルが、Microsoft Dynamics 365 for Finance and Operations がサポートするレイアウトと一致することが重要です。 口座取引明細書の基準が厳しいために、ほとんどの統合が正しく動作します。 ただし、明細書ファイルがインポートできない場合または不正確な結果が含まれている場合があります。 通常、これらの問題は口座取引明細書ファイルの小さな差異によって引き起こされます。 この記事は、これらの差異を修正し問題を解決する方法を説明します。

<a name="what-is-the-error"></a>エラーは何ですか?
------------------

口座取引明細書ファイルのインポートを試行した後に、データ管理ジョブ履歴および実行の詳細に移動し、エラーを検索します。 エラーは、明細書、残高、または明細行を指し示すのに役立ちます。 ただし、問題の原因となっているフィールドまたは要素を識別するために十分な情報を提供することは少ないです。

## <a name="what-are-the-differences"></a>差異は何ですか?
銀行ファイル レイアウト定義を Finance and Operations のインポート定義と比較し、フィールドおよび要素の差異を確認します。 口座取引明細書ファイルを関連する Finance and Operations ファイルのサンプルと比較します。 ISO20022 ファイルでは、差異が一目で分かります。

## <a name="transformations"></a>変換
通常、変更は次の 3 つの変換のいずれかで行われます。 各変換は、指定された標準形式で書き込まれます。

| リソース名                                         | ファイル名                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>デバッグの変換
### <a name="adjust-the-bai2-and-mt940-files"></a>BAI2 と MT940 ファイルの調整

BAI2 と MT940 ファイルはテキスト ベースのファイルで、XSLT (Extensible Stylesheet Language Transformations) デバッグを有効にするためには調整が必要です。 プログラムは、ファイルのインポート時にこの調整を行います。

1.  XML ファイルを作成し、次のテキストをコピーします。

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  口座取引明細書ファイルの内容をコピーし、XML ファイルに貼り **PASTESTATEMENTFILEHERE** を置換します。

### <a name="debug-the-xslt"></a>XSLT のデバッグ

詳細については、「<https://msdn.microsoft.com/en-us/library/ms255605.aspx>」を参照してください。

1.  Microsoft Visual Studio を起動します。
2.  コンソール アプリケーションを作成します。
3.  適切な XSLT を開きます。
4.  XLST とプロパティ ページをクリックします。
5.  口座取引明細書ファイルの場所の入力を設定します。
6.  出力の場所とファイル名を定義します。
7.  必要な区切り点を設定します。
8.  メニューで、**XML** &gt; **XSLT デバッグの開始** をクリックします。

### <a name="format-the-xslt-output"></a>XSLT 出力の書式設定

変換を実行すると、Visual Studio で表示可能な出力ファイルを作成します。 Ctrl+A、Ctrl+K と Ctrl+D を使用して、出力ファイルをすばやく書式設定します。

### <a name="adjust-the-transformation"></a>変換の調整

口座取引明細書ファイルの適切なフィールドまたは要素を得るために変換を調整します。 次に適切な Finance and Operations の要素にそのフィールドまたは要素をマップします。

### <a name="debitcredit-indicator"></a>借方/貸方インジケーター

場合によっては、借方は貸方としてインポートされ、貸方が借方としてインポートされる場合があります。 この問題を解決するには、適切な XSLT を変更する必要があります。 口座取引明細書を複数の銀行から取得する場合、すべてが同じ借方/貸方を使用しているか、または別の変換を作成していることを確認してください。

-   BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator テンプレート
-   ISO20022XML-to-Reconcilation.xslt GetCreditDebit テンプレート
-   MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator テンプレート

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>口座取引明細書の形式と技術的な配置の例
次の表は、詳細な口座調整のインポート ファイルの技術的な配置の定義、および 3 つの関連する口座取引明細書のサンプル ファイルの一覧を表示します。 サンプル ファイルと技術的な配置はここでダウンロードできます。https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  


| 技術的なレイアウトの定義                             | 口座取引明細書のサンプル ファイル          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |





