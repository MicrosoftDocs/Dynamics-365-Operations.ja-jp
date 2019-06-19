---
title: ガント管理作成ガイド
description: このトピックでは、Gantt コントロールを使用して新しいフォームを作成する方法について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 11/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 17311
ms.assetid: e5cd372c-6ac2-4995-bb3c-ff863b40fedb
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 90659ea7fb0eb6cbfa6ac7ce7e0deedcfab2e7c4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572524"
---
# <a name="gantt-control-development-guide"></a>ガント管理作成ガイド

[!include [banner](../includes/banner.md)]

このトピックでは、Gantt コントロールを使用して新しいフォームを作成する方法について説明します。 Tutorial_Gantt フォームにあるコードを調べることを強くお勧めします。 このコードは、Gantt コントロールのすべての機能を示し、データをロードしてアプリケーション プログラミング インターフェイス (API) を操作する方法を示しています。

<a name="whats-new-for-gantt"></a>ガント チャートの新機能
--------------------

Microsoft Dynamics AX 2012 では、クライアントは Win32 アプリケーションで、拡張機能は Microsoft ActiveX、WinForm、または Microsoft Windows Presentation Foundation (WPF) のコントロールを使用していました。 ActiveX と ManagedHost コントロールは、HTML ベースのプラットフォームと互換性がないため、カスタム コントロールを追加するためには使用できなくなります。 代わりに、新しい拡張可能コントロール フレームワークで HTML と JavaScript を使用してコントロールを追加することができます。 新しいガント管理は、このフレームワークを使用して実装されています。 以前のバージョンとは異なり、独自のフォームの使用およびコントロールの拡張に追加のライセンス手数料を支払う必要はないことに注意してください。

## <a name="high-level-overview-of-the-control"></a>コントロールの高レベルの概要
次の図は、ガント管理の視覚的要素を示しています。

[![ガントの要素](./media/ganttchartelements.png)](./media/ganttchartelements.png)

コントロールを新しいフォームに追加するには、フォーム デザインの一番上のノードを右クリックし、**新規追加**&gt;**Gantt** を選択します。 **高さ**および**幅**プロパティを **SizeToAvailable** に設定した後、デザイナーで設定する必要がある他のプロパティはありません。 他の多くのコントロールとは異なり、Gantt コントロールはデータ ソースにバインドすることはできません。 代わりに、コードからコントロールにすべてのデータを追加する必要があります。

## <a name="adding-activities-links-and-milestone-markers"></a>活動、リンク、マイルストーン マーカーの追加
ガント チャートの最も基本的な要素はタスク活動です。 各活動は、個々の行がグラフに割り当てられます。 活動は、親活動を参照することによって、ツリーのような階層を形成できます。 また、任意の 2 つの活動は、リンクを使用して (階層間で) 互いに接続できます。 コントロールにデータを追加するには、追加する要素のインスタンスを含むリストを作成します。 次に、**parm** メソッドを使用して、リストをコントロールに割り当てます。 データを変更するときに、リストの内容だけの変更はできないことに注意してください。 データが変更されたことをクライアントに通知し、リフレッシュをトリガーするには、**parm** メソッドを使用してリストをコントロールに再割り当てする必要があります。

[![活動およびリンクの API](./media/ganttchartactivitiesapi.png)](./media/ganttchartactivitiesapi.png)

各活動は、すべてのアクティビティ タイプに固有の ID を持つ必要があります。 この ID は、階層とリンクをビルドするために必要です。 ID は、ユーザー操作後にサーバーに通知されたときに活動を識別するためにも使用します。 マイルストーンには 2 つのタイプがあります。マイルストーン アクティビティは、チャート内で独自の行を受け取り、リンクから参照できるスタンドアロン アクティビティです。マイルストーン マーカーは関連するアクティビティと同じ行に表示されます。 両方のタイプのマーカーは、Dynamics Symbol フォントの記号を使用して表されます。

## <a name="column-headers-and-content"></a>列のヘッダーとコンテンツ
コントロールの左側にある「グリッド」で、データを列に配置できます。 列の定義は、**GanttControlColumn** オブジェクトのリストである **GanttControl.parmColumns** プロパティを使用して提供されます。 列の内容は、**GanttControlActivity.parmColumnTexts** プロパティを通じてアクティビティのテキスト文字列を含む単純な**リスト** オブジェクトとして指定されます。 列リスト内の値は文字列でなければならないことに注意してください。 したがって、数字、列挙型、日付などの書式は、サーバー側で発生する必要があります。 **utcdatetime** の書式設定では、ユーザーの優先時間帯を考慮する必要があります。これは、ガント チャートが表示されるときにその時間帯が使用されるためです。

