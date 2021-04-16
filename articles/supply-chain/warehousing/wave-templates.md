---
title: ウェーブ テンプレート
description: このトピックでは、ウェーブが手動でまたは自動的に処理されるかを判断する基準を設定する方法、およびウェーブが処理されるときに倉庫のために生成される作業について説明します。
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: b02283a6e0a4ef0d61be8b66f82be8c125028cb0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813630"
---
# <a name="wave-templates"></a>ウェーブ テンプレート

[!include [banner](../includes/banner.md)]

このトピックでは、ウェーブが手動でまたは自動的に処理されるかを判断する基準を設定する方法、およびウェーブが処理されるときに倉庫のために生成される作業について説明します。 販売注文、製造オーダー、およびかんばんのリリース済み行のあるウェーブと一致する、ウェーブ テンプレートおよびクエリを設定し、基準を指定します。

## <a name="settings-for-wave-templates"></a>ウェーブ テンプレートの設定

ウェーブ テンプレートを設定するときは、以下を指定します。

- テンプレートが作業を作成する **サイト** および **倉庫**。
- テンプレートが評価される順序。 販売注文、製造オーダー、およびかんばんのリリース済み行とテンプレートが一致する順序。 行がリリースされると、その行が基準を満たす最初のウェーブ テンプレートが適用されます。 基準が広いほど行が基準を満たす可能性が高いため、具体的な基準があるテンプレートをリストの最上部に表示する必要があります。 リストのテンプレートを配置するには、アクション ウィンドウの **上へ移動** または **下へ移動** ボタンを使用します。
- 各テンプレートが実行するアクション。 ウェーブ テンプレートの各タイプに対する作業の作成や配布など、ウェーブ **メソッド** は、テンプレートが作成するアクションを実行します。
- 使用するウェーブ テンプレートに適用する必要があるウェーブ属性 (フィルター)。

> [!NOTE]
> 必要に応じて、開発者は他のメソッドを作成できます。 **ウェーブ処理メソッド** ページでメソッドのフル リストを表示できます。

一部の設定は、次のように、ウェーブ処理の戦略的決定を表しています。

- テンプレートを販売注文と移動オーダーの品目の出荷に使用する場合、または製造オーダーまたはかんばんの生産に品目を移動するために使用する場合。
- ウェーブを手動または自動で処理する場合は、次のとおりです。

  - **手動処理** – 明細行がウェーブに追加されて在庫が予約されますが、**すべてのウェーブ** リスト ページの **プロセス** を選択して、注文のピッキング作業を作成する必要があります。
  - **自動処理** – ウェーブ処理は完全にまたは部分的に自動化できます。 ウェーブ処理を完全に自動化する場合、販売注文、製造オーダー、またはかんばんが作成されるとき、販売注文、製造オーダー、またはかんばんからの明細行を含むウェーブが作成されます。 品目は手持の棚卸資産から控除され、ピッキング作業が作成されます。 ウェーブ処理を部分的に自動化する場合は、ウェーブ処理をトリガーする値を指定できます。 たとえば、ウェーブの明細行の合計重量が値に達したときにウェーブ処理をトリガーする、出荷の最大重量を指定できます。

- オープン ウェーブに出荷を割り当てる場合。 たとえば、午後 12:00 までの注文は 24 時間以内に出荷すると顧客に約束する場合、注文明細行を午後 12:00 までオープン ウェーブに自動的に割り当てるウェーブ テンプレートを設定できます。 その時間にウェーブは自動的に処理されます。

ウェーブが処理されるとき、作成済みのピッキング作業は、作業テンプレート、および倉庫に対して指定された場所のディレクティブに基づきます。 作業テンプレートは、ピッキング作業の作成方法を指定し、場所のディレクティブはピッキングとプットの場所を指定します。

## <a name="create-a-wave-template"></a>ウェーブ テンプレートの作成

ウェーブ テンプレートを設定するには、次の手順に従います。

1. **倉庫管理** \> **設定** \> **ウェーブ** \> **ウェーブ テンプレート** の順に移動します。
1. **新規** を選択して、新しいウェーブ テンプレートを作成します。
1. **ウェーブ テンプレート タイプ** フィールドで、次のいずれかのオプションを選択します。

    - *出荷* - 販売注文と移動オーダーの出荷品目にウェーブ テンプレートを使用します。
    - *製造オーダー* - 製造オーダーの品目を移動するためにウェーブ テンプレートを使用します。
    - *かんばん* - かんばんオーダーの品目を移動するためにウェーブ テンプレートを使用します。

1. **ウェーブ テンプレート名** および **ウェーブ テンプレートの説明** フィールドに、ウェーブ テンプレートの名前と説明を入力します。

    > [!NOTE]
    > 複数のテンプレートが倉庫に対して作成されている場合、**ウェーブ テンプレートの順序** フィールドの番号は、テンプレートの基準に一致したときにテンプレートが適用される順序における、テンプレートの位置を示します。 **上へ移動** または **下へ移動** を選択して、テンプレートの順序を変更できます。

