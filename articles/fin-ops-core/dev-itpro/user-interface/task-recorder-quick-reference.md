---
title: タスク レコーダーのクイック リファレンス
description: この記事では、タスク レコーダー メニュー内の各ボタンの動作を説明するクイック リファレンス シートを提供します。
author: RobinARH
ms.date: 12/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 31141
ms.assetid: 8536e688-33f1-4f0c-a402-b1de2d253fbc
ms.search.region: global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e558684465b7d84360c2bc61ca15c721036d4c24e60090c91fc7853dfac4431
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719315"
---
# <a name="task-recorder-quick-reference"></a>タスク レコーダーのクイック リファレンス

[!include [banner](../includes/banner.md)]

この記事では、タスク レコーダー メニュー内の各ボタンの動作を説明するクイック リファレンス シートを提供します。

## <a name="main-menu"></a>メイン メニュー

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><a href="./media/Task-recorder-menu-create-play-edit-playback.png"><img src="./media/Task-recorder-menu-create-play-edit-playback.png" alt="Task recorder menu" class="alignnone size-full wp-image-290291" width="206" height="199" /></a></td>
<td><h3 id="create-recording">記録の作成</h3>
新しい記録の作成を開始するには、このオプションを選択します。
<h3 id="play-recording-as-guide">記録をガイドとして再生</h3>
このオプションを選択すると、ヘルプ トピックとして表示されたり、タスク ガイドとして再生されたときのレコードの概要を確認できます。
<h3 id="change-recording-text">記録の編集</h3>
ステップで表示される記録名、説明、またはテキストを変更する必要がある場合は、このオプションを選択します。
<h3 id="playback-recording">記録の再生</h3>
手順を追加または削除する必要がある場合は、このオプションを選択します。 このモードを使用して記録を自動的に再生することもできます。</td>
</tr>
</tbody>
</table>

## <a name="open-and-save-options"></a>オプションを開いて保存する
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td> <a href="./media/Update-recording-steps-menu.png"><img src="./media/Update-recording-steps-menu.png" alt="Open and save options" class="alignnone size-full wp-image-290301" width="197" height="136" /></a><a href="./media/Save-menu.png"><img src="./media/Save-menu.png" alt="Open and save options" class="alignnone size-full wp-image-290311" width="197" height="136" /></a></td>
<td><h3 id="opensave-fromto-this-pc">開く/保存/この PC に</h3>
これらのオプションを使用すると、コンピューターに保存されている記録を開くか、コンピューターに記録を保存できます。
<h3 id="opensave-fromto-lcs">Lifecycle Services を開き保存する</h3>
このオプションを使用すると、Lifecycle Services ライブラリに保存されているレコーディングを開くか、Lifecycle Services ライブラリにレコーディングを保存できます。
<h3 id="open-from-recents">最新から開く</h3>
このオプションを使用すると、最近作成したタスク記録のリストから選択できます。
<h3 id="export-as-work-document">Word ドキュメントとしてエクスポート</h3>
このオプションを使用すると、記録のステップのリストを含む Word 文書をダウンロードできます。
<h3 id="publish-for-mobile-application">モバイル アプリケーション用に発行する</h3>
このオプションを使用すると、モバイル アプリケーションのタスク記録を発行することができます。
<h3 id="save-as-developer-recording">開発者の記録として保存</h3>
このオプションを使用すると、開発者の記録としてタスクの記録を保存することができます。</td>
</tr>
</tbody>
</table>

## <a name="playback-controls"></a>再生コントロール
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><a href="./media/playback-controls-menu-Playnext-Playall.png"><img src="./media/playback-controls-menu-Playnext-Playall.png" alt="Play next and Play all" class="alignnone size-full wp-image-290321" width="208" height="120" /></a><a href="./media/playback-controls-menu-Pause.png"><img src="./media/playback-controls-menu-Pause.png" alt="Pause" class="alignnone size-full wp-image-290331" width="208" height="120" /></a></td>
<td><h3 id="play-next-pending-step">次の保留中のステップの再生</h3>
このオプションを使用すると、ステップ リストの矢印で示す、次の保留中のステップがタスク レコーダーで実行および記録されます。
<h3 id="play-to-selected-step">選択したステップまで再生</h3>
このオプションを使用すると、タスク レコーダーが次の保留中のステップから保留中のステップの再生と記録を開始し、このオプションがクリックされたときにリストで選択されたステップを再生した後に停止します。
<h3 id="play-all-pending-steps">保留中のすべてのステップの再生</h3>
このオプションを使用すると、保留中の残りのステップがなくなるまで、保留中の残りのステップがタスク レコーダーですべて再生および記録されます。
<h3 id="pause">一時停止</h3>
このオプションは、再生中のみ表示されます。 このオプションを使用すると再生を手動で一時停止できます。</td>
</tr>
</tbody>
</table>

