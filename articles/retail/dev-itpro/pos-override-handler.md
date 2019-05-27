---
title: Retail ソフトウェア開発キット (SDK)
description: このトピックでは、Retail SDK に関する一般情報を提供します。 Retail SDK は、小売クライアントをカスタマイズするために使用できる、コード、コード サンプル、テンプレート、およびツールが含まれています。
author: RobinARH
manager: AnnBe
ms.date: 09/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 17771
ms.assetid: c54d34a5-32e2-4d0d-a1c2-4a9940d95ade
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2018-05-30
ms.dyn365.ops.version: AX 7.3.5
ms.openlocfilehash: 0fb70e2dea907f2d6becf18fdc323b65894cb09b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537546"
---
# <a name="pos-override-request-handler-sdk"></a>POS オーバーライド要求ハンドラー (SDK)

[!include [banner](../../includes/banner.md)]

このトピックでは、POS 要求ハンドラーをオーバーライドする方法について説明します。 POS ビジネス ロジックをオーバーライドするための新しい拡張パターンを導入しました。ビジネス ロジックをコア POS 業務フローに変更/追加するシナリオがある場合、このパターンに従うことができます。

例: シリアル品目を販売するとき、POS にはスキャン後にその品目のシリアル番号を入力するためのダイアログが表示されますが、コードを使用してシリアル番号を入力することでシリアル番号のプロセスを自動化する場合、このシリアル番号ハンドラーをオーバーライドしてカスタマイズできます。 POS のビジネス ロジックは、要求と応答に基づいています。 そのため、関連する要求をオーバーライドし、ビジネス シナリオに従って応答を返すことができます。

注意: すべての業務要求がカスタマイズできるように公開されるわけではありませんいくつかの要求のみオーバーライド可能です。 ビジネス ロジックをカスタマイズする場合で、その要求がオーバーライド可能でない場合、サポート チケットを作成するか、LCS 機能拡張ツールでリクエストを登録します。 この記事の後方では、オーバーライドできる要求の一覧を示します。
