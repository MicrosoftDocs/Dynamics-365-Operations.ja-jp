---
title: 変更を行っていないにもかかわらず、品目補充設定を保存するように求められます
description: 変更を行っていないにもかかわらず、品目補充設定を保存するように求められます。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 29ee23164430f219ff3d0c94216a8be43f480ce309f6cdac3dac6ed5b6d030af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730085"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a>変更を行っていないにもかかわらず、品目補充設定を保存するように求められます

KB 番号: 4615588

## <a name="symptoms"></a>現象

シナリオによっては、*品目補充 V2* エンティティを通じて品目をインポートした後に **品目補充** ページを開くと、次のメッセージが表示される場合があります:

> 閉じる前に変更内容を保存しますか?

何も変更を行っていない場合でも、このメッセージが表示されます。

## <a name="resolution"></a>解決策

**品目補充** ページには複雑な既定のロジックが含まれており、エンティティ インポートなどにより、データベースに直接変更が行われた後にメッセージが表示されることがあります。 たとえば、`AREGENERALSETTINGSOVERRIDDEN` のエンティティ フィールドは *いいえ* に設定されていますが、`PRODUCTCOVERAGEGROUPID` や `VENDORACCOUNTNUMBER` などのフィールドに新しい値や変更された値を提供するファイルをインポートします。 この場合、`AREGENERALSETTINGSOVERRIDDEN` フィールドが *いいえ* に設定されているため、**品目補充** ページをインポート後に初めて開いたときにフィールドから値が自動的にクリアされます。 メッセージ ボックスのプロンプトに従って変更を保存すると、変更内容はデータベースに保存されます。 そうしない場合は、次にページを開いた時に同じメッセージが表示されます。

この動作を回避し、エンティティ インポートで `PRODUCTCOVERAGEGROUPID` などのフィールドの値も含めるには、インポート時に `AREGENERALSETTINGSOVERRIDDEN` を *はい* に設定します。
