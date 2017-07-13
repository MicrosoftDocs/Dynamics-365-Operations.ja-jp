---
title: "電子申告ツールを使用して、電子ドキュメントを生成し、およびアプリケーション データを更新します"
description: "送信する電子ドキュメントを生成するために、Finance and Operations アプリケーションで使用できる電子申告 (ER) 形式をデザインできます。 受信した電子ドキュメントを解析し、これらのドキュメントの内容を使用してアプリケーション データの更新を行う ER 形式をデザインすることもできます。"
author: kfend
manager: AnnBe
ms.date: 05/11/2017
ms.topic: article
ms.prod: 
ms.service: Lifecycle Services
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.2, Operations
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d37d20b26d8ae755a6c5a688afd1ad0541d1f693
ms.openlocfilehash: 7e4e0acb374fe091c0e099355204116345c62997
ms.contentlocale: ja-jp
ms.lasthandoff: 06/13/2017

---


送信する電子ドキュメントを生成するために、Finance and Operations アプリケーションで使用できる電子申告 (ER) 形式をデザインできます。 受信した電子ドキュメントを解析し、これらのドキュメントの内容を使用してアプリケーション データの更新を行う ER 形式をデザインすることもできます。 

この機能により、送信する電子ドキュメントを生成しアプリケーション データを更新するのに、1 つの ER 形式を使用できます。 この機能は以下のシナリオでも使用できます。

- その後のプロセスでアプリケーション データが繰り返し使用されないために、電子ドキュメントを生成するのに使用した直後にアプリケーション データをマークできます。 たとえば、支払トランザクションが生成された支払メッセージに含められた直後に、既に処理済みとしてマークすることができます。
- ER ロジックを使用して生成された電子ドキュメントの処理の詳細を格納します。 たとえば、固有の支払メッセージ ID は ER 式を使用して生成されます。 ER 形式がドキュメントを生成するために実行される場合、式は ER ダイアログ ボックスに入力された情報に基づいています。

この機能の詳細については、一連の「ER 生成ドキュメントとアプリケーション データ更新」タスク ガイド (7.5.4.3 IT サービス / ソリューション コンポーネントの取得 / 開発 (10677) ビジネス プロセスの一部) を再生します。 次のファイルでは、これらのタスク ガイド内の特定の手順を実行する必要があります。 ローカル コンピューターにダウンロードし、これらのファイルを保存します。

- [ER データ モデル コンフィギュレーション: イントラスタット (モデル)](https://go.microsoft.com/fwlink/?linkid=849038)
- [ER モデル マッピング コンフィギュレーション: イントラスタット (マッピング)](https://go.microsoft.com/fwlink/?linkid=849038)
- [ER 形式コンフィギュレーション: イントラスタット (形式)](https://go.microsoft.com/fwlink/?linkid=849038)

