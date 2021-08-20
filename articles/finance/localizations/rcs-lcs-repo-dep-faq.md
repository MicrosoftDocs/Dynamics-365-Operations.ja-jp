---
title: Regulatory Configuration Service (RCS) - Lifecycle Services (LCS) 記憶域の廃止
description: このトピックでは、Regulatory Configuration Service (RCS) グローバル リポジトリの機能拡張の一部として計画されている Microsoft Dynamics Lifecycle Services (LCS) 記憶域の廃止に関する情報を提供します。
author: JaneA07
ms.date: 05/25/2021
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
ms.openlocfilehash: 7a738af04da4425e76bd3b224400f91bc4eb8364d323da67ea457eaba9e65643
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782201"
---
# <a name="regulatory-configuration-service-rcs--lifecycle-services-lcs-storage-deprecation"></a>Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) 記憶域の廃止

[!include [banner](../includes/banner.md)]

Electronic Reporting (ER) コンフィギュレーションの記憶域リポジトリとして Microsoft Dynamics Lifecycle Services (LCS) を使用することは廃止される予定です。 この廃止には、次の変更が含まれます。

- Microsoft Dynamics 365 アプリケーションで使用されている Microsoft が作成したコンフィギュレーションは、LCS の共有資産ライブラリに公開されなくなります。 代わりに、RCS グローバル リポジトリを通じてのみ公開されます。 ただし、Dynamics AX 2012 のコンフィギュレーションは、AX 2012 のサポート ライフサイクルが終了するまで、LCS の共有資産ライブラリに引き続き公開 されます。
- Finance and Operations アプリ、および RCS から LCS のプロジェクト資産ライブラリにコンフィギュレーションをアップロードできる機能は無効になります。 ただし、LCS のブラウザを使用して、コンフィギュレーションをプロジェクト資産ライブラリにアップロードすることは引き続きできます。 したがって、LCS にコンフィギュレーションを追加してソリューション パッケージに含めることはまだできます。
- LCS からのコンフィギュレーションのインポートは、Finance and Operations アプリおよび RCS で引き続き使用可能であり、当面の間はサポートされます。 ただし、この機能は最終的に非推奨となります。 (正確な廃止予定日は、後日発表となります。)

## <a name="deprecation-notice"></a>廃止のお知らせ

記憶域としての LCS の使用の廃止は、[Dynamics 365 Finance - LCS 廃止のお知らせ](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release)で通知されました。 廃止予定日は 2022 年 4 月 1 日です。

## <a name="key-features"></a>主な機能

- RCS を使用してコンフィギュレーションを作成および編集できます。 その後、これらのコンフィギュレーションをデザイナーから接続されたアプリケーションに直接プッシュできます。 そのため、コンフィギュレーションをすばやく変更およびテストできます。
- グローバル リポジトリは、すべての ER コンフィギュレーション用の集中記憶域です。

## <a name="guidance-for-one-time-and-ongoing-actions"></a>1 回および進行中のアクションのガイダンス

このセクションでは、1 回度実行する必要がある一連のステップについて説明します。 また、後で継続的に完了する必要があるステップも説明します。

### <a name="one-time-action"></a>1 回のアクション

LCS から RCS に必要なすべてのコンフィギュレーションをインポートし、それを RCS からグローバル リポジトリに公開します。 プロジェクト固有の資産ライブラリを使用して派生コンフィギュレーションを LCS に保存する場合は、LCS にアクセス可能な間に次のステップを実行する必要があります。

1. RCS インスタンスを使用できない場合は、プロビジョニングします。 詳細については、[RCS 概要](rcs-overview.md)を参照してください。
2. プロビジョニングされた RCS インスタンスでは、派生 ER コンフィギュレーションを含む資産ライブラリ内のすべての LCS プロジェクトに対して、適切な LCS リポジトリを登録します。
3. LCS から RCS に ER コンフィギュレーションをインポートします。 詳細については、[LCS からコンフィギュレーションをインポートする](../../dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services.md)を参照してください。
4. グローバル リポジトリに自動的に提供されていない場合は、RCS に登録します。
5. 現在の RCS インスタンスからすべての派生コンフィギュレーションをグローバル リポジトリにアップロードします。 **ユーザーが 1 回の操作ですべてのコンフィギュレーションを GR にアップロードできるコンフィギュレーション パッケージ** 機能を使用 して、アップロードを支援します。 詳細については、[RCS グローバル リポジトリのアップロード](rcs-global-repo-upload.md)を参照してください。

### <a name="going-forward"></a>今後の手順

すべての新しいコンフィギュレーションを作成するには、RCS のビジュアル デザイナーを使用します。 次に、コンフィギュレーションをグローバル リポジトリにアップロードして保存します。 詳細については、[RCS に ER コンフィギュレーションを作成してグローバル リポジトリへアップロードする](rcs-global-repo-upload.md)を参照してください。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a>この変更を行った場合、LCS をコンフィギュレーションの中央記憶域として使用できなくなりますか。

はい。 Finance and Operations アプリから LCS のプロジェクト資産ライブラリにコンフィギュレーションをアップロードできる機能は廃止されます。 ただし、LCS のブラウザを使用して、コンフィギュレーションをプロジェクト資産ライブラリにアップロードすることは必要に応じて可能です。

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a>RCS は、グローバル テンプレート ファイルをインポートする代わりのリポジトリだと思っていました。 コンフィギュレーションの保存に使用されているとは考えていませんでした。 正しいのはどちらですか。

RCS は、ER コンフィギュレーションを作成および編集するためのデザイン サービスです。 RCS には、グローバル リポジトリと呼ばれる独自のリポジトリがあります。 このリポジトリは、RCS で作成されたコンフィギュレーションを保存するために使用されます。 記憶域として LCS を使用する予定が推奨されない場合、グローバル リポジトリは Microsoft コンフィギュレーションの単一ソースになります。 LCS から RCS に必要なすべてのコンフィギュレーションをインポートし、そのコンフィギュレーションを RCS からグローバル リポジトリに公開するには、1 回操作を実行する必要があります。

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a>LCS がない場合、"テスト" コンフィギュレーションと "プロダクション" コンフィギュレーションを容易に管理および転送するためのコンフィギュレーション保存方法としてする推奨されるものは何ですか。

RCS は、*接続されたアプリケーション* の概念を使用します。 接続されたアプリケーションは、RCS と Finance and Operations アプリの任意のインスタンス間の接続を形成します。 RCS を使用してコンフィギュレーションを編集することができるため、接続されているアプリケーションを使用すると、デザイナーから Finance and Operations アプリケーション環境にコンフィギュレーションを直接プッシュできます。 したがって、LCS プロジェクトレベルの記憶域を使用する必要なく、コンフィギュレーションをすばやく変更およびテストできます。

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a>設定と管理の例を示す例がありますか。

例はありません。ただし、このトピックで説明した手順を実行して、コンフィギュレーションを RCS グローバル リポジトリに移行できます。
