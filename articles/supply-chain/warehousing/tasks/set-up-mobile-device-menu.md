---
title: タイプが発注書のタスクを完了するためのモバイル デバイスのメニュー項目を設定します。
description: この記事では、モバイル デバイスのメニュー項目の設定方法について説明します。
author: Mirzaab
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09286e8e482780523b61006081205868be487755
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882289"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a>タイプが発注書のタスクを完了するためのモバイル デバイスのメニュー項目を設定します。

[!include [banner](../../includes/banner.md)]

この記事では、モバイル デバイスのメニュー項目の設定方法について説明します。 この例では、メニュー項目は、発注書タイプの作業を実行するのに使用されます。 メニュー項目に関連付けられている作業クラスにより、有効な作業が決定します。 デモ データの会社 USMF でこのガイドを使用できます。 この手順は通常、倉庫マネージャーによって実施されます。


## <a name="create-a-mobile-device-menu-item"></a>品目のモバイル デバイス メニューの作成
1. **モバイル デバイス メニュー項目** を検索バーに入力して表示します。
2. **新規** を選択します。
3. **メニュー項目名** フィールドで、値を入力します。 固有値を入力してください。 たとえば、`POMove` と入力できます。 この値は後で必要になるので、記憶します。  
4. **タイトル** フィールドに値を入力します。 これは、モバイル デバイスに表示されるタイトルです。 たとえば、`PO Move` と入力できます。  
5. **モード** フィールドで、**作業** を選択します。
6. **既存の作業を使用** フィールドで **はい** を選択します。
    - このモバイル デバイスのメニュー項目は、既存の作業を実行するために使用されます。 したがってこの値を **はい** に設定する必要があります。  
    - **在庫状態の表示** フィールドは、モバイル デバイス上の倉庫の作業者に、手持在庫の在庫のステータスが表示されるかどうかを決定します。  
7. **指示者** フィールドで **システム グループ化** を選択します。 **指示者** フィールドから何かを選択すると、このページの **一般** セクションに追加のフィールドが表示されます。 表示されるフィールドは選択内容によって異なります。 **システム グループ化** を選択すると、新しいフィールドが 2 つ追加されます。 これらについて以下に詳しく説明します。  
8. **システム グループ化** フィールドで **WorkPoolId** を選択します。 倉庫作業者が、このメニュー項目を開くと、作業プール ID をスキャンするように求められます。 この [作業プール ID] を使用するワーク オーダーすべてと、このメニュー項目に追加された作業クラスの 1 つを使用するオープン ワーク オーダー明細行が、ユーザーにプッシュされます。  
9. **システム グループ化ラベル** フィールドに値を入力します。 これが、モバイル デバイスのユーザーに表示されるテキストです。 たとえば、**作業プール** と入力できます。  
10. **プット中のライセンス プレートの上書き** フィールドで **はい** を選択します。 このオプションにより、倉庫作業者はライセンス プレートにより制御されている場所に品目を降ろすときに、ターゲットのライセンス プレートを上書きできます。  
11. **グループ プット アウェイ** フィールドで、**はい** を選択します。
    - ワーク オーダーのプット明細行すべてが同じ場所を共有している場合、すべての明細行に対して 1 つの組み合わされたプットの指示が表示されます。 
    - 監査テンプレート ID: 作業監査テンプレートを使用すると、別の操作を実行できるように、中断する必要があるメニュー項目の作業プロセスを指定できます。 たとえば、このメニュー項目が入荷作業用の場合、監査テンプレートは、作業者が温度を確認するように要求する場合があります。 プロセスが中断される時点は、たとえば、作業の開始や完了の時点、またはそのステータスが変化した時点などで、監査テンプレートで指定されます。  
12. **作業クラス** のセクションを展開します。
13. **新規** を選択します。
14. **作業クラス ID** フィールドに `Purchase` と入力します。 作業プールは、メニュー項目が使用できる作業を制限します。 この場合、購買作業クラス ID があるオープン ワーク オーダー明細行に使用されます。  
15. **保存** を選択します。

## <a name="set-up-work-confirmation"></a>作業確認の設定
1. **作業確認の設定** を選択します。
2. **作業タイプ** フィールドで **ピック** を選択します。
3. **自動確定** チェック ボックスをオンにします。 作業の種類の選択と作業指示は、自動で確認されます。 この指示は、ユーザーには表示されません。  
4. **新規** を選択します。
5. **作業タイプ** フィールドで「プット」を選択します。
6. **場所の確認** チェック ボックスをオンにします。 品目を降ろすときに、倉庫作業者は場所の確認スキャンを実行するように求められます。  
7. **保存** を選択します。

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>モバイル デバイス メニューへのメニュー項目の追加
1. **モバイル デバイス** メニューを検索バーに入力して表示します。
2. **編集** を選択します。
3. クイック フィルターを使用して、レコードを見つけます。 たとえば、**inbound** という値を含む **名前** フィールドをフィルターします。 入荷メニュー項目で使用するメニューを検索するとします。 USMF では、これは **入荷** と呼ばれます。  
4. ツリーで、**値** を選択します。
5. 右を指している矢印を選択します。
6. **保存** を選択します。
7. ページを閉じます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]