---
title: 勘定構造のアクティブ化のパフォーマンス強化
description: この記事では、勘定構造のアクティブ化プロセスに対する新たなパフォーマンス強化について説明します。
author: RyanCCarlson2
ms.date: 10/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-10-08
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: 42f8fcebba6465261489f74a9bb1dd46c2d5fa16
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/22/2022
ms.locfileid: "9714002"
---
# <a name="account-structure-activation-performance-enhancement"></a>勘定構造のアクティブ化のパフォーマンス強化

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

このパフォーマンス強化により、複数のトランザクションの更新を同時に実行することで、勘定構造をさらに迅速にアクティブ化できるようになります。 また、検証後に構造自体がアクティブとしてマークされ、既存の未転記トランザクションが新しい構造に更新される間、トランザクション処理を続行できます。 トランザクションの更新には時間がかかる場合があるため、**勘定構造** ページのグリッドの上の **アクティブ化状態の表示** を選択することで、アクティブ化の状態を追跡できます。 また、アクション ペインで **表示** を選択し、ドロップダウン メニューで **アクティブ化の状態** を選択することで、アクティブ化の状態を表示することもできます。

[![勘定構造ページ。](./media/AccountStructure1.png)](./media/AccountStructure1.png)

**アクティブ化状態の表示** を選択すると、アクティブ化プロセスの一環として実行されている個々のタスクを示すダイアログ ボックスが表示されます。 各タスクについて状態を確認できるほか、タスクの完了後は完了日時を確認できます。

[![勘定構造のアクティブ化のタイムライン。](./media/AccountStructureTimeline.png)](./media/AccountStructureTimeline.png)

## <a name="account-structure-activation-tips"></a>勘定構造のアクティブ化のヒント

ドラフトの勘定構造に対して **アクティブ化** を選択した場合に表示される [勘定構造の有効化] ダイアログ ボックスには、**未転記のトランザクションの更新** という名前のタブ セクションがあります。 このセクションには、**強制的に更新する** という名前のオプションが含まれています。 すべての未転記のトランザクションを現在の構造に更新する場合は、このオプションを選択できます。 ただし、このオプションは、エラーが発生した場合、または Microsoft サポートから指示された場合にのみ使用してください。

アクティブ化プロセスのパフォーマンスに影響を与える可能性がある要因を次に示します。

- 大量の未転記の仕訳帳レコード
- 自由書式の請求書や仕入先請求書のほか、元伝票フレームワークを使用し、未処理の勘定配賦を含んでいる関連ドキュメントなどの大量の未処理の元伝票レコード
- TaxUncommitted のデータ量
- オープン予算データの量
- アクティブ化タスクの実行中の仕訳帳データのインポート

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
