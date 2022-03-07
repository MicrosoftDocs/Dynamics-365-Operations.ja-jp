---
title: ビジネス プロセス モデラー (BPM) でのタスクの完了
description: このトピックでは、業務プロセス モデル (BPM) で完了できるその他のタスクに関する情報が提供されます。
author: AngelMarshall
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 13301
ms.assetid: ''
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 813c46acba3b3d4934d7b08e5cea453b3857a80e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752740"
---
# <a name="complete-tasks-in-business-process-modeler-bpm"></a>ビジネス プロセス モデラー (BPM) でのタスクの完了

[!include [banner](../includes/banner.md)]

## <a name="upload-a-task-recording"></a>タスク記録のアップロード

1. Microsoft Dynamics Lifecycle Services (LCS) で、プロジェクトの **業務プロセス ライブラリ** ページにて、タスク記録をアップロードするライブラリを選択します。

    ![業務プロセス ライブラリ ページのライブラリ](./media/choose-library.PNG "業務プロセス ライブラリ ページのライブラリ")

2. タスクの記録をアップロードするプロセスを選択します。 

    ![プロセスの選択](./media/select-upload.PNG "プロセスの選択")

3. **概要** ウィンドウで、**アップロード** を選択します。 **参照** を選択して、アップロードするファイルを検索して選択し、次に **アップロード** を選択します。

    ![AXTR のアップロード ダイアログ ボックス](./media/upload.PNG "AXTR のアップロード ダイアログ ボックス")
    
## <a name="download-a-task-recording"></a>タスク記録のダウンロード

BPM プロセスにアップロードされたタスク記録 (AXTRファイル) をダウンロードできます。 

1. **業務プロセス ライブラリ** ページの LCS プロジェクトで、タスク記録をダウンロードするライブラリを選択します。

2. タスク記録をアップロードするプロセスを選択します。 

3. **概要** ウィンドウで、**ダウンロード** を選択して タスク記録 (AXTR) を保存します。 

    ![AXTR のダウンロード](./media/Download%20AXTR.png "AXTR のダウンロード")
    
## <a name="export-a-methodology-to-word"></a>方法を Word へエクスポート

1. LCS プロジェクトの **業務プロセス ライブラリ** ページで、エクスポートするライブラリを選択します。
2. エクスポートするプロセスを選択し、右ウィンドウで **ドキュメント** を選択してダウンロードを開始します。

    > [!NOTE]
    > この手法は、選択したプロセス ステップから開始されます。

## <a name="publish-a-bpm-library"></a>BPM ライブラリの公開

- LCS プロジェクトの **業務プロセス ライブラリ** ページで、コピーするライブラリのタイルの省略記号ボタン (...) を選択し、**パブリッシュ** を選択します。

    ![BPM ライブラリの公開](./media/PUB_DIS.png "BPM ライブラリの公開")

## <a name="distribute-a-bpm-library"></a>BPM ライブラリを配分

BPM ライブラリを配布すると、そのライブラリは、組織に所属するすべてのユーザーが利用できます。 つまり、組織のドメインを使用して LCS にサインインするすべてのユーザー (たとえば、 @contoso.com アカウントを持つすべてのユーザー)が利用できるようになります。

1. プロジェクトに招待するよう顧客に依頼します。
2. 組織のアカウントを使用して、顧客の LCS プロジェクトにログインします。
3. **業務プロセス ライブラリ** ページで、ライブラリを **コーポレート ライブラリ** ウィンドウから、顧客のプロジェクトにコピーします。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]