## <a name="step-actions"></a>ステップ アクション
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><a href="./media/Steps-menu-Delete-step.png"><img src="./media/Steps-menu-Delete-step.png" alt="Delete step" class="alignnone size-full wp-image-290341" width="225" height="98" /></a><a href="./media/Steps-menu-Restore-step.png"><img src="./media/Steps-menu-Restore-step.png" alt="Restore step" class="alignnone size-full wp-image-290351" width="223" height="99" /></a></td>
<td><h3 id="start-sub-taskend-sub-task">サブ タスク/終了サブ タスクを開始</h3>
これらのオプションを使用すると、録音に特別な手順を追加できます。 これらの特別なステップはタスク ステップであり、これらを使用してサブ タスクが開始および終了されるタイミングを示します。 これらのオプションは、再生の進行中は無効になっています。
<h3 id="delete-steprestore-step">ステップの削除/復元ステップ</h3>
これらのオプションを使用すると、録音から手順を削除できます。 保留中のステップを削除した場合は、再生中にスキップされ、記録されません。 記録されたステップを削除する場合は、そのステップに削除のフラグが設定されるため、記録を保存するときに記録に含まれません。 正常に記録された手順のみを復元することができます。 進行中には、タスクを削除することはできません。</td>
</tr>
</tbody>
</table>

## <a name="steps-list"></a>ステップ リスト

![ステップ一覧の例。](media/example-step-list.png)

### <a name="step-counter"></a>ステップ カウンター
<img src="media/step-counter.png" alt="Step counter"/>

これにより、記録されたステップの数が記録されます。 これには、再生コントロールを使用して実行されるステップと、クライアントで実行するアクションによって記録されたステップが含まれます。

### <a name="pending-step"></a>保留中のステップ
<img src="media/pending-step.png" alt="Pending-step"/>

この記号は、保留中でまだ記録されていないステップを表します。 保留中の手順は、再生コントロールを使用して再生できます。 保留中のステップが正常に再生されたとき、そのステップが記録され、シンボルが適切に更新されます。 <em>保留中のステップは、記録を保存するときに記録に含まれません。</em> 記録できるように、保留中のステップを最初に再生する必要があります。 手順が再生され、正常に記録されている場合、手順は記録の保存時に含まれます。

### <a name="next-pending-steptd"></a>次の保留中のステップ</td>
<img src="media/next-pending-step.png" alt="Next pending step"/>

この記号は、次の保留中のステップを表します。 再生を開始する場合、これが再生される最初の手順になります。

### <a name="queued-pending-step"></a>キューに入っている保留中のステップ
<img src="media/queued-pending-step.png" alt="Queued pending step"/>

この記号は再生待ちの保留中のステップを表します。 再生が一時停止されるとき、またはキューに入っている保留中のステップが再生されるとき、この記号は更新されます。

### <a name="recorded-action-step"></a>記録されたアクションのステップ
<img src="media/recorded-action-step.png" alt="Recorded action step"/>

この記号は、再生されたかまたは手動で記録されたかのいずれかで、正常に記録されたステップを表します。

### <a name="recorded-info-step"></a>記録された情報のステップ
<img src="media/recorded-info-step.png" alt="Recorded info step"/>

この記号は、再生され、記録された情報ステップを表します。 情報ステップは、アプリケーションでのアクションの実行にはつながりません。

### <a name="recorded-begin-sub-task-step"></a>記録の開始サブタスク ステップ
<img src="media/recorded-begin-sub-task-step.png" alt="Recorded begin sub-task step"/>

このシンボルは、サブタスクの開始を示します。 サブタスク ステップは、アプリケーションでのアクションの実行にはつながりません。

### <a name="recorded-end-sub-task-step"></a>記録の終了サブタスク ステップ
<img src="media/recorded-end-sub-task-step.png" alt="Recorded end sub-task step"/>

このシンボルは、サブタスクの終了を示します。 サブタスク ステップは、アプリケーションでのアクションの実行にはつながりません。

### <a name="deleted-recorded-step"></a>削除された記録されたステップ
<img src="media/deleted-recorded-step.png" alt="Deleted recorded step"/>

この記号は、削除対象としてマークした正常に記録されたステップを表します。 削除対象としてマークされている記録された手順は、記録を保存するときに含められません。 ステップを削除するときにステップが正常に記録されていれば、記録を保存する前に削除されたステップを復元することができます。

### <a name="deleted-pending-step"></a>削除された保留中のステップ
<img src="media/deleted-pending-step.png" alt="Deleted pending step"/>

保留中のステップを削除すると、再生されるまで保留中の記号が保持されます。 再生時にそれはスキップされます。 再生およびスキップされていない限り、保留中のステップを復元することができます。

### <a name="skipped-step"></a>スキップされたステップ
<img src="media/skipped-step.png" alt="Skipped step"/>

この記号は、保留中に削除され、再生中にスキップされたステップを表します。 省略した手順は、再生されず、記録されません。 スキップされたステップは記録されないため、記録を保存する際には含まれません。 スキップされたステップを復元することはできません。

### <a name="error-step"></a>エラー ステップ
<img src="media/error-step.png" alt="Error step"/>

この記号は、再生システムによって試行されたものの、再生に失敗したステップを表します。 エラー ステップは記録されません。また、記録を保存する際には含まれません。 エラー ステップを復元することはできません。 エラー手順が発生したときに再生が自動的に一時停止します。 これにより、再生を続行する前に交換ステップを記録できます。 エラー ステップは次の理由で発生する可能性があります。
<ul>
<li>ステップで必要なフォームまたはルックアップが開いていないため、ステップを再生できませんでした。</li>
<li>ステップで必要なボタンまたはフィールドが無効になっているか、表示されていないか、フォームに表示されていないため、ステップを再生できませんでした。</li>
<li>フォームの名前またはコントロールの名前が変更されたため、ステップが再生できませんでした。</li>
<li>このステップは、コントロールへのフレームワークの変更のために再生できませんでした。</li>
</ul>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]