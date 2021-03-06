---
title: Lifecycle Services (LCS) によるサービスの更新の構成
description: このトピックでは、環境の最新のサービスを受け取る方法とタイミングを指定する方法について説明します。
author: angelmarshall
ms.date: 06/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: c6f4655a1219fed878e7303a817e1def221ce4b4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752734"
---
# <a name="configure-service-updates-through-lifecycle-services-lcs"></a>Lifecycle Services (LCS) によるサービスの更新の構成

[!include [banner](../includes/banner.md)]

Microsoft Dynamics Lifecycle Services (LCS) で、環境のサービス更新を Microsoft から受け取る方法とタイミングを指定できます。

> [!IMPORTANT]
> この機能は **バージョン 8.1 以降** を使用しているお客様、または **バージョン 7.3** を使用していて、[初回リリース](../../fin-ops/get-started/public-preview-releases.md) プログラムに参加して **いない** お客様だけが利用できます。 Microsoft はこの機能を初回リリースのお客様が利用できるようにすることを目指しています。 バージョン 7.1、7.2、または 8.0 のお客様は、通常のサービス フローを使用して手動で更新を行うことができます。

LCS で **プロジェクト所有者** ロールが割り当てられているユーザー (顧客またはパートナー) のみが更新を構成できます。 さらに、更新は **実装プロジェクト** に対してのみ構成できます。

構成設定を変更するには、これらの手順を実行します。

> [!NOTE]
> これらの設定は、サービス更新にのみ適用されます。 毎月、環境に適用されているオペレーティング システム レベルのセキュリティ更新には影響がありません。

1. 実装プロジェクトの LCS で **プロジェクト設定** ページを開きます。

    このページには **更新プログラムの設定** という名前の新しいタブがあります。

2. **更新設定** タブで、必要に応じて、次のコンフィギュレーション オプションを設定します。

    - **更新環境**: 生産更新の前に更新する代替サンドボックス環境を選択します。

        既定では、マイクロソフトは、まず基本サービスに含まれる第 2 層標準受け入れテスト (サンドボックス) 環境を更新します。 次に、更新プログラムを実稼働環境に適用します。 第 2 層以上のサンドボックス アドオン環境を購入し、別のサンド ボックスを更新する場合は、代替環境に既定の環境を変更するためにこのフィールドを使用できます。

        > [!IMPORTANT]
        > ここで選択した環境は、実稼働環境に選択されている更新頻度の 7 暦日前に更新されます。

    - **製造環境更新頻度**: 実稼働環境への定期更新の頻度を選択します。 **環境の更新** フィールドで選択したサンドボックス環境は、選択されている頻度の 7 暦日前に更新されます。 次のオプションを使用できます。

        - **頻度を選択**: 月の第 1 週、第 2 週、第 3 週に更新を受け取るかどうかを選択します。
        - **3つのタイム ゾーンのいずれかを選択**: 実稼働環境を更新するタイム ゾーンを選択します: 東部標準時 (UTC - 5)、香港時 (UTC + 8)、またはグリニッジ標準時 (UTC + 0)。
        - **曜日を選択:** 更新を受信する曜日を選択します。
        - **時間帯を選択:** 更新プログラムを受信する時間帯を選択します。

        > [!NOTE]
        > 現時点では、曜日および時間帯オプションはいくつかのオプションのみ使用できます。 Microsoft は、顧客の平日など、他のオプションもすぐに追加します。
        
        > [!IMPORTANT]
        > 上記の時間帯で要望を満たせない場合は、通常のサービスのフローを使用してご自身の環境にアップグレードを適用することで、ご都合のいい時間に変更するオプションを選択することができます。

 3. コンフィギュレーション オプションの設定が完了したら **保存** を選択します。
 
更新環境および更新頻度を設定したら、Microsoft は、今後6か月の更新カレンダーを生成します。 このカレンダーは、コンフィギュレーション済のサンド ボックスと生産環境がいつ更新されるを正確に表示します。 したがって、各更新の予想される時期を特定できます。 カレンダーを表示するには、**実稼働環境の更新頻度** オプションで **更新カレンダーを表示** リンクを選択します。

> [!IMPORTANT]
> 設定を保存した後いつでも変更できます。 ただし、進行中の展開がある場合、新しい設定は、既存の展開タイミングを更新するために使用されません。 代わりに、次の展開で使用され始めます。 進行中の展開は、サンド ボックス環境の更新に関する電子メール通知が送信された日付から、実稼働環境の更新時の日付までの14日間の期間によって定義されます。

構成されたサンドボックス環境および実稼働環境への更新を一時停止する方法の詳細は、[Lifecycle Services (LCS) によるサービスの更新の一時停止](pause-service-updates.md) を参照してください。

1 つのバージョンおよび Microsoft が管理するサービスの更新の詳細は、[1 つのバージョンのサービス更新に関するよく寄せられる質問](../../fin-ops/get-started/one-version.md) を参照してください。

## <a name="canceled-updates"></a>キャンセルされた更新
スケジュールされた更新は、さまざまな理由でキャンセルされる場合があります。 スケジュールされた更新が Microsoft によってキャンセルされる原因となる可能性のある一般的な理由を次に示します。 
- 更新の準備中にエラーが検出されました。 更新の準備が更新の約4時間前に開始され、環境が正常な状態にあることが確認されます。 環境が失敗状態またはメンテナンス モードであった場合、スケジュールされた更新は開始前にキャンセルされます。    
- 環境の更新中にエラーが検出されました。 更新中に問題が発生した場合、スケジュールされた更新はキャンセルされ、環境は前の状態にロールバックされます。  
- この環境は、最新バージョンで既に実行されています。  更新を再度適用する必要はありません。スケジュールされた更新は、開始前にキャンセルされます。 
- ターゲット環境が見つかりません。 指定したサンドボックスが削除されたか、または実稼動環境が配置されていない場合、スケジュールされた更新は開始される前にキャンセルされます。
- [ファースト リリース プログラム](https://experience.dynamics.com) に登録されています。  ファースト リリース プログラムは、異なるリリース リズムを備えており、以前にスケジュールされた更新がキャンセルされます。 

キャンセルされた更新は、更新の設定で **最近キャンセルされた更新を表示** を介して確認できます。 最後の2つのスケジュールされた更新で、キャンセルされた更新がある場合はすべて表示されます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]