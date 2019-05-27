---
title: ビジネス プロセス モデラー (BPM) でのタスクの完了
description: このトピックでは、業務プロセス モデル (BPM) で完了できるその他のタスクに関する情報が提供されます。 たとえば、BPM ライブラリの発行、方法のエクスポート、および BPM ライブラリを配布することができます。
author: kfend
manager: AnnBe
ms.date: 09/17/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012, Operations
ms.custom: 13301
ms.assetid: ''
ms.search.region: Global
ms.author: ntecklu
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 0036a1d6ea408f58ca84de0d2a782b0e0142ad2d
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537282"
---
# <a name="complete-tasks-in-business-process-modeler-bpm"></a>ビジネス プロセス モデラー (BPM) でのタスクの完了

[!include [banner](../includes/banner.md)]

## <a name="upload-a-task-recording"></a>タスク記録のアップロード

1. Microsoft Dynamics Lifecycle Services (LCS) で、プロジェクトの**業務プロセス ライブラリ**ページにて、タスク記録をアップロードするライブラリを選択します。

    ![業務プロセス ライブラリ ページのライブラリ](./media/choose-library.PNG "業務プロセス ライブラリ ページのライブラリ")

2. タスクの記録をアップロードするプロセスを選択します。 

    ![プロセスを選択](./media/select-upload.PNG "プロセスを選択")

3. 右ウィンドウで**アップロード**を選択します。 **参照** を選択して、アップロードするファイルを検索して選択し、次に **アップロード** を選択します。

    ![AXTR ダイアログ ボックスのアップロード](./media/upload.PNG "AXTR ダイアログ ボックスのアップロード")

## <a name="export-a-methodology-to-word"></a>方法を Word へエクスポート

1. LCS プロジェクトの**業務プロセス ライブラリ** ページで、エクスポートするライブラリを選択します。
2. エクスポートするプロセスを選択し、右ウィンドウで **ドキュメント** を選択してダウンロードを開始します。

    > [!NOTE]
    > この手法は、選択したプロセス ステップから開始されます。

## <a name="publish-a-bpm-library"></a>BPM ライブラリの公開

- LCS プロジェクトの**業務プロセス ライブラリ** ページで、コピーするライブラリのタイルの省略記号ボタン (...) を選択し、**パブリッシュ**を選択します。

    ![BPM ライブラリを発行する](./media/PUB_DIS.png "BPM ライブラリを発行する")

## <a name="distribute-a-bpm-library"></a>BPM ライブラリを配分

BPM ライブラリを配布すると、そのライブラリは、組織に所属するすべてのユーザーが利用できます。 つまり、組織のドメインを使用して LCS にサインインするすべてのユーザー (たとえば、 @contoso.com アカウントを持つすべてのユーザー)が利用できるようになります。

1. プロジェクトに招待するよう顧客に依頼します。
2. 組織のアカウントを使用して、顧客の LCS プロジェクトにログインします。
3. **業務プロセス ライブラリ**ページで、ライブラリを**コーポレート ライブラリ**ウィンドウから、顧客のプロジェクトにコピーします。
