---
title: テスト データ転送ツールを使用した AX 2012 R3 のデモ データのインポート
description: このチュートリアルでは、テスト データ転送ツール (ベータ) を使用して Microsoft Dynamics AX 2012 R3 のデモ データをインポートします。
author: kfend
manager: AnnBe
ms.date: 01/02/2020
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 13401
ms.assetid: c16c9fb5-b1c1-4f22-a955-ff7325621a22
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: b1e397eb711ac6641d011b3ebe36507d569adef8
ms.sourcegitcommit: 632d39c992bbeea76d5b78990b6fa3341a436995
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/02/2020
ms.locfileid: "2931275"
---
# <a name="import-demo-data-for-ax-2012-r3-by-using-the-test-data-transfer-tool"></a>テスト データ転送ツールを使用した AX 2012 R3 のデモ データのインポート

[!include [banner](../../includes/banner.md)]

このチュートリアルでは、テスト データ転送ツール (ベータ) を使用して Microsoft Dynamics AX 2012 R3 のデモ データをインポートします。

AX 2012 R3 のビジネス データベースが格納されているデータベース サーバーでローカルに作業することを強くお勧めします。 これは、より高速で、インポート中のネットワーク通信の問題を回避します。

## <a name="prerequisites"></a>前提条件
**注意:** テスト データ転送ツール (ベータ) は、開発、テスト、またはデモ環境でのみ使用できます。 実稼働環境では、この手順を実行しないでください。

## <a name="download-the-demo-data-and-test-data-transfer-tool-beta"></a>デモ データおよび Test Data Transfer Tool (beta) をダウンロード
1.  AX 2012 R3 デモ データを、「[PartnerSource](https://go.microsoft.com/fwlink/?LinkId=403073)」のリリース ページからダウンロードします。
2.  デモ データをパッケージから、使用している環境用の AX 2012 R3 ビジネス データベースをホストするデータベース サーバーに抽出します。
3.  Test Data Transfer Tool (beta) ツール インストーラーを「[Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com)」の Downloadable ツール セクションからダウンロードし、使用環境に合わせて AX 2012 R3 ビジネス データべースをホストするデータベース サーバーにインストールします。
4.  データをインポートするための適切なアクセス許可があることを確認します。 デモ データが保存されている場所への読み取りアクセスが必要です。SQL Server Management Studio では、**選択** ステートメントおよび **一括挿入** ステートメントを実行するためのアクセス許可が必要です。 詳細については、 [テスト データ転送ツール (ベータ) のインストール](install-test-data-transfer-tool-beta.md) を参照してください。

## <a name="run-the-test-data-transfer-tool-beta"></a>テスト データ転送ツール (ベータ) の実行
1.  **コントロール パネル** &gt; **サービス**に移動し、環境に関連付けられている AOS インスタンスを停止します。
2.  Windows エクスプ ローラーを使用して、**テスト データ転送ツール (beta)** を参照します。
3.  Windows エクスプローラーの**ファイル**メニューで、**管理者としてコマンド プロンプトを開く**をクリックします。
4.  コマンド プロンプト で、次のコマンドを入力してデモデータをインポートします: **dp.exe import** \location\_of\_demo\_data \Name\_of\_AX\_business\_database \ServernameInstanceName. 

    ローカル コンピューター上でテスト データ転送ツール (beta) を実行していると仮定します。 ローカル コンピューターに名前付きインスタンスがある場合は、localhostInstanceName または **.** という構文を使用できます。 InstanceName. 次の例では、データが E ドライブの demodata フォルダーにあり、ビジネス データベースには MicrosoftDynamicsAX: **dp.exe import e:demodata MicrosoftDynamicsAX** と名前が付けられています。 

    > [!NOTE]
    > デモ データのインポートに 30 分以上がかかる場合があります。 インポート中に問題が発生した場合は、ログ ファイル **DPLog.xml** を開くことができ、テスト データ転送ツール (ベータ) を実行したフォルダに作成されます。
5.  **コントロール パネル** &gt; **サービス**に移動し、環境に関連付けられている AOS インスタンスを再起動します。


<a name="additional-resources"></a>追加リソース
--------

[テスト データ転送ツール (ベータ)](test-data-transfer-tool-beta-2012.md)

[テスト データ転送ツール (ベータ) のインストール](install-test-data-transfer-tool-beta.md)

[テスト データ転送ツール (ベータ) の実行](run-test-data-transfer-tool-beta.md)



