---
title: ビジネス プロセス モデラー (BPM) ビジネス プロセス ライブラリ
description: このトピックでは、ビジネス プロセス ライブラリを表示する方法、コピーおよび変更する方法、ライブラリに関する情報を Microsoft Word にエクスポートする方法について説明します。
author: RobinARH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 13301
ms.assetid: 94c88919-39de-4a7b-9d1a-359b99500abe
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: afe5eb36ba17fb6efd83df19fabef16282e869b5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752742"
---
# <a name="business-process-libraries-in-business-process-modeler-bpm"></a>ビジネス プロセス モデラー (BPM) ビジネス プロセス ライブラリ

[!include [banner](../includes/banner.md)]

この記事では、ビジネス プロセス モデラーで標準ビジネス プロセス ライブラリを表示する方法、ビジネス プロセス ライブラリをコピーおよび変更する方法、ビジネス プロセス ライブラリに関する情報を Microsoft Word にエクスポートする方法について説明します。

このトピックでは、標準ビジネス プロセス ライブラリを表示する方法、ビジネス プロセス ライブラリをコピーおよび変更する方法、ビジネス プロセス ライブラリに関する情報を Microsoft Word にエクスポートする方法について説明します。

## <a name="view-and-copy-a-standard-business-process-library"></a>標準のビジネス プロセス ライブラリの表示とコピー
業務プロセス ライブラリ ページで標準業務プロセス ライブラリを選択することができます。 このページを開くには、Lifecycle Services にサインインしてプロジェクトを開き、[ビジネス プロセス モデラー] タイルをクリックします。

> [!IMPORTANT]
> 利用可能なビジネス プロセス ライブラリは、Lifecycle Services プロジェクトの作成時に選択された業種によって異なります。

標準のビジネス プロセス ライブラリを選択するには、次の手順を実行します。

1.  Lifecycle Services にサインインしてプロジェクトを開き、**ビジネス プロセス モデラー** タイルをクリックします。
2.  **グローバル ライブラリ** または **コーポレート ライブラリ** セクションで、ライブラリを右クリックします。
3.  アプリ バーで、**コピー** をクリックします。 ライブラリは、**自分のライブラリ** セクションに追加されます。
4.  **自分のライブラリ** セクションで、ライブラリをクリックして業務プロセス ライブラリを表示します。

## <a name="search-for-a-process-within-a-library"></a>ライブラリ内のプロセスの検索
業務プロセス ライブラリ内で関連業務プロセスを検索することができます。

1.  Lifecycle Services にサインインしてプロジェクトを開き、**ビジネス プロセス モデラー** タイルをクリックします。
2.  業務プロセス ライブラリを開きます。
3.  検索フィールドで、検索語または語句、または $ の後にオブジェクトの AOT 名を入力します。 たとえば、$LedgerJournalTransDaily。

## <a name="modify-a-business-process-library"></a>業務プロセス ライブラリの変更
前の手順で説明したように、プロジェクトに関連付けられている場合は、業務プロセス ライブラリを変更することができます。 ビジネス プロセス ライブラリを変更するするには、次の手順を実行します。
1.  Lifecycle Services にサインインしてプロジェクトを開き、**ビジネス プロセス モデラー** タイルをクリックします。
2.  業務プロセス ライブラリを開きます。
3.  業務プロセス ライブラリに変更を加えます。
    -   既存のライブラリ ノードを変更するには、ノードを右クリックして [アプリ] バーを表示し、**編集** をクリックします。 変更を行ってから、**保存** をクリックします。
    -   ライブラリ ノードを追加するには、ノードを **活動** 一覧からライブラリにドラッグします。 新しいノードを右クリックし、**編集** をクリックしてノードの名前およびアクティビティの他の情報を変更します。 変更を行ってから、**保存** をクリックします。
    -   ライブラリ ノードを削除するには、ノードを右クリックし、**削除** をクリックします。

## <a name="export-a-business-process-library-to-word"></a>業務プロセス ライブラリを Word へエキスポート
業務プロセス ライブラリ、および関連付けられたすべてのフローチャートに関する情報を、Word 文書にエクスポートすることができます。 ビジネス プロセス ライブラリを Word にエクスポートするには、次の手順を実行します。
1.  Lifecycle Services にサインインしてプロジェクトを開き、**ビジネス プロセス モデラー** タイルをクリックします。
2.  業務プロセス ライブラリを開きます。
3.  **主要な業務プロセス** リストで、ライブラリの最上位ノードを右クリックします。
4.  アプリ バーで、**Doc** をクリックして、ドキュメントを保存します。







[!INCLUDE[footer-include](../../../includes/footer-banner.md)]