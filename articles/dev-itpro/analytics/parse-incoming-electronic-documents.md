---
title: "アプリケーションのデータを更新するために受信したドキュメントを解析する"
description: "このトピックでは、受信したドキュメントを解析し、選択したコンテンツをアプリケーション データに適用して更新できるように電子報告 (ER) 形式を設定する方法について説明します。"
author: nickselin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2017-11-10
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 5d2d9e52833f345ca2c555a429429a62d1e7c315
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---
# <a name="parse-incoming-documents-to-update-application-data"></a>アプリケーションのデータを更新するために受信したドキュメントを解析する
[!include [banner](../includes/banner.md)]

電子申告 (ER) 書式をデザインして Microsoft Dynamics 365 for Finance and Operations 内で実行し、受信した電子ドキュメントを解析し、その内容を使用してアプリケーション データを更新することができます。

導入された次の新しい ER 機能は、XML 形式の受信する電子ドキュメンの解析を改善します。

- **CASE** 形式要素は、XML 形式の受信電子ドキュメントを解析するように構成された ER 形式のルート要素として使用することができます。 **FILE** 形式要素は、**CASE** 要素の入れ子になった要素としてサポートされます。 したがって、1 つの ER フォーマットを設定して、異なるルート XML 要素を含む可能性のある受信電子ドキュメントを解析することができます。
- **入れ子になった要素の順序を解析**属性が ER 形式の XML 形式要素に導入されました。 この属性を使用すると、読み込まれるファイルで予期される 1 つの XML 要素を定義することができます。 ネストされた要素には 2 つの有効なシーケンスがあります。

    - **形式どおり** - 受信ファイルは、ファイル内の入れ子になった要素の順序は、ER 形式に記載されている順序と同じ場合に有効です。
    - **任意** - 着信ファイルは、そのファイル内の順番に関係なく、ER 形式のすべての入れ子になった要素が解析ファイルに存在する場合に有効です。

この機能の詳細をよく理解するためには、タスク ガイド、\[ER - 受信ドキュメントを解析してアプリケーション データを更新する\] (「7.5.4.3 IT サービス/ソリューション コンポーネントの取得/開発」(10677) ビジネス プロセスの一部) を再生します。 このタスク ガイドは、Web サービスからの応答を ER 形式を使用して解析する方法を説明しています。

タスク ガイドのいくつかの手順を完了するには、次のファイルをダウンロードする必要があります。

| コンテンツの説明           | ファイル                                                              |
--------------------------------|-------------------------------------------------------------------|
| ER データ モデル構成   | [EFSTAmodel.xml](https://go.microsoft.com/fwlink/?linkid=862266)  |
| ER フォーマット構成       | [EFSTAformat.xml](https://go.microsoft.com/fwlink/?linkid=862266) |
| Web サービス応答サンプル 1 | [Response1.xml](https://go.microsoft.com/fwlink/?linkid=862266)   |
| Web サービス応答サンプル 2 | [Response2.xml](https://go.microsoft.com/fwlink/?linkid=862266)   |
| Web サービス応答サンプル 3 | [Response3.xml](https://go.microsoft.com/fwlink/?linkid=862266)   |
| Web サービス応答サンプル 4 | [Response4.xml](https://go.microsoft.com/fwlink/?linkid=862266)   |


