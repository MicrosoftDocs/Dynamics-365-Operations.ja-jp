---
title: バリエーションのレベルを上げて実験を完了する
description: このトピックでは、Dynamics 365 Commerce のバリエーションのレベルを正常に上げて、実験を完了する方法について説明します。
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930232"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>バリエーションのレベルを上げて実験を完了する

このトピックでは、実験で最良の結果が得られたバリエーションのレベルを上げる方法と実験を完了する方法について説明します。 次の図は、Dynamics 365 Commerce の電子商取引 web サイトでの実験の設定と実行に関連するすべての手順を示しています。 追加の手順については、個別のトピックで説明します。

[![実験ユーザー体験 - 確認と完了](./media/experimentation_review_complete.svg)](./media/experimentation_review_complete.svg#lightbox)

[実験を実行](experimentation-run-monitor.md) して、実際のサイトで使用するバリエーションを決定するのに十分なデータを収集したら、バリエーションのレベルを上げて実験を終了します。

## <a name="promote-a-variation"></a>バリエーションのレベルを上げる
サードパーティ サービスの実験に関連するデータと分析を使用して、どのバリエーションが最適な結果を得たかを判断します。 実際のサイトの現在のコンテンツを、成功するバリエーションに置き換えて、Web サイトのすべてのユーザーが使用できるようにするには、次の操作を行います。 

1. サイト ビルダーの**実験**タブに移動して、実験を選択します。
1. 上部バーで**実験の完了**を選択します。
1. **実験の完了**ダイアログ メニューで、**実験データの確認**を選択します。 サードパーティ サービスが開き、メトリックスを検証して、どのバリエーションが最も効果的かを判断します。
1. サイト ビルダーの**実験の完了**ダイアログ メニューで、成功するバリエーションを選択して、**次へ**を選択します。
1. サードパーティ サービスを開いて、実験を停止します。
1. サイト ビルダーで、**完了**を選択して、元の実際のページを上書きし、成功するバリエーションを公開して、Web サイトのすべてのユーザーが使用できるようにします。 

> [!NOTE]
> 現在の実際のページを保持し、バリエーションを公開しないことを選択した場合は、**元のページの再公開**を選択します。

## <a name="delete-your-experiment"></a>実験の削除
Commerce で完了した実験を削除する必要はありませんが、容量を節約したり、ワークスペースをクリーンアップするために、実験を削除することを選択できます。 実験を削除するには、次の操作を行います。

1. サイト ビルダーの**実験**タブに移動して、実験を選択します。 
    > [!NOTE]
    > 実験がまだ有効な場合は、続行する前にサードパーティサービスの実験を停止してください。
1. コマンド バーの**発行取り消し**を選択して、実際のサイトからバリエーションのコンテンツを削除します。
1. コマンド バーで**削除**を選択し、実験を削除します。

## <a name="previous-step"></a>前のステップ
[実験の実行と監視](experimentation-run-monitor.md)
