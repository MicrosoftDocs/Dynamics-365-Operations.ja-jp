---
title: "ファイルのアップロード コントロール"
description: "このトピックでは、ファイル アップロード コントロールについて説明します。 このコントロールを使用して、ファイルをアップロードできます。"
author: aneesmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 54311
ms.assetid: 82f47d4d-912c-4f85-81f9-b09c723f72fc
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 46c18e6966b15e96c61f1dfced7ebfe6ab6ce727
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="file-upload-control"></a>ファイルのアップロード コントロール

[!include [banner](../includes/banner.md)]

このトピックでは、ファイル アップロード コントロールについて説明します。 このコントロールを使用して、ファイルをアップロードできます。

<a name="overview"></a>概要
--------

ファイル アップロード コントロールを使用してユーザーはファイルをアップロードできます。 また、これにより開発者は要件に基づいてアップロード処理を制御し、アップロードされたファイルを管理します。 

[![FileUpload001](./media/fileupload001.png)](./media/fileupload001.png) 

ファイル アップロード コントロールには 3 つのスタイルがあります。 スタイルを制御するには、**スタイル** プロパティを使用します。

-   **標準** スタイルは、**参照**、**アップロード**、および **キャンセル** ボタンと同時にファイル名フィールドを表示します。
-   **最小限** スタイルは **参照** ボタンのみ表示します。
-   **MinimalWithFileName** スタイルは、ファイル名フィールドと **参照** ボタンを表示します。

ファイル アップロード コントロールの **FileTypesAccepted** プロパティを使用すると、ユーザーがアップロードできるファイルの種類を制限できます。 ユーザーがアップロードできるファイル タイプは、主に関連するアップロード方法によって制御されます。 ファイル アップロード コントロールの **FileTypesAccepted** プロパティは、さらに制限が必要な場合にのみ使用してください。 アップロード コントロールは、アップロード戦略によって制限されているファイルの種類を指定するしようとすると、**参照**ボタンが使用できなくなります。

| 許可されたファイル タイプ    | アップロード戦略の許可されたファイル タイプ | 最終結果                          |
|-----------------------|---------------------------------------------|---------------------------------------|
| 「.jpg、.png」           | 「.jpg、.png、.gif、.txt」                       | 「.jpg、.png」                           |
| 「image/png」           | 「image/\*」                                  | 「image/png」                           |
| 「image/\*」            | 「image/png」                                 | **参照** ボタンは使用できません。 |
| 「.jpg、.png、.gif、.txt」 | 「.jpg、.png」                                 | **参照** ボタンは使用できません。 |

**OnBrowseButtonClicked**、**OnUploadAttemptStarted**、および**OnUploadCompleted** オーバーライドを使用すると、ファイル アップロード プロセスの様々なステージにフックすることができます。 また、カスタム ファイル アップロード戦略を作成して、**FileUpload Strategy Class** プロパティを使用してファイル アップロード コントロールと関連付けることができます。

## <a name="design-classes"></a>デザイン クラス
開発者がファイル アップロード コントロールのために使用できるクラスには、主に 2 種類あります。

-   **戦略クラスをアップロード** – このクラスにより、開発者はユーザーがアップロードできるファイルの種類およびファイルの最大サイズなどのアップロードされたファイルに適用される必要があるさまざまなパラメータを制御できます。 また、これにより開発者はアップロード済みのファイルが保存される場所および方法を決定します。 すべてのアップロードは抽象 **FileUploadStrategyBase** クラスから戦略クラスへ継承する必要があります。
-   **結果クラスをアップロード** – このクラスにより、開発者は、名前、コンテンツ タイプ、アップロード状態など、ユーザーがアップロードしたファイルの詳細にアクセスできます。 また、これにより開発者は対応するファイルを開いたり削除したりします。 すべてのアップロードは抽象 **FileUploadResultBase** クラスから結果クラスへ継承する必要があります。

このフレームワークは、**FileUploadTemporaryStorageStrategy** という名前のデフォルトのアップロード戦略クラスと **FileUploadTemporaryStorageResult** というデフォルトのアップロード結果クラスを提供します。 このアップロード結果クラスは、アップロードされたファイルを一時的な BLOB ストレージに格納し、ダウンロード URL を提供します。 開発者は、独自のカスタム アップロード戦略を実装し、必要に応じて結果クラスをアップロードすることもできます。 アップロード方法については、**FileUploadStrategyBase** クラスからの 2 つの抽象メソッドは、実装される必要があります: **uploadFile** および **getResultClassName**。 **uploadFile** メソッドは、ファイルが保管される場所および方法を処理します。 **getResultClassName** メソッドは、この方法で使用されるアップロード結果クラスを取得します。 **FileUploadResultBase** クラスには、ファイル名、アップロード ステータス、ファイルのコンテンツタイプ、およびログ メッセージのフィールドがあります。 このクラスは、必要に応じて拡張できます。 すべての新しいプロパティはシリアル化および逆シリアル化することができます。 **openResult** メソッドはストリームとしてファイルを開き、**deleteResult** メソッドは対応するデータ ストレージからファイルを削除します。

## <a name="sequence-diagram"></a>シーケンス図
ファイル アップロード コントロールは、クライアントのファイルとアップロード方法を受け入れ、ファイル サービスに送信します。 ファイル サービスは新しいセッションを開始し、戦略クラスのインスタンスを作成し、**uploadFile** メソッドを呼び出します。 **uploadFile** メソッドがデータ ソース内へのファイルの格納を完了したとき、ファイルのアップロード結果クラスがファイル サービスへを返されます。 このクラスはクライアントに送り返され、後処理に対処する **OnUploadCompleted** イベントをトリガーする可能性があります。 

[![FileUploadControlUsageAndDesign1](./media/fileuploadcontrolusageanddesign1.png)](./media/fileuploadcontrolusageanddesign1.png)




