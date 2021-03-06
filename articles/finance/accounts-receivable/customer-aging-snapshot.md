---
title: 顧客エイジングのスナップショット
description: このトピックでは、顧客エイジング スナップショットに関する情報を提供します。 経過期間スナップショットは、ある時点での顧客のグループのエイジングされた残高を計算します。
author: JodiChristiansen
ms.date: 05/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b88d3fe97d14d3e2f766367de501148063582000
ms.sourcegitcommit: 16376a301a0f121f384d77f9976638f701f8e88e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2021
ms.locfileid: "6123365"
---
# <a name="customer-aging-snapshots"></a>顧客エイジングのスナップショット

[!include [banner](../includes/banner.md)]

このトピックでは、顧客エイジング スナップショットに関する情報を提供します。 経過期間スナップショットは、ある時点での顧客のグループのエイジングされた残高を計算します。 すべての顧客または顧客プール内の顧客のいずれかに対して経過期間スナップショット レコードを作成します。

経過期間スナップショットからの情報は、**エイジングした残高** リスト ページと **コレクション** ページに表示されます。 **エイジングした残高** リスト ページを使用する前に、経過期間スナップショットを作成する必要があります。 リスト ページでは、経過期間スナップショットを作成した顧客に対してのみ情報が一覧表示されます。

**顧客の与信および回収** ワークスペースには、顧客のエイジングも表示されます。 詳細については、[与信および回収管理 Power BI コンテンツ](credit-collections-power-bi.md) を参照してください。

> [!NOTE]
> エイジング スナップショットの作成に必要な時間の短縮を図る場合は、**機能管理** ワークスペースで **顧客エイジング パフォーマンス向上** 機能 を有効 にします。 ただし、この機能を有効にした場合は、顧客管理システムを使用することはできません。 顧客管理グループが選択されている場合は機能しませんが、エイジング スナップショットを作成できます。

顧客エイジング スナップショットを作成する場合は、次のフィールドを使用して顧客エイジング スナップショットに関する情報を入力します。

- **エイジング期間の定義** - 経過期間スナップショットで、作成したエイジング期間の定義を選択します。 各エイジング期間の定義に対して、経過期間スナップショットを 1 つずつ持たせることができます。 エイジング スナップショットとエイジング期間の定義は、個別に作成する必要があります。
- **プール ID** - このフィールドはオプションです。 プールを使用して、経過期間スナップショットで処理する必要がある一連の顧客を定義できます。 顧客プールを選択した場合、経過期間スナップショット プロセスは顧客プールの一部である顧客カウントにのみ適用されます。 選択した顧客プールは、**エイジング スナップショット** タイプである必要があります。 このフィールドを空白のままにすると、すべての顧客に対して経過期間スナップショットが作成されます。

    > [!NOTE]
    > **顧客エイジング パフォーマンス拡張** 機能が有効になっている場合は、顧客管理グループを選択しない。

- **基準** - 経過期間スナップショットは、選択した日付に基づいて変化します。

    - **トランザクションの日付** - トランザクションの日付に基づいて各トランザクションをエイジングします。
    - **期日** - 期日に基づいて各トランザクションをエイジングします。
    - **ドキュメントの日付** - ドキュメントの日付に基づいて各トランザクションをエイジングします。

- **エイジング日** - 経過期間スナップショットに対して **現在の日付** として使用する日付を選択します。 その後、エイジング期間はこの日付に基づいて計算されます。 

    - **今日の日付** - システム日付を使用します。 定期的なバッチで処理をおこなうように設定されている場合は、このオプションを選択します。 その後、バッチを実行毎回、その実行のシステム日付が使用されます。
    - **選択した日付** - 指定した日付を使用します。 このオプションを選択した場合は、エイジング日を入力する必要もあります。

    たとえば、現在のエイジング期間は 30 日です。 このフィールドで **今日の日付** を選択した場合、現在のエイジング期間は今日の日付から始まり 、29 日前の日付が含まれます。 **選択した日付** を選択して日付を入力した場合、現在のエイジング期間は指定された日付から始まり 、その前 29 日間が含まれます。

- **収集ステータスの更新** - このオプションを はい に設定すると、エイジング日付が **支払約束日** フィールドの日付を超えた場合に **取り込み** ページのトランザクションの収集ステータスが **支払を約束** から **支払の約束が破棄された** を **はい** に更新されます。 **コレクション** ページでコレクションのステータスを変更しない場合は、このオプションを **いいえ** に設定します。
- **顧客残高がゼロの顧客を含める** - 残高に関係なく、すべての顧客を含める場合は、このオプションを **はい** に設定します。 すべての顧客を含める場合は、**顧客エイジング パフォーマンス向上** 機能を有効にし、顧客管理を使用しない方が推奨されます。 残高がある顧客のみを含める場合は、このオプションを **いいえ** に設定します。 残高を持たない顧客はスキップされるので、この設定を使用するとパフォーマンスが速く向上します。
- **会社範囲** - **会社範囲** タブで、経過期間スナップショットに含める 法人 (会社) を選択します。 集中型支払用に設定されている法人のみを選択できます。 選択した法人のトランザクションは、すべての法人で同じ当事者 ID を持つ顧客のエイジング期間に含まれます。 通貨の値は、経過期間スナップショットを作成する時にサインインしている法人の会計通貨でカバーされます。

このプロセスをバッチで実行するスケジュールを設定することをお勧めします。

> [!NOTE]
> 経過期間スナップショットの作成時にバッチパフォーマンスを改善するには、**売掛金勘定パラメーター** ページの **コレクション** タブの **コレクション既定値** クイック タブの **バッチ タスクの最大数** フィールドに数値を入力します。 **年齢顧客残高** フィールドでは、最初に既定値を **100** に設定し、その値を調整して状況に合わせて処理を最適化することをお勧めします。

