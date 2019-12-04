---
title: 採用データの変更の追跡
description: プロセスの監査機能を使用すると、レポートやコンプライアンスの理由で、応募者、求人、またはジョブアプリケーションの変更を追跡することができます。
author: tracykeya
manager: AnnBe
ms.date: 04/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: trkeya
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: 0b0be541416d2e4be78da223ec8e95c195d90bbc
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832645"
---
# <a name="track-changes-in-recruiting-data"></a>採用データの変更の追跡

[!include [banner](includes/banner.md)]

監査プロセスを使用して、求人、職務申請、またはジョブアプリケーションに加えられた変更を追跡できます。 これは、レポートやコンプライアンスのために役立ちます。

OData コネクタを使用して、Power BI で追跡データを表示できます。 詳細については、[Power BI Desktop で OData フィードに接続する](https://docs.microsoft.com/power-bi/desktop-connect-odata)を参照してください。

## <a name="track-changes"></a>追跡の変更
採用データの変更履歴を設定するには、次の手順に従います。

1. [Power Apps](https://web.powerapps.com) で、適切な環境を選択します。

2. **設定** (ギア アイコン) を選択し、**高度なカスタマイズ**を選択して、**開発者リソース**の下で**リソース**を選択します。 

3. **開発者リソース**ページで、**インスタンス Web API 値**フィールドをコピーします。 たとえば、値は次のようになります : https://yourorgname.api.crm.dynamics.com/api/data/v9.1/。

4. その後、次のいずれかのエンティティからデータを照会できます。
  - ジョブ開始履歴 (msdyn_jobopeninghistories)
  - 職務申請履歴 (msdyn_jobapplicationhistories) 
  - 候補者履歴 (msdyn_candidatehistories)

## <a name="data-reported"></a>レポートされたデータ

以下のデータはプロセス監査で使用可能です。

| レポートされたデータ | 説明 |
| --- | --- |
| 変更者 (msdyn_ChangedbyId) | ユーザーへの参照 |
| 作成日 (作成者) |  変更が発生したときの UTC の日付と時刻 |
| タイプの変更 (msdyn_changetype) | 発生した変更 |
| 候補者の一般的な値、職務申請、 <br></br>および職務申請 | 作成済<br></br>更新済 |
| 職務申請履歴 | コンポーネントを追加 <br></br>コンポーネントを削除 |
| ジョブ開始履歴 | TODO: 転記の追加 <br></br>TODO: 転記の削除 <br></br>TODO: 転記の更新 <br></br>TODO: 参加者の追加 <br></br>TODO: 参加者の削除 |
| 候補者履歴 | コンポーネントの追加 <br></br>コンポーネントの削除 <br></br>作業経験の追加 <br></br>作業経験の削除 <br></br>教育の追加 <br></br>教育の削除 <br></br>スキルの追加 <br></br>スキルの削除 <br></br>タグの追加 <br></br>タグの削除 <br></br>ソーシャル ネットワークの追加 <br></br>ソーシャル ネットワークの削除 <br></br>個人情報の追加 <br></br>個人情報の更新<br></br> |
| 変更されたフィールド (msdyn_changedfields) | 変更されたフィールドを一覧表示する JSON オブジェクトには、すべてのフィールドの値が格納されない場合があります。<br></br><br></br>「作成」および「更新」の変更については、作成または変更されたレコードのフィールドが一覧表示されます。<br></br><br></br>「追加」変更タイプについては、子レコードのフィールドが一覧表示されます。<br></br><br></br>**例 :**<br></br><br></br>{<br></br>  "msdyn_applyurl": { "newValue": "" },<br></br>  "msdyn_description": { "valueOmitted": true } <br></br>} |
|職務申請履歴 | ジョブアプリケーション (msdyn_JobapplicatonId)<br></br>ステータス (msdyn_status) <br></br>ステータスの理由 (msdyn_statusreason) <br></br>却下の理由 (msdyn_rejectionreason) |
| ジョブ開始履歴 | 求人 (msdyn_JobopeningId) <br></br>ステータス (msdyn_jobopeningstatus) <br></br>ステータスの理由 (msdyn_jobopeningstatusreason) |
| 候補者履歴 | 候補者 (msdyn_CandidateId) |
