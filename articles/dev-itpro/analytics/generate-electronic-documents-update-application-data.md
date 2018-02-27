---
title: "電子申告ツールを使用して、電子ドキュメントを生成し、およびアプリケーション データを更新します"
description: "送信する電子ドキュメントを生成するために、Finance and Operations アプリケーションで使用できる電子申告 (ER) 形式をデザインできます。 受信した電子ドキュメントを解析し、これらのドキュメントの内容を使用してアプリケーション データの更新を行う ER 形式をデザインすることもできます。"
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7378c1d205b9a9cd61044dc33fc52ff75c6b94b7
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="generate-electronic-documents-and-update-application-data-using-the-electronic-reporting-tool"></a>電子申告ツールを使用して、電子ドキュメントを生成し、およびアプリケーション データを更新します

[!include[banner](../includes/banner.md)]

送信する電子ドキュメントを生成するために、Finance and Operations アプリケーションで使用できる電子申告 (ER) 形式をデザインできます。 受信した電子ドキュメントを解析し、これらのドキュメントの内容を使用してアプリケーション データの更新を行う ER 形式をデザインすることもできます。 

この機能により、送信する電子ドキュメントを生成しアプリケーション データを更新するのに、1 つの ER 形式を使用できます。 この機能は以下のシナリオでも使用できます。

- その後のプロセスでアプリケーション データが繰り返し使用されないために、電子ドキュメントを生成するのに使用した直後にアプリケーション データをマークできます。 たとえば、支払トランザクションが生成された支払メッセージに含められた直後に、既に処理済みとしてマークすることができます。
- ER ロジックを使用して生成された電子ドキュメントの処理の詳細を格納します。 たとえば、固有の支払メッセージ ID は ER 式を使用して生成されます。 ER 形式がドキュメントを生成するために実行される場合、式は ER ダイアログ ボックスに入力された情報に基づいています。

この機能の詳細についてさらに知るには、イントラスタットのレポート作成とアーカイブの詳細について説明している、アプリケーションデータ更新のタスクガイド (7.5.4.3 ITサービス/ソリューションコンポーネントの取得/開発（10677）ビジネスプロセスの一部) を使用してER Generate ドキュメントのセットを再生します。 次のファイルでは、これらのタスク ガイド内の特定の手順を実行する必要があります。 ローカル コンピューターにダウンロードし、これらのファイルを保存します。

- [ER データ モデル コンフィギュレーション: イントラスタット (モデル)](https://go.microsoft.com/fwlink/?linkid=849038)
- [ER モデル マッピング コンフィギュレーション: イントラスタット (マッピング)](https://go.microsoft.com/fwlink/?linkid=849038)
- [ER 形式コンフィギュレーション: イントラスタット (形式)](https://go.microsoft.com/fwlink/?linkid=849038)

