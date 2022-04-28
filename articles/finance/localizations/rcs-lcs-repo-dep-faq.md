---
title: Regulatory Configuration Service (RCS) - Lifecycle Services (LCS) 記憶域の廃止
description: このトピックでは、Regulatory Configuration Service (RCS) グローバル リポジトリの機能拡張の一部として計画されている Microsoft Dynamics Lifecycle Services (LCS) 記憶域の廃止に関する情報を提供します。
author: JaneA07
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, LCS storage, LCS storage deprecation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.19
ms.openlocfilehash: 8862f42f3ceaed7e1413c49cf9b91f0449fab67b
ms.sourcegitcommit: 4c8223c9540fbc1c1e554962938058d432e4c681
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/05/2022
ms.locfileid: "8547985"
---
# <a name="regulatory-configuration-service-rcs--lifecycle-services-lcs-storage-deprecation"></a>Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) 記憶域の廃止

[!include [banner](../includes/banner.md)]

Electronic Reporting (ER) コンフィギュレーションの記憶域リポジトリとして Microsoft Dynamics Lifecycle Services (LCS) を使用することは廃止される予定です。 この廃止には、次の変更が含まれます。

- Microsoft Dynamics 365 アプリケーションで使用されている Microsoft が作成したコンフィギュレーションは、LCS の共有資産ライブラリに公開されなくなります。 代わりに、RCS グローバル リポジトリを通じてのみ公開されます。 ただし、Dynamics AX 2012 のコンフィギュレーションは、AX 2012 のサポート ライフサイクルが終了するまで、LCS の共有資産ライブラリに引き続き公開 されます。
- 財務と運用アプリ、および RCS から LCS のプロジェクト資産ライブラリにコンフィギュレーションをアップロードできる機能は無効になります。 ただし、LCS のブラウザを使用して、コンフィギュレーションをプロジェクト資産ライブラリにアップロードすることは引き続きできます。 したがって、LCS にコンフィギュレーションを追加してソリューション パッケージに含めることはまだできます。
- LCS からのコンフィギュレーションのインポートは、財務と運用アプリおよび RCS で引き続き使用可能であり、当面の間はサポートされます。 ただし、この機能は最終的に非推奨となります。 (正確な廃止予定日は、後日発表となります。)

## <a name="deprecation-notice"></a>廃止のお知らせ

記憶域としての LCS の使用の廃止は、[Dynamics 365 Finance の削除済みまたは非推奨の機能 - LCS 廃止のお知らせ](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release) で通知されました。 廃止予定日は 2022 年 4 月 1 日です。

## <a name="key-features"></a>主な機能

- RCS を使用して、ER コンフィギュレーションおよびグローバリゼーションの機能を作成および編集できます。
- RCS デザイナーから Dynamics 365 Finance 環境などの接続されたアプリケーションにコンフィギュレーションを直接プッシュすることで、コンフィギュレーションの変更やテストを迅速に行うことができます。
- グローバル リポジトリの一元的なストレージで、ER コンフィギュレーションおよびグローバリゼーションの機能の両方のライフサイクルを一元的に保存、共有、および管理します。

## <a name="guidance-for-one-time-and-ongoing-actions"></a>1 回および進行中のアクションのガイダンス

このセクションでは、1 回度実行する必要がある一連のステップについて説明します。 また、後で継続的に完了する必要があるステップも説明します。

### <a name="one-time-action"></a>1 回のアクション

LCS から RCS に必要なすべてのコンフィギュレーションをインポートし、それを RCS からグローバル リポジトリに公開します。 プロジェクト固有の資産ライブラリを使用して派生コンフィギュレーションを LCS に保存する場合は、LCS にアクセス可能な間に次のステップを実行する必要があります。

1. RCS インスタンスを使用できない場合は、プロビジョニングします。 詳細については、[RCS 概要](rcs-overview.md)を参照してください。
2. プロビジョニングされた RCS インスタンスでは、派生 ER コンフィギュレーションを含む資産ライブラリ内のすべての LCS プロジェクトに対して、適切な LCS リポジトリを登録します。
3. LCS から RCS に ER コンフィギュレーションをインポートします。 詳細については、[LCS からコンフィギュレーションをインポートする](/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services)を参照してください。
4. グローバル リポジトリに自動的に提供されていない場合は、RCS に登録します。
5. 現在の RCS インスタンスからすべての派生コンフィギュレーションをグローバル リポジトリにアップロードします。 **コンフィギュレーション パッケージ** 機能を使用して、アップロードを支援します。 詳細については、[RCS グローバル リポジトリのアップロード](rcs-global-repo-upload.md)を参照してください。

