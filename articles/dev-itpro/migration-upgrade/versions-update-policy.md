---
title: "ソフトウェアのライフサイクル ポリシーおよびクラウド リリース"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations のオンライン サービスにおけるライフサイクルおよびサポート ポリシーの概要を説明します。"
author: RyanCCarlson2
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SysAbout
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: 69914
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 9290114388b210dfdfd980e293df2e21d0aa50ea
ms.openlocfilehash: 518a1799fe61b5818dfd42a7ad0bc483d6fe6748
ms.contentlocale: ja-jp
ms.lasthandoff: 12/20/2018

---

# <a name="software-lifecycle-policy-and-cloud-releases"></a>ソフトウェアのライフサイクル ポリシーおよびクラウド リリース

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations のオンライン サービスにおけるライフサイクルおよびサポート ポリシーの概要を説明します。

## <a name="modern-lifecycle-policy"></a>Modern Lifecycle ポリシー
Dynamics 365 for Finance and Operations オンライン サービスは、Modern Lifecycle ポリシーの対象となります。 Modern Lifecycle Policy は、継続的に保守およびサポートされる製品およびサービスをカバーします。 このポリシーの詳細については、[Modern Lifecycle ポリシー](https://support.microsoft.com/en-us/help/30881) を参照してください。 ライセンス供与された顧客は、次のサービスとシステムの要件に従って、Dynamics 365 for Finance and Operations オンライン サービスに対する更新で最新の状態にする必要があります。

- Microsoft Dynamics 365 for Finance and Operations のサブスクリプションを購入し、以下のアプリケーション バージョンで運用している顧客では、プラットフォームおよび財務諸表の継続的な更新が行われます。 Microsoft は、30 日まで更新プログラムを延期するオプションでこれらのコンポーネントを継続的に更新します。
    - Dynamics 365 for Operations バージョン 1611 (2016 年 11月)
    - Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月)
    - Dynamics 365 for Finance and Operations, Enterprise Edition 7.3
    - Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 4 月)

- プラットフォーム バージョンには、アプリケーション サポート ライフサイクル内のプラットフォームのリリース時点でサポートされているアプリケーション バージョンとの互換性が維持されます。 プラットフォーム バージョンの詳細については、[クラウド プラットフォームの毎月の更新に関するよく寄せられる質問](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/faq-platform-monthly-updates) を参照してください。

- 重要な修正および重要でない更新は、次のように処理されます。

    - **重要な修正** - 重要な修正には、セキュリティ修正およびサービスがサポートする可用性サービス レベル アグリーメント (SLA) に準拠するために必要な修正が含まれます。 重要な修正プログラムは、最新のプラットフォーム更新プログラム バージョンで、およびバージョン 8.1 で動作している顧客の場合は最新のサービス更新プログラムで利用可能になります。 さらに、顧客とオンライン サービスを保護するため、Microsoft は顧客の Dynamics 365 for Finance and Operations 環境に重要な修正プログラムを直接適用する場合があります。 重要な修正プログラムを適用する必要がある場合、Microsoft は必要なダウンタイム ウィンドウ (ダウンタイムが発生する場合) についてお客様に通知し、修正プログラムを適用可能な環境に適用します。 重要な修正プログラムにより、システムが最新の更新バージョンに更新されます。

    - **重要ではない更新** – 以下のアプリケーション リリースで動作しているユーザーは、重要ではない更新を導入するには、最新の Finance and Operations プラットフォームと財務レポートのバージョンに更新する必要があります。 
    
       - Dynamics 365 for Operations バージョン 1611 (2016 年 11月)
       - Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月)
       - Dynamics 365 for Finance and Operations, Enterprise Edition 7.3
       - Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 4 月)
     
      リリース 8.1 で動作しているユーザーは、重要ではない更新を展開するには、最新の Finance and Operations サービス更新プログラムに更新する必要があります。

> [!Note]
> アプリケーションおよびプラットフォーム リリースは、ソフトウェアのライフサイクルの月末に期限が切れます。
>
> Microsoft は、サービスの終了に達しているバージョンの問題を修正しません。 Microsoft は、以前のバージョンで発生した問題の調査とトラブルシューティングも行いません。 サービスの終了に達したバージョンで問題が発生した場合は、最新の更新プログラムに更新し、それでも問題が解決されない場合は、その問題を報告する必要があります。
>
> すべての環境は、引き続き Microsoft によって運用されます。 環境に関するすべての自動プロセス (監視や自動修復など) も、引き続きそのままです。

