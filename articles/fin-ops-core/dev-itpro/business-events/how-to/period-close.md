---
title: 財務期間終了のビジネス イベント
description: このトピックでは、財務期間終了の業務プロセスでビジネス イベントを使用して、情報を取得し、内部コントロールを提供する方法について説明します。
author: suhasrao1985
manager: AnnBe
ms.date: 10/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: Platform update 26
ms.dyn365.ops.version: 2019-6-30
ms.openlocfilehash: b8131e332dcaee11b4d36cbe0c2e3e60983ef007
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688099"
---
# <a name="business-events-in-financial-period-close"></a>財務期間終了のビジネス イベント
[!include [banner](../../includes/banner.md)]

このトピックでは、財務期間終了の業務プロセスでビジネス イベントを使用して、情報を取得し、内部コントロールを提供する方法について説明します。

このトピックを完了するには、プラットフォーム アップデート 26 以降で、バージョン 10.0.2 (2019 年 5 月) を実行する必要があります。

## <a name="scenario-overview"></a>シナリオの概要

タスク管理は、業界全体にわたる業務プロセスを管理するための基本となる要素です。 最初から用意されている機能により、ユーザーは業務プロセス タスクを構造化された方法で管理できるようになります。 **財務期間終了** ワークスペースは、会社の会計期間の終了プロセスでのタスクを管理するため中心となる場所を提供することにより、これらの機能を示しています。

このトピックでは、**財務期間終了** ワークスペースを使用して、すべての期間終了に関連付けられたタスクを追跡およびレポートする方法を調査することに最近決めた組織について取り上げます。 パフォーマンス管理とトレーサビリティは、現在の設定でこの組織が直面する課題の一部です。 そのため、組織は業務プロセスの変革に取り組み、**財務期間終了** ワークスペースの機能を識別しました。 この演習では、次のような業務要件が明らかになりました。

1. タスクを開始する必要があるときに通知を受ける機能
2. ドキュメントを添付するための機能
3. 添付ファイルの記録管理と廃棄機能
4. 事前に定義されたロジックに基づいて、複数の承認者がタスクを承認する機能
5. 監査のためのタスク アンケート
6. 期間終了プロセスの現在のステータスを追跡し、効率を把握するためのパフォーマンス分析を行うレポート機能

## <a name="high-level-design"></a>高レベル設計

前述の要件を達成するために、組織は **財務期間終了** ワークスペースに最初から用意されている機能を使用しました。 ギャップ分析により、ワークスペースと基礎となるデータ エンティティに対してマイナーな拡張を実行することにより、組織は要件 2、5、および 6 を達成し、要件 4 を 部分的に達成できることが明らかになりました。 要件 1 と 3、および要件 4 の一部を達成するために、組織は Power Automate の使用を選択しました。 次の図は、ソリューションのアーキテクチャの概要を表示します。

<img alt="High-level design" src="../../media/Image1.PNG" width="70%">

## <a name="managing-attachments-by-using-microsoft-power-automate-and-sharepoint-online"></a>Microsoft Power Automate および SharePoint オンライン を使用した添付ファイルの管理

経理担当者は **財務期間終了** ワークスペースにタスクを表示して、作業を開始します。 SharePoint Online ドキュメント タイプを使用して、添付ファイルがタスクに追加されます。 Microsoft Power Automate の SharePoint トリガーは、次の図に示す Power Automate をトリガーするために使用されます。 この Power Automate は SharePoint メタデータを、 **財務期間終了** ワークスペースのタスクからのメタデータで更新します。 この目的のために、ドキュメント ライブラリに SharePoint 列が作成されました。 **財務期間終了** ワークスペースに追加されるすべての添付ファイルの添付ファイル メタデータを保持するために、個別の添付ファイル データ エンティティが作成されました。 カスタム エンティティのフィールドは、 Power Automate 内の SharePoint オンライン列にマップされました。 指定されたドキュメント タイプを使用するドキュメントが定義済みの SharePoint Online ライブラリに作成されると、Power Automate がトリガーされ、カスタム データ エンティティからメタデータを取得し、SharePoint Online のドキュメントのメタデータ列を更新します。

<img alt="Power Automate for managing attachments" src="../../media/Image2.png" width="70%">

## <a name="enabling-internal-controls-by-using-business-events-and-power-automate"></a>ビジネス イベントと Power Automate を使用した内部コントロールの有効化

