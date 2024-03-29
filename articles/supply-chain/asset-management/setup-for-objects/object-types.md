---
title: 資産タイプ
description: この記事では、資産管理で資産タイプを作成する方法について説明します。 また、資産タイプに関連する要素についても説明します。
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectJobType, EntAssetObjectType, EntAssetObjectTypeDefaultSparePart, EntAssetObjectTypeDefaultSparePartApprove, EntAssetObjectTypeDefaultCreateCombinations, EntAssetObjectTypeDefault, EntAssetObjectTypeDefaultCopy
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d3a51fdb55e9158e88e89549e3d0049e699c233e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887634"
---
# <a name="asset-types"></a>資産タイプ

[!include [banner](../../includes/banner.md)]



この記事では、資産タイプの作成方法を説明します。 また、資産タイプに関連する要素についても説明します。 資産タイプは、資産の一般的なカテゴリとして使用されます。 例としては、CNC マシン、測定機器、トラック エンジンが含まれます。 資産タイプは、メンテナンス ジョブ タイプ (メンテナンス タスク)、資産ライフサイクル状態、カウンター、資産属性、条件評価テンプレート、および資産に対して選択できる資産モデルを管理するために使用されます。 資産を作成するときは、資産タイプを指定する必要があります。

資産タイプごとに、資産タイプ設定のバリエーションを作成することができます。 たとえば、**トラック** という名前の資産タイプがある場合、さまざまな資産メーカーや資産モデルに対してその資産タイプのバリエーションを作成できます。 各資産タイプの設定に、必要な予備部品とメンテナンス計画を追加できます。

最初に、必要な資産タイプを設定します。 次に、資産タイプに関連する資産モデルを作成します。 最後に、**資産タイプの既定値** ページで、機器に必要な資産タイプのすべてのバリエーションを作成します。

## <a name="create-an-asset-type"></a>資産タイプの作成

1. **資産管理** > **設定** > **資産タイプ** > **資産タイプ** を選択します。
2. **新規** を選択して資産タイプを作成します。
3. **資産タイプ** フィールドで、資産タイプ ID を入力します。
4. **名前** フィールドに、名前を入力します。
5. **資産ライフサイクル モデル** フィールドで、資産ライフサイクル モデルを選択します。 資産ライフサイクルの状態と資産ライフサイクル モデルの詳細については、[資産ライフサイクルの状態](object-stages.md)を参照してください。
6. この資産タイプを持つ資産に対して集計された主要業績評価指標 (KPI) 値を計算する場合は、**合計** オプションを **はい** に設定します。
7. **保存** を選択します。
8. **メンテナンス ジョブ タイプ** クイック タブで、メンテナンス タイプに関連するメンテナンス ジョブ タイプを選択します。

    - メンテナンス ジョブ タイプを選択するには、**残りのメンテナンス ジョブ タイプ** フィールドでそれを選択し、右矢印ボタン ![右矢印ボタン。](media/29-setup-for-objects.png) を選択して、 **選択されたメンテナンス ジョブ タイプ** セクションに移行します。
    - 使用可能なすべてのメンテナンス ジョブ タイプを選択するには、![すべての矢印を転送する。](media/30-setup-for-objects.png) ボタンを 選択します。 すべてのメンテナンス ジョブ タイプは、**残りのメンテナンス ジョブ タイプ** フィールドから、**選択されたメンテナンス ジョブ タイプ** フィールドに転送されます。
    - メンテナンス ジョブ タイプの選択をキャンセルするには、**選択されたメンテナンス ジョブ タイプ** フィールドでそれを選択し、左矢印ボタン ![右矢印ボタン。](media/31-setup-for-objects.png) を選択して、 **残りのメンテナンス ジョブ タイプ** フィールドに移行します。

9. 資産タイプに関連するカウンターを選択することもできます。 **カウンター** クイック タブで、ステップ 8 のメンテナンス ジョブ タイプについて説明されている方法を使用して選択を行います。 カウンターの設定の詳細については、[カウンター](counters.md) を参照してください。
10. 資産タイプに関連する属性タイプを選択することもできます。 **属性タイプ** クイック タブで、ステップ 8 のメンテナンス ジョブ タイプについて説明されている方法を使用して選択を行います。 次に、属性タイプの優先順序を作成するには、**選択された属性タイプ** フィールドの属性タイプを選択し、上矢印と下矢印ボタンを使用して移動します。 属性タイプの順序は、この資産タイプを使用する資産に表示されます。 資産属性の詳細については、[メンテナンス属性タイプ](../setup-for-functional-locations/specification-types.md)を参照してください。

    > [!NOTE]
    > **属性タイプ** クイック タブに新しい属性タイプを追加すると、既存の資産はその情報で自動的に更新されます。

11. 資産タイプに関連する条件評価テンプレートを選択することもできます。 **条件評価** クイック タブで、ステップ 8 のメンテナンス ジョブ タイプについて説明されている方法を使用して選択を行います。 条件評価テンプレートと登録の詳細については、[条件評価](../setup-for-objects/condition-assessment.md)を参照してください。
12. **資産モデル** クイック タブには、選択した資産タイプに設定されている資産メーカーとモデルのすべての組み合わせが表示されます。 メーカー別に分割された組み合わせを表示するには、**資産モデル** を選択して **資産モデル** ページを開きます。

    **資産モデル** ページで、資産モデル - 資産タイプの関係を追加できます。 また、**資産タイプ** ページで、資産メーカー - 資産モデルの関係を資産タイプに直接追加できます。 最後に、**資産モデル** ページ (**資産管理** \> **設定** \> **資産** \> **資産モデル**) で、新しい資産メーカー - 資産モデル - 資産タイプの関係を作成できます。 したがって、資産メーカー - 資産モデル - 資産タイプの関係を設定および編集するには、3 つの方法があります。 使用可能なすべての組み合わせが異なる視点から表示され、セットアップを操作するときに優先するエントリ ポイントを選択できます。

