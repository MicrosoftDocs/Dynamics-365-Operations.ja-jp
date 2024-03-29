---
title: メンテナンス計画のスケジュール
description: この記事では、資産管理におけるメンテナンス計画のスケジュールについて説明します。
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fc9212d0945c05af9dbc054a5a1d2bf7b996b93f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857985"
---
# <a name="schedule-maintenance-plans"></a>メンテナンス計画のスケジュール

[!include [banner](../../includes/banner.md)]

 

予防的メンテナンスのスケジューリングは、資産に設定されたメンテナンス計画に基づいて、資産にカレンダー エントリを生成します。 選択したメンテナンス計画、資産タイプ、および資産に基づいてカレンダー エントリをスケジュールできます。

1. **資産管理** > **定期処理** > **予防的メンテナンス** > **メンテナンス計画のスケジュール** をクリックします。

2. **期間** と **期間頻度** のフィールドで時間間隔を選択できます。

>[!NOTE]
>**期間** および **期間頻度** のフィールドには、作成したメンテナンス計画 (時間ベースまたはカウンターベース) に基づいて、メンテナンス スケジュール行をどれだけ先に作成するかが示されます。 次の図では、メンテナンス スケジュール行 (= ワーク オーダー提案) が現在の日付および 3 か月後から作成されます。

3. メンテナンス計画行に従ってワークー オーダーを自動的に作成する場合は、**行で指定されている場合は自動作成** のトグル ボタンで「はい」を選択します。

>[!NOTE]
>このトグル ボタンが 「はい」に設定されている場合、*また*、**メンテナンス計画** のメンテナンス計画行で **自動作成** チェック ボックスも選択されている場合、ワーク オーダーはメンテナンス計画行に基づいて作成され、「ワーク オーダー作成済」ステータスのメンテナンス計画行も作成されます。 オプションを 1 つだけ選択した場合 (このダイアログの **行で指定されている場合は自動作成** トグル ボタン、または **メンテナンス計画** フォームの **自動作成** チェック ボックス)、メンテナンス スケジュール行が「作成済」ステータスで作成されます。 その場合、ワーク オーダーは作成されません。

4. メンテナンス計画 (時間またはカウンター)、資産、資産タイプ、機能的な場所、および機能的な場所タイプに基づいて、カレンダー エントリを生成することができます。 **フィルター** ボタンをクリックして、必要に応じて選択を行います。

- 機能的な場所のメンテナンス計画のスケジュールについて : メンテナンス計画をスケジュールした後に、**すべての機能的な場所** > **メンテナンス計画** クイック タブで、資産タイプ、メーカー、およびモデルのメンテナンス計画の設定を更新する場合は、その機能的な場所に関連する既存のメンテナンス スケジュール エントリは自動的に削除されます。 機能的な場所の更新されたメンテナンス計画設定に対応する新しいカレンダー エントリを作成するには、その機能的な場所に対する新しいメンテナンス計画スケジュールを実行する必要があります。 機能的な場所の資産タイプ、メーカー、およびモデルの設定については、[機能的な場所の作成](../functional-locations/create-functional-locations.md)を参照してください。

>*例* : 特定の機能的な場所のメンテナンス計画を作成すると、メンテナンス計画をスケジュールする際に、その機能的な場所に設定された資産が常に含まれます。 この場合、メンテナンス計画を作成し、特定の機能的な場所を選択しますが、メンテナンス計画に資産を追加することはしません。 その結果、そのメンテナンス計画をスケジュールすると、その時点で機能的な場所に関連付けられているすべての資産のメンテナンス スケジュール行が作成されます。

- **資産タイプ** の資産タイプ、メーカー、モデルに変更を加えた場合、それらの変更は更新された資産タイプを使用する新しい資産にのみ影響します。 資産タイプ設定の詳細については、[資産タイプ](../setup-for-objects/object-types.md)を参照してください。  

5. **OK** をクリックして、資産のメンテナンス スケジュール エントリの生成を開始します。 生成されたエントリは、**すべてのメンテナンス スケジュール** リストのページに表示されます。 次の図は、**メンテナンス計画のスケジュール** ダイアログの例を示します。

![図 1。](media/09-preventive-maintenance.png)

- **メンテナンス計画のスケジュール** ダイアログでは、**バックグラウンドで実行** クイック タブでバッチ ジョブを設定して、定期的にカレンダー エントリを自動的に生成することができます。  
- 予防的メンテナンスをスケジュールすると、開始日がシステム日付と時刻よりも前のメンテナンス スケジュール行は作成されません。  

次の図は、時間ベースのメンテナンス計画の計算を図解したものです。  

![図 2。](media/10-preventive-maintenance.jpg)

カウンターベースのメンテナンス計画について : 次の図では、2 つの異なるカウンター登録サイクルが示されています。 これらは、資産 V0001 に対して設定されたメンテナンス計画に基づいており、毎月約 2,000 km を走る資産 (自動車) を想定しています。

最初の例では、予想される 2,000 km に毎月達することはありません。 カウンターベースのメンテナンス計画によれば、しきい値は 2,000 km です。つまり、メンテナンス計画のスケジューリングを実行した場合、毎回 2,000 km のしきい値に達するたびに、メンテナンス スケジュール行を作成する必要があります。 例 1 には、4 つの登録行がありますが、2,000 キロメートルしきい値に達するのは 1 回だけです。 したがって、たとえば 3 か月の期間、この資産のメンテナンス計画のスケジュールを実行すると、1 つのメンテナンス スケジュール行のみが作成されます。

次の図では、2,000 km 以上が毎月登録されています。 したがって、3 か月の期間、この資産のメンテナンス計画をスケジュールすると、3 つのメンテナンス行が作成されます。 

これらの例は、資産に対してなされたすべてのカウンター登録が、資産の消耗を示す傾向を示していることを説明しています。 その傾向は、メンテナンス計画のスケジューリング時に計算基準として使用されます。

![図 3。](media/11-preventive-maintenance.png)

![図 4。](media/12-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]