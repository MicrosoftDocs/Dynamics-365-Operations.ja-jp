---
title: 出荷の自動更新
description: この記事では、出荷の自動更新機能の概要を示します。
author: Mirzaab
ms.date: 11/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable,SalesTableListPage,SalesTable,WHSWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e5816a7cddf509260511368b74655a9fd5bfc485
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067884"
---
# <a name="shipment-auto-updates"></a>出荷の自動更新

[!include [banner](../includes/banner.md)]

自動更新出荷機能を使用すると、出荷に関連付けられている積荷を倉庫にリリースした後に、出荷に関連付けられている積荷明細行の数量 (増加と減少の両方) が自動的に更新されます。 この機能は、出荷または積荷の積荷明細行がウェーブで処理されるまで有効です。 この機能を使用すると、注文の更新が自動的に倉庫にフローするため、倉庫作業が作成されるまで、手動による操作は必要ありません。

自動更新出荷機能が使用されていない場合は、倉庫作業が作成されるまで、数量減少だけが自動的にフローします。 ユーザーは明細行を手動で更新または削除する必要があります。注文数量が増加するか、新しい注文明細行が追加された場合は、明細行を再度リリースする必要があります。 自動更新出荷機能を使用することで、企業は、関連する出荷や積荷が注文明細行の更新に反映されないことを心配することなく、倉庫にシームレスに更新を提供できます。

自動更新出荷機能は、販売注文明細行と在庫移動指示明細行の両方に適用され、特定の倉庫に対して有効になります。 そのため、企業は、必要に応じて倉庫間で異なる自動更新出荷ポリシーを適用できます。 既定では、数量減少の出荷ポリシーの自動更新は、倉庫管理プロセス (WMS) を使用するすべての倉庫に適用されます。 この既定のポリシー設定を使用すると、倉庫作業が作成されるまで、数量減少だけが出荷と積荷に自動的にフローします。 この動作は、自動更新出荷機能が導入される前に使用されていた動作に似ています。

## <a name="main-elements-of-the-functionality"></a>機能の主要な要素

自動更新出荷機能は、主に出荷ステータスに基づいて、販売注文明細行または在庫移動指示明細行に変更が加えられたときに、積荷明細行の数量を変更するかどうかを決定します。 また、主に出荷ステータスに基づいて、新しい積荷明細行を既存の積荷に自動的に追加するタイミングを決定します。 出荷ステータスが **ウェーブ済** またはそれよりも大きい場合は、自動更新は行われません。

また、自動更新のためにウェーブの状態も考慮されます。 積荷明細行に関連するウェーブの状態が **保有**、**実行中**、**リリース済**、**ピッキング済**、または **出荷済** の場合に、ユーザーが積荷明細行の数量を削減しようとすると (販売注文明細行または在庫移動指示明細行で数量を減らす)、「引当に依存する作業が作成されているため、引当を削除できません」というエラーメッセージが表示されます。 また、ウェーブが前述のウェーブの状態のいずれかの場合に、ユーザーが販売注文明細行または在庫移動指示明細行の数量を増加させ、積荷明細行の数量を間接的に増加させようとしても、この数量は自動的に増加されません。 この場合、積荷明細行を手動で更新する必要があります。

## <a name="scenarios"></a>シナリオ

自動更新出荷機能は、新しい注文明細行の追加、注文明細行の数量の増加、注文明細行の数量の減少、および注文明細行の削除という 4 つのシナリオをサポートしています。

