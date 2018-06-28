---
title: "タスク ガイドと BPM を使用して承認テスト スイートを作成する"
description: "このトピックでは、タスク ガイドと BOMを 使用して受け入れテスト スイートを作成する方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 03/27/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 13301
ms.assetid: 
ms.search.region: Global
ms.author: ntecklu
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: ab8d54d8493d4fe208168b5f4be169905cb6fa12
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="create-an-acceptance-test-suite-using-task-guides-and-bpm"></a>タスク ガイドと BPM を使用して承認テスト スイートを作成する

タスク ガイドおよびビジネス プロセス モデラー (BPM) を使用して、ユーザー承認テスト計画を作成することができます。 業務プロセスごとに承認テストを整理してから BPM を Visual Studio Team Services (VSTS) に同期し、テストの実行と結果を管理することができます。 このトピックでは、手動テストまたは自動テストに使用する受入れテスト スイートを作成するプロセスについて説明します。

## <a name="create-a-bpm-library"></a>BPM ライブラリの作成

ビジネス プロセス モデラー (BPM) ライブラリを作成するにはいくつかの方法があります。 BPM でライブラリを作成する方法の詳細については、[BPM ライブラリの作成、編集、および参照](creating-editing-browsing.md) を参照してください。

説明目的で、このトピックでは、経費精算書の作成および注文要求の承認などの一般的な業務プロセスを含むライブラリを使用します。 Excel インポート機能を使用してライブラリを作成しました。  

![Excel からインポート](./media/import_from_excel.png.PNG "Excel からインポート")

## <a name="record-test-cases-and-upload-to-bpm"></a>テスト ケースを記録して BPM にアップロード 

BPMライブラリを作成した後は、タスク レコーダーを使用してテスト ケースを作成し、それから BPM にそのケースをアップロードする必要があります。 これを行うにはいくつかの方法があります。 

既に必要なタスク記録が付属されているライブラリを使用している場合、この手順を省略できます。 それ以外の場合、クライアントで新しいタスク記録を作成して LCS に直接保存するか、AXTR ファイルをダウンロードしてから後で BPM ライブラリにアップロードします。 

### <a name="create-and-save-a-new-task-recording"></a>新しいタスク記録を作成して保存する 
1. クライアントを開いて、サインインします。 
2. 記録中に使用する会社を選択します。
3. **設定** > **タスク レコーダー**に移動します。

![タスク レコーダーの選択](./media/select_task_recorder.png.PNG "タスク レコーダーの選択")

4. **新しい記録の作成**をクリックします。
5. コンフィギュレーション名を入力し、**開始**をクリックします。 記録は、**開始** をクリックすると開始されます。
6. 記録が完了したら、タスク レコーダー ウィンドウで、**停止** をクリックします。
7. 添付された BPM にタスク記録を保存するには、**Lifecycle Services に保存** をクリックします。

![タスク レコーダー オプション](./media/task_recorder_options.png.PNG "タスク レコーダー オプション")

8. 記録を保存するライブラリを選択し、**保存** をクリックします。 それ以外の場合、**ディスクに保存** を選択し、次のセクション「BPM に AXTR ファイルをアップロードする」の手順に従います。

### <a name="upload-an-axtr-file-to-bpm"></a>BPM に AXTR ファイルをアップロード 

1. Lifecycle Services (LCS) で、プロジェクトの**業務プロセス ライブラリ** ページで、タスク記録をアップロードするライブラリを選択します。
2. **作成と編集**をクリックして、明細行内で、タスク記録をアップロードするプロセスを特定し選択します。
3. 右ウィンドウで**アップロード**をクリックします。 

![AXTR 1 のアップロード](./media/upload_axtr_1.png.PNG "AXTR 1 のアップロード")

4. **参照**をクリックして、アップロードするファイルを検索して選択し、次に**アップロード**をクリックします。

![AXTR 2 のアップロード](./media/upload_axtr_2.png.PNG "AXTR 2 のアップロード")

### <a name="save-an-existing-task-recording-to-bpm"></a>既存のタスク記録を BPM を保存

1. 既存のタスクの記録を添付するには、クライアントにサインインします。
2. **設定** > **タスク レコーダー**に移動します。
3. **タスクの記録を編集** を選択し、LCS に直接を保存するか、AXTR にダウンロードしてから BPM にアップグレードすることによって、そのファイルを添付します。

