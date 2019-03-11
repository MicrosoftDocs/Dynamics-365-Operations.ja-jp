---
title: 標準および対象となるサービス更新
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations の各種のリリース オプションについて説明します。
author: meeramahabala
manager: AnnBe
ms.date: 01/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2017-10-31
ms.dyn365.ops.version: Platform update 11
ms.openlocfilehash: f09fa9e01e47e3bb3ebddce1638aa85d83784ea9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368588"
---
# <a name="standard-and-first-release-service-updates"></a>標準および最初のリリース サービス更新

[!include [banner](../includes/banner.md)]

Dynamics 365 for Finance and Operations では、コストのかかるアップグレードを数年おきに実行する代わりに月 1 回新しいサービス更新および機能を受け取ります。 組織がこれらの更新プログラムを受信する方法を管理することができます。 たとえば、初期リリースにサインアップすると、組織が最初に更新プログラムを受け取ります。 特定の環境だけが更新プログラムを受け取ることを指定できます。 または、既定のリリース スケジュールにとどまり、更新プログラムを後で受け取ることができます。 このトピックでは、さまざまなリリース オプションと、組織でそれらを使用する方法について説明します。

*サービスの更新*には、規制の更新を含むサービスの重要な改良であるアプリケーション (財務、レポート、小売を含む) とプラットフォームの変更の両方が含められます。 サービスの更新には、新しい機能が含まれます。

## <a name="release-processes"></a>プロセスのリリース

それぞれの新しいリリースは、Dynamics 365 for Finance and Operations チームによって設計、開発されます。 新しいリリースはまず機能チームによって、次に Dynamic 365 for Finance and Operations および Retail チームによってテストおよび検証されます。 このとき、広範なテストがさまざまなトポロジで行われます。 互換性チェックでは、下位互換性を確保するためのテストも実行されます。 さらに、複数の顧客データベースおよびコードが、中断が生じないようにするために自動化によりベンチマーク テストされます。

- リング 2 は、対象となるリリースです。 今回のリリースは、[Insider プログラム](https://experience.dynamics.com/)を通じてオプトインし、Preview Early Access Program (PEAP) に参加しているパートナー、顧客、および ISV が利用できます。 対象となるリリース時、Microsoft はテレメトリを監視してフィードバックを収集し、主なメトリックスを監視することによってさらに品質を検証します。 この段階では、リリースを開発またはテスト環境に展開する必要があります。 このプレビュー フェーズでは、パートナー、顧客、および ISV はリリースを使用してカスタマイズを検証し、フィードバックを提供します。 このリリースを運用環境で使用することはできません。
- リング 3 は、オプトインした顧客向けの運用環境に対応した*最初のリリース*です。 この段階では、顧客は、運用環境までこのリリースを使用することを選択でき、Microsoft が更新を管理するか、更新を自己管理するかを選択できます。 最初のリリースに参加することには、更新を正常に行うため、Microsoft エンジニアリング チームに異常がないか更新を詳細に監視してもらえるという利点があります。
- リング 4 は、最終的な既定のリングであり、すべての顧客が使用できます。 Microsoft は、設定された保守時間帯に基づいてすべての環境を管理および更新します。

> [!Note]
> [ソフトウェア ライフ サイクル ポリシー](../../dev-itpro/migration-upgrade/versions-update-policy.md)は、リング 3 とリング 4 に適用されます。

リリースを次の図に示します。

![リリース プロセス](media/release-process.png)

## <a name="standard-release-ring-4"></a>標準リリース (リング 4)

標準のリリース、つまりリング 4 は、既定のオプションです。 このリリースでは、最新リリースがすべての顧客にリリースされたときに、そのリリースの Finance and Operations にアクセスすることができます。 標準リリースでは、予測可能性を確保するため、更新日時を設定します。 また、ユーザー受け入れテスト (UAT) の環境を指定することができます。 この環境は、実稼働環境を更新する 5 営業日前に更新されます。 詳細は、[1 つのバージョンのサービス更新に関するよく寄せられる質問](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version)を参照してください。

## <a name="first-release-ring-3"></a>最初のリリース (リング 3)

最初のリリースでは、Microsoft が、最新の運用環境対応サービス更新を顧客が利用できるようにします。

- **最初のリリースの自動更新**: このプログラムでは、Microsoft が UAT および運用環境の両方の更新を管理します。 このプログラムでは、次の更新について通知された後、指定されたレベル 2 サンドボックスに対するその次の更新について通知されます。 参加者は、Microsoft に直接フィードバックを提供しながら新しい環境で作業することができます。 参加者は、提示された問題について Microsoft から直接サポートを受けます。 その後、次の週に検証済みの更新が運用環境に適用されます。 [Insider プログラム](https://experience.dynamics.com/insider) を通じてプログラムにサインアップすることができます。
- **最初のリリースを自己更新**: このプログラムでは、運用環境対応更新に早期アクセスでき、選択した環境 (サンドボックスまたは運用環境) に適用することを選択できます。 更新の適用は顧客によって管理され、問題を Microsoft に報告することができます。 このプログラムには、必要な場合に検証のための追加の時間が提供されるという利点があります。 このプログラムのサインアップ オプションは LCS から入手できます。

## <a name="targeted-release-ring-2"></a>対象となるリリース (リング 2)

Preview Early Access Program (PEAP) は、顧客、パートナー、および ISV がそのサンドボックスに展開できます。 参加者は、この時間枠内に最新のサービス更新プログラムに自己更新する必要があります。 参加者は、Microsoft に問題を報告することができます。 これには、運用環境を更新する前に、更新プログラムを早期にテストできるという追加の価値があります。

## <a name="access-targeted-releases-or-first-release"></a>対象となるアクセス リリースまたは最初のリリース 

Finance and Operations の対象となるリリースまたは最初のリリースの参加に興味のあるユーザーで、使用可能なオプションについて知りたい場合は、[Insider プログラム](https://experience.dynamics.com/)を参照します。