## <a name="dates-and-versions-for-finance-and-operations-application-and-platform-releases"></a>Finance and Operations アプリケーションおよびプラットフォーム リリースの日付とバージョン

### <a name="table-1-continuous-update-releases"></a>表 1: 継続的な更新リリース

各リリースに含まれる新機能の詳細については、**バージョン**列でリンクをクリックします。

| **リリース**                             | **メジャー リリースまたはサービスの更新** | **バージョン**                                                                                                                       | **ビルド番号** | **適用の対象** | **サービス終了**           |
|-----------------------------------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|------------------|------------------|------------------------------|
| Dynamics 365 for Finance and Operations | メジャー リリース                       | [8.1](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-changed-8-1-october-2018) | 8.1.136          | 2018 年 10 月     | 該当なし (継続的に更新)\* |

\*サービスの更新を通じて更新するのにメジャー リリースが必要なことを示します。 サービス更新は本質的に累積的であり、次の一部またはすべてのコンポーネントの更新が含まれることがあります: プラットフォーム、アプリケーション、財務報告、Retail、およびオペレーティング システムの更新。  3 か月以内に更新する必要があります。 8.1.x バージョン シリーズは、バージョン 10.0 によって置き換えられます。2019 年 4 月リリースを目標としています。 詳細については、[1 つのバージョン サービスに関してよく寄せられる質問](../../fin-and-ops/get-started/one-version.md)を参照してください。

### <a name="table-2-application-releases"></a>テーブル 2: アプリケーション リリース

各リリースに含まれる新機能の詳細については、**バージョン**列でリンクをクリックします。

| **リリース**                                                 | **メジャーまたはマイナー リリース** | **バージョン**                                                                                                                                           | **ビルド番号** | **適用の対象** | **サービス終了** |
|-------------------------------------------------------------|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|------------------|--------------------|
| Dynamics 365 for Finance and Operations                     | メジャー リリース              | [8.0](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-changed-8-0-april-2018)                       | 8.0.30           | 2018 年 4 月       | 2019 年 4 月         |
| Dynamics 365 for Finance and Operations, Enterprise edition | メジャー リリース              | [7.3](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-application-7.3-update)                       | 7.3.11971.56116  | 2017 年 12 月    | 2019 年 4 月\*       |
| Dynamics 365 for Finance and Operations, Enterprise edition | メジャー リリース              | [2017 年 7 月](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-application-july-2017-update)           | 7.2.11792.56024  | 2017 年 6 月        | 2019 年 4 月         |
| Dynamics 365 for Operations                                 | メジャー リリース              | [1611](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-dynamics-365-operations-1611)                | 7.1.1541.3036    | 2016 年 11 月    | 2019 年 4 月         |
| Dynamics AX                                                 | マイナー リリース              | [7.0.1](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-changed-application-version-7-0-1-may-2016) | 7.0.1265.23014   | 2016 年 5 月         | 2017 年 6 月          |
| Dynamics AX                                                 | メジャー リリース              | [7.0](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-changed-7-0-february-2016)                    | 7.0.1265.3015    | 2016 年 2 月    | 2017 年 6 月          |


\*すべてのユーザーは、2019 年 4 月までに Finance and Operations の最新バージョンにする必要があります。 ただし、Microsoft に提出された[拡張要求](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/extensibility/extensibility-home-page)を実行しなかったユーザーには例外を設けます。 2019 年 1 月 1 日までに拡張機能要求を送信したユーザーは、拡張機能要求が満たされるまでバージョン 7.3 がサポートされます。 ユーザーは、拡張機能要求が満たされてから 90 日以内に最新バージョンにアップグレードする必要があります。 詳細については、[1 つのバージョン サービスに関してよく寄せられる質問](../../fin-and-ops/get-started/one-version.md)を参照してください。

### <a name="table-3-platform-releases"></a>表 3: プラットフォームのリリース

各リリースに含まれる新機能の詳細については、**リリース**列でリンクをクリックします。

