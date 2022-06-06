---
title: ソフトウェアのライフサイクル ポリシーおよびクラウド リリース
description: このトピックでは、Finance and Operations のオンライン サービスにおけるライフサイクルおよびサポート ポリシーの概要を説明します。
author: sericks007
ms.date: 05/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAbout
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 69914
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: a59a7f6d80a14ef99788e5895c7af99ac4a1cbc1
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723153"
---
# <a name="software-lifecycle-policy-and-cloud-releases"></a>ソフトウェアのライフサイクル ポリシーおよびクラウド リリース

[!include [banner](../includes/banner.md)]

この記事では、財務と運用オンライン サービスにおけるライフサイクルおよびサポート ポリシーの概要を説明します。

## <a name="modern-lifecycle-policy"></a>Modern Lifecycle ポリシー
Finance and Operations オンライン サービスは、Modern Lifecycle ポリシーの対象となります。 Modern Lifecycle Policy は、継続的に保守およびサポートされる製品およびサービスをカバーします。 このポリシーの詳細については、[Modern Lifecycle ポリシー](https://support.microsoft.com/help/30881) を参照してください。 ライセンス供与された顧客は、次のサービスとシステムの要件に従って、Finance and Operations オンライン サービスに対する更新で最新の状態にする必要があります。

- 財務と運用アプリのサブスクリプションを購入し、以下のアプリケーション バージョンで運用している顧客には、プラットフォームおよび Financial Reporting の継続的な更新が行われます。 Microsoft は、これらのコンポーネントを継続的に更新します。 顧客は、最大 3 回のサービス更新を延期できます。
    - 財務と運用アプリ、バージョン 10.0+ (2019 年 4 月)
    - 財務と運用アプリ、バージョン 8.0 (2018 年 4 月)
    - Dynamics 365 for Finance and Operations、Enterprise edition 7.3 (2017 年 12 月)   
    - Dynamics 365 for Finance and Operations、Enterprise Edition (2017 年 6 月)
    - Dynamics 365 for Operations バージョン 1611 (2016 年 11 月)
    

- プラットフォーム バージョンには、アプリケーション サポート ライフサイクル内のプラットフォームのリリース時点でサポートされているアプリケーション バージョンとの互換性が維持されます。 プラットフォーム バージョンの詳細については、[プラットフォーム更新プログラムの新機能および変更された機能](../get-started/whats-new-home-page.md) を参照してください。

- 重要な修正および重要でない更新は、次のように処理されます。

    - **重要な修正** - 重要な修正には、セキュリティ修正およびサービスがサポートする可用性サービス レベル アグリーメント (SLA) に準拠するために必要な修正が含まれます。 重要な修正プログラムは、最新のプラットフォーム更新プログラム バージョンで、およびバージョン 8.1 で動作している顧客の場合は最新のサービス更新プログラムで利用可能になります。 さらに、顧客とオンライン サービスを保護するため、Microsoft は顧客の環境に重要な修正プログラムを直接適用する場合があります。 重要な修正プログラムを適用する必要がある場合、Microsoft は必要なダウンタイム ウィンドウ (ダウンタイムが発生する場合) についてお客様に通知し、修正プログラムを適用可能な環境に適用します。 重要な修正プログラムにより、システムが最新の更新バージョンに更新されます。

    - **重要ではない更新** – 以下のアプリケーション リリースで動作しているユーザーは、重要ではない更新を導入するには、最新の Finance and Operations プラットフォームと財務レポートのバージョンに更新する必要があります。 
    
      - 財務と運用アプリ、バージョン 10.0+ (2019 年 4 月)
      - 財務と運用アプリ、バージョン 8.0+ (2018 年 4 月)
      - Dynamics 365 for Finance and Operations、Enterprise edition 7.3 (2017 年 12 月)   
      - Dynamics 365 for Finance and Operations、Enterprise Edition (2017 年 6 月)
      - Dynamics 365 for Operations バージョン 1611 (2016 年 11 月)          

> [!NOTE]
> Microsoft は、サービスの終了に達したバージョンの問題を修正しません。 また、Microsoft は、3 つ以上のサービス更新プログラムより古いバージョンで発生した問題の調査とトラブルシューティングも行いません。 サービスの終了に達したバージョンで問題が発生した場合は、最新の更新プログラムに更新し、問題が解決されない場合はその問題を報告する必要があります。
>
> すべての環境は、引き続き Microsoft によって運用されます。 監視や自動修復など、環境に関するすべての自動プロセスも、サポートされるバージョンにおいては引き続きそのままです。

## <a name="dates-and-versions-for-application-and-platform-releases"></a>アプリケーションおよびプラットフォーム リリースの日付とバージョン

アプリケーションおよびプラットフォームのリリースの日付とバージョンについての詳細については、 [財務と運用アプリ ホーム ページの新機能および変更事項](../../fin-ops/get-started/whats-new-changed.md) を参照してください。

> [!NOTE]
> -  サービス更新は本質的に累積的であり、次の一部またはすべてのコンポーネントの更新が含まれることがあります: プラットフォーム、アプリケーション、Financial Reporting、Commerce、およびオペレーティング システムの更新。 
> -  Microsoft Dynamics Lifecycle Services (LCS) プロジェクトの更新設定を使用して、すべてのサンドボックス環境と運用環境が利用可能な最新の更新プログラムより 3 バージョン以内の場合、顧客はサービス更新プログラムを一時停止、遅延、またはオプトアウトできます。 詳細については、[更新を遅らせることができますか? ポリシーとは何ですか?](../../fin-ops/get-started/one-version.md#can-the-updates-be-delayed-what-is-the-policy) を参照してください。
> -  Microsoft に提出された[拡張要求](../extensibility/extensibility-home-page.md) を実行しなかったユーザーを除き、すべてのユーザーは 2019 年 4 月までに財務と運用アプリの最新バージョンにする必要がありました。 2019 年 1 月 1 日までに拡張要求を送信したユーザーは、拡張要求が満たされるまでバージョン 7.3 がサポートされます。 ユーザーは、拡張機能要求が満たされてから 90 日以内に最新バージョンにアップグレードする必要があります。 詳細については、[1 つのバージョン サービスに関してよく寄せられる質問](../../fin-ops/get-started/one-version.md)を参照してください。 

## <a name="downloadable-virtual-hard-drive-vhd-releases"></a>ダウンロード可能な仮想ハード ドライブ (VHD) をリリース
財務と運用アプリのダウンロード可能な VHD の更新は、メジャーリリースと同時に、4 月と 10 月に、1 年に 2 回リリースされます。 VHD が最新のサービス更新にバンドルされている場合、そのリリースは関連付けられているサービス更新のリリースに従います。 メジャーサービス更新が一般にすべての顧客に提供された後に VHD 更新が行われる予定です。 財務と運用のリリース日は、[サービス更新の可用性](../../fin-ops/get-started/public-preview-releases.md#targeted-release-schedule-dates-subject-to-change) に表示されています。

VHD の使用の際には、[ソフトウェア ライセンス条件](https://go.microsoft.com/fwlink/?linkid=851163)が適用されます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
