---
title: AX 2009 の移行 － 移行グループの作成
description: この記事では、Microsoft Dynamics AX 2009 から財務と運用アプリにアップグレードするために移行グループを作成する方法について説明します。
author: kfend
ms.date: 09/13/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2018-06-21
ms.dyn365.ops.version: Platform update 17
ms.openlocfilehash: e090e1712c7661a66585268e2d7eb12540408d92
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124900"
---
# <a name="ax-2009-migration--create-migration-groups"></a>AX 2009 の移行 – 移行グループの作成

[!include [banner](../includes/banner.md)]

移行の定義を作成するときは、パッケージ化してまとめてエクスポートするエンティティを決定し、すべてのエンティティを移行グループにまとめて配置する必要があります。 移行グループは、順番に処理する必要があるか、論理的にグループ化できる一連のエンティティです。 移行グループのエンティティは、ソースからステージングまたはファイル パッケージに直接まとめてエクスポートされます。 移行グループでは、法人を関連付けることもできます。 エクスポート プロセスを開始する前に、移行グループを設定する必要があります。

移行グループを作成するには、次の手順に従います。

1. Microsoft Dynamics AX 2009 のナビゲーション ウィンドウで、**データ移行** \> **共通フォーム** \> **移行グループの作成** の順にクリックします。
2. **移行グループ** フォームで、CTRL+N を押すか **新規** をクリックして、新しい移行グループを作成します。
3. 移行グループの名前を入力します。 その後に、Tab キーを押して **会社** フィールドに移動し、**会社の選択** をクリックします。
4. **会社コードの選択** フォームで、移行グループに追加する 1 つまたは複数の会社を選択し、**OK** をクリックします。
5. **移行グループ** フォームで、**エンティティ** をクリックし、移行に含める行を選択します。
6. 必要に応じて、フィールド マッピングの空白を埋めます。
7. **順序の適用** をクリックしてフォームを閉じます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
