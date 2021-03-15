---
title: 電子申告の生成および ER によるアプリケーション データの更新
description: 送信する電子ドキュメントを生成するために、アプリケーションで使用できる電子申告 (ER) 形式をデザインできます。
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ae3405a882ac37fd9758d8ff0902896562fa06b
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093876"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a>ER を使用して電子ドキュメントを生成し、アプリケーション データを更新する

[!include [banner](../includes/banner.md)]

送信する電子ドキュメントを生成するために、アプリケーションで使用できる電子申告 (ER) 形式をデザインできます。 受信した電子ドキュメントを解析し、これらのドキュメントの内容を使用してアプリケーション データの更新を行う ER 形式をデザインすることもできます。

この機能により、送信する電子ドキュメントを生成しアプリケーション データを更新するのに、1 つの ER 形式を使用できます。 この機能は以下のシナリオでも使用できます。

- その後のプロセスでアプリケーション データが繰り返し使用されないために、電子ドキュメントを生成するのに使用した直後にアプリケーション データをマークできます。 たとえば、支払トランザクションが生成された支払メッセージに含められた直後に、既に処理済みとしてマークすることができます。
- ER ロジックを使用して生成された電子ドキュメントの処理の詳細を格納します。 たとえば、固有の支払メッセージ ID は ER 式を使用して生成されます。 ER 形式がドキュメントを生成するために実行される場合、式は ER ダイアログ ボックスに入力された情報に基づいています。

この機能の詳細についてさらに知るには、イントラスタットのレポート作成とアーカイブの詳細について説明している、アプリケーションデータ更新のタスクガイド (7.5.4.3 ITサービス/ソリューションコンポーネントの取得/開発（10677）ビジネスプロセスの一部) を使用してER Generate ドキュメントのセットを再生します。 次のファイルでは、これらのタスク ガイド内の特定の手順を実行する必要があります。 ローカル コンピューターにダウンロードし、これらのファイルを保存します。

- [ER データ モデル コンフィギュレーション: イントラスタット (モデル)](https://go.microsoft.com/fwlink/?linkid=849038)
- [ER モデル マッピング コンフィギュレーション: イントラスタット (マッピング)](https://go.microsoft.com/fwlink/?linkid=849038)
- [ER 形式コンフィギュレーション: イントラスタット (形式)](https://go.microsoft.com/fwlink/?linkid=849038)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]