[![コントロールを構成するための API](./media/ganttchartconfigurationapi.png)](./media/ganttchartconfigurationapi.png)

## <a name="working-times"></a>作業時間
活動はカレンダーを参照できます。 カレンダーは基本的に、作業時間間隔のリストです。 カレンダーを使用すると、「セル」(行とタイム スケール間隔の交差) に異なる背景色を付けることによって、作業時間を非作業時間から視覚的に区別することができます。 これらの作業時間間隔は、標準カレンダー テーブルから取得する必要はないことに注意してください。 間隔は、どこからでも読み込むことができる単なるデータです。 カレンダーは良い概要を与えることができる素晴らしい機能ですが、いくつかのパフォーマンスの問題を考慮する必要があります。 カレンダーを有効にすると (**GanttControlConfiguration.parmUseCalendars** を **true** に設定して)、各「セル」は HTML 形式で表示されます。 カレンダーが非常に粒度の細かいタイムスケールで長期間にわたり多くの活動を示している場合は、多くの DIV 要素が存在します。 ブラウザおよびハードウェアによっては、多数の DIV 要素がユーザーにパフォーマンスの問題を引き起こす可能性があります。 この場合、カレンダーをオフにしなければならない場合があります。 この方法で、表示する必要がある DIV 要素の数を大幅に削減します。 コントロールでは、カレンダーをオフにしてパフォーマンスを向上させることはできません。 特定のシナリオに基づいて、ユーザーに最適なものを決定する必要があります。

## <a name="color-use"></a>色の使用
活動およびマイルス トーン マーカーなどの要素には、色プロパティがあります。 通常、**WinAPI::RGB2int** メソッドを使用して特定の色の整数値を計算するか、カラー ピッカーを使用して値を設定します (カラー ピッカーは **ColorSelection::selectColor** メソッドを使用して開きます)。 自身で色を制御するではなく、色が現在のテーマに従うことを指定できます。 **GanttControlConfiguration.parmUseThemeColors** オプションを **true** に設定すると、現在のテーマにはない色の値が設定されている場合、それらはオーバーライドされます (どの色も手動では指定できません)。 テーマ色を使用するときは、活動を暗色または明色のいずれで表示するかを決定するために、**parmIsActive** フラグが活動に対して使用されます。

## <a name="interactions"></a>相互関係
ユーザーがガント チャートにかかわるたびに、サーバー側のコードを通知するためにイベントが発生します。 現在、以下のイベントが利用可能です。

-   onActivitySelected(str \_activityId, GanttControlActivityIdCollection \_allSelectedActivityIds)
-   onActivityDblClick(str \_activityId)
-   onSummaryActivityExpand(str \_activityId)
-   onSummaryActivityCollapse(str \_activityId)
-   onActivityChanged(GanttControlActivityModification \_modification, GanttControlActivityModificationResponse \_response)

これらすべてのイベントはクライアントからの一方向の通知です。 ただし、応答を設定できるため、**onActivityChanged** イベントは多少特殊なものです。 通常、ユーザーが変更を加えた場合 (たとえば、アクティビティを新しい時間にドラッグする)、他のアクティビティも更新するか、アクティビティ自体を調整する必要があります (たとえば、列テキストを変更する必要がある)。 **GanttControlActivityModificationResponse** 応答で、更新する必要のあるアクティビティの一覧を提示することができます。 ユーザーによる変更がそのまま受け入れられる場合、応答を設定する必要はありません。 ただし、少なくとも、新しい開始日と終了日を表示するよう保証するため、ほとんどの場合現在の活動の列テキストは更新される必要があります。 活動で、**parmAllowMove** フラグは、活動が移動できるかどうかを決定します。 ただし、**GanttControlConfiguration** の高レベルのフラグは、任意の活動を移動 (**parmAllowMoveActivities**) またはサイズを変更 (**parmAllowResizeActivities**) できるかどうか、または、活動の完了率を変更 (**parmAllowCompletionChange**) できるかどうかを決定します。



