---
title: "ワークフローでの条件付き意思決定のコンフィギュレーション"
description: "条件判断のプロパティをコンフィギュレーションするには、次の手順に従います。"
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 3bba3d849d02cd84c2c0e0c5c15f7b649b3e125c
ms.lasthandoff: 03/31/2017


---

# <a name="configure-a-conditional-decision-in-a-workflow"></a>ワークフローでの条件付き意思決定のコンフィギュレーション

[!include[banner](../includes/banner.md)]


条件判断のプロパティをコンフィギュレーションするには、次の手順に従います。

条件判断は、ワークフローが 2 つの分岐に分かれるポイントです。 条件判断をコンフィギュレーションするには、ワークフロー エディターで条件判断を右クリックし、[**プロパティ**] をクリックして、[**プロパティ**] フォームを開きます。

## <a name="name-a-decision"></a>名前の設定
条件判断の名前を入力するには、次の手順に従います。
1.  左ウィンドウで [**基本設定**] をクリックします。
2.  [**名前**] フィールドに、条件判断の固有の名前を入力します。

## <a name="set-conditions"></a>条件の設定
使用される分岐は、提出されたドキュメントが特定の条件を満たすかどうかをシステムが評価して決定します。
1.  左ウィンドウで [**基本設定**] をクリックします。
2.  [**条件の追加**] をクリックします。
3.  条件を入力します。
4.  必要に応じて、追加条件を入力します。
5.  入力した条件が正しくコンフィギュレーションされていることを確認するには、次の手順を実行します。
    1.  [**テスト**] をクリックして、[**ワークフロー条件のテスト**] フォームを開きます。
    2.  フォームの [**条件の検証**] 領域でレコードを選択します。
    3.  [**テスト**] をクリックします。 システムによってレコードが評価され、定義した条件を満たすかどうかが判定されます。
    4.  [**OK**] または [**キャンセル**] をクリックして、[**プロパティ**] フォームに戻ります。






