---
title: "ビジネス プロセス モデラー"
description: "この記事では、Microsoft Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラーに関する情報を提供します。 このツールを使用すると、Microsoft Dynamics AX の業務プロセス ライブラリおよびフローチャートを作成、表示、および変更することができます。 また、前提条件の一覧を示し、ビジネス プロセス モデラーの使用を開始する方法についても説明します。"
author: kfend
manager: AnnBe
ms.date: 09/25/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 15031
ms.assetid: 01c38560-f588-4558-a7ec-3af1bb518069
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 98aaa1fda9bd28705d39ea85e845e91f3092bde0
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="business-process-modeler"></a>ビジネス プロセス モデラー

[!include [banner](../../includes/banner.md)]

この記事では、Microsoft Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラーに関する情報を提供します。 このツールを使用すると、Microsoft Dynamics AX の業務プロセス ライブラリおよびフローチャートを作成、表示、および変更することができます。 また、前提条件の一覧を示し、ビジネス プロセス モデラーの使用を開始する方法についても説明します。

Microsoft Dynamics Lifecycle Services では、ビジネス プロセス モデラ－を使用して、Microsoft Dynamics AX の業務プロセス ライブラリおよびフローチャートを作成、表示、および変更することができます。 ビジネス プロセス モデラーは、[アメリカ生産性品質センター (APQC)](http://www.apqc.org/) によって説明された業界標準プロセスを使用して、Microsoft Dynamics AX プロセスを配置するのに役立ちます。 Microsoft Dynamics AX で、業務上のニーズと既定のプロセスの間でフィットギャップ分析を実行することができます。 また、新しい業務プロセスを追加して、Microsoft Dynamics AX 2012 でまだ定義されていないプロセスのためにフローチャートを作成することができます。 ビジネス プロセス モデラーのコンポーネントは、次のアプリケーションで使用することができます。

-   Microsoft Visual Studio Team Foundation Server (TFS) – ギャップの連結リストを生成して、プロセス フローへの参照を含む作業項目としてそれらを TFS に手動でインポートすることができます。
-   Microsoft Word – 業務プロセスのドキュメントを生成できます。
-   Microsoft Visio – 業務プロセスのマップを Visio ファイルにエクスポートできます。

## <a name="prerequisites"></a>前提条件
ビジネス プロセス モデラーを使用するには、次の製品が必要です。

-   AX 2012 R3 および Microsoft Dynamics AX 2012 R2 の累積的な更新プログラム 7 に含まれるタスク レコーダーは、ビジネス プロセス モデラーにおけるカスタム プロセスの生成をサポートしています。 前のリリースでは、更新されたタスク レコーダーは修正プログラムとして使用できます。 この修正プログラムには、クライアントの更新プログラムとモデル ファイルが含まれています。 Microsoft Dynamics AX 2012 のすべてのクライアントに、クライアント用更新プログラムをインストールする必要があります。 2 つの修正プログラムを使用できます。
    -   Microsoft Dynamics AX 2012 R2 – サポート技術情報の記事 [2863182](http://go.microsoft.com/fwlink/?LinkId=309911)
    -   Microsoft Dynamics AX 2012 と Microsoft Dynamics AX 2012 Feature Pack – サポート技術情報の記事 [2863182](http://go.microsoft.com/fwlink/?LinkId=309910)
-   Microsoft Office 2010 以降のバージョンではドキュメントの生成をサポートします。
-   Windows Media Player は業務プロセス ビデオの再生をサポートします。

## <a name="getting-started"></a>はじめに
ビジネス プロセス モデラーにアクセスするには、次の手順を実行します。

1.  [Lifecycle Services に移動](https://lcs.dynamics.com).
2.  サインインしてプロジェクトを開き、**ビジネス プロセス モデラー** タイルをクリックします。 **業務プロセス ライブラリ**には 3 つのセクションが表示されます。
    -   **自分のライブラリ**には、ユーザーが作成または追加したビジネス プロセスが含まれています。
    -   **コーポレート ライブラリ**には、組織内のユーザーによってアップロードされた独自の業務プロセスが含まれます。
    -   **グローバル ライブラリ**には、産業間の標準の業務プロセスが含まれています。

3.  標準的なビジネス プロセス ライブラリを **グローバル ライブラリ** セクションから **マイ ライブラリ** セクションにコピーするには、**グローバル ライブラリ** セクションでタイルを右クリックし、[アプリ] バーで **コピー** をクリックします。
4.  業務プロセス ライブラリが**自分のライブラリ** セクションに追加された後、タイルをクリックして業務プロセス ライブラリを表示します。


<a name="additional-resources"></a>その他のリソース
--------

[ビジネス プロセス モデラーの業務プロセス ライブラリ](../business-process-libraries-business-process-modeler.md)

[ビジネス プロセス モデラーのフローチャート](../flowcharts-business-process-modeler.md)