| **リリース**                                                                                                                                                  | **ビルド番号** | **在庫状態** | **有効期限**        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|------------------|----------------------------|
| [プラットフォーム update 21](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-21)               | 7.0.5073         | 2018 年 10 月   | 該当なし (継続的に更新) |
| [プラットフォーム update 20\*\*](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-20)               | 7.0.5030         | 2018 年 10 月   | 該当なし (継続的に更新) |
| [プラットフォーム update 15\*](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-15)                 | 7.0.4841         | 2018 年 3 月       | 該当なし (継続的に更新/サポートされなくなりました) |
| [プラットフォーム update 12](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-12)                   | 7.0.4709         | 2017 年 11 月    | 2018 年 11 月              |
| [プラットフォーム update 11](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-11)                   | 7.0.4679.35176   | 2017 年 10 月     | 2018 年 10 月               |
| [プラットフォーム update 10](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-10)                   | 7.0.4641.16233   | 2017 年 8 月      | 2018 年 8 月                |
| [プラットフォーム update 9](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-9)                     | 7.0.4612.35162   | 2017 年 7 月        | 2018 年 7 月                  |
| [プラットフォーム update 8](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-8)                     | 7.0.4565.16212   | 2017 年 6 月        | 2018 年 6 月                  |
| [プラットフォーム update 7](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-7)                     | 7.0.4542.16189   | 2017 年 5 月         | 2018 年 5 月                   |
| [プラットフォーム update 6](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-6)                     | 7.0.4509.16180   | 2017 年 4 月       | 2018 年 4 月                 |
| [プラットフォーム update 5](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-5)                     | 7.0.4475.16165   | 2017 年 3 月       | 2018 年 3 月                 |
| [プラットフォーム update 4](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-4)                     | 7.0.4425.16161   | 2017 年 2月    | 2018 年 2 月              |
| [プラットフォーム update 3](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-3)                     | 7.0.4307.16141   | 2016 年 11 月    | 2017 年 11 月              |
| [プラットフォーム update 2](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-2)                     | 7.0.4230.16130   | 2016 年 8 月      | 2017 年 8 月                |
| [プラットフォーム update 1](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-changed-platform-version-7-1-may-2016) | 7.0.4127.16103   | 2016 年 5 月         | 2017 年 5 月                   |
| [プラットフォーム 7.0](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-changed-7-0-february-2016)                  | 7.0.4030.16079   | 2016 年 2 月    | 2017 年 1 月               |

\*\* プラットフォーム更新プログラム 16、17、18、19 は一般的には利用できませんでした。

\* プラットフォーム更新プログラム 13 および 14 は一般的には利用できませんでした。

### <a name="table-4-application-updates"></a>表 4: アプリケーション更新プログラム

以下の一覧に示すアプリケーション更新プログラムは、Dynamics 365 for Finance and Operations バージョン 8.0、7.3 および 7.2 (2017 年 7 月) に加えてリリースされた、アプリケーション拡張機能の小規模なセットで構成されています。 これらの更新は、リリースのサポート ライフサイクルには影響しません。サポートは、各リリースのポリシーに沿っています。

アプリケーションの更新プログラムは累積的ではないことに注意してください。 個々のパッケージには、その特定のリリースに含まれていた機能拡張のみが含まれます。 ただし、2 つのパッケージの間に依存関係がある場合、両方のパッケージが含まれます。

各更新に含まれる新機能の詳細については、**バージョン**列でリンクをクリックします。