> [!NOTE]
> - 資産タイプのカウンターを選択した場合、**カウンター** ページ (**資産管理** > **設定** > **資産** > **の資産タイプ** > **カウンター**) で、選択内容が自動的に更新されます。
> - **一般** クイック タブの **詳細** セクションのフィールドには、選択した資産タイプに設定されているメンテナンス ジョブ タイプ、カウンター、属性などの数が表示されます。

通常、手動で作成されるワーク オーダーは修繕メンテナンスに関連しますが、自動的に作成されるワーク オーダーは予防的メンテナンスに関連します。 ワーク オーダーを手動で作成する場合、**資産タイプ** ページの **メンテナンス ジョブ タイプ** クイック タブで選択されたメンテナンス ジョブ タイプのみ使用できます。 ただし、自動的に作成されたワーク オーダーでは、**メンテナンス ジョブ タイプ** ページ (**資産管理** \> **設定** \> **職務** \> **メンテナンス ジョブ タイプ**) で作成したすべてのメンテナンス ジョブ タイプを使用できます。

## <a name="create-asset-type-setup-lines"></a>資産タイプの設定明細行の作成

1. **資産管理** \> **設定** \> **資産** \> **資産タイプ** \> **資産タイプ設定** を選択します。 または、**資産管理** \> **設定** \> **資産** \> **資産タイプ** \> **資産タイプ** を選択し、資産タイプを選択してから、**資産タイプ設定** を選択します。
2. **資産タイプ設定** ページを初めて使用するときは、**組み合わせの作成** ボタンが役立つ場合があります。 このボタンを使用して、資産タイプの資産モデルのすべての組み合わせをすばやく作成できます。 **組み合わせの作成** を選択し、組み合わせを作成するアセットタイプを選択して、**OK** を選択します。

    > [!NOTE]
    > 自動的に作成されたすべての資産タイプの設定の組み合わせを使用しない場合は、設定を選択してから **削除** を選択して削除できます。

3. **新規** を選択して、資産タイプ設定を手動で作成します。
4. 資産タイプ設定の具体性に応じて、**資産タイプ**、**メーカー**、および **モデル** フィールドで選択を行います。
5. 保証契約が資産タイプに関連している場合は、**仕入先保証** および **顧客保証** フィールドで契約を選択します。 
6. **予備部品** クイック タブで、**追加** を選択して、選択した資産タイプ設定に予備部品を追加します。
7. 予備部品を承認するには、予備部品の明細行を選択し、**承認** を選択します。 承認のために複数の明細行を選択できます。
8. 予備部品が別の場所で使用されているかどうかを確認するには （たとえば、資産やワーク オーダーに関連して）、予備部品の明細行を選択し、**使用したアイテム** ページを開くために **使用したアイテム** を選択します。 リスト内のすべての有効な予備部品を表示するには、**有効** チェック ボックスを選択します。 承認済み予備部品のみを表示するには、**承認済** チェック ボックスを選択します。
9. **メンテナンス計画** クイック タブで、**追加** を選択して、選択した資産タイプ設定にメンテナンス計画を追加します。
10. 資産タイプ設定を別の設定にコピーするには、コピー機能を使用します。 設定をコピーする資産タイプ設定を選択し、**設定のコピー** を選択して、設定をコピーする資産タイプ設定を選択します。 さまざまなオプションの設定によって、含まれる情報の量が決まります。 完了したら、**OK** を選択して設定をコピーします。

> [!NOTE]
> 再利用する予備部品の明細行とメンテナンス計画の明細行が多数ある場合、コピー機能を使用すると、多くの資産タイプ設定の組み合わせに対してデータをすばやく簡単に設定できます。

## <a name="spare-parts-on-the-asset-type-setup"></a>資産タイプ設定の予備部品

「資産タイプ設定の明細行の作成」セクションで説明したように、予備部品は **資産タイプ設定** ページの資産モデルで設定されます。 したがって、**資産タイプ設定** ページを開くと、資産タイプ、資産メーカー、および資産モデルの選択された組み合わせに関連する予備部品のみが表示されます。 すべての予備部品レコードのリストを表示するには、**予備部品** ページ (**資産管理** \> **照会** \> **予備部品**) を開きます。

**予備部品** ページでは、資産タイプ、資産メーカー、および資産モデルの既存の組み合わせに対して新しい予備部品を作成することもできます。 **資産タイプ設定** ページまたは **予備部品** ページで、予備部品レコードを作成するかどうかを決定できます。 **資産タイプ設定** ページには、資産タイプ、資産メーカー、および資産モデルの選択した組み合わせに関するデータの概要が表示されますが、**予備部品** ページにはすべての資産タイプ設定の明細行の完全な概要が表示されます。 **予備部品** ページに多くのレコードが含まれている場合は、**資産タイプ設定** ページで概要が改善される場合があります。

選択した明細行の予備部品が資産管理の他の場所 (たとえば、資産やワーク オーダーに関連して) で使用されているかどうかを確認するには、**使用したアイテム** を選択して **使用したアイテム** ページを開きます。 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]