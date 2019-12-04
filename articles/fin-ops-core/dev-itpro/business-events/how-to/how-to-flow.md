---
title: ビジネス イベントと Microsoft Power Automate
description: このトピックでは、コネクタを使い Microsoft Power Automate で使用可能なビジネス イベントに関する情報を提供します。
author: ibenbouzid
manager: AnnBe
ms.date: 11/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: imbenbou
ms.search.validFrom: Platform update 27
ms.dyn365.ops.version: 2019-6-30
ms.openlocfilehash: a823ea5c0033059b3b78ab7d32852a140388e531
ms.sourcegitcommit: ae0efac749ab34d423fac44d00a597801c143fbb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/22/2019
ms.locfileid: "2830222"
---
# <a name="business-events-and-microsoft-power-automate"></a>ビジネス イベントと Microsoft Power Automate

[!include[banner](../../includes/banner.md)]

このトピックでは、Power Automate エンドポイントからビジネスイ ベントを設定および使用する手順を示します。

このトピックでは、以下のタスクを実行する方法について説明します:

-   Power Automate で、新しいフローを作成します。
-   ビジネス イベントのトリガー

## <a name="create-a-new-flow-in-power-automate"></a>Power Automate で、新しいフローを作成する

1.  Power Automate portal にサインインします。

2.  Power Automate リソースを作成するために必要なアクセス許可のある既存の環境を選択します。 既定の環境は、すべての会社に対して開かれています。

3.  **空白から新規 \> を作成する**選択します。

4.  **Dynamics 365 for Finance and Operations** を検索して、コネクタを選択します。
     
5.  **ビジネス イベントが発生した場合**という名称のトリガーを確認できます。 このトリガーを選択します。

6.  環境インスタンス、カテゴリ、イベント名称、法的エンティティを選択します。 
    > [!TIP]
    > 環境インスタンス URL の一部またはイベント名の一部のみを入力することで Power Automate が提供するオート コンプリート機能を利用できます。

    <img alt="Microsoft Power Automate buisness event trigger" src="../../media/BEF-Howto-Flow-04.png" width="50%">

7.  **新規ステップ** ボタンを選択して新しいアクションを追加します。

8.  **JSON解析** データ処理を検索します。 この手順は、データ コントラクトのスキーマを使用して、メッセージを解析するために必要となります。

    <img alt="Parse JSON action " src="../../media/BEF-Howto-Flow-06.png" width="50%">

9.  **Jsonの解析** アクションの コンテンツ フィールドを選択すると、前のステップの **Body** がオプションとして表示されます。 **Body** を選択します。

    <img alt="Parse JSON input " src="../../media/BEF-Howto-Flow-07.png" width="50%">

10. コントラクトのスキーマを入力します。 アプリでは、サンプルのペイロードしか提供されないため、ペイロードからスキーマを生成する Power Automate の機能を使用することができます。 カタログ内のイベントを選択し (例えば、顧客の支払)、**スキーマのダウンロード**リンクを選択します。 テキストファイルがダウンロードされます。 テキストファイルを開き、内容をコピーします。

    <img alt="Event payload" src="../../media/BEF-Howto-Flow-08.png" width="50%">

11. Power Automate に戻り、 **サンプル ペイロードを使用してスキーマを生成する** リンクを選択します。 テキストファイルの内容を貼り付け、 **完了** を選択します。

    <img alt="Parse JSON schema input " src="../../media/BEF-Howto-Flow-09.png" width="70%">

12. サンプル ペイロードの品質により、ジェネレーターは整数と実数を区別できません。 これは、サンプル ペイロードに実数が整数として提供される場合に該当します。 生成されたスキーマを確認し、「整数」を「数値」に変更する必要があるかどうかを確認します。 (JSONでは、"数値" データ型は実数値を意味します)。

    <img alt="JSON data types " src="../../media/BEF-Howto-Flow-10.png" width="100%">

13.  ビジネス イベント コンテンツを使用するための最終アクションを選択します。 たとえば、電子メールで (または、テキストメッセージをチームに共有する) 支払の詳細を顧客に送信することができます。 **電子メールの送信** アクションを検索し、自分の Office 365 アカウントにログインします。

14.  メッセージの本文および、必須項目を入力します。

    <img alt="Microsoft Power Automate send email action " src="../../media/BEF-Howto-Flow-12.png" width="70%">

15. フローを保存します。

## <a name="trigger-a-business-event"></a>ビジネス イベント の トリガー

Power Automate では、アプリケーションを自動的にコンフィギュレーションできます。 フローを保存すると、エンドポイントが作成され、ビジネス イベントが有効となります。 イベントを起動する前に、エンドポイントが正しく構成されていることを確認する以外に、必要とされる構成手順はありません。

1. クライアントにサイン インします。

2.  **システム管理 \> 設定 \> ビジネス イベント** に移動します。

3.  **エンドポイント** を選択します。

4.  新たなエンドポイントが作成され、名称にGUIDが追加されていることを確認します。

    <img alt="Microsoft Power Automate buiness event GUID" src="../../media/BEF-Howto-Flow-13.png" width="100%">

5.  **有効なイベント** タブをオンにした場合は、法的エンティティGBSIに対し **支払転記済** が有効化されていることも確認することができます。

    <img alt="Active business events " src="../../media/BEF-Howto-Flow-14.png" width="100%">

6.  最後の手順では、転記された顧客支払のビジネス イベントをトリガーし、フローの実行と顧客の支払詳細を含む電子メールを受信するかどうかをチェックします。

## <a name="troubleshooting-a-flow"></a>フローのトラブルシューティング
トラブルシューティングの推奨事項を次に示します。
- Power Automate では、失敗したフローの問題点を特定するのに役立つ、実行の完全な履歴を提供しています。
- 失敗した実行を確認する場合は、トリガーおよびアクション ブロックの入力と出力を慎重に確認してください。 
- フローに変更が加えられたら、最新の実行または特定の実行に移動し、入力を **再送信** して、フローを再度実行します。
