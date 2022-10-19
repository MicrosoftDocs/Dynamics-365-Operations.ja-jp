---
title: ソフトウェアのライフサイクル ポリシーおよびオンプレミス リリース
description: この記事では、Microsoft Dynamics 365 Finance + Operations (on-premises) リリースにおけるライフサイクルおよびサポート ポリシーの概要を説明します。
author: faix
ms.date: 12/14/2021
ms.topic: article
ms.prod: dynamics-365
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2017-07-15
ms.dyn365.ops.version: Platform update 2
ms.custom: 69914
ms.search.form: SysAbout
ms.service: ''
ms.openlocfilehash: 7f12898a71b0a3c11ba67f39690a618eab7586cd
ms.sourcegitcommit: 9f1f6993763fb9ba8755fae3b2afe28bc3035a21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/06/2022
ms.locfileid: "9635183"
---
# <a name="software-lifecycle-policy-for-microsoft-dynamics-365-finance--operations-on-premises"></a>Microsoft Dynamics 365 Finance + Operations (on-premises) のソフトウェアのライフサイクル ポリシー

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Finance + Operations (on-premises) リリースにおけるライフサイクルおよびサポート ポリシーの概要を説明します。

## <a name="product-life-time"></a>製品の有効期限

Finance + Operations (オンプレミス) ソフトウェアの有効期限は、**2027 年 12 月** に終了します。 このポリシーに準拠しているライセンスを供与された顧客は、製品サポートを受けることができます。 製品サポートは、最低でも 2027 年 12 月 31 日まで利用可能です。

## <a name="modern-lifecycle-policy"></a>Modern Lifecycle ポリシー

