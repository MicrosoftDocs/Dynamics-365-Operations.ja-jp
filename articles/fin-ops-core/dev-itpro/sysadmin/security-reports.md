---
title: 最初から用意されているセキュリティ レポート
description: この記事では、環境内で実行されている一連のセキュリティ ロールと、各ロールに割り当てられているユーザーを理解するのに役立つセキュリティ レポートについて説明します。
author: peakerbl
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecConfiguration, SrsReportViewerForm
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 96a8428843efa275668f05fc1d598ca7bb05cc1f
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109008"
---
# <a name="out-of-box-security-reports"></a>最初から用意されているセキュリティ レポート

[!include [banner](../includes/banner.md)]

財務と運用は、環境内で実行されている一連のセキュリティ ロールと、各ロールに割り当てられている一連のユーザーを理解するのに役立つ豊富なセキュリティ レポートを用意しています。 この記事に記載されているレポートに加え、開発者は **Visual Studio > Dynamics 365 > アドイン > すべてのロールの関連オブジェクトとライセンスを表示** を使用して、すべてのロールのすべてのユーザーのセキュリティ権限を含むワークブックを生成することができます。

これらのセキュリティ レポートはそれぞれ、 **システム管理 \> 照会 \> セキュリティ** で見つかる場合があります。 各レポートの説明は下で用意されています。

## <a name="user-role-assignments"></a>ユーザー ロールの割り当て

**ユーザー ロールの割り当て** レポートは、システムにおける現在のユーザー ロールの割り当てのビューを生成します。 既定では、ロールが割り当てられているすべてのユーザーがレポートに含まれます。 必要に応じて、レポートを生成するときにユーザーのリストを入力することによって、レポートを特定のユーザーのセットに限定することができます。 **ユーザー ロールの割り当て** パラメータ ウィンドウで、**対象に含めるレコード** > **フィルター** に移動します。 ここから、レポートが生成されるユーザーのリストに対してフィルターを追加または削除できます。

![ユーザー ロールの割り当て。](media/User-role-assignments.PNG)

レポート内の各ユーザーに対して、法人または組織レベルで任意の制限と共に、ロールの一覧が提供されます。

## <a name="role-to-user-assignments"></a>ユーザーへのロールの割り当て 

**ユーザーへのロールの割り当て** レポートは、ロールの割り当ての集計を提供します。 レポートのロールを展開すると、ロールに割り当てられたユーザーの一覧が表示され、ユーザー名を展開すると、ロールが適用された制限が表示されます。 **ユーザー ロールの割り当て** レポートで説明したように、ユーザーのセットをフィルタリングするのと同じ方法をこのレポートに適用できます。

![ユーザーへのロールの割り当て。](media/role-to-user-assignments.png)

## <a name="security-role-access"></a>セキュリティ ロール アクセス

**セキュリティ ロールのアクセス権** レポートには、各セキュリティ ロールの有効なアクセス許可が表示されます。 このレポートには、ロールに含まれるすべてのサブロール、職務、および権限全体にタイプごとにグループ化された権限のフラット化されたリストが表示されます。

**セキュリティ ロール アクセス** レポートをバックアップしているデータ セットは非常に大きく、レポートの実行に時間がかかることがあります。 前回レポートが実行されてからセキュリティ ロールへの変更がなかった場合は、レポート パラメーター ウィンドウの **コレクションを再構築** オプションを **いいえ** に設定すると、レポート構築がスキップされます。 これにより、既存のデータ セットからのレポートがレンダリングされます。 レポートの実行が初めてである場合、または役割の定義が変更される可能性が場合、**コレクションの再構築** オプションを **はい** に設定する必要があります。 必要に応じて、**対象に含めるレコード** の下にフィルターを追加することにより、ロールをレポートに含めるように制限することができます。

![セキュリティ ロール アクセス。](media/security-role-access.png)

ロールを展開すると、ロールがアクセスできるオブジェクトのカテゴリが表示されます。 オブジェクトタイプの 1 つを展開すると、ロールに含まれるタイプの各オブジェクトの詳細なリストが表示されます。

## <a name="security-duty-assignments"></a>セキュリティ職務権限の割り当て

**セキュリティ職務権限割り当て** レポートには、ロール内に含まれるすべての職務権限のビューが表示されます。 このレポートは、任意の役割のコレクションで実行されるように構成され、職務分掌が役割間で確実に維持されます。 既定では、すべてのロールがレポートに含まれます。 含まれるロールを制限するには、**含めるレコード** セクションに記載されているフィルタ処理を活用します。

![セキュリティ職務権限の割り当て。](media/security-duty-assignments.png)

**セキュリティ職務権限割り当て** レポートのロール展開では、役割に割り当てられた各職務権限および職務権限の詳細が表示されます。

## <a name="batch-processing-of-reports"></a>レポートのバッチ処理
上記のレポートのいずれかを、バッチ ジョブとして実行するように設定するには、レポートのパラメータ ウィンドウの **バックグラウンドで実行** セクションに移動します。 **バッチ処理** を **はい** に設定し、バッチ タスクジョブ名、バッチ グループ、ジョブをプライベートまたは重大なとして実行するかどうかを指定します。 バッチ タスクが実行されると、レポートが作成されます。

![レポートのバッチ処理。](media/a6142c903497381171bf6c6b27495895.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
