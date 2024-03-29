---
title: 独自の業務プロセスからビジネス プロセス モデラー (BPM) へのアップロード
description: Microsoft Dynamics Lifecycle Services では、タスク レコーダーの更新されたバージョンを使用して独自の業務プロセスに関する情報を記録できます。
author: gianugo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: gianura
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 18991
ms.assetid: 74808085-e971-4e7b-8547-d3549273d14a
ms.openlocfilehash: 84e2070f147b19a489bfcfcb189ce1bfca404e7b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280007"
---
# <a name="upload-custom-business-processes-to-business-process-modeler-bpm"></a>独自の業務プロセスからビジネス プロセス モデラー (BPM) へのアップロード

[!include [banner](../includes/banner.md)]

Microsoft Dynamics Lifecycle Services では、タスク レコーダーの更新されたバージョンを使用して独自の業務プロセスに関する情報を記録できます。 記録するファイルをビジネス プロセス モデラーにアップロードすることができます。

この記事では、タスク レコーダーの更新バージョンの場所と、記録するカスタム ビジネス プロセス ファイルをアップロードする方法について説明します。 タスク レコーダーの更新されたバージョンは修正プログラムとして使用できます。 以下のサイトから修正プログラムをダウンロードすることができます。

-   Microsoft Dynamics AX 2012 および Microsoft Dynamics AX 2012 Feature Pack – サポート技術情報の記事 [2863182](https://go.microsoft.com/fwlink/?LinkId=309910)
-   Microsoft Dynamics AX 2012 R2 – サポート技術情報の記事 [2863182](https://go.microsoft.com/fwlink/?LinkId=309911)

更新されたタスク レコーダーを操作する方法の詳細については、[Microsoft Dynamics AX 2012 のタスク レコーダー更新](https://go.microsoft.com/fwlink/?LinkID=310185) を参照してください。

## <a name="upload-custom-recorded-business-processes"></a>カスタムで記録した業務プロセスのアップロード
業務プロセス コンポーネント (\*.axbpm ファイル) を業務プロセス ライブラリにアップロードすることができます。 これらのファイルは、タスク レコーダーから生成されます。 アップロード後、ビジネス プロセス モデラーに記録されたプロセスを表示および変更できます。 記録したカスタム ビジネス プロセスをアップロードするには、次の手順を実行します。

1.  **プロジェクト** ホーム ページで、**業務プロセス モデラー** タイルをクリックします。
2.  **業務プロセスのライブラリ** ページで、**自分のライブラリ** セクションまたは **コーポレート ライブラリ** で、**アップロード** をクリックします。
3.  **アップロード** ページで、業種を選択し、名前と説明をアップロードするファイルを入力します。 **アップロード** をクリックし、.axbpm ファイルを選択し、**OK** をクリックします。 アップロード プロセスには少し時間がかかる場合があります。 **管理** ページでは、アップロードの状態を表示できます。
4.  業務プロセスのファイルをアップロードした後、**業務プロセスのライブラリ** ページから業務プロセス フレームワークを表示できます。


## <a name="additional-resources"></a>追加リソース

[Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM)](/dynamicsax-2012/appuser-itpro/business-process-modeler-lcs)

[ビジネス プロセス モデラー (BPM) ビジネス プロセス ライブラリ](business-process-libraries-business-process-modeler.md)

[ビジネス プロセス モデラー (BPM) のフローチャート](flowcharts-business-process-modeler.md)





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