## <a name="sync-with-vsts"></a>VSTS と同期   

次に、VSTS プロジェクトと BPM ライブラリを同期する必要があります。 詳細については、「[LCS プロジェクトのコンフィギュレーションおよび LCS に接続](synchronize-bpm-vsts.md#configure-your-lcs-project-to-connect-to-vsts)」を参照してください。 

コンフィギュレーションが完了した後、VSTS プロジェクトと BPM ライブラリを同期します。
1. **業務プロセス ライブラリ**ページで、同期するライブラリのタイルの省略記号ボタン (...) を選択し、**VSTS 同期**を選択します。

![VSTS Sync1](./media/vsts_sync_1.png.png "VSTS Sync1")

また、BPM ライブラリ内のツールバーから VSTS 同期を開始することができます。 省略記号ボタン (...) を選択し、**VSTS の同期** を選択します。

![VSTS Sync2](./media/vsts_sync_2.png.png "VSTS Sync2")

2. VSTS の同期が完了した後、省略記号ボタン (…) を選択し、**テスト ケースの同期**を選択します。

![テスト ケースの同期](./media/sync_test_case.png.PNG "テスト ケースの同期")

3. このステップが完了したら、タスク記録は VSTS のテスト_ケースになり、**要件** タブの下にリンクが表示されます。 

![テスト ケースの表示](./media/view_test_case.png.PNG "テスト ケースの表示")


テスト ステップに加えて、タスクを記録する XML ファイルが VSTS テスト ケースに付属します。 テストの実行を自動化する場合、このファイルを必要とします。 

## <a name="create-a-test-suite-in-vsts"></a>VSTS でテスト スイートを作成する

次に、VSTS でテスト スイートを作成する必要があります。 これにより一連のテストを実行できるので、結果の管理、調査、追跡が容易になります。 

1. VSTS にログインし、テストするプロジェクトとテスト計画を選択します。 
2. ツール バーで、**テスト**を選択します。
3. 左ウィンドウで、**+** を選択してから、**静的スイート**を選択します。 
4. スイート名を入力します。
5. **既存の追加**をクリックし、**LCS:Test Cases** タグを照会します。
6. **実行** > **テスト ケースの追加**の順にクリックします。

![テスト ケースの追加](./media/add_test_cases.PNG "テスト ケースの追加")
 
7. 詳細と関連付けられている XML ファイルを表示し、作業項目を作成するには、テスト ケースを選択します。   

![テスト ケースの詳細](./media/test_case_details.png.PNG "テスト ケースの詳細")

 >[!NOTE]
 > この例は、すべてのテスト ケースが追加された包括的受入れテスト スイートを作成する方法を示しています。 さまざまなテスト スイートを作成して、カスタム クエリを使用し特定のテスト ケースを追加することができます。 

### <a name="run-manual-test-cases"></a>手動テスト ケースを実行

テスト スイートがある場合、サンドボックスおよびテスト環境で Dynamics 365 for Finance and Operations アプリケーションが更新された後、回帰テストを使用する準備ができるようになります。 テスト スイートで手動でテスト ケースを実行、またはテスト スイートの一部であるタスク記録を再生し、VSTS を使用してテスト ケースを成功または失敗としてマークすることができます。

![マーク済み VSTS テスト](./media/vsts_test_marked.png.png "マーク済み VSTS テスト")

VSTS は、**テスト ランナー** というツールを提供して、手動テスト ケースの実行も管理します。 テスト ランナーの使用の詳細については、[手動テストの実行](https://docs.microsoft.com/en-us/vsts/manual-test/getting-started/run-manual-tests) を参照してください。

VSTS はテストだけでなく、結果の管理と軽減策のための豊富な管理機能セットを提供するので、VSTS の活用をお勧めします。

### <a name="run-automated-test-cases"></a>自動テスト ケースを実行

Dynamics 365 Unified Operations プラットフォームは、タスク記録に基づいてテスト ケースを作成し、VSTS を使用してそれらのテスト ケースの自動実行を管理するためのツールを開発者を提供します。 テスト ケースの実行は、**ビルドおよびテスト**環境トポロジのビルドおよびテストの自動化機能の一部です。
詳細については、[継続的な配信ホーム ページ](../dev-tools/continuous-delivery-home-page.md) および [開発 ALM ブログ](http://blogs.msdn.microsoft.com/axdevalm/) を参照してください。

