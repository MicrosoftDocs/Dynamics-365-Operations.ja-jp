---
title: "AX 2012 からのアップグレード - Go live"
description: "このトピックでは、AX 2012 をオフにしてから、Microsoft Dynamics 365 for Finance and Operations でコードとデータベースのアップグレード バージョンの実行が完了するまでの最終的な切替えプロセスについて説明します。"
author: robadawy
manager: AnnBe
ms.date: 03/22/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2018-03-31
ms.dyn365.ops.version: Platform update 12
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: dfb80d58fd70866b52d54365d87ead187e011d2d
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="upgrade-from-ax-2012---cutover-process-go-live"></a>AX 2012 からのアップグレード - 切替プロセス (Go live)

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

標準またはプレミア承認テスト環境 (サンドボックス レベル 2 またはそれ以上) でアップグレード テストを正常に完了した場合、および正常にテスト切替を完了した後、実稼働環境をアップグレードして稼働するその時が来ました。

*切替*という用語は、新しいシステムを稼働させる最後のプロセスに使用します。 この切替プロセスは、Microsoft Dynamics AX 2012 をオフにした後、Microsoft Dynamics 365 for Finance and Operations をオンにする前に実行されるタスクで構成されています。 最終的な切替を計画する前に、[切替テスト](./upgrade-cutover-testing.md)で説明されているように成功した切替モックを正常に完了する必要があります。

次の図は、実稼動環境で発生するような、切替中の全体的なプロセスを示しています。

![切替プロセス](./media/cutover_1.png)

> [!NOTE]
> この記事では、*サンドボックス* という用語を使用して SQL Azure データベースに接続されている標準またはプレミア承認テスト (レベル 2 または 3)、またはより高度な環境を示します。

## <a name="overall-process"></a>全体的なプロセス

これらは、実稼働環境のアップグレード プロセスの大まかな手順です。

1.  Lifecycle Services (LCS) を通じて **その他のタイプ** サービス要求を送信し、実稼働環境をアップグレードするという目的を Microsoft サービス エンジニア リング (DSE) チームに通知します。 Microsoft solution architect と協力して十分の通知期間 (2、3 週間前) があることを確認します。 これが最終的な切替であることをサービス要求で示します。
    - 正常に切替モックが完了したことを確認します。
    - 切替要求は DSE チームの空き状況に左右されますので、事前に計画してください。
2.  AX 2012 AOS のすべてのインスタンスをオフにします。
3.  AX 2012 データベースをバックアップし、元のデータベースに対して T-SQL スクリプトを実行します。
4.  SQLPackage.exe (ダウンロード可能な無料の SQL Server ツール) を使用して、コピーされたデータベースを bacpac ファイルにエクスポートします。 このツールでは、SQL データベースにインポートできる特別な種類のデータベース バックアップを提供します。 
5.  bacpac ファイルをアップロードします。
6.  サンドボックス環境で bacpac ファイルを Application Object Server (AOS) 仮想マシンにダウンロードし、SQLPackage.exe を使用してインポートします。 
7.  データベースがアップグレード準備完了であることを Microsoft DSE チームに通知し、サンドボックスから実稼働環境にインポートされたデータベースをコピーします。
8.  Microsoft DSE チームは、インポートされたデータベースに対して適切なデータ アップグレードを実行します。
9.  データ アップグレードが完了すると、Microsoft DSE チームにより通知されます。この時点で、ログインして、ポスト アップグレードに必要な機能構成タスクを完了し、エンド ユーザーが新しいシステムに戻ることができます。

上記の手順は、モック切替中に実行した手順に似ています。詳細な手順については、「[切替テスト](./upgrade-cutover-testing.md)」を参照してください。

## <a name="prerequisites"></a>前提条件 
実稼動環境でアップグレードを実行する前に、次の前提条件を満たす必要があります。
-   サンドボックス環境でコードのアップグレードとデータのアップグレードを完了し、機能テスト パスを正常に完了しました
-   実稼働環境を配置します。 実稼働環境の配置を要求するオプションが点灯する前に完了しておく必要があります。
    - LCS のサブスクリプション見積もりツール。 必要なスループットの詳細を提供しているため、これを使用して実稼働環境のサイズの変更を支援します。
    - LCS での手法のテスト フェーズ。 これは、プロダクション環境でテストを開始する準備ができているプロジェクトの段階にあることを確認するためです。
    - 実稼働環境を配置するために要求が Microsoft に送信された後、配置には、約 24 時間かかるので、そのために十分な時間を確保してください。
-   すべての必要な更新プログラムおよびカスタマイズ (AOT 配置可能パッケージ) を実稼動環境に適用します。
-   Microsoft Solution Architect と協力してアップグレードをスケジュールします。 アップグレードをスケジュールするには、LCS から「その他の」タイプのサービス要求を送信することで DSE チームにタイムスロットを要求します。 これは、優先タイム スロットが使用できるようにすることです。 週末の間などスロットの需要が大幅に高くなるため注意してください。できるだけ早くこれらを要求することにより優先スケジュールを達成できます。

## <a name="related-articles"></a>関連記事
- [研修](../../fin-and-ops/imp-lifecycle/onboard.md)
- [サービス要求を送信する](../lifecycle-services/submit-request-dynamics-service-engineering-team.md)
- [AX 2012 からのアップグレード - 切替テスト](./upgrade-cutover-testing.md)

