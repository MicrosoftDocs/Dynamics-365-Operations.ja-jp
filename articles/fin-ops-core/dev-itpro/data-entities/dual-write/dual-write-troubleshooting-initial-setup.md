---
title: 初期セットアップ中の問題のトラブルシューティング
description: このトピックでは、デュアル書き込み統合の初期設定中に発生する問題を修正するために役立つ情報を提供します。
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: c9bf5d9017579b4207e09769cff38361442e3938
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781443"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>初期セットアップ中の問題のトラブルシューティング

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Finance and Operations アプリと Dataverse 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。 このトピックでは、 デュアル書き込み統合の初期設定を行う際に、発生する可能性がある問題を修正するトラブルシューティングに特化した情報を提供します。

> [!IMPORTANT]
> このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。 各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Finance and Operations アプリを Dataverse にリンクさせることはできません。

**デュアル書き込みの設定に必要なロール:** Finance and Operations アプリと Dataverse 両方のシステム管理者権限。

一般的には、 **Dataverseへのリンク設定** ページで発生するエラーは、設定が不完全な場合やアクセス権限の問題が原因で発生するします。 次の図に示すように、**Dataverseへのリンク設定** ページで正常性チェック全体が合格になっていることを確認してください。 正常性チェック全体で合格しない限りは、デュアル書き込みをリンクすることはできません。

![正常性チェックの成功。](media/health_check.png)

Azure AD 環境と Finance and Operations 環境えおリンクするには、Dataverse テナント管理者の資格情報が必要です。 環境をリンクした後、ユーザーはアカウントの資格情報を使用してログインし、既存のテーブル マップを更新できます。

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>デュアル書き込み対してにリンク可能な、リーガル テーブルまたは会社数の制限を確認する

マッピングを有効化した際に、次のエラー メッセージが表示される場合があります。

*デュアル書き込みエラー - プラグインの登録に失敗: (プロジェクト DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea のパーティション マッピングを取得できません。エラーDWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea で許容されるマッピングの最大パーティション数を超えています)、1 つまたは複数のエラーが発生しました。*

現在のところ、環境をリンク可能なリーガル テーブルの制限は、約 40 件です。 このエラーは、マッピングを有効化する際に発生し、環境間で 40 以上のリーガル テーブルがリンクされている場合に発生します。

## <a name="connection-set-failed-while-linking-environment"></a>環境のリンク中に接続設定に失敗

デュアル書き込み環境のリンク中に、アクションの実行に失敗してエラー メッセージが表示されます。

*接続設定の保存に失敗しました! 同じキーを持つ品目が既に追加されています。*

デュアル書き込みでは、同じ名前を持つ複数の法人/会社はサポートされていません。 たとえば、Dataverse に「DAT」という名前の 2 つの会社がある場合、このエラー メッセージが表示されます。

顧客のブロックを解除するには、Dataverse の **cdm_company** テーブルから重複レコード テーブルを削除します。 また、**cdm_company** テーブルに空白の名前のレコードがある場合は、それらのレコードを削除または修正します。

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Finance and Operations アプリでデュアル書き込みページを開く際のエラー

Dataverse の環境をデュアル書き込みにリンクしようとすると、以下のエラーメッセージが表示されることがあります。

*応答状態コードが成功とならない: 404 (Not Found)。*

このエラーは、アプリの同意の手順が完了していない場合に発生します。 テナント管理者アカウントを使用して `portal.azure.com` にログオンし、ID が `33976c19-1db5-4c02-810e-c243db79efde` のサード パーティ アプリが AAD のエンタープライズ アプリケーション リストに表示されているかどうかを確認することで、同意が提供されているかどうかを検証できます。 それ以外の場合は、次のセクションで説明するように、同意の手順を再実行します。

### <a name="providing-app-consent"></a>アプリへの同意をする場合

+ 管理者の資格情報を使用して、次の URL を起動します。

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ 同意するには、**同意** を選択します。 テナントにアプリ (`id=33976c19-1db5-4c02-810e-c243db79efde`) をインストールすることについて同意されたものとします。
+ このアプリは、Dataverse が Finance and Operations アプリに通信するために必要です。

    ![初期同期設定のトラブルシューティング。](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> これが動作しない場合は、Microsoft Edge のプライベート モードまたは Chrome の匿名モードで URL を起動します。

## <a name="finance-and-operations-environment-is-not-discoverable"></a>Finance and Operations 環境は検出できません

次のエラー メッセージが表示される場合があります。

*Finance and Operations アプリ環境 \*\*\* .cloudax.dynamics.com は検出できません。*

環境が検出されないという問題を引き起こす可能性のあるものが 2 つあります。

+ ログインに使用するユーザーが、Finance and Operations インスタンスと同じテナントではない。
+ Microsoft がホストしている従来の Finance and Operations インスタンスの中に、検出に問題があった。 これを修正するには、Finance and Operations インスタンスを更新します。 どのようなアップデートでも、この環境は検出可能になります。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