1. **サイト** と **倉庫** フィールドで、ウェーブ テンプレートがウェーブおよびピッキング作業を作成するサイトと倉庫を選択します。
1. ウェーブ処理を自動化する場合は、必要に応じて次の設定を行います。

    - **ウェーブ作成の自動化** - 販売注文、製造オーダー、またはかんばんが倉庫にリリースされるときに、自動的にウェーブを作成するには、*はい* に設定します。
    - **オープン ウェーブに割り当てる** - 明細行がリリースされるときにオープン ウェーブに明細行を自動的に割り当てるようするには、*はい* に設定します。 明細行はウェーブ テンプレートのクエリ フィルターに基づいてウェーブに割り当てられます。
    - **倉庫へのリリース時にウェーブを処理する** - この値を *はい* に設定すると、明細行が倉庫にリリースされたときに自動的にウェーブを処理し作業を作成します。
    - **しきい値でウェーブを自動的に処理する** - *はい* に設定すると、**ウェーブのしきい値** フィールド グループで指定されている重量、出荷、明細行のしきい値に達したときに自動的にウェーブを処理します。 この設定は、**ウェーブ テンプレート タイプ** フィールドで *出荷* が選択されている場合にのみ有効です。
    - **ウェーブのリリースを自動化する** - *はい* に設定して、自動的にウェーブをリリースします。 ピッキング作業が作成され、モバイル デバイス上で利用できます。
    - **補充作業のリリースを自動化する** - 要求ベースの補充作業を作成して自動的にリリースするには、このオプションを *はい* に設定します。 ウェーブのテンプレートに補充ウェーブ メソッドを追加し、*ウェーブの需要* タイプの補充テンプレートを作成する必要があります。 **補充テンプレート** ページで補充テンプレートを設定します。 このためには、ウェーブ テンプレートに [補充] メソッドを追加する必要があります。
    - **作業の作成が失敗したときにウェーブの処理を続行する** - これを *はい* に設定した場合、ロケーション ディレクティブで提案された場所で在庫の引当ができない場合は、空白の場所が使用されます (在庫が既にない場合など)。 *いいえ* に設定する場合は、システムで在庫の引当ができないと、ウェーブは失敗します。

1. 必要に応じて、**ウェーブのしきい値** フィールド グループを設定します。
    - **ウェーブ重量のしきい値** - ウェーブが含むことができる最大重量を入力します。
    - **出荷のしきい値** - ウェーブに含むことができる最大出荷数を入力します。
    - **明細行のしきい値** - ウェーブに含むことができる最大明細行数を入力します。

1. **既定値** フィールド グループで、ウェーブ テンプレートの他の追加基準として使用するウェーブ属性を選択します。 ウェーブの属性は、ウェーブ テンプレートに対して、特定の顧客名などの追加基準を割り当てる場合に便利です。 **ウェーブ属性** ページでこれらの属性を作成します。 

1. **ウェーブ通知ポリシー** を、このテンプレートを使用するウェーブに関連する通知を生成するために使用するポリシーに設定します。 ウェーブ通知ポリシーの例については、[ウェーブ実行通知](wave-execution-notifications.md) を参照してください。

1. **メソッド** クイックタブの **選択したメソッド** ウィンドウは、選択したウェーブ テンプレート タイプのメソッドを一覧表示します。 作業の作成や配布など、ウェーブ メソッド は、テンプレートが作成するアクションを実行します。 これらのアクションも、ウェーブの手順と呼ばれます。 ウェーブ メソッドは、ウェーブ テンプレートの種類ごとにあらかじめ定義されています。 事前定義のウェーブ メソッドは削除できませんが、メソッドの順序を並び替え、さらにメソッドを追加できます。 たとえば、出荷のウェーブ テンプレートを作成する場合、補充およびコンテナー詰めのメソッドを追加できます。 ウェーブのコンテナー詰めをウェーブ メソッドの順序に追加して、ウェーブ テンプレートで処理される明細行のコンテナー詰めを定義できます。 さらにメソッドを追加するには、次の操作を行います。

    - **残りのメソッド** ウィンドウでメソッドを選択してから **左** 矢印を選択して、**選択したメソッド** ウィンドウに追加します。
    - 順序を変更するには、メソッドを選択し、**上** または **下** 矢印を選択します。

    > [!NOTE]
    > メソッドを追加するとき、メソッドは手順の順序の適切な場所に自動的に一覧表示されます。

1. リリースされた明細行を適切なウェーブと一致するクエリを設定するには、アクション ウィンドウで **クエリの編集** を選択します。
1. ウェーブ テンプレートの設定が有効であることを確認するには、**テンプレートの検証** を選択します。