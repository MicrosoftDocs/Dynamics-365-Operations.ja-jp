---
title: JSON 形式で受信したドキュメントを解析する
description: このトピックでは、受信した JavaScript Object Notation (JSON) 形式のドキュメントを解析するように電子報告 (ER) 形式を設定する方法について説明します。
author: kfend
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 4e598dc15b619c2f6a0525ea18c371484ca26fa4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755157"
---
# <a name="parse-incoming-documents-in-json-format"></a>JSON 形式で受信したドキュメントを解析する

[!include[banner](../includes/banner.md)]

JavaScript に基づくテキスト形式 (つまり、JavaScript Object Notation \[JSON\] 形式のファイル) のデータを表す、受信した電子ドキュメントを解析するよう、電子申告 (ER) 形式をデザインすることができます。

この機能の詳細については、次のテーブルに示すファイルをダウンロードし、外部 JSON ファイルからデータをインポートするための形式コンフィギュレーションの ER 作成というタスク ガイドを再生します。 このタスク ガイドは、受信する JSON ファイルを解析し、アプリケーション データを更新するために ER 形式を使用する方法を説明します。

| 肩書き                                  | ファイル名 |
|----------------------------------------|-----------|
| ER フォーマット構成                | [仕入先の trans_JSON.xml をインポートするための形式](https://go.microsoft.com/fwlink/?linkid=874111) |
| .csv 形式の受信ファイルのサンプル | [1099entries_JSON.txt](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a>必要量

外部 JSON ファイルからデータをインポートするための形式コンフィギュレーションの ER 作成のタスク ガイドを完了する前に、次の条件を満たす必要があります。

- JSON ファイルの親要素は、オブジェクト要素にのみなることができます。
- オブジェクトに対して入れ子になった要素はプロパティ要素である必要があるので、有効な JSON 構造が作成されます。
- JSON 配列は、オブジェクトのプロパティ要素に入れ子になった要素にのみなることができます。
- JSON 配列には JSON オブジェクトのみ含めることができます。 文字列、数値、および入れ子になった配列を直接含めることはできません。 これらの配列の要素は、形式内で指定されている順序で解析されます。 各 JSON オブジェクトの多様性の設定が考慮されます。

また、まだ完了していない場合は、[外部ファイルからデータをインポートするのに必要なコンフィギュレーションの ER 作成](tasks/er-required-configurations-import-data.md) タスク ガイドを完了する必要があります。 タスクガイドを完成させるには、次のファイルをダウンロードしてください。

| 肩書き                  | ファイル名 |
|------------------------|-----------|
| ER モデル構成 | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=874111) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]