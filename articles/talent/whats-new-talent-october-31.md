---
title: Dynamics 365 Talent - Core HR (2018 年 10 月 31 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent - Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4851c62a19bb562c7f5f578aecbae99cfcdb982f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461771"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-31-2018"></a>Dynamics 365 Talent - Core HR (2018 年 10 月 31 日) の新機能および変更された機能

**ビルド 8.1.2031**

このトピックでは、Core HR の新機能または変更された機能について説明します。

## <a name="create-links-from-talent-to-finance"></a>Talent から Finance へのリンクの作成
この新しいナビゲーション機能により、Talent から Finance へリンクすることができ、Finance ページへの直接のナビゲーションが提供されます。 リンクがコンフィギュレーションされている場合、リンクの名前およびグループを指定することができますが、そのリンクは Talent 内で表示され、ターゲット ページは Finance 内で開かれます。

#### <a name="coming-soon"></a>間もなく公開
フィールド コンテキストは、直接ナビゲーションのために、Finance の対応するレコードに将来追加されます。 たとえば、**フィールドへのリンク** を使用して、Finance 内の特定の従業員または職位へ直接移動するためのコンテキストを提供できます。

### <a name="configure-target-systems"></a>ターゲット システムの構成

Talent において、システム管理者は、システム管理ワークスペースを通じて表示されるリンクを定義することができます。 リンクの「ターゲット」となる移動先の Finance 環境は、コンフィギュレーションの一部です。 この操作は、ターゲット システムに名前を付け、Finance 環境の URL を提供することによって行われます。 提供できる Finance URL の例を次に示します。https://devax00124aos.cloud.test.dynamics.com/ ターゲット システムのコンフィギュレーションの後に、リンクを定義することができます。

### <a name="configure-links"></a>リンクを構成する

作成される各リンクには、次の情報が定義されます。

- リンク - リンクの名前、識別のためにのみ使用。

- このリンクを有効にする - Talent のユーザーにリンクを表示する場合、**はい** に設定します。

- 表示名 - Finance へのリンクとして表示される名前を定義します。 このデータは、現在翻訳されていません。

- フォームのサーフェス リンク - リンクを表示するページを選択します。

- グループ - グループは必須ではありませんが、グループを使用してリンクを整理する場合、既存のグループを選択するか、または **グループ** フィールドを使用して新しいグループを作成します。

- ターゲット システム - **ターゲット システムのコンフィギュレーション** オプションを使用して作成されたターゲット システムを選択します。 これは、リンクを使用して移動する時に使用される Finance 環境になります。

- ユーザーの現在の会社を使用する - Finance へ移動する時にユーザーの現在の会社のコンテキストを使用する場合に **はい** を選択します。 **いいえ** が選択されている場合、使用する会社を選択することができます。

- ターゲット メニュー項目 - 移動する時にリンクが使用する Finance からメニュー項目を入力します。 直接移動できるメニュー項目は使用可能です。 必要なメニュー項目を検索するために、Finance を開き、ナビゲーションのターゲットとなるページを開きます。 URL からメニュー項目をコピーします。 たとえば、リンクにより Finance and Operations の従業員リストに移動したい場合、URL の「&mi」の後に表示される値を入力します。 https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees。 この例の従業員リスト ページに移動するメニュー項目は、HcmWorkerListPage_Employees です。

- データ ソースへのリンク - リンクが参照しているデータのソースを選択します。 **作業者** および **職位** など、最も一般的なソースが利用可能です。

- フィールドへのリンク - (間もなく公開) このフィールドの選択により、Talent の 1 つのレコードから Finance の 1 つのレコードへの直接ナビゲーションが可能になります。

### <a name="access-to-links"></a>リンクへのアクセス

**このリンクを有効にする** オプションが **いいえ** に設定されている場合でも、システム管理者は、定義されたページ上で新しく作成されたリンクを参照することができます。 これは、リンクをテストするために、他の従業員に表示されるより前に使用できます。 他のすべてのロールには、**このリンクを有効にする** オプションを **はい** に設定した後、コンフィギュレーションされたリンクのみ表示されます。 リンクが表示されるページにアクセスできる従業員は、このリンクにアクセスできます。

ユーザーには、Finance and Operations のページにアクセスするために定義された Finance 内でのセキュリティ権限もあります。 そうでない場合、リンクを使用する時に、セキュリティ ダイアログ ボックスが表示されます。


## <a name="other-changesfixes"></a>その他の変更または修正

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a>将来の開始日を持つ職位は、新しい従業員に割り当てることができません。

従業員が将来の日付に設定された職位に割り当てられるように、変更が行われました。 将来の開始日が設定された職位を選択することができ、ワークフローの保存または完了において従業員の割り当てができます (ワークフローが有効の場合)。

### <a name="new-employee-cannot-be-assigned-existing-position"></a>新しい従業員は既存の職位に割り当てることができません。

新しい従業員の割り当てが既存の職位に割り当てられるように、変更が行われました。

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a>従業員の開始日が過去の日付でレコードが保存されている場合、勤続年数または職場の場所は表示されなくなります

過去の従業員について変更を保存する場合、**勤続日数** および **職場の場所** の可視を修正できるように、変更が行われました。

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a>作業者ページにおいて、将来の日付の雇用にデータを入力することはできません

将来の日付の雇用に対する雇用データは、作業者のメイン ページでは無効にされています。 雇用データは、**日付マネージャー** のページを通じて入力できます。 ワークフロー プロセス中の雇用データの直接入力を有効にできるように、将来のリリースで追加の変更が行われます。

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a>HcmPersonalContactPersonEntity への ValidFrom および ValidTo の追加

特定の給付金統合シナリオを有効にするために「発効日」および「失効日」を日付に含められるよう、Data Management Framework (DMF) エンティティの HcmPersonalContactPersonEntity が更新されました。 

## <a name="known-issue"></a>既知の問題
- **問題**: 作業者に新しい添付ファイルを追加する時、**新規** および **編集** ボタンが灰色表示になります。 
- **回避策:** 添付ファイル ページを開く前に、**作業者** ページの Factbox が閉じていることを確認します。 **作業者** ページが読み込まれる時、FactBoxes が閉じている場合には、添付ファイルボタンが有効になります。 (この問題は次のプラットフォーム更新プログラムで修正されます。)
