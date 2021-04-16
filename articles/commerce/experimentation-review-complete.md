---
title: バリエーションのレベルを上げて実験を完了する
description: このトピックでは、Dynamics 365 Commerce のバリエーションのレベルを正常に上げて、実験を完了する方法について説明します。
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 0ea0fc8d50c25312b184ec1d3bd613695870d121
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792562"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>バリエーションのレベルを上げて実験を完了する

このトピックでは、実験で最良の結果が得られたバリエーションのレベルを上げる方法と実験を完了する方法について説明します。 次の図は、Dynamics 365 Commerce の電子商取引 web サイトでの実験の設定と実行に関連するすべての手順を示しています。 追加の手順については、個別のトピックで説明します。

[![実験ユーザー体験 - 確認と完了](./media/experimentation_review_complete.svg)](./media/experimentation_review_complete.svg#lightbox)

[実験を実行](experimentation-run-monitor.md) して、実際のサイトで使用するバリエーションを決定するのに十分なデータを収集したら、バリエーションのレベルを上げて実験を終了します。

## <a name="promote-a-variation"></a>バリエーションのレベルを上げる
サードパーティ サービスの実験に関連するデータと分析を使用して、どのバリエーションが最適な結果を得たかを判断します。 実際のサイトの現在のコンテンツを、より最適なバリエーションに置き換えて、Web サイトのすべてのユーザーが使用できるようにするには、次の操作を行います。

最適なバリエーションに置き換えるには、次の手順に従います。 

1. Commerce のサイト ビルダーで **実験** を選択し、 対象の実験を選択します。
1. 上部のコマンド バーで **実験の完了** を選択します。
1. **実験の完了** ダイアログ ボックスで、**実験データの確認** を選択します。 サードパーティ サービスが開き、メトリックスを検証して、どのバリエーションが最も効果的かを判断します。
1. **実験の完了** ダイアログ ボックスで、最適なバリエーションを選択して、**次へ** を選択します。
1. サードパーティ サービスを開いて、実験を停止します。
1. サイト ビルダーで、**完了** を選択して、元の実際のページを上書きし、成功するバリエーションを公開して、Web サイトのすべてのユーザーが使用できるようにします。 

> [!NOTE]
> 現在の実際のページを保持し、バリエーションを公開しないことを選択した場合は、**元のページの再公開** を選択します。

## <a name="delete-your-experiment"></a>実験の削除
Commerce で完了した実験を削除する必要はありませんが、容量を節約したり、ワークスペースをクリーンアップするために、実験を削除することを選択できます。 

Commerce サイト ビルダーで実験を削除するには、次の手順に従います。

1. 左のナビゲーション ペインで **実験** を選択し、 対象の実験を選択します。 
    > [!NOTE]
    > 実験がまだ有効な場合は、続行する前にサードパーティサービスの実験を停止してください。
1. コマンド バーの **発行取り消し** を選択して、実際のサイトからバリエーションのコンテンツを削除します。
1. **削除** を選択して実験を削除します。

## <a name="previous-step"></a>前のステップ
[実験の実行と監視](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]