- **新しい注文明細行の追加** – **倉庫** ページの **倉庫** クイックタブにある **自動更新出荷** フィールド (**倉庫管理 \> 設定 \> 倉庫 \> 倉庫**) が **常時** に設定されている場合、販売注文の積荷が既に作成された後に、注文に対する出荷が存在し、新しい注文明細行が販売注文または在庫移動指示に追加される場合、既存の積荷は更新されません。 既存の積荷への参照がない新しい積荷明細行が作成され、既存の出荷に関連付けられます。 新しい明細行が積荷に追加され、リリースされます。
- **注文明細行の数量の増加** – **自動更新出荷** フィールドを **常時** に設定した場合、注文に出荷が存在し、販売注文の積荷が既に作成された後に、既存の販売注文明細行または在庫移動指示明細行の数量が増加すると、積荷明細行は注文明細行と同じ数量ずつ増加します。 積荷がリリースされたが、作業が作成されなかった場合、積荷明細行は注文明細行と同じ数量ずつ増加します。
- **注文明細行の数量の減少** – **自動更新出荷** フィールドが **常時** または **数量減少** に設定されている場合、注文に出荷が存在し、販売注文の出荷が既に作成された後に、既存の販売注文明細行または在庫移動指示明細行が削減された場合、関連する積荷明細行の数量は一致するように更新されます (積荷明細行の数量が新しい注文明細行の数量と等しいかそれ以下でない場合)。 この場合、積荷明細行は影響を受けません。 積荷がリリースされたが、作業が作成されなかった場合、積荷明細行の数量が既に注文明細行の新しい数量と等しいかそれより少ない場合を除いて、関連付けられている積荷明細行の数量が一致するように更新されます。 この場合、積荷明細行は影響を受けます。
- **注文明細行の削除** – **自動更新出荷** フィールドを **常時** または **数量減少** に設定する場合、ユーザーが積荷明細行が存在する注文明細行を削除しようとすると、エラーメッセージが表示されます。

## <a name="example-scenario"></a>シナリオ例

このシナリオでは、デモ データをインストールして、**USMF** デモ データの会社を使用する必要があります。

### <a name="turn-on-the-auto-update-shipment-functionality"></a>自動更新出荷機能を有効にします。

自動更新出荷機能を有効にして、次の手順に従います。

1. **倉庫管理 \> 設定 \> 倉庫 \> 倉庫** の順に移動します。
2. 倉庫 **24** を選択します。
3. **倉庫** クイックタブの、**自動更新出荷** フィールドで、値を **数量減少** から **常時** に変更します。

値を **常時** に変更すると、販売注文明細行および在庫移動指示明細行の数量、および新しい明細行の追加が、選択した倉庫の出荷と積荷に反映され、前述の制約の更新が適用されます。

### <a name="change-the-wave-template-so-that-load-lines-arent-automatically-processed"></a>ウェーブ テンプレートを変更して、積荷明細行が自動的に処理されないようにします。

積荷明細行が自動的に処理されないようにウェーブ テンプレートを構成するには、次の手順に従います。

1. **倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート** の順に移動します。
2. ウェーブ テンプレート **24 出荷の既定** を選択します。
3. **編集** を選択します。
4. **一般** クイックタブで、**ウェーブの作成を自動化** オプションを **はい** に設定し、他のすべてのオプションが **いいえ** に設定されていることを確認します。

ウェーブの作成プロセスの一部として、作業が自動的に作成されたり、リリースされたりしないようにすることは重要です。 販売注文明細行に作成された積荷明細行に関連する作業が作成されると、販売注文明細行の数量が変更された場合、積荷明細行は自動的に更新されなくなります。

### <a name="create-a-sales-order"></a>販売注文の作成

販売注文を作成するには、次の手順に従います。

1. **販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。
2. 顧客 **US-003** を選択します。
3. 品目番号 **A0001** の明細行を作成します。
4. 数量 **10** を入力します。 (倉庫 **24** を使用していることを確認してください。)
5. **保存** を選択します。
6. アクション ペインの、**倉庫** タブにある **アクション** グループで、**倉庫にリリース** を選択します。 出荷とウェーブが作成されます。

前の手順でウェーブ テンプレートを変更したため、積荷または作業は作成されません。 出荷ステータスが **オープン** になり、ウェーブの状態が **作成済** になります。

### <a name="decrease-the-quantity-on-a-sales-order-line"></a>販売注文明細行の数量の減少

