---
title: 部門の作成および部門階層への追加
description: 部門は、組織のカテゴリまたは機能領域を表す作業単位です。 部門は、販売、会計、または人事管理など、組織内の特定の領域を担当します。 機能領域の報告に部門を使用できます。 部門は損益の職責を持つ場合があります。
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HierarchyDesigner, OMOperatingUnit, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 3c4382336e53bc09c51dd845446af9a20a2ba8af
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794472"
---
# <a name="create-departments-and-include-them-in-the-department-hierarchy"></a>部門の作成および部門階層への追加

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

部門は、組織のカテゴリまたは機能領域を表す作業単位です。 部門は、販売、会計、または人事管理など、組織内の特定の領域を担当します。 機能領域の報告に部門を使用できます。 部門は損益の職責を持つ場合があります。

部門はコスト センターのグループを含む場合があります。 職位は部門に割り当てることができます。 部門を作成するには、**人事管理** &gt; **部門** &gt; **部門** の順にクリックします。 次の表に、使用できるフィールドを示します。

| フィールド               | 説明                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 氏名                | 部門の名前を入力します。                                                                                                                                                                                  |
| 部門番号   | 番号順序コードが、**組織番号** 参照に、**番号順序** ページで割り当てられている場合、既定値が自動的に生成されることがあります。                                                 |
| 検索名         | 部門の検索に使用できる名前あるいは略称を入力します。                                                                                                                                            |
| メモ                | 追加情報をここに入力します。                                                                                                                                                                            |
| 階層        | チェック ボックスがオンの場合、部門が部門の階層に含まれることを示します。 部門の階層に部門を追加する方法については、この記事の情報を参照してください。 |
| DUNS 番号         | DUNS は、データ普遍的の番号付けシステムを意味します。 これは Dun and Bradstreet が発行する 9 桁の番号です。                                                                                                     |
| マネージャー             | 部門を管理するペルソナを入力します。                                                                                                                                                                    |
| 住所           | 部門の住所情報を追加します。 たとえば、部門が位置する建物の住所を追加します。                                                                          |
| 連絡先情報 | 部門の連絡先情報を追加します。 たとえば、部門のサービスデスクの電話番号を追加します。                                                                                           |

部門の階層に部門を追加するには、次の手順に従います。

1.  **人事管理** &gt; **部門** &gt; **部門の階層** の順にクリックします。
2.  **編集** をクリックし、部門があるべき組織を選択します。
3.  **挿入** をクリックし、リストから **部門** を選択します。
4.  表示される部門の一覧で、階層に追加する部門を選択します。
5.  変更を保存します。 階層のドラフト バージョンが作成されたことを知らせるメッセージが表示されます。
6.  準備が整ったら、階層デザイナーで **公開** をクリックします。 階層をいつ公開する必要があるかを示す有効日を入力できます。 たとえば、次の暦年の期首に新しい部門を追加する場合、新しい暦年の 1 月 1 日に有効日を設定します。 階層を変更すると、その日付に対して有効になります。

## <a name="steps-for-creating-a-department"></a>部門を作成する手順
新しい部門を作成するためのステップ バイ ステップの手順については次の記事 [新しい部門の定義](../fin-and-ops/hr/tasks/define-new-departments.md) を参照してください。 


[!INCLUDE[footer-include](../includes/footer-banner.md)]