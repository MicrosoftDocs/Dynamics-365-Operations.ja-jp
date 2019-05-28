---
title: ワークフロー履歴の表示
description: 処理および承認のためにワークフロー システムに送信されたドキュメントの状態を表示するには、これらのステップを使用します。
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a40fe377322e2d64b751f6cace3eda20736cd321
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560455"
---
# <a name="view-workflow-history"></a>ワークフロー履歴の表示

[!include [task guide banner](../../includes/task-guide-banner.md)]

処理および承認のためにワークフロー システムに送信されたドキュメントの状態を表示するには、これらのステップを使用します。 この手順の作成に使用するデモ データの会社は USMF です。

1. [共通] > [照会] > [ワークフロー] > [ワークフロー履歴] へ移動します。
    * 処理および承認のためにワークフロー システムに送信されたドキュメントの状態を表示するには、このフォームを使用します。  
    * ワークフロー インスタンス ID は、ドキュメントを処理中または処理済のワークフロー インスタンスにおけるワークフロー ID コードです。  
    * 状態はドキュメントのワークフローの状態です。  
    * ワークフロー ID はドキュメントを処理中のワークフロー、またはドキュメントを処理したワークフローの ID コードです。  
    * ドキュメントはドキュメントの ID コードです。  
    * ドキュメント タイプは、処理用に送信されたドキュメントのタイプです。  
    * ワークフローはドキュメントを処理中のワークフロー、またはドキュメントを処理したワークフローの名前です。  
    * バージョンはドキュメントを処理中のワークフロー、またはこのドキュメントを処理したワークフローのバージョン番号です。  
    * 作成日時はドキュメントを送信した日時です。  
    * 経過時間はドキュメントが送信されてからの経過時間です。  
    * [再開] ボタンを使用すると、選択したドキュメントのワークフロー プロセスを再開することができます。  
    * [取り消し] ボタンはを使用すると、選択したドキュメントが処理されないように取り消すことができます。   
2. 一覧で、選択された行のリンクをクリックします。
    * 作業項目セクションが展開されていることを確認します。    このセクションでは、選択したドキュメントに関連付けられている作業項目を表示することができます。 たとえば、完了する必要があるタスクや、承認する必要があるドキュメントが表示されます。  
    * [再割り当て] ボタンは、作業項目を別のユーザーに再度割り当てることができるダイアログ ボックスを開きます。  
    * 追跡の詳細セクションが展開されていることを確認します。    このセクションでは、選択したドキュメントのワークフロー履歴を表示することができます。  

