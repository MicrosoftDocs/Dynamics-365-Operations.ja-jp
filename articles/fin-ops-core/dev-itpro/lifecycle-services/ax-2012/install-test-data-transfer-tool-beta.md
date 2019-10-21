---
title: テスト データ転送ツール (ベータ) のインストール
description: このトピックでは、Microsoft Dynamics AX 2012 のテスト データ転送ツールをインストールする方法について説明します。
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 17551
ms.assetid: 1681290d-93f0-489d-9746-7793b2ffe690
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 16ae6a0f5fded1702a1131592511b36ff568b86e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183247"
---
# <a name="install-the-test-data-transfer-tool-beta"></a>テスト データ転送ツール (ベータ) のインストール

[!include [banner](../../includes/banner.md)]

このトピックでは、Microsoft Dynamics AX 2012 のテスト データ転送ツール (ベータ) をインストールする方法について説明します。 上級者のみ、このツールを使用する必要があります。 

Microsoft SQL Server の使用経験がある開発者またはデータベース管理者である必要があります。 また、処理している Microsoft Dynamics AX 2012 データベースに直接読み取り/書き込みを行って、データベースをホストしているコンピューター上で直接アプリケーションを実行するためのアクセス許可が必要です。 開始する前に、環境には次のコンポーネントが含まれている必要があります。

-   ビジネス用に構成されている Microsoft Dynamics AX 2012 データベース。
-   SQL Server 一括コピー ツール (bcp) がコマンド プロンプト パスにあるように、SQL Server クライアント ツールは、ローカル コンピューターと、データの転送先のデータベース サーバーにインストールされます。

エクスポート中に、ツールが各テーブルに対して 3 つのファイルを作成します。 エクスポートされるすべてのテーブルに対して十分なハード ディスク領域があることを確認します。

## <a name="install-the-test-data-transfer-tool-beta"></a>テスト データ転送ツール (ベータ) のインストール
1.  「[Microsoft Dynamics Lifecycle Services](http://go.microsoft.com/fwlink/?LinkId=228148)」のダウンロード可能なツール セクションからツールを取得し、ローカル フォルダーに展開します。
2.  **AX2012TestDataTransferTool.msi** を右クリックして**管理者として実行** をクリックします。
3.  **設定** **ウィザード**で、ライセンス条項に同意してからツールのバイナリおよびファイルをインストールする場所を選択します。 既定では、ツールは %Program Files%/Microsoft Dynamics AX 2012 のテスト データ転送ツール (ベータ) にインストールされています。



<a name="additional-resources"></a>追加リソース
--------

[Microsoft Dynamics AX 2012 用のテスト データ転送ツール (ベータ)](test-data-transfer-tool-beta-2012.md)

[Microsoft Dynamics AX 用のテスト データ転送ツール (ベータ) の実行](run-test-data-transfer-tool-beta.md)



