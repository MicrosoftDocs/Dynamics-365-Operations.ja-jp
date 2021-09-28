---
title: 二重書き込み設定後に法人を編集する
description: このトピックでは、二重書き込みの設定後に、会社または法人を追加または削除する方法について説明します。
author: nhelgren
ms.date: 07/21/2020
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: nhelgren
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ad991ba994928085035c785db648176e68a3d3a
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416669"
---
# <a name="edit-a-legal-entity-after-dual-write-setup"></a>二重書き込み設定後に法人を編集する 

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



二重書き込みウィザードにより、二重書き込みの設定後に会社または法人を追加または削除することが可能になります。 これは、二重書き込み環境のリンクを解除して再リンクすることなく実行できます。 

このウィザードを使用すると、Finance and Operations アプリを Dataverse 環境にリンクすることができます。 このウィザードの一部として、1 つ以上の会社または法人を選択することもできます。 企業または法人の一覧は静的なままではなく、常に変化しています。 これは、特に段階的なロールアウトまたは買収の一部として、新しい会社を追加する必要があるためです。 これまでは、システムのダウンタイムがないと企業や法人を追加できませんでした。そのため、環境のリンクを解除して再リンクする必要がありました。 これらはすべて、特に既存のデータのために、費用が高くなる場合があります。 この機能を使用すると、既存の二重書き込み環境とのリンクを解除することなく、実稼働環境に会社を追加することができます。

## <a name="add-a-company-or-legal-entity-after-dual-write-has-been-set-up"></a>二重書き込みが設定された後の会社または法人の追加 

二重書き込みが設定された後に会社または法人を追加するには、以下の手順に従います。

1. **二重書き込みテーブル マップ** リスト ページで、**環境の詳細** ボタンを選択します。

![環境の詳細ボタンを選択します。](media/select-environment-details.png)

2. **法人** タブには、環境をリンクするための二重書き込みウィザードで選択した会社が表示されます。 この例では、会社は USMF です。

![選択した会社が表示されている法人タブ。](media/legal-entities.png)

3. **法人を追加** を選択して、1 つ以上の会社を二重書き込みに追加します。 この例では、GBSI です。 **保存** を選択します。

![新しい法人を追加します。](media/add-legal-entity.png)

  この時点で、法人は更新を開始します。 現在実行中または一時停止中のテーブル マップは、既存のデータをコピーすることによって初期書き込みプロセスを実行します。 プロセスが完了するまでは、テーブル マップを変更するアクションは実行しないことをお勧めします。 

![法人の更新が進行中です。](media/update-progress.png)

  >[!NOTE]
  > この操作は、次のいずれかの条件に当てはまる場合に失敗することがあります。 
  >
  > * 1 つ以上のテーブル マップが既に初期書き込みの状態になっているときに、新しい会社を追加または削除します。 これは、システムが既存のデータをコピーするプロセスです。 
  >
  > * 1 つ以上のテーブル マップが一時停止の状態になっているときに、会社を削除します。 

4. プロセスが完了すると、法人が正常に更新されたことを示すバナーが表示されます。 これで、テーブル マップの更新を再開することができます。 

![法人の更新に成功しました。](media/legal-entities-updated.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]