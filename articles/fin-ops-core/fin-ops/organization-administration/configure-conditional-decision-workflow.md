---
title: ワークフローでの条件付き意思決定のコンフィギュレーション
description: 条件判断のプロパティをコンフィギュレーションするには、次の手順に従います。
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0fa708b4ac1f17a9ed6852a9eeb3e764b750a4a4
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070961"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a>ワークフローでの条件付き意思決定のコンフィギュレーション

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

条件判断のプロパティをコンフィギュレーションするには、次の手順に従います。

条件判断は、ワークフローが 2 つの分岐に分かれるポイントです。 条件判断をコンフィギュレーションするには、ワークフロー エディターで条件判断を右クリックし、**プロパティ** をクリックして、**プロパティ** フォームを開きます。

## <a name="name-a-decision"></a>名前の設定

条件判断の名前を入力するには、次の手順に従います。

1. 左ウィンドウで **基本設定** をクリックします。
2. **名前** フィールドに、条件判断の固有の名前を入力します。

## <a name="set-conditions"></a>条件の設定

使用される分岐は、提出されたドキュメントが特定の条件を満たすかどうかをシステムが評価して決定します。

1. 左ウィンドウで **基本設定** をクリックします。
2. **条件の追加** をクリックします。
3. 条件を入力します。
4. 必要に応じて、追加条件を入力します。
5. 入力した条件が正しくコンフィギュレーションされていることを確認するには、次の手順を実行します。

    1. **テスト** をクリックして、**ワークフロー条件のテスト** フォームを開きます。
    2. フォームの **条件の検証** 領域でレコードを選択します。
    3. **テスト** をクリックします。 システムによってレコードが評価され、定義した条件を満たすかどうかが判定されます。
    4. **OK** または **キャンセル** をクリックして、**プロパティ** フォームに戻ります。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]