Finance + Operations (オンプレミス) ソフトウェアは、Modern Lifecycle ポリシーの対象となります。 Modern Lifecycle ポリシーは、継続的に保守およびサポートされる製品およびサービスを規定しています。 このポリシーの詳細については、[Modern Lifecycle ポリシー](https://support.microsoft.com/help/30881/modern-lifecycle-policy) を参照してください。  

ライセンス供与された顧客は、Finance + Operations (オンプレミス) ソフトウェアの配置を定期的に更新する必要があります。 サービス ポリシーでは、ソフトウェア保証 (SA) または拡張計画を維持し、[継続的なサービス更新](on-prem-version-update-policy.md#continuous-service-updates)を通じて提供される更新リリースを展開する必要があります。

> [!NOTE]
> 修正サポート ライフサイクル ポリシー (5 + 5) を使用する顧客は、Microsoft Dynamics AX 2012 R3 にダウングレードする必要があります。 代わりに SA または拡張計画を失うと、Microsoft Dynamics AX 2012 R3 への永久ライセンスの権利のみが適用され、Microsoft Dynamics 365 for Finance + Operations (オンプレミス) をアンインストールしなければなりません。

## <a name="on-premises-software-update-policies"></a>オンプレミス ソフトウェアの更新ポリシー

顧客はオンプレミス配置を完全に制御できるため、このポリシーに従わなければなりません。 オンプレミス環境に更新プログラムをインストールすることを制御できます。

Microsoft は、このポリシーに従って配置されたソフトウェアを最新の状態に保つ場合にのみ、Finance + Operations (オンプレミス) ソフトウェアの配置をサポートします。

重要な修正および重要でない更新は、次のように処理されます。

- **重要な修正** - 重要な修正には、セキュリティの修正および、信頼性と可用性をサポートするために必要な修正が含まれます。 重要な修正は、最新のプラットフォーム更新版で利用可能になります。
- **重要ではない更新** – 重要ではない更新を導入するには、Finance + Operations プラットフォームと財務レポートの最新バージョンに更新する必要があります。

## <a name="finance--operations-on-premises-release-dates"></a>Finance + Operations (オンプレミス) リリース日

### <a name="continuous-service-updates"></a>継続的なサービスの更新

2018 年 11 月以降、オンプレミス サービスの更新が継続的にリリースされています。 バージョン番号と利用可能な日付の詳細については、「[ソフトウェアのライフ サイクル ポリシーおよびクラウド リリース](versions-update-policy.md)」を参照してください。 1 つのバージョンのサービス更新の詳細については、「[1 つのバージョンのサービス更新に関するよく寄せられる質問](../../../fin-ops-core/fin-ops/get-started/one-version.md)」を参照してください。

すべてのサービス更新リリースには特定の有効期限があり、それ以降はリリースがサポートを受けることはできません。

#### <a name="continuous-combined-releases-application-and-platform"></a>継続的な複合リリース (アプリケーションおよびプラットフォーム)

[継続的なサービスの更新](on-prem-version-update-policy.md#continuous-service-updates)により、アプリケーションとプラットフォームが共にリリースされます。 [1 つのバージョンのスケジュール](../../fin-ops/get-started/public-preview-releases.md#targeted-release-schedule-dates-subject-to-change)は、早期アクセス、公開リリース、およびリリースの有効期限の日付を指定します。

| 製品 | 配置オプション | 申請バージョン | リリース日または有効期限|
|--------|-----------------------|-----------------------|------------------------|
| Finance + Operations | 基本配置 + サービス更新 | 10.0.38 | [1 つのバージョンのスケジュール](../../fin-ops/get-started/public-preview-releases.md?#targeted-release-schedule-dates-subject-to-change) |
| Finance + Operations | サービスの更新 | 10.0.37 | [1 つのバージョンのスケジュール](../../fin-ops/get-started/public-preview-releases.md?#targeted-release-schedule-dates-subject-to-change) |
| Finance + Operations | サービスの更新 | 10.0.36 | [1 つのバージョンのスケジュール](../../fin-ops/get-started/public-preview-releases.md?#targeted-release-schedule-dates-subject-to-change) |
| Finance + Operations | 基本配置 + サービス更新 | 10.0.35 | [1 つのバージョンのスケジュール](../../fin-ops/get-started/public-preview-releases.md?#targeted-release-schedule-dates-subject-to-change) |
| Finance + Operations | サービスの更新 | 10.0.34 | [1 つのバージョンのスケジュール](../../fin-ops/get-started/public-preview-releases.md?#targeted-release-schedule-dates-subject-to-change) |
| Finance + Operations | サービスの更新 | 10.0.33 | [1 つのバージョンのスケジュール](../../fin-ops/get-started/public-preview-releases.md?#targeted-release-schedule-dates-subject-to-change) |
| Finance + Operations | 基本配置 + サービス更新 | 10.0.32 | [1 つのバージョンのスケジュール](../../fin-ops/get-started/public-preview-releases.md?#targeted-release-schedule-dates-subject-to-change) |
| Finance + Operations | サービスの更新 | 10.0.31 | [1 つのバージョンのスケジュール](../../fin-ops/get-started/public-preview-releases.md?#targeted-release-schedule-dates-subject-to-change) |
| Finance + Operations | サービスの更新 | 10.0.30 | [1 つのバージョンのスケジュール](../../fin-ops/get-started/public-preview-releases.md?#targeted-release-schedule-dates-subject-to-change) |
| Finance + Operations | 基本配置 + サービス更新 | 10.0.29  | [1 つのバージョンのスケジュール](../../fin-ops/get-started/public-preview-releases.md?#targeted-release-schedule-dates-subject-to-change) |
| Finance + Operations | サービスの更新 | 10.0.28 | [1 つのバージョンのスケジュール](../../fin-ops/get-started/public-preview-releases.md?#targeted-release-schedule-dates-subject-to-change) |
| Finance + Operations | サービスの更新 | 10.0.27* | [1 つのバージョンのスケジュール](../../fin-ops/get-started/public-preview-releases.md?#targeted-release-schedule-dates-subject-to-change) |
| Finance + Operations | 基本配置 + サービス更新 | 10.0.26*  | [1 つのバージョンのスケジュール](../../fin-ops/get-started/public-preview-releases.md?#targeted-release-schedule-dates-subject-to-change) |
| Finance + Operations | サービスの更新 | 10.0.25* | [1 つのバージョンのスケジュール](../../fin-ops/get-started/public-preview-releases.md?#targeted-release-schedule-dates-subject-to-change) |

\* 期限切れのバージョン。 すべての顧客は、[Modern Lifecycle ポリシー](https://support.microsoft.com/help/30881/modern-lifecycle-policy)に従って、最新バージョンの Finance + Operations を使用している必要があります。

### <a name="older-application-releases"></a>以前のアプリケーションのリリース

  > [!NOTE]
  > 以前のプラットフォーム リリースは有効期限を過ぎており、現在サポートされていません。 2019 年 1 月 1 日以降、拡張要求をログに記録することはできません。
  >
  > [Modern Lifecycle ポリシー](https://support.microsoft.com/help/30881/modern-lifecycle-policy)および[継続的なサービスの更新](on-prem-version-update-policy.md#continuous-service-updates)に従わない顧客は、展開されたアプリケーション バージョンの有効期限が切れるとサポートを受けられない場合があります。 期限切れのバージョンは、サービスおよび LCS からのそのようなバージョンの展開が不可能になりそうな時点で、LCS から削除されます。

| 品目          | 申請バージョン |公的可用性| 有効期限 |
|------------------|---------|---------|---------|
| Finance + Operations (オンプレミス) |10.0 (10.0.8) |2019 年 3 月 | 2019 年 6 月 |
| Finance + Operations (オンプレミス) |8.1 (8.1.136) | 2018 年 11 月 | 2019 年 4 月     |
| Finance + Operations、Enterprise Edition (オンプレミス) | 7.3 (7.3.11971) | 2018 年 3 月 | 2020 年 4 月* |
| Finance + Operations、Enterprise Edition (オンプレミス) | 2017 年 7 月 (7.2.11792) | 2017 年 6 月 | 2019 年 4 月 |

\*すべてのユーザーは、Finance + Operations の最新バージョンにする必要があります。 この要件の期限は 2019 年 4 月 30 日です。 [継続的なサービスの更新](on-prem-version-update-policy.md#continuous-service-updates)への移行時に、Microsoft に提出された[拡張要求](../extensibility/extensibility-home-page.md)を実行しなかったユーザーには例外を設けます。 それらのユーザーは、2020 年 4 月までバージョン 7.3 を使用することができます。 詳細については、[1 つのバージョン サービスに関してよく寄せられる質問](../../../fin-ops-core/fin-ops/get-started/one-version.md)を参照してください。

#### <a name="older-platform-releases"></a>以前のプラットフォームのリリース

> [!NOTE]
> 以前のプラットフォーム リリースは有効期限を過ぎており、現在サポートされていません。 2019 年 1 月 1 日以降、拡張要求をログに記録することはできません。

| プラットフォームのリリース          |ビルド番号         | 適用の対象          | 有効期限   |
|------------------|----------------------|------------------|--------------|
|  プラットフォーム update 20 | 7.0.5030  | 2018 年 11 月  | 2019 年 2 月 |
|  プラットフォーム update 15 | 7.0.4841  | 2018 年 6 月  | 2018 年 9 月 |
|  プラットフォーム update 12 | 7.0.4709.41182  | 2018 年 3 月  | 2018 年 6 月 |
|  プラットフォーム update 11 | 7.0.4679.35176 | 2017 年 10 月 | 2018 年 4 月 |
|  プラットフォーム update 10 | 7.0.4641.16233 | 2017 年 8 月 | 2018 年 4 月 |
|  プラットフォーム update 9 | 7.0.4612.35162 | 2017 年 8 月 | 2018 年 4 月 |
|  プラットフォーム update 8 | 7.0.4565.1612 | 2017 年 7 月 | 2018 年 4 月 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
