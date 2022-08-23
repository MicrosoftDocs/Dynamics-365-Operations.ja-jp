---
title: ファイル サイズとコンテンツ量に基づいて、生成された XML ファイルを分割する
description: この記事では、ファイルのサイズおよびコンテンツの品目数量に基づいて生成されるファイルを分割する方法に関する情報を提供します。
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 5347d4e85198893dd94f14508176db93ccd47c22
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280098"
---
# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a>ファイル サイズとコンテンツ量に基づいて、生成された XML ファイルを分割する

[!include[banner](../includes/banner.md)]

XML 形式で送信ドキュメントを生成するための電子申告 (ER) 形式をデザインできます。 場合によっては、それらのドキュメントは、ファイルの最大サイズまたはいくつかの XML ノードの最大数などの特定の条件を満たしている場合にのみ受領できます。 それらのドキュメントの受信者が指定する要件を満たす電子ドキュメントを生成する ER 形式をデザインできます。

- FILE 形式要素については、ER 式としてファイル サイズの制限を定義できます。 ER レポートの生成時に定義されている制限を超過した場合、ER は現在のファイルを作成し終えて次のファイルの作成に移ります。
- 任意の XML ELEMENT 形式については、ER 式として要素の数の制限を定義できます。 生成されるファイルで XML ノードの数が ER レポートの実行時に定義される制限を超過する場合、ER は現在のファイルを作成し終えて次のファイルの作成に移ります。
- 任意の XML SEQUENCE 形式要素については、ER 式として子要素の数の制限を定義できます。 生成されるファイルで形式要素の入れ子になった XML ノードの数が ER レポートの実行時に定義される制限を超過する場合、ER は現在のファイルを作成し終えて次のファイルの作成に移ります。
- 任意の XML ELEMENT 形式要素を non-breakable としてマークできます。 この方法で、単一の生成されるファイルの形式要素で生成される XML ノードの入れ子になった品目を保持できます。

XML ELEMENT および XML SEQUENCE 形式要素を使用して生成されるファイルに XML ノードを追加するだけでなく、未加工の XML 形式要素を使用できます。 ただし、未加工の XML 形式要素の使用により追加するノードは、ノードの数の計算時に要素の数の制限を評価するとは見なされません。

特定の制限を超えるたびに生成された出力を分割するように構成された FILE 形式要素のファイルの出力先をコンフィギュレーションした場合、それぞれの生成された出力が個別のファイルとして構成されたファイルの出力先に送信されます。 出力を分割して作成されるファイルに固有の名前を付けるには、FILE 形式要素の ER 式をコンフィギュレーションする必要があります。 NUMBER SEQUENCE タイプの ER データ ソースを含める場合、番号順序は個々の分割出力に対して増加します。

この機能の詳細については、**7.5.4.3 IT サービス/ソリューション コンポーネントの取得/開発 (10677)** 業務プロセスの一部である **ファイルのサイズおよびコンテンツの品目数量に基づく ER 分割 XML ファイル** タスクガイドを再生し、[Microsoft ダウンロード センター](https://go.microsoft.com/fwlink/?linkid=874684) からダウンロードできます。 このタスク ガイドでは、ファイル サイズおよびコンテンツの品目数量の制限に基づいて生成されたファイルを分割するため、ER 形式のコンフィギュレーションのプロセスについて説明します。 タスクガイドを完了するには、次のファイルをダウンロードする必要があります。

- [ER モデル コンフィギュレーション - XmlFilesSplittingModel.xml](https://download.microsoft.com/download/e/a/f/eaffe96a-22ec-4a32-898a-f4328c91c387/XmlFilesSplittingModel.xml)
- [ER 形式コンフィギュレーション - XmlFilesSplittingFormat.xml](https://download.microsoft.com/download/e/9/c/e9c5849b-8254-4cdf-bb00-4c2ebc72ddec/XmlFilesSplittingFormat.xml)

## <a name="additional-resources"></a>追加リソース
[電子申告 (ER) の送信先](electronic-reporting-destinations.md)

[電子申告 (ER) のフォーミュラ デザイナー](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