### <a name="going-forward"></a>今後の手順

次の目的で RCS のビジュアル デザイナーを使用します:

- Microsoft が提供するテンプレートを拡張する。
- 組織が必要とする新しいコンフィギュレーションを作成する。
- 電子請求および税計算サービス用のグローバリゼーション機能をカスタマイズする。

次の目的でグローバリゼーション リポジトリを使用します:

- Microsoft が生成したコンフィギュレーションおよびグローバリゼーションの機能にアクセスする。
- 作成または拡張したコンフィギュレーションを、記憶域用のグローバル リポジトリにアップロードし、組織の Dynamics 365 アプリケーション環境全体または外部組織と共有します。 詳細については、[RCS に ER コンフィギュレーションを作成してグローバル リポジトリへアップロードする](rcs-global-repo-upload.md)を参照してください。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a>この変更を行った場合、LCS をコンフィギュレーションの中央記憶域として使用できなくなりますか。

はい。 財務と運用アプリから LCS のプロジェクト資産ライブラリにコンフィギュレーションをアップロードできる機能は廃止されます。 ただし、LCS のブラウザを使用して、コンフィギュレーションをプロジェクト資産ライブラリにアップロードすることは必要に応じて可能です。

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a>RCS は、グローバル テンプレート ファイルをインポートする代わりのリポジトリだと思っていました。 コンフィギュレーションの保存に使用されているとは考えていませんでした。 正しいのはどちらですか。

RCS は、ER コンフィギュレーションを作成および編集するためのデザイン サービスです。 RCS には、グローバル リポジトリと呼ばれる独自のリポジトリがあります。 このリポジトリは、RCS で作成されたコンフィギュレーションを保存するために使用されます。 記憶域として LCS を使用する予定が推奨されない場合、グローバル リポジトリは Microsoft コンフィギュレーションの単一ソースになります。 LCS から RCS に必要なすべてのコンフィギュレーションをインポートし、そのコンフィギュレーションを RCS からグローバル リポジトリに公開するには、1 回操作を実行する必要があります。

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a>LCS がない場合、"テスト" コンフィギュレーションと "プロダクション" コンフィギュレーションを容易に管理および転送するためのコンフィギュレーション保存方法としてする推奨されるものは何ですか。

RCS は、*接続されたアプリケーション* の概念を使用します。 接続されたアプリケーションは、RCS と財務と運用アプリの任意のインスタンス間の接続を形成します。 RCS を使用してコンフィギュレーションを編集することができるため、接続されているアプリケーションを使用すると、デザイナーから財務と運用アプリ環境にコンフィギュレーションを直接プッシュできます。 したがって、LCS プロジェクトレベルの記憶域を使用する必要なく、コンフィギュレーションをすばやく変更およびテストできます。

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a>設定と管理の例を示す例がありますか。

例はありません。ただし、このトピックで説明した手順を実行して、コンフィギュレーションを RCS グローバル リポジトリに移行できます。

### <a name="is-rcs-a-prerequisite-to-configure-electronic-reporting"></a>RCS は電子申告を構成するための前提条件ですか?

はい。 RCS には、電子請求や税計算サービスなどのグローバリゼーション サービスで使用されるグローバリゼーション機能の設定をサポートする機能が含まれています。 ただし、このサービスには、ER コンフィギュレーションを拡張または新規作成するための、同じビジュアル デザイナー機能があります。 また、RCS は、ER コンフィギュレーションとグローバリゼーションの機能の両方のライフサイクル管理も提供します。

### <a name="which-regions-can-rcs-be-deployed-in"></a>どの地域で RCS を展開できますか?

RCS は以下の Azure リージョンで利用できます:

- 米国
- インド
- フランス
- ヨーロッパ

製品サポートの詳細については、[Dynamics グローバリゼーション サービスの概要](globalization-services-overview.md) を参照してください。 地理的なサポートについては [Dynamics 365 および Power Platform: 使用可能性、データの場所、言語、およびローカライズ](https://aka.ms/rcs/D365Productavailabilityguide) を参照してください。

### <a name="whats-the-cost-of-using-rcs"></a>RCS を使用するためのコストはいくらですか?

RCS およびグローバリゼーション リポジトリは、既存の財務と運用アプリ ライセンスの一部として無料で提供されます。 グローバル リポジトリでの RCS デザイン サービスの使用やコンフィギュレーションの保存に関連する個別のコストはありません。 現在、コンフィギュレーションまたは接続されているアプリケーションの数に制限はありません。