| **リリース**                                                 | **バージョン**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | **ビルド番号** | **在庫状態** |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|------------------|
| Dynamics 365 for Finance and Operations                     | 8.1.1: [KB 4470000 プラットフォーム更新プログラム 21 を含む Microsoft Dynamics 365 for Finance and Operations バージョン 8.1.1\*](https://go.microsoft.com/fwlink/?linkid=2038101)                                      | 8.1.170     | 2018 年 10 月      |
| Dynamics 365 for Finance and Operations                     | 8.0.4: [KB 4458992 Microsoft Dynamics 365 for Finance and Operations - バージョン 8.0.4 (バイナリ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Details?kb=4458992&bugId=239612&qc=70318005e232acfe98df16bf3ab4cdf8df463634e28ff3ce2ef1db29c8678863)、[KB 4458993 Microsoft Dynamics 365 for Finance and Operations - バージョン 8.0.4 (X++ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Details?kb=4458993&bugId=239610&qc=70318005e232acfe98df16bf3ab4cdf8df463634e28ff3ce2ef1db29c8678863)                                      | 8.0.35.15532     | 2018 年 8 月      |
| Dynamics 365 for Finance and Operations                     | 8.0.3: [KB 4346176 Microsoft Dynamics 365 for Finance and Operations - バージョン 8.0.3 (バイナリ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Details?kb=4346176&bugId=230723&qc=15b7470493e66efed8446f7ad2269bde9804da7174d135900c99b7318bb26e34)、[KB 4346172 Microsoft Dynamics 365 for Finance and Operations - バージョン 8.0.3 (X++ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Details?kb=4346172&bugId=230724&qc=15b7470493e66efed8446f7ad2269bde9804da7174d135900c99b7318bb26e34)                                      | 8.0.35.15342     | 2018 年 7 月        |
| Dynamics 365 for Finance and Operations                     | 8.0.2: [KB 4340414 Microsoft Dynamics 365 for Finance and Operations - バージョン 8.0.2 (バイナリ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Details?kb=4340414&bugId=219341&qc=0d87f4d28eb75753e9c4ceeb997ab6bf2a0ff5d0b58342ecd9512cc721e0cc80)、[KB 4340413 Microsoft Dynamics 365 for Finance and Operations - バージョン 8.0.2 (X++ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Details?kb=4340413&bugId=219344&qc=0d95ca5957e7b1288e6d56bcf3bc6c014baf9e916d976fd100ae24db3d2b1a14)                                      | 8.0.35.15211     | 2018 年 7 月        |
| Dynamics 365 for Finance and Operations                     | 8.0.1: [KB 4295107 Microsoft Dynamics 365 for Finance and Operations - バージョン 8.0.1 (バイナリ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Details?kb=4295107&bugId=192587&qc=70f6f8fbdd96b01197fedc9442b5c43c2e01e2748eb0d5a20d87bceb4c0b939d)、[KB 4294515 Microsoft Dynamics 365 for Finance and Operations - バージョン 8.0.1 (X++ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Details?kb=4294515&bugId=194698&qc=70f6f8fbdd96b01197fedc9442b5c43c2e01e2748eb0d5a20d87bceb4c0b939d)                                      | 8.0.30.15107     | 2018 年 6 月        |
| Dynamics 365 for Finance and Operations, Enterprise edition | 7.3.2: [KB 4093261 Microsoft Dynamics 365 for Finance and Operations - バージョン 7.3.2 (バイナリ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Details?kb=4093261&bugId=3937217&qc=848a3e7a82137b3ac4412537f1fdb4fafacab7d7565e0a7a6930b0c96406c96a)、[KB 4093262 Microsoft Dynamics 365 for Finance and Operations - バージョン 7.3.2 (X++ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Details?kb=4093262&bugId=3937219&qc=848a3e7a82137b3ac4412537f1fdb4fafacab7d7565e0a7a6930b0c96406c96a)                                    | 7.3.11971.62687  | 2018 年 3 月       |
| Dynamics 365 for Finance and Operations, Enterprise edition | 7.3.1: [KB 4093139 Microsoft Dynamics 365 for Finance and Operations - バージョン 7.3.1 (バイナリ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Details?bugId=3933782&qc=419638525c20d4bcd818cd40be05a12876e4c00a39124d2e44a0d950af21be89)、[KB 4091727 Microsoft Dynamics 365 for Finance and Operations - バージョン 7.3.1 (X++ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Details?bugId=3933783&qc=419638525c20d4bcd818cd40be05a12876e4c00a39124d2e44a0d950af21be89)                                                          | 7.3.11971.62430  | 2018 年 3 月       |
| Dynamics 365 for Finance and Operations, Enterprise edition | アプリケーション更新プログラム 5: [Microsoft Dynamics 365 for Finance and Operations の KB 4053277 アプリケーション更新プログラム 5 (バイナリ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4053277&bugId=3893141&qc=ee9db96dd13dc341e7019fad3d36d01c6dfc4edf631f752f66d87f2ebbd256f5)、[Microsoft Dynamics 365 for Finance and Operations の KB 4053278 アプリケーション更新プログラム 5 (X++ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4053278&bugId=3893143&qc=ee9db96dd13dc341e7019fad3d36d01c6dfc4edf631f752f66d87f2ebbd256f5) | 7.2.11792.62725  | 2017 年 11 月    |
| Dynamics 365 for Finance and Operations, Enterprise edition | アプリケーション更新プログラム 4: [KB 4047325 アプリケーション更新プログラム 4 Dynamics 365 for Finance and Operations (バイナリ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4047325&bugId=3866272&qc=dfcd40f8c5d0d863cc6ae10fe7dd3fb57450327d4f82f10c57886d579e6d4838)、 [KB 4047321 アプリケーション更新プログラム 4 Dynamics 365 for Finance and Operations (X++ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4047321&bugId=3866273&qc=dfcd40f8c5d0d863cc6ae10fe7dd3fb57450327d4f82f10c57886d579e6d4838)                     | 7.2.11792.62509  | 2017 年 10 月     |
| Dynamics 365 for Finance and Operations, Enterprise edition | アプリケーション更新プログラム 3: [Dynamics 365 for Finance and Operations の KB 4043284 アプリケーション更新プログラム 3 (バイナリ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4043284&bugId=3857197&qc=e6921e68e9b9037bf91c26b3b553e479890731b4b4dd5e6dcb45b0ca13895d8d)、 [Dynamics 365 for Finance and Operations の KB 4043285 アプリケーション更新プログラム 3 (X++ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4043285&bugId=3857199&qc=54ee2e988aace65d26834ced54cc11326f5d5e435520ccaf951d41bd1276f672)                     | 7.2.11792.62370  | 2017 年 9 月   |
| Dynamics 365 for Finance and Operations, Enterprise edition | アプリケーション更新プログラム 2: [Dynamics 365 for Finance and Operations の KB 4039142 アプリケーション更新プログラム 2 (バイナリ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4039142&bugId=3850590&qc=5339dbbd18aacbc8bdcbe4123d749d28803653d6c68f787bd8fc3337e97693df)、 [Dynamics 365 for Finance and Operations の KB 4039487 更新プログラム 2 (X++ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4039487&bugId=3850591&qc=5339dbbd18aacbc8bdcbe4123d749d28803653d6c68f787bd8fc3337e97693df)                     | 7.2.11792.62192  | 2017 年 9 月   |
| Dynamics 365 for Finance and Operations, Enterprise edition | アプリケーション更新プログラム 1: [Dynamics 365 for Finance and Operations の KB 4035749 アプリケーション更新プログラム 1 (バイナリ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4035749&bugId=3845890&qc=5339dbbd18aacbc8bdcbe4123d749d28803653d6c68f787bd8fc3337e97693df)、 [Dynamics 365 for Finance and Operations の KB 4035751 アプリケーション更新プログラム 1 (X++ パーツ)\*](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4035751&bugId=3845891&qc=5339dbbd18aacbc8bdcbe4123d749d28803653d6c68f787bd8fc3337e97693df)                     | 7.2.11792.62089  | 2017 年 7 月        |


\* リンクは、サポート技術情報 (KB) の記事を指します。 KB の記事を表示するには、Lifecycle Services (LCS) にログインする必要があります。

## <a name="support-matrix"></a>サポート マトリックス

プラットフォーム更新プログラムには、リリースの時点でサポートされているすべてのアプリケーション バージョンとの互換性があります。

### <a name="table-5-downloadable-virtual-hard-drive-vhd-releases"></a>テーブル 5: ダウンロード可能な仮想ハード ドライブ (VHD) をリリース

VHD の使用の際には、[ソフトウェア ライセンス条件](https://go.microsoft.com/fwlink/?linkid=851163)が適用されます。

| **リリース**                                  | **VHD 名**                 | **VHD 有効期限** |
|----------------------------------------------|------------------------------|-------------------------|
| プラットフォーム アップデート 12 / アプリケーション リリース 7.2 | FinandOps7.2PlatUpdate12.vhd | 2018 年 5 月 24 日            |
| プラットフォーム アップデート 12 / アプリケーション リリース 7.3 | FinandOps7.3PlatUpdate12.vhd | 2018 年 6 月 5 日           |
| プラットフォーム アップデート 15 / アプリケーション リリース 7.3 | FinandOps7.3withPlatUpdate15 | 2018 年 12 月       |

