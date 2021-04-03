---
title: ワークフロー内の並列分岐のコンフィギュレーション
description: 並列分岐をコンフィギュレーションするには、ワークフロー エディターで次の手順を実行します。
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37c177e8c4c4e40bd81287430d9ee7598cf917d8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566994"
---
# <a name="configure-parallel-branches-in-a-workflow"></a>ワークフロー内の並列分岐のコンフィギュレーション

[!include [banner](../includes/banner.md)]

並列分岐をコンフィギュレーションするには、ワークフロー エディターで次の手順を実行します。

並列分岐は、基本的に、親ワークフローのコンテキストで実行されるワークフローです。

## <a name="name-a-branch"></a>分岐に名前をつける

並列分岐の名前を入力するには、次の手順に従います。

1. 並列分岐を右クリックし、**プロパティ** をクリックします。 **プロパティ** フォームが表示されます。
2. 左ウィンドウで **基本設定** をクリックします。
3. **名前** フィールドに、並列分岐の一意な名前を入力します。
4. **閉じる** をクリックします。

## <a name="design-and-configure-the-elements-of-a-branch"></a>分岐の要素のデザインとコンフィギュレーション

並列分岐の要素のデザインとコンフィギュレーションを行うには、次の手順に従います。

1. 並列分岐をダブルクリックします。
2. 他のワークフローを作成する場合と同様に、ワークフロー要素をキャンバスにドラッグし、要素をコンフィギュレーションします。 詳細については、[ワークフロー作成の概要](create-workflow.md)を参照してください。

## <a name="additional-resources"></a>追加リソース

[ワークフローの作成の概要](create-workflow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]