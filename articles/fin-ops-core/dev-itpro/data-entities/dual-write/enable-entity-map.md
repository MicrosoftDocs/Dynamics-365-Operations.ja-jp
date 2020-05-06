---
title: エンティティ マップの二重書き込みの有効化
description: このトピックでは、エンティティ マップが二重書き込みでどのように機能するかついて説明します。
author: sabinn-msft
manager: AnnBe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Developer
ms.reviewer: v-douklo
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2ceadd0906699a475ceec5b1ad2b511385f946c
ms.sourcegitcommit: e9fadf6f6dafdcefaff8e23eaa3c85f53437db3f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2020
ms.locfileid: "3279123"
---
# <a name="enable-entity-maps-for-dual-write"></a>エンティティ マップの二重書き込みの有効化

[!include [banner](../../includes/banner.md)]



エンティティ マップの二重書き込みを有効にすると、**実行していません** 状態で開始されます。 次に、エンティティ マップは初期化フェーズを実行し、両側のエンティティに既存のデータをコピーすることにより初期書き込みを行います。 最後に、エンティティが完全に有効化されると、エンティティ マップは状態を **実行中** に設定します。

![エンティティ マップの有効化](media/enabling-entity-map.png)

状態が **実行中** の間、エンティティを一時停止できます。 その後、すべての変更は、再開するまでキューに配置されます。 再開すると、エンティティは "キャッチ アップ モード" になり、キューに入れられたすべての変更が再生されます。

次の図で、一時停止しているエンティティの例を示します。

![一時停止したエンティティ](media/stop-pause-entity.png)

| ステータス | 説明 | 使用可能なアクション |
|---|---|---|
| 実行していません | エンティティは、まだ二重書き込みが有効になっていません。 すべてのエンティティは、**実行していません** 状態で開始します。 | 実行 |
| 初期化 | 最初の書き込みが発生しています。 | None |
| 実行中 | エンティティの二重書き込みが有効になっています。 | 停止、 一時停止 |
| 一時停止 | エンティティは一時停止状態にあり、すべての新しい要求がキューに入れられます。 | 実行 |
| 再開中 | エンティティは、エンティティが一時停止中にキューに入れられたレコードを処理します。 | None |

初期化フェーズでは、既存のデータが初期書き込みフェーズの一部としてコピーされます。

![既存のデータのコピー](media/initial-write-phase.png)

エンティティには複数の依存エンティティがあります。 たとえば、顧客-連絡先エンティティには、顧客グループと通貨が依存エンティティとしてあります。

![依存エンティティ](media/dependent-or-related-entities.png)

これらはリレーショナル データを持つリレーショナル アプリであるため、依存エンティティを有効にしないと、後でエラーが発生する可能性があります。 これらのエラーを防ぐために、エンティティ マップを有効にする前に、有効にすることを推奨する関連エンティティの一覧が提供されます。

## <a name="example-enabling-the-customers-v3contacts-entity-map"></a>例: 顧客 V3の有効化—連絡先エンティティ マップ

エンティティ マップ (たとえば、**顧客 V3—連絡先**) を選択して、**実行** を選択すると、エンティティ マップが有効になる前にダイアログ ボックスが表示されます。 このダイアログ ボックスには、すべての依存エンティティが一覧表示されます。 **関連エンティティ マップの表示** オプションを選択すると、すべての関連するエンティティ マップを表示できます。 選択したエンティティ マップとそれに関連するすべてのエンティティを有効にするには、ダイアログ ボックスの **実行** を選択します。

> [!NOTE]
> エンティティを一時停止したときの動作も同様です。 その場合は、すべての関連するエンティティを一時停止することもできます。

![すべての依存エンティティの一覧表示](media/related-entity-maps.png)

競合を解決するために使用する別のマスターを指定することによって、これをさらにカスタマイズできます。 (既定では、Common Data Service が使用されます。) 既存のデータをコピーしない場合は、**初期同期** チェック ボックスをオフにして、初期同期をスキップします。 または、1 つ以上の関連エンティティの選択をキャンセルして、それらを解除します。 エンティティ マップをドラッグして、同期される順序を変更することもできます。

ダイアログ ボックスで選択を完了し、**実行** を選択すると、エンティティ マップと関連するすべてのエンティティが初期書き込みフェーズを実行します。 エンティティ マップ一覧ページにリダイレクトされます。 エラーが発生した場合は、**初回同期の詳細** タブで詳細を確認できます。このタブでは、既存のデータのコピー中に発生するすべてのエラーの詳細を表示します。 原因となっているエラーを修正した後、実行を再実行し、結果を監視できます。 または、既存のデータを同期する必要がなくなった場合や、基になるデータが原因で繰り返し問題が発生する場合は、初期書き込みフェーズをスキップできます。 代わりに、**初期同期をスキップ** を選択して、ライブ書き込みを有効にできます。

![初期書き込みのスキップ](media/skip-initial-writes.png)

## <a name="criteria-for-linking-entities"></a>エンティティをリンクするための基準

エンティティ マップの二重書き込みを有効にするには、Common Data Service で代替キーを定義する必要があります。 Common Data Service の代替キーの値は、Finance and Operations アプリで定義されているキーと一致する必要があります。

たとえば、Finance and Operations アプリでは、**CustomerAccount** がアカウント エンティティのキーです。

![Finance and Operations アプリでのアカウント エンティティのキー](media/define-alternative-key.png)

Common Data Service では、**accountnumber** はアカウント エンティティのキーとして定義されます。

![Common Data Service で定義されたアカウント エンティティ](media/define-account-entity.png)

顧客 V3 エンティティ マップでは、**accountnumber** が **CustomerAccount** にマップされていることがわかります。

![エンティティ マップでのマッピング](media/mapped-to-entity-map.png)

## <a name="next-steps"></a>次のステップ

[エンティティとフィールドのマッピングのカスタマイズ](customizing-mappings.md)
