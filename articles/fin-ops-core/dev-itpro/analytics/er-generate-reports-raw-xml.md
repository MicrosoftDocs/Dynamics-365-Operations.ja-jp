---
title: コンテンツを XML のままで追加してレポートを生成する
description: XML 形式で送信ドキュメントを生成する電子申告 (ER) 形式をデザインできます。
author: NickSelin
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 3e007b4feac612ecf74f60dd8a87d76efc7ab4c7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752795"
---
# <a name="generate-reports-by-adding-content-as-raw-xml"></a>コンテンツを XML のままで追加してレポートを生成する

[!include[banner](../includes/banner.md)]

XML 形式で送信ドキュメントを生成する電子申告 (ER) 形式をデザインするための、新しい **未加工の XML** 形式要素を使用できます。 場合によっては、次の 1 つ以上の理由により未加工の XML データをこれらのレポートに追加します。

- XML 構造がランタイム式を実行することによって自動生成されるため、レポートの元のデザインおよび継続的なメンテナンスに対する未加工の XML を使用する方がより便利です。 したがって、デザイン時に複数のバインディングを複数の形式要素に対して特定する必要はありません。 使用しているデータ ソースに、レポートの生成時に XML 要素を構成するのに使用される情報が含まれる場合もあります。
- 以前に受信されシステムに格納された XML コンテンツでレポートを入力するのに使用できる他のメソッドはありません。 たとえば、生成される XML 応答には、以前に送信された XML 要求のコンテンツが含まれる必要があります。
- その数値コードに基づいて生成されるドキュメントに文字を挿入するのに使用できる他のメソッドはありません。 一部の言語および文字については、このタイプのコードは存在しません。 たとえば、ギリシャ文字 rho (ρ) と \&eacute などの HTML エンティティ コードがあります; *e* については鋭アクセント (é) があります。

> [!NOTE]
> フレームワークは、**未加工の XML** 形式要素を使用して生成されるドキュメントに配置される XML コンテンツが正しいかどうかを制御しないことに注意してください。

この機能の詳細については、**7.5.4.3 IT サービス/ソリューション コンポーネントの取得/開発 (10677)** 業務プロセスの一部である **ER 未加工 XML データを使用して XML レポートを生成する (第 1 部: データ モデルの設計)** および **ER 未加工 XML データを使用して XML レポートを生成する (第 2 部: レポートの設計および実行)** タスク ガイドを再生し、[Microsoft ダウンロード センター](https://go.microsoft.com/fwlink/?linkid=874684) からダウンロードできます。 これらのタスク ガイドでは、生成されるファイルに未加工の XML データを挿入するための、ER 形式のコンフィギュレーションのプロセスについて説明します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]