経理担当者がタスクを完了し、タスクのレビュー準備が整うと、**確認状態** カスタム フィールドの値が **確認準備完了** に更新されます。 この更新が行われると **変更ベースのアラートがトリガーされる** ビジネス イベントによって Power Automate がトリガーされます。 このビジネス イベントのペイロードには、タスク名と領域名が含まれています。 Power Automate は、タスク名と領域名の組み合わせと **確認状態** フィールドの値を使用して、 Power Automate によって調整された電子メール ベースのワークフローを介してタスクをルーティングします。 この Power Automate は、承認を待機し、タスク ログに新しいコメントを追加し、承認プロセスの結果と関連するメタデータの両方に基づいて **財務期間終了** ワークスペースでタスクを更新します。 カスタム データ エンティティは、Power Automate を使用して、**財務期間終了** ワークスペースをクエリおよび更新するために構築されました。

### <a name="subscribing-to-the-business-event"></a>ビジネス イベントの購読

次の例は、変更ベースのアラート ビジネス イベントをサブスクライブする一般的な手順を示しています。

1. コネクタ トリガーを Power Automate アプリに追加し、変更ベースのアラート ビジネス イベントをサブスクライブします。

    <img alt="Subscribing to the business event" src="../../media/Image3.png" width="70%">

2. ビジネス イベントのペイロードを解析します。

    ビジネス イベントがトリガーされると、それは Power Automate をトリガーします。 このビジネス イベントにはペイロードが含まれています。 この手順では、ペイロードを解析し、必要な変数を初期化します。

    <img alt="Parsing the business event payload" src="../../media/Image4.PNG" width="70%">

3. ペイロードの値に基づいてタスクを取得します。

    タスクが更新されると、ビジネスイベントは Power Automate をトリガーします。 この時点で、ペイロードが解析された後、タスクに関する基本情報がわかります。 この手順では、カスタム データ エンティティを使用して、タスクに関する詳細情報を取得します。

    <img alt="Retrieving the task" src="../../media/Image5.png" width="70%">

4. 基準に基づいて Microsoft Excel ファイルから承認者を取得します。

    次に、承認者の一覧を決定して、適切な方法で承認要求を送信できるようにする必要があります。 このリストは、SharePoint Online ライブラリ内のカスタム Excel ファイルです。 この手順では、Excel ファイルをクエリして承認者の一覧を取得します。 また、各タスクの添付ファイルへのリンクを取得して、添付ファイルを承認者に送信できるようにします。

    <img alt="Retrieving approvers" src="../../media/Image6.png" width="70%">

5. 承認要求を送信するための準備を行います。

    このステップでは、前の手順で収集および組み立てたすべての情報を使用して、承認要求を送信するように Power Automate を準備します。

    <img alt="Preparing to send the request for approval, part 1" src="../../media/Image7.png" width="70%">

    <img alt="Preparing to send the request for approval, part 2" src="../../media/Image8.png" width="70%">

    <img alt="Preparing to send the request for approval, part 3" src="../../media/Image9.png" width="70%">

6. 承認プロセスを開始します。

    このステップでは、承認要求は Power Automate から送信されます。

    <img alt="Starting the approval process" src="../../media/Image10.png" width="70%">

7. 承認者が実行する承認アクションを処理します。

    承認者が承認要求を受信し、アクションを実行すると、 Power Automate が通知され、追加の処理が行われます。

    <img alt="Processing the approval action" src="../../media/Image11.png" width="70%">

8. 承認結果を使用してタスクを更新します。

    承認プロセスの結果に基づいて、タスクがその結果で更新されます。

    <img alt="Updating the task, part 1" src="../../media/Image12.png" width="70%">

    <img alt="Updating the task, part 2" src="../../media/Image13.png" width="70%">

## <a name="conclusion"></a>まとめ

このトピックで説明する組織の業務要件については、このソリューションの開発は最小限であり、主に **財務期間終了** ワークスペース、ビジネス イベント、SharePoint Online、および Power Automate に依存して機能を推進しています。 開発は、ページへのフィールドの追加、カスタム データ エンティティの作成、およびページ ラベルの変更に制限されています。 Power Automate は、承認プロセスの柔軟性も高めています。 このソリューションは Microsoft 365 スイート内のさまざまなアプリケーションを利用するため、内部ユーザーは既に使い慣れているアプリケーションを使用できます。 したがって、必要な変更管理の量は限られています。

結論として、ビジネス イベントは機能を拡張する固有の機会を提供しますが、アプリ内での広範なカスタマイズを回避させることもできます。 ビジネス イベントの使用を開始する前に、以下の点について考慮する必要があります。

- ソリューションのセキュリティ要件を設定します。 ビジネス イベントはロールベースのセキュリティを遵守します。 この動作は、一部のユース ケースでは有益な場合があります。
- ビジネス イベント機能は、今後も拡張されます。 新しい機能に注目してください。

ビジネスイベントおよび Power Automate はローコードまたはコードなしの拡張機能を実装するための優れた機会を提供します。 重要な点は、このフレームワークが役立つ機会を特定することですが、いくつかの制限事項についても理解しておく必要があります。
