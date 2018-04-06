---
title: "Microsoft Project クライアント統合"
description: "プロジェクト スケジュールの計画や管理は複雑な題目になるため、プロジェクト マネージャーは、これらのタスク管理に役立つツールを使用する必要があります。 Microsoft Project クライアントとの統合により、プロジェクト作業分解構造を開いて管理するためのサポートが提供されます。"
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 4a3445417d5ae88e2ff3676962a82921a7ab475d
ms.contentlocale: ja-jp
ms.lasthandoff: 03/26/2018

---

# <a name="microsoft-project-client-integration"></a>Microsoft Project クライアント統合

[!include[banner](../includes/banner.md)]

プロジェクト スケジュールの計画や管理は複雑な題目になるため、プロジェクト マネージャーは、これらのタスク管理に役立つツールを使用する必要があります。 Microsoft Project クライアントとの統合により、プロジェクト作業分解構造を開いて管理するためのサポートが提供されます。 プロジェクト マネージャーは、変更を Finance and Operations のプロジェクト作業分解構造に公開できます。

> [!NOTE]
> Microsoft Dynamics 365 for Finance and Operations 2017 年 7 月の更新プログラムを使用している場合、KB 4054797 および 4055884 をインストールする必要があります。

## <a name="configure-the-microsoft-project-client-add-in"></a>Microsoft Project クライアント アドインの構成
Microsoft Project クライアントとの統合を有効にするためには、 ユーザ クライアントの Microsoft Project アプリケーションに Microsoft Dynamics 365 アドインがインストールされていることが必要です。 これは**プロジェクト管理ワークスペース**を使用して行われます。

•   ワークスペースの [**リンク**] > [**設定**] セクションの [** クライアント アドインの構成**] フォームをクリックします。

•   [**開く**] をクリックし、要求されたら [**実行**] をクリックします。

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Microsoft Project クライアントの、既存のドラフト作業分解構造を開き、編集します。
Finance and Operations のプロジェクトで既に作業分解構造が作成されている場合、作業分解構造がドラフト ステータスの場合は、Microsoft Project クライアント アプリケーションで作業分解構造を開くことができます。 [**プロジェクト**] ページから開くには、[**計画**] タブから [**Microsoft Project で開く**] リンクをクリックします。このページは Microsoft Project クライアント アプリケーション内で、[**Microsoft Dynamics 365**] タブの [**開く**] をクリックすることでも開くことができます。一覧から [**法人**] および [**プロジェクト**] を選択します。

> [!NOTE]
> ブラウザーとして Internet Explorer を使用している場合、 [**保存**] をクリックして、ファイルがダウンロードされた場所から手動で開く必要があります。 または、[**保存して開く**] をクリックし、Microsoft Project クライアントのファイルを開きます。 保存するときにファイル名を変更できません。

Microsoft Project クライアントを使用してファイルを編集する前に、チェックする必要があります。[**Microsoft Dynamics 365**] タブの [**チェック アウト**] をクリックします。これにより、他のユーザーが同時に Finance and Operations 内から作業分解構造を編集することを防ぐことができます。 編集を完了した後に作業分解構造を公開するには、[**Microsoft Dynamics 365**] タブの [**チェック イン**] をクリックします。

プロジェクト チームがすでに Finance and Operations のプロジェクトに追加されている場合、リソース リストにはチームメンバーが配置されます。 プロジェクト チームがまだプロジェクトに追加されていない場合は [**Microsoft Dynamics 365**] タブの [**リソース**] ボタンをクリックして、リソースを選択して Microsoft Project クライアント内でチームを構築できます。 

次のデータは、チェックイン プロセスの一部として Finance and Operations に同期されます。

•   タスク名

•   開始日

•   終了日

•   先行処理

•   リソース名

•   カテゴリ

•   リソース カテゴリ

•   作業時間

•   メモ

•   優先順位

> [!NOTE]
> 他の列を Microsoft Project クライアント ファイルに追加する場合、それらはファイルに保存されず、ファイルが再び開かれた時には表示されません。

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Microsoft Project クライアントを使用して既存のプロジェクトの作業分解構造を作成します。
Microsoft Project クライアントを使用して新しい作業分解構造を作成するには、次の手順に従います。


1.  Microsoft Project クライアントを開きます。

2.  [**Microsoft Dynamics 365**] タブの、[**開く**] をクリックします。

3.  プロジェクトの [**法人**] を選択します。

4.  [**プロジェクト**] を選択します。

5.  [**Microsoft Dynamics 365**] タブの [**チェック アウト**] をクリックします。

6.  Finance and Operations に公開する準備ができたら、[**Microsoft Dynamics 365**] タブの [**チェック イン**] をクリックします。

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Microsoft Project クライアントを使用して既存プロジェクトの既存の作業分解構造を置換します。
Microsoft Project クライアントを使用して新しい作業分解構造を作成し、既存のプロジェクトの既存の作業分解構造を置換するには、次の手順に従います。

1.  Microsoft Project クライアントを開きます。

2.  Microsoft Project クライアントのスケジュールの作成。

3.  [**Microsoft Dynamics 365**] タブで、[**変更を保存**] > [**既存のプロジェクトを置き換え**] をクリックします。

4.  プロジェクトの [**法人**] を選択します。

5.  [**プロジェクト**] を選択します。

6.  [**OK**] をクリックします。

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Microsoft Project クライアントから新しいプロジェクトを作成します。


1.  Microsoft Project クライアントを開きます。

2.  Microsoft Project クライアントのスケジュールの作成。

3.  [**Microsoft Dynamics 365**] タブで、[**変更を保存**] > [**新しいプロジェクトに保存**] をクリックします。

4.  プロジェクトの [**法人**] を選択します。

5.  必要に応じて**プロジェクト ID** を入力します。

6.  **プロジェクト名**を入力します。

7.  [**プロジェクト タイプ**]、[**プロジェクト グループ**] および [**プロジェクト契約 ID**] を選択します。 または、[**新規**] をクリックして新しいプロジェクト契約を作成します。

8.  リソースに使用する [**カレンダー**] を選択します。

11. [**OK**] をクリックします。

