---
title: ユーザー指定のチームの所有者
description: このトピックでは、既定のチーム所有者を使用する代わりに、ユーザー指定のチーム所有者を設定する方法について説明します。
author: sabinn-msft
ms.date: 04/26/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2021-04-26
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c59b4d31a6bebbacb6df4af0b36f5482cf7b1f06
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346534"
---
# <a name="user-specified-team-owner"></a>ユーザー指定のチームの所有者

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Finance and Operations アプリでは、グローバル テーブルは会社または法人に関連付けられません。 これらのテーブルでは、二重書き込みを使用して Microsoft Dataverse に書き込む場合、チームを指定することができますが、所有者として既定のチームを使用できません。 

既定では、二重書き込みを有効にする場合、ルートの事業単位の既定チームは二重書き込みを通して統合されたすべての行の既定の所有者になります。 これらのレコードへのアクセスをユーザーのサブセットに限定する場合は、これは必要ではないかもしれません。 組織が対応するチームを持つ事業単位で複数の部門を定義し、その下に対応するチームを持つのは珍しいことではありません。 既定のチームのすべてのユーザーによって、二重書き込みを介して統合されたすべてのレコードにアクセスされることを望まないとします。 このような場合は、それらのレコードの所有者として、グローバル テーブルごとに異なるチームを指定できます。 

## <a name="change-the-owning-team"></a>所有チームの変更

**テーブル マッピング** で、**グローバル製品** のようなグローバル テーブル マップを選択する場合、**所有チームの更新** セクションでチームのリストを表示できます。 既定では、二重書き込みでは既定のチームが使用され、これは空白の値で示されます。 新しいバージョンで新しいマップを作成した後に、所有チームの一覧から新しいチームをピッキングして新しい値を保存することで、既定の動作を変更します。 **所有チーム** フィールドには次のスクリーンショットが表示されます。

:::image type="content" source="media/owning-team-1.png" alt-text="所有チームの更新。":::
  
>[!NOTE]
> 所有チームを設定した後は、初期同期とライブ同期の両方を実行できます。所有チームの設定は、環境をまたがって転送されません。 

## <a name="view-the-owning-team-after-initial-sync"></a>初期同期後の所有チームの表示

初期同期を実行した後、統合されたレコードに所有者が表示されます。 次のスクリーンショットでは、所有者は **グローバル製品** テーブル マップで、統合されたレコードのために **dwteam** を **売上** に変更しました。　
  
:::image type="content" source="media/owning-team-2.png" alt-text="既定およびユーザー指定のチームとの初期同期。":::
  
[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