販売注文明細行の数量を減少させるには、次の手順に従います。

1. **販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。
2. 倉庫にリリースした販売注文を選択します。
3. 販売注文明細行を選択します。 **数量** フィールドで、値を **10** から **8** に変更します。
4. 販売注文明細行から、**倉庫 \> 出荷詳細** を選択します。 **出荷詳細** ページの **積荷明細行** クイックタブの数量は、販売注文明細行の変更を反映します。

### <a name="increase-the-quantity-on-a-sales-order-line"></a>販売注文明細行の数量の増加

販売注文明細行の数量を増加させるには、次の手順に従います。

1. **販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。
2. 倉庫に以前にリリースした販売注文を選択します。
3. 明細行の数量を **8** から **12** に変更します。
4. **保存** を選択します。
5. **すべての販売注文** ページに戻り、販売注文をもう一度選択します。
5. アクション ウィンドウの、**倉庫** タブの、**関連情報** グループで、**出荷詳細** を選択します。 **出荷詳細** ページの **積荷明細行** クイックタブの数量は、販売注文明細行の変更を反映します。

積荷明細行の数量は 8 から 12 に増加しましたが、自動引当が有効になっていない場合、引当済の品目は 8 つしかありません。 既存の出荷に追加された数量が引き当てられていないので、この時点で引当なしで処理されるウェーブの場合、既に引き当てられている数量に対してのみ作業が作成されます。

> [!NOTE]
> 注文明細行の数量を減少すると、注文明細行の数量が注文明細行の新しい数量と同じかそれより少ない場合には、影響を受けません。 注文明細行の数量が増加すると、積荷明細行が注文明細行と同じ数量ずつ増加します。 注文明細行の数量と積荷明細行の数量が異なる場合は、差額が残ります。

### <a name="add-a-sales-order-line"></a>販売注文明細行の追加

販売注文明細行を追加するには、次の手順に従います。

1. **販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。
2. 倉庫に以前にリリースした販売注文を選択します。
3. 品目番号 **A0002** の明細行を作成します。
4. **数量** フィールドに **10** と入力します。 (倉庫 **24** を使用していることを確認してください。) 新しい明細行が自動的に既存の出荷に追加されます。
5. **保存** を選択します。
6. **すべての販売注文** ページに戻り、販売注文をもう一度選択します。
7. アクション ウィンドウの、**倉庫** タブの、**関連情報** グループで、**出荷詳細** を選択します。 **出荷詳細** ページの **積荷明細行** クイックタブに、2 番目の積荷明細行が表示されます。

既存の出荷に追加したばかりの販売注文明細行は引き当てられていないため、この時点でウェーブが処理されると、最初の販売注文明細行および最初の積荷明細行の数量に対してのみ作業が作成されます。

### <a name="process-a-wave"></a>ウェーブの処理

ウェーブを処理するには、これらの手順に従います。

1. **倉庫管理 \> 出庫ウェーブ \> 出荷ウェーブ \> すべてのウェーブ** の順に移動します。
2. 以前に作成したウェーブを選択します。
3. アクション ペインの、**ウェーブ** タブの、**ウェーブ** グループで、**処理** を選択します。

このウェーブが処理され、積荷明細行の引当済数量に対する作業が作成されます。 出荷ステータスが **オープン** から **ウェーブ済** に更新されます。 出荷ステータスが **ウェーブ済** に更新されると、明細行の数量の増減や、販売注文への新しい明細行の追加などの変更が発生した場合に、ウェーブ出荷に関連付けられている既存の積荷明細行は影響を受けません。

出荷のステータスが **ウェーブ済** またはそれ以上である場合、販売注文明細行の数量に対する更新は、出荷に関連付けられている積荷明細行に対して反映または検証されません。 積荷明細行の数量を変更する場合は、積荷明細行で直接行う必要があります。

検証は、積荷明細行に対する作業が作成され、引当が行われた後に行われます。 販売注文明細行の数量の減少は、作業明細行の引当に対して検証されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]